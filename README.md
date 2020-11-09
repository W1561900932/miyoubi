# 近期有关公告  
因为本人最近破事很多，可能要等待到1月份才有时间更新了（当然也欢迎大佬们提交pr），如果急需的话推荐以下项目：  
https://github.com/jianggaocheng/mihoyo-signin/tree/61881edf0ba41d0134fa0b4d183b30541fd6c073  
虽然该项目的最新版本支持github action，但是本人并不推荐，目前mhy对本项目封杀力度挺大的（对比隔壁原神签到），用action的话可能会导致ip异常而被mhy发现的概率提高（特别是在原神项目热度如此高的情况下），为了该项目的可持续性，请有条件的用户尽量搭建本地版本  
最后感谢所有为本项目做出贡献的人！

# 恭喜你发现了宝藏！
此版本会继续维护并添加更多反爬虫处理和更多功能  

此版本目前已实现：

米游币任务全部完成！

自动完成全板块点赞收藏回帖任务！

~~自动发帖（已实装至崩坏3水区 现仅提供崩坏3水区发帖模块）~~ （存在风控，待修复）

# 用前必看

此程序**严禁**分享到**nga 贴吧 米游社**等**大型社交平台**大面积传播  
具体原因可以看一下master版本的更新日志


# miyoubi
这是一个一键完成米游社的米游币的python程序

## 功能

只需要输入一次cookies就可以完成米游社所有米游币任务

登录失效会弹出提示  

理论上cookies有效期为一年但是只有米哈游才知道cookies有效期有多长  

软件分为无提示版和有提示版，区别在软件完成任务时是否弹出已完成的提示框  
无提示版建议放在电脑计划任务里可以自动完成
（本项目提供无提示版下载）

**自动完成点赞收藏任务**

## 食用方法

1 到下载miyoubi.py 编译版本请到目录里dist文件夹里下下载

并打开米游社官网https://bbs.mihoyo.com/bh3/

2，重新登录米游社（已登录的要退出重新登录）  

3，按F12打开控制台，并输入以下代码  

javascript:(function(){var a=function getCookie(name){var strCookie=document.cookie;var arrCookie=strCookie.split("; ");for(var i=0;i<arrCookie.length;i++){var arr=arrCookie[i].split("=");if(arr[0]==name)return arr[1]}return""};var b={};b.a=a("account_id");b.b=a("login_ticket");alert(JSON.stringify(b))})()  

4，复制弹窗中 b冒号后的内容 注意**不含**冒号和引号（如图）  

![b](https://github.com/lhllhx/miyoubi/blob/master/b.png)

5，输入到程序里面 等待数分钟

6，完成！（有提示版本会弹出成功提示）  

注意：当你需要更改账号信息或初始化程序时，请删除同目录下的cookies.dat文件

## 开发相关

软件使用python3.7编写并使用PyInstaller打包

第三方模块：  requests  

源文件为miyoubi.py 其他为编译副产物

## 更新日记
2020.5.10  
~~摸了很多天，差点忘了。。。~~  
其实早就改好了，为了稳定性测试了很多天，没有问题

2020.4.30  
发现自从4.29开始 浏览帖子和完成点赞任务失效，原因排查中  
而且回帖和发帖模块因太水的缘故被ban几率很高（我两个号都被ban了），正在想办法解决，现阶段解决办法为暂时屏蔽 

2020.3.21  
修复分享模块功能 更新反爬虫处理  
实装发帖模块

2020.3.18  
更新反爬虫处理  
更新发帖模块（未实装）

2020.3.13  
增加反爬虫处理 防检测和封禁

2020.2.28  
增加发帖模块（未实装）

2020.2.19  
实现全板块签到点赞收藏任务  
新增评论功能

2020.2.17  
全板块签到实现

2020.2.15  
修复bug  

2020.2.14  
创建项目

