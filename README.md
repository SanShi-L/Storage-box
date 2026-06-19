# 小忆收纳 · Spoke Storage

用网页技术做的「物品收纳记忆」原型 App。

> 上传时请把本文件夹里的 `index.html`、`xiaoshi.png`、`manifest.webmanifest`、`service-worker.js`、`CNAME` 和 `icons/` 一起上传，否则手机安装图标或离线缓存可能不完整。

## 用 GitHub Pages 发布

### 方法 A：网页操作

1. 登录 GitHub，进入仓库。
2. 点 **Add file -> Upload files**，把本文件夹里的所有文件一起拖进去，然后点 **Commit changes**。
3. 点仓库顶部 **Settings -> Pages**。
4. **Build and deployment -> Source** 选 **Deploy from a branch**。
5. **Branch** 选 `main`，文件夹选 `/ (root)`，点 **Save**。

如果使用当前自定义域名，Pages 的 **Custom domain** 填：

```text
app.lxlsanshi.site
```

## 命令行发布

```bash
git add index.html xiaoshi.png manifest.webmanifest service-worker.js CNAME icons README.md
git commit -m "Make app installable on mobile"
git push
```

## 在手机上像 App 一样使用

本项目已经加入 PWA 配置。手机浏览器打开发布网址，选择分享，然后点 **添加到主屏幕**。桌面会出现「小忆收纳」图标，点开后会以独立 App 窗口运行。

发布后的地址：

```text
https://app.lxlsanshi.site
```

如果 DNS 还没有生效，可以先用 GitHub Pages 默认地址访问。

## 修改后重新发布

本 `index.html` 是打包产物。需要大改功能时，建议回到原项目编辑源文件，重新打包后再覆盖这里的 `index.html`。
