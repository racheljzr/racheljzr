---
layout: post
title: 【Java】内部类
excerpt: 内部类，局部内部类，匿名内部类，静态嵌套类
categories: Java
comments: true
share: true
---

【转载】source: http://liuzxc.github.io/blog/java-advance-02/
### 什么是内部类

定义在其他类（outer class）中的类被称作内部类。内部类可以有访问修饰服，甚至可以被标记为 abstract 或
final。 内部类与外部类实例有特殊的关系，这种关系允许内部类访问外部类的成员，也包括私有成员。

内部类分为以下四种：

1. inner class
2. 局部内部类
3. 匿名内部类
4. 静态嵌套类

#### Inner Class

一个内部类被声明在另外一个类当中：

{% highlight java %}
//Top level class definition
class MyOuterClassDemo {
   private int myVar= 1;

   // inner class definition
   class MyInnerClassDemo {
      public void seeOuter () {
         System.out.println("Value of myVar is :" + myVar);
      }
    } // close inner class definition

} // close Top level class definitio
{% endhighlight %}

##### 实例化一个内部类

为了实例化一个内部类的实例，需要一个外部类的实例。内部类的实例只能通过外部类的实例来创建。

{% highlight java %}
//Top level class definition
class MyOuterClassDemo {
 private int myVar= 1;

 // inner class definition
 class MyInnerClassDemo {
    public void seeOuter () {
       System.out.println("Value of myVar is :" + myVar);
    }
  } // close inner class definition

 void innerInstance(){
	MyInnerClassDemo inner = new MyInnerClassDemo();
	inner.seeOuter();
 }
 public static void main(String[] args){
	 MyOuterClassDemo outer = new MyOuterClassDemo();
	 outer.innerInstance();
 }
} // close Top level class definitio

Output: Outer Value of x is :1
{% endhighlight %}

上面的例子 mian 方法也可以这样写：

{% highlight java %}
 public static void main(String[] args){
	 MyOuterClassDemo.MyInnerClassDemo inner = new MyOuterClassDemo().new MyInnerClassDemo();
	 inner.seeOuter();
 }
{% endhighlight %}

#### 局部内部类

局部内部类被定义在外部类的方法当中。

* 如果你想使用内部类，必须同一方法中实例化内部类
* 只有 abstract 和 final 这两个修饰符被允许修饰局部内部类
* 只有在方法的局部变量被标记为 final 或 局部变量是 effectively final的， 内部类才能使用它们。

> 什么是 effectively final？
> "Starting in Java SE 8, a local class can access local variables and parameters of the enclosing block that are final or effectively final. A variable or parameter whose value is never changed after it is initialized is effectively final."
>因此当变量或参数在初始化之后，值再也没有改变过，那么就说明该变量或参数是 effectively final。

{% highlight java %}
//Top level class definition
class MyOuterClassDemo {
 private int x= 1;

 public void doThings(){
    String name ="local variable"; // name is effectively final
    // inner class defined inside a method of outer class
    class MyInnerClassDemo {
      public void seeOuter() {
         System.out.println("Outer Value of x is :" + x);
         System.out.println("Value of name is :" + name);
      } //close inner class method
    } // close inner class definition
    MyInnerClassDemo inner = new MyInnerClassDemo();
    inner.seeOuter();
 } //close Top level class method
 public static void main(String[] args){
	 MyOuterClassDemo outer = new MyOuterClassDemo();
	 outer.doThings();
 }
} // close Top level class

Output:

Outer Value of x is :1
Value of name is :local variable
{% endhighlight %}

#### 匿名内部类

匿名内部类有以下特点：

1. 没有名字
2. 只能被实例化一次
3. 通常被声明在方法或代码块的内部，以一个带有分号的花括号结尾
4. 因为没有名字，所以没有构造函数
5. 不能是静态的（static)

为什么要使用匿名类，我们先看一个例子：

{% highlight java %}
abstract class Animal {
	abstract void play();
}

class Dog extends Animal{
	void play(){
		System.out.println("play with human");
	}
}

class Demo{
	public static void main(String[] args){
		Animal d = new Dog();
		d.play();
	}
}

Output:  play with human
{% endhighlight %}

如果此处的 Dog 类只使用了一次，那么单独定义一个Dog类是否会显得有点麻烦？
这个时候我们可以引入匿名类：

{% highlight java %}
abstract class Animal {
	abstract void play();
}

class Person{
	public static void main(String[] args){
		Animal d = new Animal(){
			void play(){
				System.out.println("play with human");
			}
		};
		d.play();
	}
}

Output:  play with human
{% endhighlight %}

由上面的例子可以看出，匿名类的一个重要作用就是**简化代码**。

匿名类的常用场景：

* 事件监听

普通的实现方式：

{% highlight java %}
 public class WindowClosingAdapter extends WindowAdapter {
     public void windowClosing( WindowEvent e ) {
         System.exit(0);
     }
 }

 ...

 addWindowListener( new WindowClosingAdapter() );
 {% endhighlight %}

匿名内部类的实现方式：

{% highlight java %}
 addWindowListener(
     new WindowAdapter() {
         public void windowClosing( WindowEvent e ) {
             System.exit(0);
         }
     });
{% endhighlight %}

* Thread 类的匿名内部类实现

{% highlight java %}
public class Demo {
    public static void main(String[] args) {
        Thread t = new Thread() {
            public void run() {
                for (int i = 1; i <= 5; i++) {
                    System.out.print(i + " ");
                }
            }
        };
        t.start();
    }
}
{% endhighlight %}

* Runnable 接口的匿名内部类实现

{% highlight java %}
public class Demo {
    public static void main(String[] args) {
        Runnable r = new Runnable() {
            public void run() {
                for (int i = 1; i <= 5; i++) {
                    System.out.print(i + " ");
                }
            }
        };
        Thread t = new Thread(r);
        t.start();
    }
}
{% endhighlight %}

#### 静态嵌套类

* 一个静态嵌套类是被标记为 static 的内部类。
* 静态嵌套类无法访问外部类的非静态成员。

>嵌套类被分为两类：静态和非静态的。被声明为 static 的被称作静态嵌套类，非静态嵌套类就是内部类

例如：

{% highlight java %}
class Outer{
   static class Nested{}
}
{% endhighlight %}

静态嵌套类可以被这样实例化：

{% highlight java %}
class Outer{// outer class
   static class Nested{}// static nested class
}

class Demo{
   public static void main(string[] args){
      // use both class names
      Outer.Nested n= new Outer.Nested();
   }
}
{% endhighlight %}

