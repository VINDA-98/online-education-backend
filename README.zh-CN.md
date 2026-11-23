# 在线教育系统后端

[English](README.md)

在线教育系统的 Java 多模块后端，首次上传于 2020 年 10 月 7 日。项目使用 Spring Boot、MyBatis-Plus 和 Nacos 服务发现。

| 模块 | 内容 |
| --- | --- |
| [教务](service/service_edu) | 课程、章节、课程分类和讲师接口。 |
| [内容与媒体](service/service_cms) | 轮播图管理，并独立划分了[对象存储](service/service_oss)和[视频点播](service/service_vod)模块。 |
| [会员](service/service_ucenter) | 会员账号，另有独立的[短信模块](service/service_msm)。 |
| [公共代码](common) | 各服务共用的配置和工具类。 |

可以从[课程控制器](service/service_edu/src/main/java/top/weidaboy/eduservice/controller/EduCourseController.java)和 [Maven 模块定义](service/pom.xml)开始看。[父 POM](pom.xml) 指定 Java 8。复现时需要按模块配置 MySQL、Redis 和 Nacos，媒体与短信集成还需要使用自己的服务商配置。
