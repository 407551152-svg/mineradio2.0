# Mineradio

Mineradio 是一款 Windows 桌面沉浸式音乐播放器，融合搜索播放、歌词舞台、桌面歌词、粒子视觉、星河特效、专辑封面粒子和 3D 歌单展示等功能。

本仓库是基于开源项目 Mineradio 的二次开发版本，用于个人学习、功能实验和桌面端音乐播放器体验优化。

## 功能特色

- 沉浸式音乐播放界面
- 歌词舞台与桌面歌词显示
- 外语歌词自动翻译开关
- 多种视觉预设和唱片样式
- 专辑封面粒子叠加
- 星河粒子叠加
- 3D 歌单架与动态视觉效果
- 网易云音乐、QQ 音乐相关搜索与播放体验接入
- Windows 安装包打包与 GitHub Releases 发布

## 下载安装

最新版安装包会发布在 GitHub Releases：

[https://github.com/407551152-svg/mineradio2.0/releases](https://github.com/407551152-svg/mineradio2.0/releases)

如果已经发布 `v1.1.1`，可以直接下载 Windows 安装包：

[https://github.com/407551152-svg/mineradio2.0/releases/download/v1.1.1/Mineradio-1.1.1-Setup.exe](https://github.com/407551152-svg/mineradio2.0/releases/download/v1.1.1/Mineradio-1.1.1-Setup.exe)

> 如果链接暂时打不开，说明对应版本的 Release 还没有上传安装包。请先执行下方打包命令，然后在 GitHub Releases 上传 `dist/` 目录里的安装包。

## 本地开发运行

请先安装 Node.js，然后在项目根目录执行：

```bash
npm install
npm start
```

## 打包 Windows 安装包

```bash
npm run build:win
```

打包完成后，安装包会生成在：

```text
dist/
```

常见文件名类似：

```text
Mineradio-1.1.1-Setup.exe
```

## 发布到自己的 GitHub

确认远程仓库是自己的仓库：

```bash
git remote -v
```

提交代码：

```bash
git add .
git commit -m "Customize Mineradio"
git push
```

创建 GitHub Release 并上传安装包：

```bash
gh release create v1.1.1 ".\\dist\\Mineradio-1.1.1-Setup.exe" --title "Mineradio v1.1.1" --notes "自定义版本发布"
```

发布后，别人就可以通过 Releases 页面下载安装包。

## 更新配置

当前应用内更新配置已经指向：

```text
owner: 407551152-svg
repo: mineradio2.0
```

也就是：

```text
https://github.com/407551152-svg/mineradio2.0
```

如果你以后更换仓库名，需要同步修改 `package.json` 里的 `build.publish` 和 `mineradio.update` 配置。

## 第三方音乐平台说明

本项目不是网易云音乐、QQ 音乐或其他音乐平台的官方客户端，也不隶属于任何音乐平台。项目中的第三方平台接入仅用于个人学习、本地客户端体验和用户自有账号的播放辅助。请遵守对应平台的用户协议、版权规则和会员权益规则。

## 致谢与授权

本项目基于原开源项目 Mineradio 二次开发。感谢原作者和开源社区的基础工作。

本项目遵循原项目许可证发布。请查看 [LICENSE](./LICENSE) 了解具体授权条款。
