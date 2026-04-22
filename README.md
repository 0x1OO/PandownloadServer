# PandownloadServer - 专业百度网盘高速下载服务系统

![Go Version](https://img.shields.io/badge/Go-1.25.0-blue.svg) ![Gin Framework](https://img.shields.io/badge/Gin-1.10.1-red.svg) ![License](https://img.shields.io/badge/License-Commercial-green.svg) ![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen.svg)

---

## 产品简介

**PandownloadServer** 是专业的Pandownload后台系统，支持多账号轮询、卡密创建、分发下载。**核心功能：** 多账号轮询（支持添加多个百度账号，自动轮询切换，避免单账号限流）、卡密创建（批量生成卡密，支持按次数、按流量、按时间计费）、分发下载（支持最新版Pandownload客户端，实现满速下载）
---

## 系统架构

```mermaid
graph LR
    A[用户客户端] --> B[使用卡密验证]
    B --> C{请求类型}
    C --> D[下载请求]
    C --> E[获取直链]
    D --> F[多账号轮询]
    E --> F
    F --> G[百度网盘API]
    G --> H[返回下载链接/直链]
    H --> A
    
    style A fill:#e1f5ff
    style H fill:#ffe1e1
```

---

## 技术支持与系统部署
**wx**：nbsl20
