# 25.11.22
## 1. Write a program to determine if a string contains only unique characters. Return true if it does and false otherwise. 
 
The string may contain any of the 128 ASCII characters. Characters are case-sensitive, e.g. 'a' and 'A' are considered different characters.

[Task link](https://www.codewars.com/kata/553e8b195b853c6db4000048/train/java)
___
### Мое рещение 
```java

public class Kata { 
 public static boolean hasUniqueChars(String str) { 
 String s=""; 
  for (int i = 0; i < str.length()-1; i++) { 
    
    String h=""; 
    h +=str.charAt(i); 
    
   if(s.contains(h)) { 
    return false; 
   } 
   s+=str.charAt(i); 
   } return true;  
 } 
}

```

### Понравившееся решение
```java

public class Kata { 
 public static boolean hasUniqueChars(String str) { 
 return str.length() == str.chars().distinct().count(); 
 } 
}

```
## 2. I will give you an integer. Give me back a shape that is as long and wide as the integer. The integer will be a whole number between 1 and 50. 
 
Example 
n = 3, so I expect a 3x3 square back just like below as a string
[Task link](https://www.codewars.com/kata/59a96d71dbe3b06c0200009c/train/java)
### Мое рещение 
```java

public class Kata { 
 public static final String generateShape(int n) { 
 int count = 0; 
 StringBuilder pattern = new StringBuilder(); 
 
 for(int x = 0; x < n; x++) { 
 if (count == n) { 
 pattern.append("\n"); 
 count = 0; 
 } 
 for (int y = 0; y < n; y++) { 
 pattern.append("+"); 
 count++; 
 } 
 } 
 return pattern.toString(); 
 } 
}

```

### Понравившееся решение
```java

public class Kata { 
 
 public static final String generateShape(int n) { 
 return ("+".repeat(n) + "\n").repeat(n).trim(); 
 } 
}

```
