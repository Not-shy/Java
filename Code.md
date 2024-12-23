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

# 报错
```java
//1、
int a;
System.out.print(a);
```


# 变量与类型
```java
//boolean
boolean a =true;
boolean b = false;
//boolean c = 1;
// if(6>5>4)
```

- 总结就是只用int
```java
//short/int/byte/long

//short:负三万多到正三万多; byte:-128-127
short a = 30000;
short b = (short)40000;
//short c = 40000;

byte d = 127;
byte e = (byte)128;
//byte f = 128

short c = (short)( a + b);
//short c = a + b;
```

```java
//double/float
float a = 1.1f;
float b = (float)1.1;
//float b = 1.1;

double c = 1.1(f);
```

```java
//包裹类型
int max = Integer.MAX_VALUE;
int min = Integer.MIN_VALUE;

String s = in.next();
char ch = s.charAt(0);
if(Character.isdigit(ch)/Character.isLetter(ch)/Character.isLetterOrDigit(ch)/Character.isWhitespace(ch))
{
}

if(Character.isLowerCase(ch)/Character.isUpperCase(ch)){
  Character.toLowerCase(ch);/Character.toUpperCase(ch);
}
```

```java
String s1 = "123456";
String s2 = "12345";

//比较
System.out.println(s1.equals(s2));

if(s1.compareTo(s2)>0){
System.out.println(s1);
}

//访问
for(int i=0;i<s1.length();i++){
  System.out.print(s1.charAt(i)+" ");
}

//获取子串(左闭右开)
System.out.println(s1.substring(1,3));
System.out.println(s1.substring(1));

//查找
System.out.println(s1.indexOf(s2));
//找到所有的r，并打印出位置
int index = s.indexOf('r');
while(index!=-1){
  sout(index);
  index = s.indeOf(index+1,'r');
}

//lastIndexOf()

//以下操作不会改变原字符串
//startswith()
//endswith()
//trim()
//replace(c1,c2)
//toLowerCase()
//toUpperCase()

```

```java
//查找某一个句子里是否含有一个单词
String sentence,word;
sentence = in.nextLine();
words = in.next();
words = " " + words + " ";
sentence = " " + sentence + " ";

int index = sentence.indexOf(words);
if(index==-1){
 ...
}
else{
...
}
```

```java
//朴素匹配子串
int index = 0;
for(int i=0;i<s1.length()&&index<s2.length();i++){
  for(int j=i;j<s1.length()&&index<s2.length();j++){
    if(s1.charAt(j)==s2.charAt(index)){
        index++
    }
}else{
  index = 0;
  break;
}
}
}
```

```java
//转换成char数组
s.toCharArray()
 String s = "hello";
 char[] str = s.toCharArray();
 System.out.println(str);//也可以直接打出来
```


# 运算符
```java
System.out.print(1*-2);

String s = "hello" + 100;
String s = 2 + 3 + "hello";
String s = "hello" + 2 + 3;
```

# 数据结构

```java
//数组
int i = in.nextInt();
int[] nums = new int[i];//默认全是0
double[] nums = new double[3];//默认全是0.0
int[] n = new int[]{1,2,3};

//匿名数组
func(new int[]{1,2,3});

//数组传参 会改变其值

for(int i:nums){
  i++;//在这里做出的改变并不会真的改变
  System.out.println(i);
}

for(int i=0;i<nums.length;i++){
  System.out.println(nums[i]);
}
```

```java
//二维数组
int[][] nums = new int[][]{
                      {1,2,3,4},
                      {1,2,3}
                      };
for(int i=0;i<nums.length;i++){
  for(int j=0;j<nums[i].length;j++){
    System.out.println(nums[i][j]);
  }
}
```

```java
//其它类型的对象
class Person{
 public int age;
 public String gender;

  Person(int age,String gender){
    this.age = age;
    this.gender = gender;
  }
@override
  public String toString(){
    String s = ""+age+" "+gender;
    return s;
  }
}

  public class Main{
    public static void main(String[] args){
      Person[] p = new Person[3];
      for(int i=0;i<p.length;i++){
          p[i] = new Person(i+18,"female");
      }
      for(Person i:p){
        i.age = 0;//这是可以改的
      }
      for(Person i:p){
      System.out.println(i);
   }
  }
 }
```


![image](https://github.com/user-attachments/assets/3b3e79cc-e277-479a-aa85-2c24f24dfd1b)



```java
//List

//ArrayList
List<Integer>list = new ArrayList();
for(int i=0;i<10;i++){
    list.add(i);
  }

list.addFirst(-1);
list.add(0,-2);

for(int i=0;i<2;i++){
    list.remove(0);
  }

for(int i=0;i<list.size();i++){
  System.out.print(list.get(i)+" ");
  }

```

```java
//toString
System.out.print("hello" + list);
```

```java
//转换成数组
list.toArray(arr);
```



```java
//集合

//HashSet
//基于HashMap实现，可null，无顺序
Set<Integer>set = new HashSet<>();
        for(int i=0;i<10;i++){
            set.add(i);
        }

        Set<Integer>set2 = new HashSet<>();
//全部复制！！！！！！！！！！！！！！List也有这个函数
        set2.addAll(set);

        for(Integer i:set2){
            System.out.println(i);
        }
        
        if(set2.contains(3)) {
            set2.remove(3);
        }
        System.out.println(set.size());
```

```java
//交集
set1.retainAll(set);//set1变成set和set1的交集
```

```java
//LinkedHashSet
//继承HashSet，但是用一个双向链表维护了插入顺序
```

```java
//TreeSet
//自然顺序，但不可容纳null
TreeSet<Integer>set = new TreeSet<>();
        for(int i=10;i>0;i--){
            set.add(i);
        }

        for(Integer i:set){
            System.out.println(i);
        }
```

```java
//对于HashSet和LinkedHashSet来说判断两个元素是否相同是根据hashcode，若相同再是equals
class Cat{
    private int size;
    public Cat(int size){
        this.size = size;
    }
    @Override
    public int hashCode(){
        return size;
    }

    @Override
    public boolean equals(Object obj){
        Cat c = (Cat)obj;
        return c.size==this.size;
    }
}

--main
Set<Cat>set = new HashSet<>();

        set.add(new Cat(5));
        set.add(new Cat(5));
        set.add(new Cat(4));

        System.out.println(set.size());
```

```java
/*TreeSet则是 1.该比较类实现接口Comparable，重写compareTo 2.重写一个实现接口Comparator<该类>的比较器，作为参数传入*/
class Cat implements Comparable{
    private int size;
    public int getSize(){
        return size;
    }
    public Cat(int size){
        this.size = size;
    }
    @Override
    public int compareTo(Object obj){
        Cat c = (Cat)obj;
        return c.size - this.size;
    }
}

 TreeSet<Cat>set = new TreeSet<>();
        for(int i=5;i>0;i--){
            set.add(new Cat(i));
        }

        for(Cat i:set){
            System.out.println(i.getSize());
        }

    }


```

```java
class Cat {
    private int size;
    public int getSize(){
        return size;
    }
    public Cat(int size){
        this.size = size;
    }

}

class CatComparator implements Comparator<Cat>{
    @Override
    public int compare(Cat o1, Cat o2) {
        return o2.getSize()- o1.getSize();
    }
}

--main
TreeSet<Cat>set = new TreeSet<>(new CatComparator());//是放在这里！！！！！！！！
        for(int i=5;i>0;i--){
            set.add(new Cat(i));
        }

        for(Cat i:set){
            System.out.println(i.getSize());
        }

```

```java


```

```java
//Map

```

# 类和对象

# static、final

# 异常


# 常用类

# 文件

















