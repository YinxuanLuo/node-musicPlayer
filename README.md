# node-musicPlayer（已归档）

> **这是 `musicPlayer` 的部署版，不是独立项目。** 前端部分与 `musicPlayer` 逐文件一致。

2019 年毕业设计把音乐播放器上线到 LeanCloud 云引擎时，把 `musicPlayer` 的前端产物
原样搬进了 `static/`，外面套了这一层 Express + LeanEngine 的壳，另外加了一个
"此 APP 仅用于毕业设计" 的首屏页。

**真正属于本仓库的代码只有 `server.js` 的约 20 行部署逻辑**，其余全部与 `musicPlayer` 重复。
因此：

- 前端源码、构建方式、运行方式 → 请看 [`musicPlayer`](https://github.com/YinxuanLuo/musicPlayer)
- 部署思路也已摘录进 `musicPlayer` 的 README
- 本仓库已归档，只作为历史留存

## 🔑 安全提醒

本仓库历史上 `server.js` 明文硬编码过 LeanCloud 的 appId / appKey / **masterKey**，
且仓库是公开的。现在代码里已改为只读环境变量，但**那组密钥仍然存在于 git 历史中**。

> 如果那个 LeanCloud 应用还在使用，**请立刻到 LeanCloud 控制台作废并重新生成密钥**。
> 同类问题也出现在 `express` 仓库（那边同样已改成读环境变量）。

## 本地运行（如需）

```bash
npm install
cp .env.example .env    # 填入自己的密钥
npm start               # 默认 http://localhost:3000
```
