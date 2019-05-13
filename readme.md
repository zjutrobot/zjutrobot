

###  第一步

```java
$ git init
```

![会在文件夹里出现.git文件夹](C:\Users\远锋\AppData\Roaming\Typora\typora-user-images\1557728015280.png)

![1557728051742](C:\Users\远锋\AppData\Roaming\Typora\typora-user-images\1557728051742.png)



### 第二步

```java
$ git add *
```

### 第三步

```JAVA
$ git commit -m "第二次提交"
```

### 第四步

```java
$ git remote add origin git@github.com:zjutrobot/zjutrobot.git
```

### 第五步

```java
$ git push origin master
```

![出现错误](C:\Users\远锋\AppData\Roaming\Typora\typora-user-images\1557728244287.png)

**出现错误的原因是你权限不够**

###  解决权限问题

1. 命令

```java
ssh-keygen -t rsa -C "your Email@email.com"
```

2. 一直按回车+yes
3.  会在用户目录文件夹里生成一个.ssh的公钥

![1557728447749](C:\Users\远锋\AppData\Roaming\Typora\typora-user-images\1557728447749.png)



![1557728465863](C:\Users\远锋\AppData\Roaming\Typora\typora-user-images\1557728465863.png)



2. 进入文件夹，用记事本打开，全部复制``id_rsa.pub``文件的内容到GitHub上

3. 登陆GitHub<https://github.com/settings/keys>

4. 点settings---->new ssh key

   



![1557728602302](C:\Users\远锋\AppData\Roaming\Typora\typora-user-images\1557728602302.png)

![1557728677565](C:\Users\远锋\AppData\Roaming\Typora\typora-user-images\1557728677565.png)



# 可能还有报错，这时候不要慌：

这个是因为你远程里GitHub有了一份，发生了冲突，需要merge，这个时候百度一下，merge一下就可以了

解决冲突问题

``git pull --rebase origin master``



![1557728794546](C:\Users\远锋\AppData\Roaming\Typora\typora-user-images\1557728794546.png)

