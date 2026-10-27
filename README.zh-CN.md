<p align="center">
  <img src="docs/images/banner-3-steps.png" width="800" alt="Community app for Clean Your TV. Clean your TV from your phone. No laptop. No coding agent. Open the app on your Android phone, tap Start, choose what to switch off, and your TV gets a calmer home screen." />
</p>

<p align="center">
  <a href="https://github.com/udhaykumarbala/cleanyourtv-app/releases/latest"><img src="https://img.shields.io/github/v/release/udhaykumarbala/cleanyourtv-app?style=flat&color=E8A84C&labelColor=15181e" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/TVs-131%20models%20%C2%B7%2046%20brands-E8A84C?style=flat&labelColor=15181e" alt="131 TV models from 46 brands">
  <img src="https://img.shields.io/badge/phone-Android%209%2B-E8A84C?style=flat&labelColor=15181e" alt="Android 9 or newer">
  <a href="LICENSE"><img src="https://img.shields.io/badge/licence-MIT-E8A84C?style=flat&labelColor=15181e" alt="MIT licence"></a>
</p>

<h3 align="center">一个由社区维护的手机应用，专为 <a href="https://github.com/Gathin23/cleanyourtv">Clean Your TV</a> 而设计。<br>不需要电脑、不需要编码代理、不需要接线，任何人都可以在手机上清理自己的电视。</h3>

<p align="center">
  <a href="https://github.com/udhaykumarbala/cleanyourtv-app/releases/latest"><b>下载 APK</b></a> ·
  <a href="https://apps.obtainium.imranr.dev/redirect?r=obtainium://add/https://github.com/udhaykumarbala/cleanyourtv-app"><b>通过 Obtainium 安装</b></a> ·
  <a href="#how-it-works"><b>它如何工作</b></a> ·
  <a href="#safe-by-design"><b>它是否安全？</b></a> ·
  <a href="#supported-tvs"><b>支持的电视</b></a>
  <br><sub>Obtainium 会自动跟随 GitHub 上的发布版本并完成更新。</sub>
</p>

<p align="center">
  <img src="docs/images/connect-analyse-clean-hd.gif" width="800" alt="Three steps: connect, analyse, clean. The app finds the TV, checks what is installed, and applies a safer home screen setup from the phone." />
</p>

## 它如何工作

| 1. 连接 | 2. 分析 | 3. 清理 |
| :-: | :-: | :-: |
| <img src="docs/images/phone-connect.png" width="220" alt="Connect to the TV: the TV asks whether to trust this phone; tick Always allow, then choose OK"> | <img src="docs/images/phone-what-we-found.png" width="220" alt="The phone scans the TV and shows the plan: what to switch off and what to keep"> | <img src="docs/images/phone-do-it.png" width="220" alt="Tap Start and the app performs the clean-up on the TV"> |
| 应用会在同一 Wi‑Fi 网络中发现你的电视，并引导你在电视上允许手机接入。 | 它会读取电视当前状态，展示清理计划：哪些应用和功能将被关闭，哪些会被保留。任何变更在此之前都不会执行。 | 你只需确认计划，然后点击“立即清理”，应用就会把相关设置发送到电视上。 |

**你需要：** 一部 Android 手机（Android 9 及以上，且已设置屏幕锁定），并与电视处在同一 Wi‑Fi 网络中。
[下载 APK](https://github.com/udhaykumarbala/cleanyourtv-app/releases/latest) 后打开安装即可。
首次连接通常需要约 1 分钟（通过遥控器打开网络调试功能，应用会一步步引导你），整个清理过程大约 5 分钟。

之后，你可以随时恢复单个应用、检查电视更新后的残留项、修改 dock 或界面外观，或者撤销全部调整。

## 两种清理电视的方式

[Clean Your TV](https://github.com/Gathin23/cleanyourtv) 为任何 Android TV 提供更安静、减少广告的主屏，并关闭无用的系统和应用“臃肿内容”，其清理规则由社区共同维护和测试。它本身需要电脑：你可以运行脚本，或者把指令交给 AI 编码代理。
这个应用则能从你的手机直接完成整套工作。

| | Clean Your TV 仓库 | **Clean Your TV 应用**（本仓库） |
| :- | :- | :- |
| **你需要** | 一台装有 ADB 的电脑，或类似 Claude Code 的编码代理 | **只需要一部与电视同 Wi‑Fi 的 Android 手机** |
| **你需要做的事** | 运行脚本，或把提示词交给代理 | **点击开始，检查计划，然后点“让它变干净”** |
| **适合谁** | 业余玩家、主题作者、电视列表维护者 | **每个人**：你、你的父母、你的朋友 |

两者都会提供相同的 Clean Your TV 主屏与社区维护的电视列表：都能关闭不想要的应用而不卸载它们，并保留恢复入口，方便日后撤销。

## 安全设计

- **每一步都可见。** 在你确认计划之前，应用不会执行任何命令；“自定义”页面会按顺序展示所有将要发送到电视的指令。
- **不会删除任何东西。** 应用会在主用户侧关闭应用，而不是卸载，因此这些应用都可以恢复。Wi‑Fi、Play 商店、遥控器、电视输入源和 Android 必需的系统组件都会被保护，永远不会被触碰；辅助功能、投屏、语音与更新只有在你明确选择时才会关闭。
- **任何调整都可以撤销。** 你可以恢复单个应用，也可以从还原点恢复全部内容。"保存副本" 会导出纯文本还原脚本，可以在任何带 ADB 的电脑上运行，即使没有这个应用也能使用。
- **电视端守护程序。** 如果手机在 150 秒内没有确认新主屏（例如 Wi‑Fi 中断、手机没电），电视会自动恢复自己的主屏。
- **风险区域会更加谨慎。** 对于已知切换主屏可能存在问题的电视，应用只会执行清理并明确说明原因。
- **隐私保护。** 没有账号、没有分析、没有广告。应用只会和你的电视通信，并在你主动请求时才会连接 GitHub 以检查更新。网络调试会在结束时关闭，除非你手动保留开启状态。

## 支持的电视

**131 个型号，覆盖 46 个品牌**，来自 Clean Your TV 社区维护的列表：TCL、Sony、小米、海信、飞利浦、亚马逊 Fire TV、松下、XGIMI、BenQ、NVIDIA Shield、onn、Google 等等，适用于 Android TV、Google TV 和 Fire OS。
如果某个型号还没有被列出，应用仍会根据品牌信息进行保守清理，并在信息有限时给出更谨慎的处理。

<details>
<summary>详细信息</summary>

- **配置文件：** TCL（24 个型号）、Sony（17）、小米（17）、海信、飞利浦、亚马逊 Fire TV、松下、XGIMI、BenQ、NVIDIA Shield、Skyworth、Haier、CHiQ、onn、Google、Vestel 生产机型（JVC、Toshiba、Cecotec）、Freebox Player 等，覆盖 Android TV、Google TV、Fire OS 以及 TCL 中国版构建。每个配置文件都会标注测试者。
- **品牌回退机制：** 对于没有配置文件的 Amazon、Hisense、Panasonic、Philips、Sony、TCL、XGIMI 和 Xiaomi 机型，应用只会关闭各品牌配置中一致认同的内容，并提示当前处于谨慎模式。更多设置可以在“自定义”中手动调整。
- **其他 Android 电视** 会获得更稳妥的主屏，并只建议那些确定无误的操作。
- **仅清理模式**（电视保留自己的主屏，并说明原因）：Fire TV、TCL 中国版构建、Android 7、应用不认识的厂商主屏、Chromecast with Google TV 和 Google TV Streamer（切换主屏会带来较高的投屏成本）、Kalley 和 PRISM+ 机型（设置向导会在每次开机时出现）、以及设置向导必须保留开启的电视。
- **网络调试：** 电视需要通过网络访问 ADB（端口 5555）。对于只提供无线调试配对码的电视，需要先用电脑配对一次；应用会展示三条命令。
</details>

**你的电视不在支持列表中？** 电视列表由 Clean Your TV 维护，因此它能帮助每个人——无论是否使用这个应用。你可以按照其
[贡献指南](https://github.com/Gathin23/cleanyourtv/blob/main/CONTRIBUTING.md) 把你的电视添加进去，然后在下一次应用更新时自动同步。
另见 [CONTRIBUTING.md](CONTRIBUTING.md#propose-a-tv-profile)。

## 构建于 Clean Your TV 之上

- 主屏由 [Gathin](https://github.com/Gathin23) 的 [Clean Your TV launcher](https://github.com/Gathin23/cleanyourtv/tree/main/launcher) 提供。这个应用内部打包了它，并使用其源码构建。
- Clean Your TV 的新电视列表和启动器版本会通过更新同步到这个应用。它本身是一个社区项目；关于 Clean Your TV 的最新消息可查看 [@gathint](https://x.com/gathint)。
- Clean Your TV 的名称，以及应用中位于 `tv.cleanyour` 下的包 ID（由 `cleanyour.tv` 派生）已获得 Gathin 明确授权。
- 应用本身出现问题？[在这里提交 issue](https://github.com/udhaykumarbala/cleanyourtv-app/issues)。
  安全问题请见 [SECURITY.md](SECURITY.md)。

<details>
<summary><b>隐私详细说明</b></summary>

- 没有账号、没有分析、没有广告、没有崩溃上报服务。
- 在你的家庭网络中，应用只会和你选择的电视通信（ADB，端口 5555），并监听电视广播（mDNS）。
- 在互联网上，它只会在你主动请求时连接 GitHub："检查更新" 会发出一次最新版本请求，可选附加组件会从 GitHub release 下载。启动器和电视进度屏位于 APK 内，因此正常设置过程中不会产生网络请求。
- 电视信任的密钥存储在手机的 Android Keystore 中，绝不会离开手机。还原点保存在手机本地，除非你自行保存副本。
- "报告问题" 和 "帮助添加此电视" 会先展示完整报告，移除地址、序列号、密钥和代码，然后由你自行决定是否分享或发布到 GitHub。
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
[CONTRIBUTING.md](CONTRIBUTING.md) 介绍了测试、截图对照、模块规则以及发行版如何构建和签名。
应用设计与评审记录见 [docs/history](docs/history/README.md)，每个版本的更新说明见 [CHANGELOG.md](CHANGELOG.md)。

该应用是在人工审查下，由 AI 编码代理协作开发：维护者负责设定设计并进行审阅和测试，而每次修改都经过自动化测试与代码审查。

## 致谢

- [Clean Your TV](https://github.com/Gathin23/cleanyourtv) 由 [Gathin](https://github.com/Gathin23) 及其社区贡献者维护，其启动器、清理列表和测试报告构成了本应用的基础。
- ADB 协议代码起源于 [dadb](https://github.com/mobile-dev-inc/dadb)（mobile.dev，Apache 2.0，见 [adb/wire/NOTICE](adb/wire/NOTICE)）。
- [Outfit](https://github.com/Outfitio/Outfit-Fonts) 字体（SIL Open Font License 1.1）。

完整名单见：[THIRD-PARTY-NOTICES](THIRD-PARTY-NOTICES)。许可证： [MIT](LICENSE)，与 Clean Your TV 一致。
