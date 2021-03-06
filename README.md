# EpidemicAreaManagementSystem
2020年春季学期软件工程大作业：疫区管理系统

## 一、用户角色
### 1、疫区人民
* 按户区分<br> 
* 同一户的任一账号可以上报该户所有人信息（考虑老人不会使用手机情况）<br> 
* 户有隔离户和非隔离户之分，由管理员确认<br> 
* 同一户的任一账号的行为会影响该户的属性（例，采购次数，防护领取等）<br>

### 2、疫区管理员
*	管理员账号应包括人民账号所有属性<br> 
*	管理员有负责的楼层信息（如果隔离户有采购需求，同一栋楼应尽量设置由一名管理员采购，减少楼与楼接触）<br> 

### 3、特殊类：户
*	每一管理员设置的非空户，应当至少有一人实名注册账号<br>
*	户有隔离户、非隔离户和病患户之分，由管理员确认，可按户设置，也可以按栋设置<br>
*	户有是否需要上报体温，和每日是否上报的属性<br>

## 二、基本功能
### 1、健康状况管理
（1）（疫区人民）每日体温及身体状况上报
* 每日有且只有一次上报机会<br> 
* 上报人的体温超过37.5℃时系统向管理员发警告<br> 

（2）（疫区人民）是否与湖北籍人员接触的上报<br> 
（3）（疫区管理员）查看当日上报情况<br> 
（4）（疫区管理员）查看负责区域疫情状况（统计分析）<br> 

### 2、防护用具发放
防护用具包括：口罩、75%消毒酒精、防护服、防护手套<br> 
（1）（疫区人民）防护用具申请领用<br> 
（2）（疫区管理员）防护物资（包括酒精等医用物资）的剩余量查看<br> 
（3）（疫区管理员）批准防护物资申请<br> 

### 3、关系网络管理
（1）（疫区人民）登记关系网络<br> 
（2）（疫区人民）非隔离户外出归家后需要登记此次外出接触过的其他人ID信息<br> 
（3）（疫区管理员）查看病人关系网络<br> 
（4）（疫区管理员）标注状态<br> 

### 4、计算/更新隔离日期
（1）（疫区人民）查看隔离时间及是否处于隔离期状态<br> 
（2）（疫区管理员）查看隔离人员列表<br> 
（3）（疫区管理员）修改隔离时间或隔离状态<br> 
（4）（系统自动）隔离户满隔离时间，且未出现病患，会转为非隔离户<br> 

## 三、附加功能
### 1、人员登记
（1）（疫区管理员）管理员最初按小区情况设置楼号，户号<br>
（2）（疫区管理员）排查后可设置一户为空户（没住人）/非空户<br>
（3）（疫区管理员）可以修改一户人员信息（例、登记疫情期间新来的长期住户）<br>
（4）（疫区人民）选择自己的房间，上传/修改全户人员信息，需要管理员账号确认（排查时）<br>

### 2、隔离户生活物资采购上报
（1）（疫区人民）上报预约管理员设置的生活物资，每户按人数有每日采购上限<br>
（2）（疫区人民）查看可以采购的生活物资及余量<br>
（3）（疫区人民）隔离户人民可以申请特殊物资（例、家中有糖尿病患，要采购特殊药品），管理员可以选择是否能够购买。<br>
（4）（疫区管理员）设置并展示可以采购的物资清单（例、武汉的小区套餐）<br>
（5）（疫区管理员）管理员可以选择是否能够购买特殊物资，同时回复信息<br> 

### 3、信息公开
（1）（疫区管理员）发布社区防控公告
（2）（疫区人民）软件主界面有社区防控公告的推送，全员可查看<br>

## 三、开发分工
### 1、前端：1811359、1811398
### 2、后台：1613415、1613368
服务器：华为云 <br>
OS：centOS <br>
语言：C++ <br>
数据库：mysql<br>
框架：<br>
进度：预计使用框架+协程+连接池完成


### 后端开发指南
### 1.后端框架
https://github.com/yhirose/cpp-httplib

### 2.后端接口规范
### 3.后端构建方式
clone下来以后
mkdir build 
cd build
每次需要构建时在build中执行
cmake ..
make
可执行文件会在build/bin之中
