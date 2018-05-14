# Gradle
关于AndroidStudio的Gradle配置笔记

## 第三方aar中引用的Android的版本冲突
### 例如Glide4.7.1使用的com.android.support是27.0.3，而我的项目使用的是26.0.1，有一下三种解决办法

1、升级自己的版本到27.0.2 

2、降级Glide到 4.3.1

3、使用exclue排除冲突 

前两种不用讲，我们来说下最后一种

<pre>
<cod>

implementation('com.github.bumptech.glide:glide:4.7.1') {
        exclude group: "com.android.support"
}

</cod>
</pre>
