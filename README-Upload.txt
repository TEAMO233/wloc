# Apple WLOC — Surge 从 URL 安装版（TEAMO233/wloc）

这是由 2026-10-11 的 Loon 备份改造后的独立 Surge 版本，**不是**社区版。

## 部署方法：只上传三个文件

1. 打开 https://github.com/TEAMO233/wloc ，确保位于 main 分支。
2. 在仓库根目录点击 Add file -> Upload files。
3. 把本 ZIP 中的以下三个文件拖进去（不要传 ZIP 本身，也不要传 README）：
   - Apple-WLOC-Converted.sgmodule
   - wloc-surge-converted.js
   - wloc-settings-converted.js
4. 点击 Commit changes 保存。不会覆盖现有的 modules/wloc.sgmodule、dist/wloc.js 等文件。
5. Surge -> 模块 -> 从 URL 安装，粘贴：

https://raw.githubusercontent.com/TEAMO233/wloc/main/Apple-WLOC-Converted.sgmodule

## 安装后

开启 MITM / HTTPS 解密，正确安装并信任 Surge 根证书；启用脚本功能和 VPN。
默认没有已保存坐标时自动透传；旧 Loon 持久化数据没有包含在备份中。

可由 Surge 本地脚本拦截的设置接口：
- 保存位置：https://gs-loc.apple.com/wloc-settings/save?lon=121.4737&lat=31.2304&acc=25
- 查询位置：https://gs-loc.apple.com/wloc-settings/save?action=query
- 清除位置：https://gs-loc.apple.com/wloc-settings/save?action=clear

上面的设置接口不是 Apple 官方接口。实际定位成效取决于 iOS 版本、证书、系统缓存、Apple 定位服务变化。

原作者标注 Yu9191 Rewrite；原项目代码总体分发许可尚未核实。
