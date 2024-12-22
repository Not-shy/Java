# 类与main函数
```java
public class HelloWorld{
  public static void main(String[] args){
    for(String str:args){
      System.out.println(str)
    }
  }
}
```

# 输入与输出
```java
//输入
Scanner in = new Scanner(System.in);
int i = in.nextInt();
double j = in.nextDouble();
String s = in.nextLine();//可读入空白符
String s1 = in.next();//不可读入空白符
```

```
//输出
System.out.print();
System.out.println();
System.out.printf("");
//%d--int %f--double/float 
//正数向左对齐，加零是向前补零；%.nf保留n位小数
```

# 变量与类型
boolen

