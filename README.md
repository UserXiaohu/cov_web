## 一、**项目简介**

当前疫情形势依旧严峻，人们逐渐淡忘了疫情，防范意识不够。本系统基于Flask的防疫宣传网站，加强防疫宣传，督促疫情并未离去，大家不能放松警惕，疫情防控人人有责。

**项目获取地址：http://shiyuncode.com/details?id=42**

## 二、**项目技术**

本项目是基于Python + Echarts + Flask + Layui + MySQL的防疫宣传网站。涉及到的关键技术有Python网络爬虫、使用MySQL做相关数据存储功能、使用Python与MySQL数据库进行交互、使用Flask构建web项目、基于Echarts制作数据可视化展示地图、使用Layui作为后台数据管理可视化框架、 以pycharm作为开发平台。

## 三、**项目功能**

l 首页防疫内容宣传；

l 抗议英雄展示宣传；

l 抗议新闻热点宣传；

l 全国新冠肺炎疫情可视化实时分析；

l 管理员用户对数据爬虫进行启动获取数据；

l 管理员后台管理系统（防疫宣传内容管理、英雄人物管理、新闻热点管理、疫情综合数据管理、数据爬虫、版本信息管理等）

## 四、**功能结构**

![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps1.png)

## 五、**运行截图**

![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps2.jpg) 
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps3.jpg)
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps4.jpg) 
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps5.jpg) 
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps6.jpg) 
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps7.jpg)
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps8.jpg)
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps9.jpg)
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps10.jpg)
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps11.jpg)
![img](file:///https://github.com/UserXiaohu/cov_web/blob/main/img/wps12.jpg) 

 

 

 

 

 

## 六、**数据库设计**

details表

| 字段名称    | 数据类型    | 是否必填 | 注释             |
| ----------- | ----------- | -------- | ---------------- |
| id          | int         | 是       |                  |
| update_time | datetime    | 否       | 数据最后更新时间 |
| province    | varchar(50) | 否       | 省               |
| city        | varchar(50) | 否       | 市               |
| confirm     | int         | 否       | 累计确诊         |
| confirm_add | int         | 否       | 新增治愈         |
| heal        | int         | 否       | 累计治愈         |
| dead        | int         | 否       | 累计死亡         |

hero表

| 字段名称 | 数据类型     | 是否必填 | 注释 |
| -------- | ------------ | -------- | ---- |
| id       | int          | 是       |      |
| name     | varchar(255) | 否       |      |
| info     | varchar(255) | 否       |      |
| filename | varchar(255) | 否       |      |

history表

| 字段名称    | 数据类型 | 是否必填 | 注释         |
| ----------- | -------- | -------- | ------------ |
| ds          | datetime | 是       | 日期         |
| confirm     | int      | 否       | 累计确诊     |
| confirm_add | int      | 否       | 当日新增确诊 |
| suspect     | int      | 否       | 剩余疑似     |
| suspect_add | int      | 否       | 当日新增疑似 |
| heal        | int      | 否       | 累计治愈     |
| heal_add    | int      | 否       | 当日新增治愈 |
| dead        | int      | 否       | 累计死亡     |
| dead_add    | int      | 否       | 当日新增死亡 |

hotsearch表

| 字段名称 | 数据类型 | 是否必填 | 注释 |
| -------- | -------- | -------- | ---- |
| id       | int      | 是       |      |
| dt       | datetime | 否       |      |
| content  | text     | 否       |      |

kinds表

| 字段名称 | 数据类型     | 是否必填 | 注释 |
| -------- | ------------ | -------- | ---- |
| id       | int          | 是       |      |
| title    | varchar(255) | 否       |      |
| content  | longtext     | 否       |      |

sys_user表

| 字段名称 | 数据类型    | 是否必填 | 注释 |
| -------- | ----------- | -------- | ---- |
| id       | int         | 是       |      |
| username | varchar(50) | 否       |      |
| password | varchar(50) | 否       |      |
| name     | varchar(50) | 否       |      |
| email    | varchar(50) | 否       |      |
| phone    | varchar(50) | 否       |      |

sys_version表

| 字段名称    | 数据类型     | 是否必填 | 注释     |
| ----------- | ------------ | -------- | -------- |
| id          | int          | 是       | 系统版本 |
| sys_name    | varchar(255) | 否       | 名称     |
| sys_version | varchar(255) | 否       | 描述     |

**
**
