# 安心伴 — AI老人陪伴与家庭健康守护系统（后端）

这是一个基于 Spring Boot 的后端服务，用于支撑“安心伴”微信小程序的老人端与家属端闭环功能。

## 功能覆盖
- 老人端：陪聊记录、情绪评分、认知筛查记录、用药记录、紧急呼叫
- 家属端：今日状态面板、趋势分析、异常提醒、对话摘要
- 风险评分：按给定公式计算并汇总日维度评分

## 技术栈
- Java 17
- Spring Boot 3.2.x
- Spring Data JPA
- MySQL

## 快速开始
1. 配置数据库连接：修改 `src/main/resources/application.yml`
2. 创建数据库：如 `anxinban`
3. 启动项目：`mvn spring-boot:run`

## 关键接口示例
- 老人端陪聊记录：`POST /api/elder/chat`
- 认知记录：`POST /api/elder/cognition-records`
- 用药记录：`POST /api/elder/medication-records`
- 家属端今日状态：`GET /api/family/today-status?userId=1`
- 家属端趋势分析：`GET /api/family/trends?userId=1&days=7`
- 家属端异常提醒：`GET /api/family/alerts?userId=1`

## 数据库表
项目已内置实体映射，可使用 JPA 自动建表（`spring.jpa.hibernate.ddl-auto=update`）。
你也可以使用 `schema.sql` 手动建表。
