**难度：7kyu**

---

**题目：**

Return the number (count) of vowels in the given string.

We will consider a, e, i, o, and u as vowels for this Kata.

The input string will only consist of lower case letters and/or spaces.

>输入一个字符串，返回字符串中元音字符（a,e,i,o,u）的数量


```java
实现代码：

public class Vowels { 
    public static int getCount(String str) { 
      int Count = 0; 
      for(char c : str.toCharArray()) {
         Count += (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') ? 1 : 0; 
         }
      return Count; 
    } 
}
```