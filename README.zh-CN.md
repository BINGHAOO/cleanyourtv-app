<p align="center">
  <img src="docs/images/banner-3-steps.png" width="800" alt="Community app for Clean Your TV. Clean your TV from your phone. No laptop. No coding agent. Open the app on your Android phone, tap Start, choose what to switch off, and your TV gets a calmer home screen." />
</p>

<p align="center">
  <a href="https://github.com/udhaykumarbala/cleanyourtv-app/releases/latest"><img src="https://img.shields.io/github/v/release/udhaykumarbala/cleanyourtv-app?style=flat&color=E8A84C&labelColor=15181e" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/TVs-131%20models%20%C2%B7%2046%20brands-E8A84C?style=flat&labelColor=15181e" alt="131 TV models from 46 brands">
  <img src="https://img.shields.io/badge/phone-Android%209%2B-E8A84C?style=flat&labelColor=15181e" alt="Android 9 or newer">
  <a href="LICENSE"><img src="https://img.shields.io/badge/licence-MIT-E8A84C?style=flat&labelColor=15181e" alt="MIT licence"></a>
</p>

<h3 align="center">一个由社区维护的手机应用，专为 <a href="https://github.com/Gathin23/cleanyourtv">Clean Your TV</a> 而设计。<br>任何人都可以清理电视：不需要笔记本电脑、不需要编码代理，也不需要连接线。</h3>

<p align="center">
  <a href="https://github.com/udhaykumarbala/cleanyourtv-app/releases/latest"><b>下载</b></a> ·
  <a href="https://apps.obtainium.imranr.dev/redirect?r=obtainium://add/https://github.com/udhaykumarbala/cleanyourtv-app"><b>通过 Obtainium 安装</b></a> ·
  <a href="#how-it-works"><b>它如何工作</b></a> ·
  <a href="#safe-by-design"><b>是否安全？</b></a> ·
  <a href="#supported-tvs"><b>支持的电视</b></a>
  <br><sub>Obtainium 会跟随这个应用的 GitHub 发布版本并自动更新。</sub>
</p>

<p align="center">
  <img src="docs/images/connect-analyse-clean-hd.gif" width="800" alt="Three steps, phone and TV side by side. 1 Connect: the app finds the TV and the TV asks to allow the phone. 2 Analyse: the phone reads the TV and shows the plan. 3 Clean: the phone sends the commands and the TV gets a calmer home screen." />
</p>

## 它如何工作

| 1. 连接 | 2. 分析 | 3. 清理 |
| :-: | :-: | :-: |
| <img src="docs/images/phone-connect.png" width="220" alt="Look at the TV: the TV asks whether to trust this phone; tick Always allow, then choose OK"> | <img src="docs/images/phone-what-we-found.png" width="220" alt="Phone reads the TV and shows the plan: what turns off and what stays on"> | <img src="docs/images/phone-do-it.png" width="220" alt="Tap Start and the app sends the commands to the TV"> |
| 应用会在 Wi‑Fi 中找到你的电视，并在电视上显示允许手机连接的操作指引。 | 它会读取电视当前状态，并展示清理计划：哪些内容会关闭，哪些内容会保留。任何变更都不会立刻生效。 | 你只需确认计划，然后点“立即清理”，应用就会执行对应设置。 |

**你需要** 一部 Android 手机（Android 9 及以上，且已设置屏幕锁定）并与电视处于同一 Wi‑Fi 网络。
[下载 APK](https://github.com/udhaykumarbala/cleanyourtv-app/releases/latest) 并打开安装即可。
连接通常需要大约一分钟（你需要使用遥控器打开网络调试功能；应用会引导你完成），整个清理过程大约五分钟。

之后你可以随时恢复某个应用、检查电视更新后的残留项、修改 dock 或界面外观，或者撤销所有已做更改。

## 两种清理电视的方式

[Clean Your TV](https://github.com/Gathin23/cleanyourtv) 为任何 Android TV 提供更安静、更少广告的主屏，并关闭无用 bloat（臃肿应用），使用的是其社区测试过的列表。它本身需要电脑：你需要运行脚本，或者将指令交给编码代理。
而这个应用则能从你的手机直接完成整套操作。

| | Clean Your TV 仓库 | **Clean Your TV 应用**（本仓库） |
| :- | :- | :- |
| **你需要** | 一台装有 ADB 的电脑，或者像 Claude Code 这样的编码代理 | **只需一部与电视同 Wi‑Fi 的 Android 手机** |
| **你做什么** | 运行脚本，或把提示词交给代理 | **点击开始，检查计划，然后点“让它变干净”** |
| **适合谁** | 业余玩家、主题和新电视列表维护者 | **每个人**：你、你的父母、你的朋友 |

两者都会提供相同的 Clean Your TV 主屏与社区电视列表，都会关闭应用但不卸载它，并保留每一次修改的回退入口。

## 安全设计

- **你能看到每一步。** 在你确认计划之前，任何命令都不会执行；“自定义”界面会按顺序展示应用将发送的所有命令。
- **不会删除任何东西。** 应用会在主用户侧关闭应用，而不是卸载，因此这些应用都能恢复。Wi‑Fi、Play 商店、遥控器、电视输入源和 Android 需要的关键功能会被保护，永远不会触碰；辅助功能、投屏、语音和更新只有在你选择时才会关闭。
- **任何改动都能撤销。** 可以恢复单个应用，也可以从还原点恢复全部内容。"保存副本" 会导出可直接在任何带 adb 的电脑上运行的纯还原脚本，即使没有这个应用也能用。
- **电视端守护程序。** 如果手机在 150 秒内没有确认新主屏（例如 Wi‑Fi 断开、手机没电），电视会自动恢复自己的主屏。
- **谨慎处理风险区域。** 对于已知可能由切换主屏造成问题的电视，应用只会执行清理，并说明原因。
- **隐私保护。** 没有账号、没有分析、没有广告。应用只会和你的电视通信，并在你主动请求时才会连接 GitHub 获取更新。网络调试会在结束时关闭，除非你手动保留开启状态。

## 支持的电视

**131 个型号，覆盖 46 个品牌**，来自 Clean Your TV 社区列表：TCL、Sony、小米、海信、飞利浦、亚马逊 Fire TV、松下、XGIMI、BenQ、NVIDIA Shield、onn、Google 等等，适用于 Android TV、Google TV 和 Fire OS。
如果某个型号还没有记录，应用仍会根据品牌进行谨慎清理，并在可用信息有限时给出保守处理。

<details>
<summary>详细信息</summary>

- **配置文件：** TCL（24 个型号）、Sony（17）、小米（17）、海信、飞利浦、亚马逊 Fire TV、松下、XGIMI、BenQ、NVIDIA Shield、Skyworth、Haier、CHiQ、onn、Google、Vestel 生产机型（JVC、Toshiba、Cecotec）、Freebox Player 等，支持 Android TV、Google TV、Fire OS 以及 TCL 的中国版构建版本。每个配置文件都会标注测试者。
- **品牌回退机制：** 对于没有配置文件的 Amazon、Hisense、Panasonic、Philips、Sony、TCL、XGIMI 和 Xiaomi 机型，应用只会关闭每个品牌配置中一致认同的内容，并提示当前处于谨慎模式。更多设置可以在“自定义”中手动调整。
- **其他 Android 电视** 会获得主屏，并且只建议那些非常确定的操作。
- **仅清理模式**（电视保留自己的主屏，并说明原因）：Fire TV、TCL 中国版构建、Android 7、应用不认识的厂商主屏、Chromecast with Google TV 和 Google TV Streamer（切换主屏会导致投屏成本过高）、Kalley 和 PRISM+ 机型（其设置向导会在每次启动时出现）、以及设置向导必须保留开启的电视。
- **网络调试：** 电视需要通过网络访问 ADB（端口 5555）。对于只提供无线调试配对码的电视，需要先用电脑配对一次；应用会展示三条命令。
</details>

**你的电视不在列表里？** 电视列表由 Clean Your TV 维护，因此它们会帮助每个人——无论是否使用这个应用。你可以按照其
[贡献指南](https://github.com/Gathin23/cleanyourtv/blob/main/CONTRIBUTING.md) 把你的电视添加进去，然后在下一次应用更新时自动同步。
另见 [CONTRIBUTING.md](CONTRIBUTING.md#propose-a-tv-profile)。

## 建立在 Clean Your TV 之上

- 主屏由 [Gathin](https://github.com/Gathin23) 的 [Clean Your TV launcher](https://github.com/Gathin23/cleanyourtv/tree/main/launcher) 提供。这个应用将其打包在内，并使用其源码构建。
- Clean Your TV 的新电视列表和启动器版本会通过更新进入这个应用。该应用是一个社区项目；关于 Clean Your TV 本身的消息来自 [@gathint](https://x.com/gathint)。
- Clean Your TV 名称，以及应用中位于 `tv.cleanyour` 下的包 ID（由 `cleanyour.tv` 派生）已获得 Gathin 授权。
- 应用本身出现问题？[在这里提交 issue](https://github.com/udhaykumarbala/cleanyourtv-app/issues)。
  安全问题请见 [SECURITY.md](SECURITY.md)。

<details>
<summary><b>隐私详细说明</b></summary>

- 没有账号、没有分析、没有广告、没有崩溃上报服务。
- 在你的家庭网络里，应用只会和你选择的电视通信（ADB，端口 5555），并监听电视自我广播（mDNS）。
- 在互联网上，它只会在你主动请求时连接 GitHub："检查更新" 会发出一次最新版本请求，可选附加组件会从 GitHub release 下载。启动器和电视进度屏位于 APK 内，因此正常设置过程中不会发生联网请求。
- 电视信任的密钥存储在手机的 Android Keystore 中，绝不会离开手机。还原点保存在手机本地，除非你自行保存副本。
- "报告问题" 和 "帮助添加此电视" 会先展示完整报告，移除地址、序列号、密钥和代码，然后才由你自行分享或发布到 GitHub。
- 权限：网络、网络状态、Wi‑Fi 组播（用于发现电视）、在执行电视操作时的前台服务、通知、屏幕锁定提示。没有定位、存储、相机或联系人权限。
- 完整政策： [PRIVACY.md](PRIVACY.md)，也发布在 [cleanyour.tv/app/android/privacy](https://cleanyour.tv/app/android/privacy)。
</details>

<details>
<summary><b>检查下载是否可信</b></summary>

每个发行版都使用同一个密钥签名，其证书 SHA-256 为（也可见 [docs/release-signer.sha256](docs/release-signer.sha256)）：

```
eaf7af3867bb29ff4bb038854842c93f42ffe4198a087e611cb18f925201cd65
```

```bash
sha256sum cleanyourtv-0.2.0.apk                 # 与发行说明中的文件比对
apksigner verify --print-certs cleanyourtv-0.2.0.apk
```

Android 会拒绝任何使用其他密钥签名的更新，因此首次安装后，后续更新都会自动检查。构建过程可复现：每个发布标签都会由 CI 从公开源码构建未签名 APK，而 `scripts/verify-release.sh` 会校验发布的 APK 与该构建结果加签名后的内容完全一致。
</details>

## 面向开发者

```bash
git clone --recurse-submodules https://github.com/udhaykumarbala/cleanyourtv-app.git
cd cleanyourtv-app
./gradlew check assembleDebug        # 需要 JDK 21 和 Android SDK
```

这是一个使用 Kotlin 和 Jetpack Compose 开发的应用，它直接与电视的 ADB 通信，不需要中间的电脑。
[CONTRIBUTING.md](CONTRIBUTING.md) 介绍了测试、截图基线、模块规则以及发行版本如何构建和签名。
应用设计与评审记录见 [docs/history](docs/history/README.md)，每个版本的更新说明见 [CHANGELOG.md](CHANGELOG.md)。

该应用在人工审查下由 AI 编码代理协作开发：维护者负责设定设计并进行审阅和测试，每次修改都经过自动化测试与代码审查。

## 致谢

- [Clean Your TV](https://github.com/Gathin23/cleanyourtv) 由 [Gathin](https://github.com/Gathin23) 及其社区贡献者维护，其启动器、清理列表和测试报告构成了本应用的基础。
- ADB 协议代码起源于 [dadb](https://github.com/mobile-dev-inc/dadb)（mobile.dev，Apache 2.0，见 [adb/wire/NOTICE](adb/wire/NOTICE)）。
- [Outfit](https://github.com/Outfitio/Outfit-Fonts) 字体（SIL Open Font License 1.1）。

完整名单见：[THIRD-PARTY-NOTICES](THIRD-PARTY-NOTICES)。许可证： [MIT](LICENSE)，与 Clean Your TV 一致。
