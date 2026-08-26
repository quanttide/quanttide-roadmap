# 量潮工作蓝图

## 仓库定位

量潮工作蓝图（quanttide-roadmap）是量潮知识管理体系中的**蓝图聚合容器**——按主体与领域聚合各业务的工作蓝图子仓库（git submodule）。每个子仓库独立维护，本仓库只追踪引用。

在量潮"正交分解"中，本仓库横跨**主体轴（Who it is）与领域轴（What it expresses）**：`default/` 聚合各法人主体蓝图，`domains/` 聚合各领域蓝图，回答"我们要走向哪里、各领域如何规划"。

## 仓库结构

```
quanttide-roadmap/
├── default/company      → 法人主体蓝图（quanttide-roadmap-of-business-entity）
├── domains/             → 领域蓝图子仓库（git submodule）
│   ├── agent            → 智能体工程蓝图（quanttide-roadmap-of-agent-engineering）
│   ├── asset            → 资产管理蓝图（quanttide-roadmap-of-asset-management）
│   ├── crowd            → 众包管理蓝图（quanttide-roadmap-of-crowd-sourcing）
│   ├── data             → 数据工程蓝图（quanttide-roadmap-of-data-engineering）
│   ├── delib            → 议事管理蓝图（quanttide-roadmap-of-deliberation-management）
│   ├── devops           → DevOps 工程蓝图（quanttide-roadmap-of-devops）
│   ├── execute          → 执行管理蓝图（quanttide-roadmap-of-execution-management）
│   ├── human            → 人力资源蓝图（quanttide-roadmap-of-human-resources）
│   ├── meta             → 元工程蓝图（quanttide-roadmap-of-philosophy）
│   ├── pay              → 支付工程蓝图（quanttide-roadmap-of-payment-engineering）
│   ├── think            → 认知工程蓝图（quanttide-roadmap-of-cognitive-engineering）
│   └── write            → 写作管理蓝图（quanttide-roadmap-of-narrative-engineering）
├── README.md            → 本文件
└── CHANGELOG.md         → 版本变更记录
```

## 子模块管理

- 子模块独立提交推送，本仓库只更新引用指针
- 新增蓝图仓库：`git submodule add <url> default/<path>`（主体蓝图）或 `domains/<path>`（领域蓝图）
- 同步全部子模块：`git submodule update --init --recursive`

## 关联

- 蓝图与日志、档案同源：`assets/quanttide-journal`（工作日志聚合）、`assets/quanttide-profile`（工作档案聚合）
- 分层关系：journal（事实）→ intention（意图）→ profile（档案/叙事），roadmap（规划）指引方向
