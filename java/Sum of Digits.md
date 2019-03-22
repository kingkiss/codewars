**难度：6kyu**

---

**题目：**

In this kata, you must create a digital root function.
A digital root is the recursive sum of all the digits in a number. Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. This is only applicable to the natural numbers.

>给定一个数字，这个数字中每一位数相加在一起得到的值再每一位进行相加，直到最后的值为个位数为止

```java
示例：
digital_root(16)
=> 1 + 6
=> 7

digital_root(942)
=> 9 + 4 + 2
=> 15 ...
=> 1 + 5
=> 6

digital_root(132189)
=> 1 + 3 + 2 + 1 + 8 + 9
=> 24 ...
=> 2 + 4
=> 6

digital_root(493193)
=> 4 + 9 + 3 + 1 + 9 + 3
=> 29 ...
=> 2 + 9
=> 11 ...
=> 1 + 1
=> 2
```

```java
实现代码：


public class DRoot {
  public static int digital_root(int n) {
    String num = String.valueOf(n);
    char chs[] = num.toCharArray();
    int result = 0;
    for(char i : chs){
        result = result + Character.getNumericValue(i);
    }
    if(result >= 10){
        return digital_root(result);
    }else{
        return result;
    }
  }
}
```