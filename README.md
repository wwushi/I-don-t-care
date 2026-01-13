## 自用，项目基于https://github.com/shuaiplus/NodeCrypt
---

## 📋 项目修改记录

- 当鼠标离开页面、页面切换、最小化或进入屏幕共享时，页面内容自动模糊
- 定义昵称库，由系统随机分配昵称
- 平铺分享与退出按钮
- 。。。。。。
## 🔧 项目维护

### 依赖检查
- 项目依赖：158 个包，1 个低风险安全漏洞，不影响项目运行
- 构建工具：Vite 6.3.5（已修复中等风险漏洞）
- 开发服务器：wrangler 4.16.1

### 安全漏洞修复情况
1. **已修复漏洞**：
   - **库**：vite 6.0.0 - 6.4.0
   - **风险等级**：中等
   - **问题**：Vite middleware 可能会服务与公共目录同名的文件、Vite 的 `server.fs` 设置没有应用到 HTML 文件、Vite 在 Windows 上允许通过反斜杠绕过 `server.fs.deny` 设置
   - **修复方法**：运行 `npm audit fix` 命令成功修复

2. **未修复漏洞**：
   - **库**：elliptic （椭圆曲线加密库）
   - **风险等级**：低
   - **问题**：Elliptic Uses a Cryptographic Primitive with a Risky Implementation
   - **现状**：目前没有可用的修复方案，只影响特定加密场景，对项目整体安全性影响较小

### 构建命令
```bash
npm run build
```

### 开发命令
```bash
npm run dev
```

### 部署命令
```bash
npm run deploy
```
