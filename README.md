# 小白接口+微信小程序示例一
众所周知，小程序搭配小白接口简直就是BUG一样的存在。不花一分钱就能发布自己的专属小程序。免费套餐强大到足以支撑一个私人小应用啦。 可免费调用15万次/月真的是很良心了。

**前端靠微信，后端靠小白！**

话不多说 源码如下[https://github.com/WillFang1997/Code](https://github.com/WillFang1997/Code)

1.下载好源码之后需配置服务器域名，已配置过的可以跳过这一步。

首先，需要登录微信公众号平台，进入：设置 - 开发设置 - 服务器域名，修改request合法域名，uploadFile合法域名，修改为你当前所在的小白接口域名。小白接口已支持HTTPS访问。如下：
![在这里插入图片描述](http://cdn7.phalapi.net/20180325091907_c20c1b1cb2a0f9822c4faad47557be7c)

特别注意！在微信服务器域名配置request合法域名时，一定要注意，域名前后不能有空格，最后不能有斜杠！！
否则会出现类似以下的错误提示：
![在这里插入图片描述](http://cdn7.okayapi.com/20180820224318_af9c1b0360728a590ce0879a2a6f0c93.png)
如果不清楚自己所在的域名，可登录小白开放平台，进入：[系统设置 - 我的套餐](http://open.yesapi.cn/?r=App/Mine)，查看接口域名。如：
![在这里插入图片描述](http://cdn7.phalapi.net/20180325092043_7568a614a5ac0011c2eaafa8ca473754)
2.配置好之后用微信小程序开发者工具打开源码
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190410232055437.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
点击授权登录后会看的以下页面
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190410232320408.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
接下来做一步十分重要的操作，打开根目录下的app.js拉到下面，把okayapiHost，okayApiAppKey，okayApiAppSecrect填写成自己的信息，在[系统设置 - 我的套餐](http://open.yesapi.cn/?r=App/Mine)查看，记得是**https**不是http
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190410233038109.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
现在离完成整个部署只差**填充后端数据**了！
打开源代码目录下CSV文件夹里modelBulid.csv。查看该程序需要的六个模型并添加相应字段。
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019041112331355.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411123403497.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
现在带大家[建第一个模型tea_swiper](http://open.yesapi.cn/?r=Data/MyModelsCreate)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411124126799.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
之后在[我的模型数据](http://open.yesapi.cn/?r=Data/MyModelsManager)内找到模型点击管管模型并加入modelBuild.csv文件内的字段名称/类型/备注
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411124526213.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411124818450.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
然后添加数据，如无想放在轮播图的照片可以按照tea_swiper.csv内的地址添加。添加后效果如图。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411125156580.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
接下来点击开发者工具-编译，即可看到轮播图已经成功调用啦！！！（您的小程序已经成功调用出放在小白数据库的数据了）
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019041112543320.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
细心的同学会发现tea_user里面也已经拿到了登录的人的微信昵称以及openID，新用户登录这个小程序并且授权，就会新增一条数据。（微信的openID是微信用户唯一标识符，如有需求也可以增加省份，语言，用户头像等字段记录用户信息，调整模型跟pages/login.js代码即可）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411130107303.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
接下来根据CSV文件夹里的tea.csv按操作添加相应的数据即可拥有自己的小程序啦（小白会员可直接用该csv文件导入到数据库哦（疯狂暗示）），tea_user，tea_order,tea_shopcar以及tea_moment都不用添加数据，下订单，发朋友圈等操作会自动添加。最终效果如下。![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411131910500.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411131922979.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411131947796.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411132011254.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/201904111320314.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20190411132040671.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjkzMjM2OQ==,size_16,color_FFFFFF,t_70)
开源不易，需要鼓励。您的支持就是我们最大的前进动力！


PowerByYesAPI
