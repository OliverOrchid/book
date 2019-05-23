#感谢 @supertaohail！！！

# 本地电子书

一款干净美观的本地电子书阅读器，为了世界和平，决定将代码开源，稍加处理，即可实现各种梦幻功能。

#源码中有三本电子书，可复制进手机进行测试



# 效果图

 <img src="https://github.com/supertaohaili/book/blob/master/S80115-180545.jpg" width="300"><img src="https://github.com/supertaohaili/book/blob/master/S80115-180528.jpg" width="300">
 <img src="https://github.com/supertaohaili/book/blob/master/S80115-162828.jpg" width="300"><img src="https://github.com/supertaohaili/book/blob/master/S80115-180602.jpg" width="300">
 <img src="https://github.com/supertaohaili/book/blob/master/S80115-180634.jpg" width="300"><img src="https://github.com/supertaohaili/book/blob/master/S80115-180708.jpg" width="300">
 <img src="https://github.com/supertaohaili/book/blob/master/S80115-180620.jpg" width="300"><img src="https://github.com/supertaohaili/book/blob/master/S80115-180655.jpg" width="300">

apk下载链接
<a href="https://www.coolapk.com/apk/174412">https://www.coolapk.com/apk/174412</a>

# 使用
```
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}

dependencies {
    compile 'com.github.supertaohaili:book:1.0.0'
}
```


示例代码:
``` java
1、获取全部图书：
List<BookList> all = DataSupport.findAll(BookList.class);

2、添加本地图书：
intent = new Intent(this, FileChooserActivity.class);
this.startActivity(intent);

3、删除本地图书：
DataSupport.delete(BookList.class, book.getId());

4、阅读单子书：
ReadActivity.openBook(book, LocalBookshelfActivity.this);
```


第三方及开源框架使用:

```
1、添加了bugly 异常上报与更新，登录https://bugly.qq.com/v2/crash-reporting/dashboard/9bb43e127f?pid=1 申请appid，替换即可

2、添加了友盟统计，可登录http://passport.umeng.com/login ,申请appkey，替换即可

3、上下拉刷新：https://github.com/lcodecorex/TwinklingRefreshLayout（这个稳定，bug少）

4、项目全局使用RecyclerView，适配器的二次封装使用：（支持多种布局）

博客：http://blog.csdn.net/fisher0113/article/details/51955845
     github:https://github.com/fishyer/StudyRecyclerView

5、数据库：使用litepal ，轻量，简单：https://github.com/LitePalFramework/LitePal
```


### Known Issues
If you have any questions/queries/Bugs/Hugs please mail @
taohailili@gmail.com
