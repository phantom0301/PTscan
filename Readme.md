# PTScan #

PTscan(Phantom scanner) 是一款界面友好的轻量级web应用资产扫描器，适合于内网渗透测试环境下web的资产快捷识别，只需Python环境，无需第三方扩展库，扫描结果使用zoomeye网页样式。

PTscan参考了F-NAScan的设计思路，在其基础上修改而成，把程序重心放在WEB扫描和识别功能上。

PTscan仅供交流学习使用，请勿用于非法行为。

<img src="http://phantom0301.cc/achiveimg/20170901103835.jpg" style="position: relative;left: 50%;transform: translate(-50%,0%);" />


## Features ##

-  快速扫描，支持多线程
-  Web banner识别功能
-  外网使用环境下支持IP反查（反查接口调用次数有限制）
-  原生Python编写，无需第三方库
-  支持IP段扫描，支持文件导入
-  Banner库支持扩展（fingerprint.py）

## Usage ##

    Usage: python PTscan.py {-f /xxx/xxx.txt or -h 192.168.1} [-p 21,80,3306]  [-m 50] [-t 10] [-n] [-b] [-r]
    
    -f  指定扫描目标文件，文件格式如list.txt所示，同时支持IP和URL
    -h  指定扫描IP或IP段，支持段扫描，如192.168.1 即为扫描C段
    								192.168 即为扫描B段
    -p  指定扫描端口，缺省使用程序中的配置端口
    -m  指定线程数
    -t  指定timeout
    -n  不进行ping操作，直接扫描
	-b  开启Banner识别
	-r  ReverseIP

扫描结果样例

![](http://phantom0301.cc/achiveimg/20170901103356.jpg)

## Update1.0 ##

1. 新增banner识别，测试指纹库为fingerprint.py，后续指纹正在添加中
2. 修改可视化样式，使用zoomeye风格

## Update2.0 ##

1. 修复opt参数错误
2. 增加IP反查功能
3. 集成whatweb指纹
4. 增加目标文件导入功能


### Other ###

Issues submit
