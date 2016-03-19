我们在Android Studio中创建项目后往往会使用版本控制来控制代码,但是项目中哪些文件该提交到版本控制呢?

其实,Android Studio自己已经帮你做好了!

在Project和app下各有一个`.gitignore`文件,如下:

Project下的忽略文件:

```xml
*.iml
.gradle
/local.properties
/.idea/workspace.xml
/.idea/libraries
.DS_Store
/build
/captures
```

app文件夹下的忽略文件:

```
/build
```

以上可以看出:

1. 所有的`.iml`文件都不需要提交
2. `build`文件夹下的文件不需要提交,这是编译文件
3. 本地设置相关文件不需要提交
4. 性能分析时的文件会在/captures文件夹下,也不需要提交

如果你把项目分享到Github上,如下操作:

1. 打开AndroidStudio,创建一个新项目
2. `VCS` ---> `Import into version control` ---> `Share Project on GitHub`

然后AS就会自动选择哪些需要提交到版本控制,如下图:

![总览](http://7xjhi6.com1.z0.glb.clouddn.com/Commit_Test_Total_Commit.png)

![Model](http://7xjhi6.com1.z0.glb.clouddn.com/Commit_Test_Model_App_Commit.png)

![Project](http://7xjhi6.com1.z0.glb.clouddn.com/Commit_Test_Project_Commit.png)

虽然这个知识点很小,但是也需要注意,所以写下来留着以后用吧!

更多文章请移步我的博客:[DevWiki Blog](http://www.devwiki.net)

**重要说明**

想随时获取最新博客文章更新,请关注公共账号DevWiki,或扫描下面的二维码:

![微信公共号](http://7xjhi6.com1.z0.glb.clouddn.com/WeiXin-DevWiki-Common.jpg)
