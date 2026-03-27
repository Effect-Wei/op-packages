# 🚀 Serverless OpenWrt APK Repository

基于 **GitHub Actions** 和 **Cloudflare R2** 打造的**零成本、全自动、全球 CDN 加速**的自定义 OpenWrt 软件源。

> ⚠️ **注意**: 本项目专为 OpenWrt **25.12 及以上版本** 设计，使用全新的 Alpine `apk` 包管理器。如果你使用的是旧版 OpenWrt (`opkg`)，请勿使用此方案。

---

## 💻 OpenWrt 客户端配置

在你的 OpenWrt SSH 终端中执行以下步骤：

**1. 导入公钥**
将公钥放入路由器的授信目录中：
```bash
wget -qO /etc/apk/keys/effectw.pub https://oppkg.effects.space/effectw.pub
```

**2. 添加软件源**
```bash
echo "https://oppkg.effects.space/$(cat /etc/apk/arch)/packages.adb" >> /etc/apk/repositories.d/customfeeds.list
```

**3. 更新并安装**
```bash
apk update
# 享受极速的包管理体验！
apk add luci-theme-argon
```
