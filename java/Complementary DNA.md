**难度：7kyu**

---

**题目：**

Deoxyribonucleic acid (DNA) is a chemical found in the nucleus of 

cells and carries the "instructions" for the development and 

functioning of living organisms.

In DNA strings, symbols "A" and "T" are complements of each other, 

as "C" and "G". You have function with one side of the DNA (string, 

except for Haskell); you need to get the other complementary side. 

strand is never empty or there is no DNA at all (again, except for ).

>输入一个DNA碱基对序列，返回对应的碱基对序列（A=T,G=C）

```java
示例：
DnaStrand.makeComplement("ATTGC") // return "TAACG"
DnaStrand.makeComplement("GTAT") // return "CATA"
```
```java
实现代码：

public class DnaStrand {
  public static String makeComplement(String dna) {
    StringBuffer newDna = new StringBuffer(dna);
    for(int i = 0 ; i < dna.length() ; i++){
        switch(dna.charAt(i)){
        case 'A':
            newDna.setCharAt(i,'T');
            break;
        case 'T':
            newDna.setCharAt(i,'A');
            break;
        case 'G':
            newDna.setCharAt(i,'C');
            break;
        case 'C':
            newDna.setCharAt(i,'G');
            break;
        }
    }
    String otherDna = new String(newDna);
    return otherDna;
  }
}
```