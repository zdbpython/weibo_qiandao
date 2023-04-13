# weibo_qiandao
微博 签到 青龙面板 python 

自动签到关注的微博超话，
这个脚本可以自动遍历选择的超话，并对每个超话进行签到操作。
在签到之间添加随机等待时间，以避免触发微博的反作弊机制。

使用方法：

青龙面板运行
安装相关依赖

1,选择 依赖管理 -> python, 选择右上角 新建依赖, 添加	requests
![image](https://user-images.githubusercontent.com/66553745/231680733-c6e3a8d7-8ac2-4afb-8e24-18acbac05ca9.png)

2,添加脚本

选择 脚本管理, 点击右上角 + 按钮, 类型 空文件, 文件名自定义即可，暂定为 weibo_checkin.py，注意后缀必须添加。点击确定完成新建。

3,添加代码

点击左侧 weibo_checkin.py, 点击右上角编辑按钮，将仓库中的 weibo_checkin.py 文件中的内容全部复制过去，然后点击保存

4,添加相关环境变量

点击 环境变量, 点击 新建变量，
名称weibo_cookie, 自动拆分选 否, 值填PC浏览器获取到的值，请自行百度如何获取https://weibo.com/网页的cookies，多个cookies建立多个同名weibo_cookie环境变量即可。
名称weibo_chaohua_id，自动拆分选 否，值填PC浏览器获取到的值，例如易烊千玺超话，值填写p/和/super_index之间的数字。多个weibo_chaohua_id建立多个同名weibo_chaohua_id环境变量即可。
例如：
https://weibo.com/p/1008087d4c56ccdd21d10f32eea97a29975b52/super_index，填写008087d4c56ccdd21d10f32eea97a29975b52

5，添加定时任务

点击 定时任务， 点击右上角新建任务，名称自定义即可，输入命令

 task weibo_checkin.py
设置自己想要的定时，点击确定保存

测试是否成功

在任务操作一栏，直接点击运行按钮，然后查看日志
