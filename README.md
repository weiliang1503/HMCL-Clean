# HMCL 簡潔版

由於原版的 HMCL 包含了很多（作為一個 Linux 用戶與開源愛好者來看）實在是多余/不純淨的功能，本項旨在刪去這些功能，得到一個純淨的 Minecraft **啓動器**。
目前刪除的部分即原因：
- 贊助信息（一堆東西看著很不爽）
- 使用開發版的主頁提示（我用開發版不用你提醒）
- 多人聯機功能（使用的技術不開源且不免費，不建議使用）
- 自我升級功能（升級功能可以交由系統包管理進行，另外本項目也沒能力再維護一個升級源）
- 反饋功能（可以直接去 github 開 issue）

除這些之外，HMCL 的功能應當正常運作。如果出現問題歡迎提 issue 與 pr。

本人並非專業的 java 開發者，不排除解決不了問題的情況。

# ⛏ Hello Minecraft! Launcher 💎
[![Build Status](https://ci.huangyuhui.net/job/HMCL/badge/icon?.svg)](https://ci.huangyuhui.net/job/HMCL)
![Downloads](https://img.shields.io/github/downloads/huanghongxun/HMCL/total)
![Stars](https://img.shields.io/github/stars/huanghongxun/HMCL)
[![Discord](https://img.shields.io/discord/995291757799538688.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/jVvC7HfM6U)
[![KOOK](https://img.shields.io/badge/KOOK-HMCL-brightgreen)](https://kook.top/Kx7n3t)

English | [中文](README_cn.md)

## Introduction
HMCL is a cross-platform Minecraft launcher which supports Mod Management, Game Customizing, Auto Installing (Forge, Fabric, Quilt, LiteLoader and OptiFine), Modpack Creating, UI Customization, and more.

HMCL has amazing cross-platform capabilities.
It can not only run on different operating systems such as Windows, Linux, and macOS, 
but also supports multiple CPU architectures such as x86, arm, mips, and loongarch.
You can easily play Minecraft on different platforms through HMCL.

For systems and CPU architectures supported by HMCL, see [this table](PLATFORM.md).

## Download
Download the latest version from [the official website](https://hmcl.huangyuhui.net/download).

Note: The recent versions released in GitHub are beta versions, which contains extra testing functions compared to the release versions on the official website. However, they may be unstable and you're more likely to encounter bugs or unexpected problems.

Although not necessary, it is recommended to download the ones from the official website.

## License
The software is distributed under [GPLv3](https://www.gnu.org/licenses/gpl-3.0.html) with additional terms.

### Additional terms under GPLv3 Section 7
1. When you distribute a modified version of the software, you must change the software name or the version number in a reasonable way in order to distinguish it from the original version. (Under [GPLv3, 7(c)](https://github.com/huanghongxun/HMCL/blob/11820e31a85d8989e41d97476712b07e7094b190/LICENSE#L372-L374))

   The software name and the version number can be edited [here](https://github.com/huanghongxun/HMCL/blob/javafx/HMCL/src/main/java/org/jackhuang/hmcl/Metadata.java#L33-L35).

2. You must not remove the copyright declaration displayed in the software. (Under [GPLv3, 7(b)](https://github.com/huanghongxun/HMCL/blob/11820e31a85d8989e41d97476712b07e7094b190/LICENSE#L368-L370))

## Contribution
If you want to submit a pull request, there are some requirements:
* IDE: Intellij IDEA
* Compiler: Java 1.8
* Do NOT modify `gradle` files

### Compilation
Simply execute the following command in project root directory:

```bash
./gradlew clean build
```

Make sure you have Java installed with JavaFX 8 at least. Liberica Full JDK 8 or later is recommended.

## JVM Options (for debugging)
| Parameter                                    | Description                                                  |
| -------------------------------------------- | ------------------------------------------------------------ |
| `-Dhmcl.self_integrity_check.disable=true`   | Bypass the self integrity check when checking for update.    |
| `-Dhmcl.bmclapi.override=<version>`          | Override API Root of BMCLAPI download provider, defaults to `https://bmclapi2.bangbang93.com`. e.g. `https://download.mcbbs.net`. |
| `-Dhmcl.font.override=<font family>`         | Override font family.                                        |
| `-Dhmcl.version.override=<version>`          | Override the version number.                                 |
| `-Dhmcl.update_source.override=<url>`        | Override the update source.                                  |
| `-Dhmcl.authlibinjector.location=<path>`     | Use specified authlib-injector (instead of downloading one). |
| `-Dhmcl.openjfx.repo=<maven repository url>` | Add custom Maven repository for download OpenJFX.            |
| `-Dhmcl.native.encoding=<encoding>`          | Override the native encoding.                                |
| `-Dhmcl.microsoft.auth.id=<App ID>`          | Override Microsoft OAuth App ID.                             |
| `-Dhmcl.microsoft.auth.secret=<App Secret>`  | Override Microsoft OAuth App secret.                         |
