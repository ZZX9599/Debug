

# 1:打断点

在程序的某一行位置，数字右边的空白部分使用鼠标左键点击一下，出现红点即为打上了一个断点

![image-20221005160809554](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005160809554.png)

# 2:执行debug

方式一：选中要进行debug的程序，点击右上角的debug按钮

![image-20221005160856389](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005160856389.png)

方式二：在要进行debug的程序处右键，选中下图选项

![image-20221005160931798](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005160931798.png)

方式三：运行的时候直接选择debug

![image-20221005161147083](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005161147083.png)

# 3:重新执行debug

点击下图按钮，会关闭当前debug的程序并重新启动debug

![image-20221005161011615](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005161011615.png)

# 4:让程序执行到下个断点暂停

点击下图的按钮，debug会继续运行程序，直到遇到下一次断点后暂停

![image-20221005161044882](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005161044882.png)



# 5:让断点处的代码加上一行代码

现在代码停在`int i=10`这里

![image-20221005161526618](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005161526618.png)

等这行代码执行结束之后，虚拟机栈就有了 i 变量，这个时候可以点击下图的加号，在断点处加一行代码

![image-20221005161702057](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005161702057.png)

点击加号下面的减号，可以删除该行代码

![image-20221005161823464](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005161823464.png)




# 6:显示所有断点

点击下图按钮，会显示所有断点

![image-20221005162225158](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005162225158.png)


 点击后出现下图所示界面，可以添加断点运行的条件，见下一条功能解释

# 7:添加断点运行的条件

选中断点，右键后即可编辑断点运行的条件

满足条件时程序才会在该断点处停下

```java
public class App {
    public static void main(String[] args) {
        while (true){
            int i=10;
            System.out.println(i);

            int j=100;
            System.out.println(j);

            int k=1000;
            System.out.println(k);
        }
    }
}
```

`我在 int k=1000前面打断点 ，右键编辑`

![image-20221005162522383](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005162522383.png)

比如添加j<5，重新debug，此时查看全部断点，可以看到下图效果

![image-20221005162647107](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005162647107.png)

发现不走断点，但是1000还是会输出，`这个不走断点并不代表程序不运行`



# 8:屏蔽所有断点

点击下图按钮，可以屏蔽所有断点

![image-20221005162808210](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005162808210.png)
如果程序调试后觉得没问题了，可以屏蔽掉所有断点继续运行程序查看效果

# 9:把光标移动到程序运行的位置

点击下图按钮后，会把鼠标光标移动到当前程序运行位置

![image-20221005162939708](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005162939708.png)当程序代码量很大的时候，可以通过该按钮快速定位到程序运行位置

# 10:单步跳过

点击下图按钮，会一行一行执行自己编写的代码

![image-20221005163034262](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005163034262.png)如果碰到方法，该按钮不会进入到该方法内部

快捷键 F8 

# 11:跳入方法内部执行代码操作

下图中的蓝色箭头和红色箭头都可以执行一行代码，如果遇到方法时会进入方法内部，区别在于
蓝色箭头只会跳进自己写的方法，如果是系统已经写好的方法，蓝色箭头无法跳入该方法
红色箭头不管是自己写的方法，还是系统已经定义好的方法，都可以跳入方法内部

![image-20221005163146465](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005163146465.png)


例如：ArrayList的add方法是系统已经写好的，蓝色箭头无法跳入方法内部，但红色箭头可以跳入方法内部

# 12:跳出方法

下图的两个按钮都可以跳出方法

![image-20221005163410393](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005163410393.png)

第二个按钮是关闭窗口的意思，同样可以起到跳出方法的作用

在进入方法内部的时候使用这两个按钮

# 13:回到光标所在位置

点击下图的按钮，程序会执行到光标所在的位置

![image-20221005163848516](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005163848516.png)

前提是光标前面没有断点，否则程序还是会在光标前面的断点处暂停

假设我现在正在跟 List 的 add 方法，感觉差不多了

![image-20221005163654002](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005163654002.png)

这个时候我想让代码直接跳到 int k=1000 这里来

```java
public class App {
    public static void main(String[] args) {
        while (true){
            List<String>list=new ArrayList<>();
            list.add("周志雄");
            
            int k=1000;
            System.out.println(k);
        }
    }
}

```

这个时候直接点击一下鼠标到这一行，然后点击上面图示的按钮即可

# 14:控制台改变正在debug的数据

在控制台选中某个变量，右键点击Set Value可以改变该变量的值
如果想测试某个地方的数据如果是正确的会是什么效果，可以手动更改该处变量的值

```java
public class App {
    public static void main(String[] args) {
        while (true){
            int k=1000;
            System.out.println(k);
        }
    }
}
```

选中 k=1000，右键，set value

![image-20221005164215412](https://zzx-note.oss-cn-beijing.aliyuncs.com/idea/image-20221005164215412.png)