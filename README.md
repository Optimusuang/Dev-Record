# Dev-Record
/* Copyright (c) Huawei Technologies Co., Ltd. 2021-2024. All rights reserved. */

PetalPay Development Record

支付用户服务由如下微服务构成

用户注册服务	PetalPayRegisterService	用户第三方授权登录、注册、公共数据查询
用户管理服务	PetalPayCustService	用户基础信息、实名信息、银行卡、额度等信息的管理
用户鉴权服务	PetalPayAuthService	用户鉴权服务，AT、RT的生成与校验

代码目录结构说明
├─auth 用户鉴权微服务
│  ├─deploy 微服务自动部署文件
│  └─src
│      ├─main
│      │  ├─java
│      │  │  └─com
│      │  │      └─huawei
│      │  │          └─petalpay
│      │  │              └─auth
│      │  │                  ├─agent 第三方服务代理
│      │  │                  ├─constant 常量
│      │  │                  ├─controller 接口
│      │  │                  ├─dao 数据库层
│      │  │                  ├─listener 外部消息监听
│      │  │                  ├─model 数据模型
│      │  │                  │  ├─biz 业务数据模型
│      │  │                  │  ├─dto 数据表
│      │  │                  │  ├─req 请求体
│      │  │                  │  └─rsp 响应体
│      │  │                  └─service 业务功能
│      │  └─resources
│      │      ├─config 业务配置
│      │      ├─META-INF 项目拦截器、过滤器、异常处理器等SPI配置
│      │      ├─rootkey 中间件根秘钥
│      │      ├─sds sds mapper 文件
│      │      ├─spring spring文件
│      │      └─sts sts配置文件
│      └─test 测试用例
├─common 项目公共代码
│  └─src
│      ├─main
│      │  ├─java
│      │  │  └─com
│      │  │      └─huawei
│      │  │          └─petalpay
│      │  │              └─member
│      │  │                  ├─cache 缓存处理工具
│      │  │                  ├─config 配置工具
│      │  │                  ├─costant 公共常量
│      │  │                  ├─exception 项目异常定义及处理工具
│      │  │                  ├─log 项目日志相关工具
│      │  │                  ├─model 公共模型
│      │  │                  │  ├─biz 业务数据模型
│      │  │                  │  ├─req 公共请求体
│      │  │                  │  └─rsp 公共响应体
│      │  │                  ├─nuwa nuwa框架相关组件
│      │  │                  ├─serveradapter 服务代理适配
│      │  │                  ├─serveragent 服务代理框架
│      │  │                  ├─service 公共服务能力
│      │  │                  └─util 公共工具
│      │  └─resources
│      └─test
├─customer 用户管理服务
│  ├─deploy 微服务自动部署文件
│  └─src
│      ├─main
│      │  ├─java
│      │  │  └─com
│      │  │      └─huawei
│      │  │          └─petalpay
│      │  │              └─customer
│      │  │                  ├─agent 第三方服务代理
│      │  │                  ├─constant 常量
│      │  │                  ├─controller 接口
│      │  │                  ├─dao 数据库层
│      │  │                  ├─dbshare 分表处理
│      │  │                  ├─event 内部事件监听
│      │  │                  ├─listener 外部消息监听
│      │  │                  ├─model 数据模型
│      │  │                  │  ├─biz 业务数据模型
│      │  │                  │  ├─dto 数据表
│      │  │                  │  ├─req 请求体
│      │  │                  │  └─rsp 响应体
│      │  │                  ├─notify 短信通知
│      │  │                  ├─service 业务功能
│      │  │                  ├─task 定时任务
│      │  │                  └─util 工具方法
│      │  └─resources
│      │      ├─config 业务配置
│      │      ├─mapper mysql mapper文件
│      │      ├─META-INF 项目拦截器、过滤器、异常处理器等SPI配置
│      │      ├─rootkey 中间件根秘钥
│      │      ├─sds sds mapper 文件
│      │      ├─spring spring文件
│      │      └─sts sts配置文件
│      └─test 测试用例
├─db-sql
│  └─1.0.1 版本归档SQL脚本
├─deploy 公共自动部署脚本
├─iac 基础设施即代码脚本
├─register 注册服务
│  ├─deploy 微服务自动部署文件
│  └─src
│      ├─main
│      │  ├─java
│      │  │  └─com
│      │  │      └─huawei
│      │  │          └─petalpay
│      │  │              └─register
│      │  │                  ├─agent 第三方服务代理
│      │  │                  ├─controller 接口
│      │  │                  ├─listener 外部消息监听
│      │  │                  ├─model 数据模型
│      │  │                  │  ├─biz 业务数据模型
│      │  │                  │  ├─req 请求体
│      │  │                  │  └─rsp 响应体
│      │  │                  ├─nuwa nuwa框架相关组件
│      │  │                  ├─serveradapter 服务代理适配
│      │  │                  ├─service 业务功能
│      │  │                  └─task 定时任务
│      │  └─resources
│      │      ├─config 业务配置
│      │      ├─META-INF 项目拦截器、过滤器、异常处理器等SPI配置
│      │      ├─rootkey 中间件根秘钥
│      │      └─spring spring文件
│      └─test 测试用例
└─script iac打包脚本

