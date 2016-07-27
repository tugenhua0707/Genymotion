## Genymotion安卓模拟器进行webview的调式代码

#### 1. 首先下载virtualbox 配置安装环境，下载地址：
https://www.virtualbox.org/wiki/Downloads；
#### 下载完后进行安装即可；
#### 2. 然后下载 Genymotion; 下载地址：https://www.genymotion.com/download/
#### 3. 安装完成后，点击进入后，出现如下图所示的界面：
#### <img src="http://images2015.cnblogs.com/blog/561794/201607/561794-20160725232621184-1194337373.png"/>
#### 4. 点击 accept 进行账号登陆，登陆成功后，我们可以点击上面的add按钮，添加一些设备(建议添加4.3以上的设备，
因为自带了google浏览器，这样的话，我们使用浏览器运行网页的时候就可以打开inspect对代码进行调试)；比如如下：
#### <img src="http://images2015.cnblogs.com/blog/561794/201607/561794-20160726234023903-920994762.png" alt="" />
#### 我已经增加了一个Google Nexus-4.1.1 的设备模拟器；
#### 5. 点击start按钮，我们就可以运行模拟器了；比如如下我运行完成后，打开铜板街的wap官网；如下：
#### <img src="http://images2015.cnblogs.com/blog/561794/201607/561794-20160725232930028-1224347670.png" alt="" />
#### 6. 在chrome浏览器运行 about:inspect 可以看到我们的设备了；如下：
#### <img src="http://images2015.cnblogs.com/blog/561794/201607/561794-20160726233827997-1474082648.png" alt="" />
#### 7. 当我们在安卓模拟器上使用浏览器打开网页的时候，我们自己的电脑的chrome下的inspect就有访问的记录，我们
只要点击inspect即可对代码调式，如下所示：
#### <img src="http://images2015.cnblogs.com/blog/561794/201607/561794-20160726234427216-404394008.png"/>

### Charles / Fiddler
#### 线上的代码如何调式？我们可以使用代理的方式，在mac系统下使用 Charles，在window下使用Fiddler即可；
但是我们可以看到上面使用模拟器调式一般的网页并没有什么作用，因为我们直接可以使用浏览器进行调式，和使用一些代理工具
进行调式线上的js和css文件即可，但是在webview下，调用webview下的某个方法的时候在一般的浏览器会报错，这个时候
我们可以使用Genymotion安卓模拟器进行代码调式了；
#### 1. 安装百度等助手软件；先进入模拟器的 系统设置——> 安全 -> 勾选未知来源 ，然后进入自带的浏览器进行百度
下载百度助手，安装完成后，我们可以打开百度助手，下载一些app或者游戏都可以；
#### <img src="http://images2015.cnblogs.com/blog/561794/201607/561794-20160727225313341-860998155.png" alt="" />  
#### 如上图；我们可以在模拟器中打开铜板街app，之后我们可以使用chrome的 inspect调式网页的css样式，或者使用
charles或者fiddler监听css文件或者js文件，进行文件替换功能替换成本地的js或者css文件；相对来说调式webview
的方法比较方便；
### 注意：那么在本地开发的安卓下的webview，我们可以叫安卓开发帮我们打包一个apk文件给我们，然后我们把apk拖动到
### 我们的模拟器就可以进行安装了，安装成功后，我们就可以预览效果，及对webview的css和js代码使用代理软件
### fiddle或者charles代理本地文件的代码了；
