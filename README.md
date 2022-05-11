**所有实验均在此md！**

# 实验一![1650794806002.png](image/README/1650794806002.png)

![1650794809606.png](image/README/1650794809606.png)

Jupyter NoteBook的安装
1.在官网https://www.anaconda.com/products/distribution点击下载

![1650794814047.png](image/README/1650794814047.png)

2.完成下载之后，双击下载文件，启动安装程序。
注意：
① 如果在安装过程中遇到任何问题，那么暂时地关闭杀毒软件，并在安装程序完成之后再打开。

② 如果在安装时选择了“为所有用户安装”，则卸载Anaconda然后重新安装，只为“我这个用户”安装。
3.选择"next"。

4. 阅读许可证协议条款，然后勾选“I Agree”并进行下一步。
5. 除非是以管理员身份为所有用户安装，否则仅勾选“Just Me”并点击“Next”。
6. 在“Choose Install Location”界面中选择安装Anaconda的目标路径，然后点击“Next”。
   注意：
   ① 目标路径中不能含有空格，同时不能是“unicode”编码。

② 除非被要求以管理员权限安装，否则不要以管理员身份安装。

7.一直点next就可以了

![1650794822859.png](image/README/1650794822859.png)

8.验证是否安装成功

① “开始 → Anaconda3（64-bit）→ Anaconda Navigator”，若可以成功启动Anaconda Navigator则说明安装成功。

② “开始 → Anaconda3（64-bit）→ 右键点击Anaconda Prompt → 以管理员身份运行”，在Anaconda Prompt中输入 conda list ，可以查看已经安装的包名和版本号。若结果可以正常显示，则说明安装成功。

9在安装成功后点击界面中的Notebook就可以跳转到http://localhost:8888/tree#notebooks

10可以new一个python就可以开始写代码了

![1650794833428.png](image/README/1650794833428.png)


# 实验二

创建一个新工程

![](image/README/1652277543713.png)

运行新程序

![](image/README/1652277647416.png)

修改fragment


```
<?xml version="1.0" encoding="utf-8"?>  
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"  
  xmlns:app="http://schemas.android.com/apk/res-auto"  
  xmlns:tools="http://schemas.android.com/tools"  
  android:layout_width="match_parent"  
  android:layout_height="match_parent"  
  android:background="@color/screenBackground"  
  tools:context=".FirstFragment">  

 <TextView  android:id="@+id/textview_first"  
  android:layout_width="wrap_content"  
  android:layout_height="wrap_content"  
  android:fontFamily="sans-serif-condensed"  
  android:text="@string/hello_first_fragment"  
  android:textColor="@android:color/white"  
  android:textSize="72sp"  
  android:textStyle="bold"  
  app:layout_constraintBottom_toBottomOf="parent"  
  app:layout_constraintEnd_toEndOf="parent"  
  app:layout_constraintStart_toStartOf="parent"  
  app:layout_constraintTop_toTopOf="parent"  
  app:layout_constraintVertical_bias="0.3" />  

 <Button  android:id="@+id/random_button"  
  android:layout_width="wrap_content"  
  android:layout_height="wrap_content"  
  android:layout_marginEnd="24dp"  
  android:background="@color/buttonBackground"  
  android:text="@string/random_button_text"  
  app:layout_constraintBottom_toBottomOf="parent"  
  app:layout_constraintEnd_toEndOf="parent"  
  app:layout_constraintTop_toBottomOf="@+id/textview_first" />  

 <Button  android:id="@+id/toast_button"  
  android:layout_width="wrap_content"  
  android:layout_height="wrap_content"  
  android:layout_marginStart="24dp"  
  android:background="@color/buttonBackground"  
  android:text="@string/toast_button_text"  
  app:layout_constraintBottom_toBottomOf="parent"  
  app:layout_constraintStart_toStartOf="parent"  
  app:layout_constraintTop_toBottomOf="@+id/textview_first" />  

 <Button  android:id="@+id/count_button"  
  android:layout_width="wrap_content"  
  android:layout_height="wrap_content"  
  android:text="@string/count_button_text"  
  android:background="@color/buttonBackground"  
  app:layout_constraintBottom_toBottomOf="parent"  
  app:layout_constraintEnd_toStartOf="@+id/random_button"  
  app:layout_constraintStart_toEndOf="@+id/toast_button"  
  app:layout_constraintTop_toBottomOf="@+id/textview_first" />  
</androidx.constraintlayout.widget.ConstraintLayout>
```

![](image/README/1652278919302.png)

修改第二个fragment

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/screenBackground"
    tools:context=".SecondFragment">

    <TextView
        android:id="@+id/textview_header"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginStart="24dp"
        android:layout_marginTop="24dp"
        android:layout_marginEnd="24dp"
        android:textColor="@color/colorPrimaryDark"
        android:text="@string/random_heading"
        android:textSize="24sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button_second"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/previous"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/textView_random"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textColor="@color/white"
        android:text="R"
        android:textSize="72sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toTopOf="@+id/button_second"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textview_header"
        app:layout_constraintVertical_bias="0.45" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

切换效果

![](image/README/1652279240151.png)

![img](image/README/1652279103193.png)
