1. +=1 和 +1的区别

   += 是java规定的运算符，short +1会自动提升表达式的类型

2.  两个Integer类型的比较。

   Integer i = 100 会翻译成Integer i = Integer.valueOf(100)，其中-128-127之间的数会进行缓存。不需要new，但其他数需要New

3. 基本类型和引用类型

![image-20210217175514670](C:\Users\94130\AppData\Roaming\Typora\typora-user-images\image-20210217175514670.png)

​	基本类型保存原始值，但是引用类型指对象在堆中的位置和地址。（对象都存储在堆中）

​	数组是引用类型 (new 产生存储在堆中)

![image-20210217184708476](C:\Users\94130\AppData\Roaming\Typora\typora-user-images\image-20210217184708476.png)

4. Stack Queue

   4.1优先队列 PriorityQueue

   出队入队是O(logn)

5. Concurrent包

   ![image-20210217210515827](C:\Users\94130\AppData\Roaming\Typora\typora-user-images\image-20210217210515827.png)

6. java创建对象的四种方法

   1. 使用new关键字
   2. 使用Class类的newInstance Class.forName.newInstance
   3. 使用clone
   4. 反序列化

7. String  StringBuffer StringBuilder

   ![image-20210218092527334](C:\Users\94130\AppData\Roaming\Typora\typora-user-images\image-20210218092527334.png)

8. java 文件读取

   File file = new File()

   FileInputStream stream = new  FileInputStream(file) (读取字节流,转化为字符流)

   InputStreamReader 解读刚才装进内存中的数据，转换为字符流。

   bufferreader,读取字符流

   ​	

9. Java 反射机制

   运行状态中、对于任何一个类都可以知道这个类所有的属性和方法。

   对于任何一个对象，都可以调用它的一个方法或者属性。

   ![image-20210218101013022](C:\Users\94130\AppData\Roaming\Typora\typora-user-images\image-20210218101013022.png)

   反射的用途：

   1. 通过反射得到Class对象
   2. 判断是否为某个类的示例 (class对象的isInstance方法)
   3. 通过反射来创建实例
   4. class.newInstance方法



10、JDK NDK JRE JNI

jRE: java核心类库和支持文件、java虚拟机

JDK:JRE、编译器和其他工具（JavaDoc以及Java调试器）

11、版本特性

jdk1.8 

lambda表达式：Lambda表达式也称作闭包，允许把函数作为一个方法的参数，使用Lamba表达式可以使代码变得更加简洁。

接口可以添加default作为非抽象方法

(参数) -> {代码块}

```
1.可选类型声明：参数的类型可以省，编译器自动识别数据类型。
2.可选的参数圆括号：参数只有一个时候可以省略圆括号。
3.可选的代码块大括号：代码块只有一行的时候可以省略大括号。
4.可选的返回关键字：代码块只有一行且有返回结果，那么return也可以省略。
```



1. jdk 命令模式：https://blog.csdn.net/luckydog1991/article/details/51718663

2. **NDK**（Native Development Kit）“原生”也就是二进制

   android常用的开发方式是java封装的库，而这些库的底层实现是由C/C++实现，如媒体，图形库等

   java调用这样实现就需要用**JNI**（Java Native Interface）

   平时用的也就是google给我们封装的好的库，即底层实现用的不是Java，但都有统一的Java接口

   NDK的作用是“我们自己写本地代码”（C/C++)，自己用JNI封装成Java接口

   比如我们想做个计算，显然这不是Java的强项，但可以用C/C++来写实现，返回一个运算结果就行了

   NDKr5已经实现了不用写一行Java代码开发程序了，只不过还是用到了虚拟机，细节被封装隐藏起来了而已





