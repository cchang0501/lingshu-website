# 灵枢连接 - Obsidian 插件

AI 驱动的笔记连接发现工具，自动发现笔记之间的深层关联。

## 📁 项目结构

```
obsidian-plugin/
├── src/                    # 源代码
│   ├── api/               # API 相关
│   ├── cache/             # 缓存管理
│   ├── errors/            # 错误处理
│   ├── utils/             # 工具函数
│   ├── views/             # 视图组件
│   ├── main.ts            # 主插件
│   └── settings.ts        # 设置
├── docs/                   # 文档
│   ├── development/       # 开发文档
│   ├── guides/            # 使用指南
│   ├── reports/           # 历史报告
│   └── archive/           # 归档文档
├── tests/                  # 测试
│   ├── api/               # API 测试
│   ├── cache/             # 缓存测试
│   ├── concurrent/        # 并发测试
│   ├── integration/       # 集成测试
│   └── utils/             # 工具测试
└── scripts/                # 构建脚本
```

## 功能特性

- 🤖 **AI 智能分析**：使用 AI 自动发现笔记之间的深层连接
- ⚡ **智能缓存**：本地缓存分析结果，秒开连接
- 🔄 **自动重试**：网络错误自动重试，提高可靠性
- 📊 **可视化展示**：侧边栏展示所有连接，一目了然
- 🎯 **精准匹配**：基于内容相似度的智能推荐

## 安装

### 方法 1：手动安装（推荐）

1. 下载最新的 `main.js`、`manifest.json` 和 `styles.css`
2. 在 Obsidian vault 中创建文件夹：`.obsidian/plugins/lingshu-connections/`
3. 将下载的文件复制到该文件夹
4. 重启 Obsidian
5. 在设置中启用"灵枢连接"插件

### 方法 2：从源码构建

```bash
# 克隆仓库
git clone https://github.com/your-repo/obsidian-lingshu-plugin.git
cd obsidian-lingshu-plugin

# 安装依赖
npm install

# 构建
npm run build

# 复制到 Obsidian 插件目录
cp main.js manifest.json styles.css /path/to/vault/.obsidian/plugins/lingshu-connections/
```

## 使用方法

### 1. 获取 API Token

1. 访问 [灵枢网站](https://lingshu-app.pages.dev/index_zh.html)
2. 登录你的账号
3. 打开浏览器开发者工具（F12）
4. 在 Console 中输入：
   ```javascript
   localStorage.getItem('lingshu_auth_token')
   ```
5. 复制返回的 Token

### 2. 配置插件

1. 打开 Obsidian 设置
2. 找到"灵枢连接"插件设置
3. 粘贴 API Token
4. 点击"测试连接"确认配置正确

### 3. 分析笔记

1. 打开任意笔记
2. 使用命令面板（Ctrl/Cmd + P）
3. 运行"分析当前笔记"命令
4. 等待 AI 分析完成
5. 在侧边栏查看发现的连接

## 命令

- **分析当前笔记**：分析当前打开的笔记，发现连接
- **清除缓存**：清除所有本地缓存数据
- **查看缓存统计**：查看缓存使用情况

## 性能优化

### 智能缓存

- 自动缓存分析结果，24 小时有效
- 内容变化时自动失效
- 离线时使用缓存数据

### 自动重试

- 网络错误自动重试（最多 3 次）
- 指数退避策略，避免服务器压力
- 友好的错误提示

## 安全说明

⚠️ **重要提示**：

- 请勿将 API Token 分享给他人
- Token 有效期 30 天，过期后需重新获取
- 建议定期更换 Token
- 如果 Token 泄露，请立即在网站退出登录

## 开发

```bash
# 安装依赖
npm install

# 开发模式（自动重新构建）
npm run dev

# 生产构建
npm run build
```

### 文档

- **开发文档**: `docs/development/` - 竞品分析、优化路线图等
- **使用指南**: `docs/guides/` - 调试指南、测试指南
- **历史报告**: `docs/reports/` - Bug 修复、测试总结等

### 测试

```bash
# API 测试
node tests/api/test-api.js

# 缓存测试
node tests/cache/test-cache-logic.js

# 集成测试
node tests/integration/test-full-flow.js
```

## 技术栈

- TypeScript
- Obsidian API
- esbuild

## 版本历史

### v1.0.0 (2025-10-24)

- ✨ 首次发布
- 🤖 AI 智能分析
- ⚡ 智能缓存系统
- 🔄 自动重试机制
- 📊 可视化连接展示

## 许可证

MIT

## 支持

如有问题或建议，请访问：
- 网站：https://lingshu-app.pages.dev
- GitHub：https://github.com/your-repo/obsidian-lingshu-plugin

---

**Made with ❤️ by Lingshu Team**
