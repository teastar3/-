# 🛡️ 成长副本 — 30-60-90 学习路径设计器

> 面向 AI Native 组织新人的入职融入工具，以 RPG 游戏化交互引导新人完成 30-60-90 天成长路径。

---

## 🔗 在线体验

👉 **[立即体验](https://ai-hr-tcamp-d8gsa525x18e048e1-1441575288.tcloudbaseapp.com/)**

---

## ✨ 功能

| 模块 | 说明 |
|------|------|
| 🎯 进度环 | 可视化 30/60/90 天整体完成率 |
| 🗺️ 三阶段地图 | 生存期→成长期→贡献期，渐进式解锁 |
| 📋 任务时间线 | 每阶段子任务，勾选标记进度 |
| 📡 技能雷达图 | 六维能力评估 |
| 🏆 成就系统 | 里程碑徽章自动解锁 |
| 🔗 配对码同步 | 跨设备共享进度 |
| 💡 学习指引 | 每阶段方法论建议 |
| 🌙 暗色 RPG 主题 | 沉浸式游戏化体验 |

---

## 🚀 使用方式

纯静态 HTML 文件，下载即用：

```bash
# 直接双击打开
index.html

# 或起个本地服务
npx serve .
python -m http.server 8080
```

> 📌 数据默认保存在浏览器 `localStorage`，关闭后不丢失。
> 如需**跨设备同步**，需自行接入 CloudBase（见下方）。

---

## 🔧 自行接入跨设备同步（可选）

如果你想让多台设备间共享进度：

1. 前往 [CloudBase 控制台](https://console.cloud.tencent.com/tcb) 创建环境
2. 开通「匿名登录」+ 「云函数」+ 「NoSQL 数据库」
3. 部署 `cloudfunctions/progressSync/` 到你的环境
4. 在 `index.html` 中将 `CLOUDBASE_ENV` 改为你的环境 ID
5. 创建 `player_progress` 集合，设置读写权限为 `auth != null`

---

## 📁 项目结构

```
├── index.html          # 主应用（纯前端单文件）
├── cloudfunctions/     # 云函数（仅同步需要，本地使用可忽略）
├── README.md
└── .gitignore
```

---

## 📄 License

MIT
