# Online Education Backend

[简体中文](README.zh-CN.md)

A multi-module Java backend for online education, built with Spring Boot, MyBatis-Plus and Nacos discovery. It organizes teaching, media and membership into separate services. The initial upload was on October 7, 2020.

| Module | What it contains |
| --- | --- |
| [Education](service/service_edu) | Course, chapter, subject, and teacher APIs. |
| [Content and media](service/service_cms) | Banner management, with separate [object storage](service/service_oss) and [video on demand](service/service_vod) modules. |
| [Membership](service/service_ucenter) | Member accounts, with a separate [SMS module](service/service_msm). |
| [Shared code](common) | Shared service configuration and utilities. |

Start with the [course controller](service/service_edu/src/main/java/top/weidaboy/eduservice/controller/EduCourseController.java) and the [Maven module definitions](service/pom.xml). The parent [POM](pom.xml) targets Java 8. Reproducing the backend requires configuring MySQL, Redis, and Nacos as needed by each module. The media and SMS integrations also require your own provider settings.
