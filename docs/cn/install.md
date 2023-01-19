# 安装说明

Zettlr是跨平台的，它可以在大多数电脑上运行。同时安装步骤也非常简单，在不同操作系统上（如macOS,Windows以及各类Linux发行版）均可一步到位。

> 请注意，受支持平台（特别是支持**macOS和Linux**）的版本可能随时发生变化。如果您使用的操作系统不受支持，或是使用时遇到问题，可以点击[此处](https://www.electronjs.org/docs/tutorial/support#supported-platforms)查看最新的受支持平台列表。

## Windows 7 或更高版本

我们只需从[下载页面](https://www.zettlr.com/download)下载并打开安装包，即可在Windows上安装Zettlr。如果您希望为使用该计算机的所有用户安装Zettlr，它将被安装到`C:\Program Files`目录。在这种情况下，您必须在安装过程中赋予其管理员权限(它将会自动请求)。如果您仅为当前登录用户安装，则不需要任何权限。

> 请注意，在可能的情况下，我们建议您为使用该计算机的所有用户安装Zettlr。如果您只为当前用户安装该应用程序，Zetllr的某些功能(如您最近的文档)将不起作用。当然，如果你不需要这些功能(或你没有该计算机管理权限)，你可以只为你自己安装本应用程序。

若要卸载Zettlr，您只需从安装目录运行uninstall.exe，或者在系统设置中使用添加/删除程序界面。如果您想完全删除与Zettlr相关的所有数据，则还需要删除目录`C:\Users\<your-user-name>\AppData\Roaming\Zettlr`。

> 注意，在撰写本文档时，Windows ARM 安装程序还没有捆绑 Pandoc。这意味着Zettlr导出可能不起作用。你必须手动安装Pandoc。如果你电脑上安装了Pandoc, Zettlr for Windows ARM 将自动识别并使用该文件。

## macOS 10.11 或更高版本

我们只需从[下载页面](https://www.zettlr.com/download)下载并打开安装包,并拖动Zettlr图标到应用程序目录，即可在macOS上安装Zettlr。

若要卸载Zettlr，只需从你的应用程序目录中删除Zettlr.app即可。如果要完全删除与Zettlr关联的所有数据，还需删除目录`/Users/<your-user-name>/Library/Application Support/Zettlr`。

> 你也可以借助[Homebrew](https://formulae.brew.sh/cask/zettlr)安装Zettlr:`$ brew install --cask zettlr`

## Linux

### Debian/Ubuntu/Fedora及其衍生品

Zettlr有预先构建的deb (Debian 8/Ubuntu 12.04或更新版本)和rpm (Fedora 24或更新版本)包。您可以使用相应的包管理器安装它们，或者从我们的[下载页面](https://www.zettlr.com/download)进行下载。

若要卸载Zettlr，请遵循删除包所需的常见步骤(通常通过图形安装程序应用程序或通过dpkg)。如果您还想删除与Zettlr关联的所有数据，请同时删除`/home/<your-user-name>/.config/Zettlr`目录

### Arch Linux

Arch Linux 有两个社区维护的包可用。[Zettlr](https://archlinux.org/packages/?name=zettlr) 包包含最新版本应用程序; [Zettlr-git](https://aur.archlinux.org/packages/zettlr-git/) AUR包则代表GitHub的最新提交。您可以在[Arch wiki 相关文章](https://wiki.archlinux.org/title/Zettlr)中找到更多信息。

> 请注意，这些软件包是由社区维护的，我们不对其稳定性、安全性或提供的版本承担任何责任。

### AppImage

在[下载页面](https://www.zettlr.com/download),您可以以`AppImage`包的形式下载适用于Linux系统的Zettlr。关于如何安装AppImage包，请参考[本指南](https://appimage.org/)。

### Flatpack

Zettlr也可以通过[Flatpack](https://flathub.org/home)进行安装。你可以在[Zettlr的FlatHub页面](https://flathub.org/apps/details/com.zettlr.Zettlr)上找到响应安装说明。[Flatpack仓库](https://github.com/flathub/com.zettlr.Zettlr)可以在GitHub上找到。任何关于Flatpack的问题,请直接在该仓库（而不是Zettlr的主仓库）进行提问。

> **注意**：如果您通过Flatpack安装Zettlr，最初Zettlr只能访问文件系统的很小一部分。除读写`Documents`目录之外的任何目录都将无法工作。您可以使用诸如[Flatseal](https://flathub.org/apps/details/com.github.tchx84.Flatseal)等拓展包，来授予Zettlr对计算机的其他部分的访问权限。

## 更新Zettlr

在您每次启动Zettlr时，应用程序都会检查是否有新的更新。您也可以通过使用帮助菜单中的对应选项手动触发搜索更新。如果有新版本可用，Zettlr会显示一个对话框，其中包含新版本的编号、您的当前版本和一个包含所有功能和错误修复的更新日志。

若要进行更新，您只需单击适合您系统的版本(64位版本或ARM版本)。之后Zettlr将自动开始下载合适的安装程序到您的下载文件夹中。下载完成后，点击“开始更新”，Zettlr将退出并重新打开最新版本文件。

您可以在我们的下载页面上找到与**Zettlr自动下载**相同的文件。若要进行手动更新，只需下载相应的安装程序并运行即可。它将自动覆盖现有版本，但仍然保留您的配置。

> 如果您对前沿版本感兴趣，可以点击首选项对话框，并选中高级选项卡中的“通知我有关测试版的版本”复选框。之后Zettlr还将为你提供测试版本，虽然它可能不像常规版本那样完善，但你可以比其他人更早了解并使用Zettlr的新功能！

## Nightly 版本

从2.0.0版本开始，我们推出了 Nightlt 版本。Nithgly是每周五中午(UTC,协调世界时)自动发行的版本（但有时我们会手动构建）。Nightly由最新修改的代码库构建而来（这意味着它甚至比beta版本新），但这也意味着它可能包含我们还没有发现的严重错误。

Nightly版本仅适用于了解并愿意承担风险的资深用户。如果您有定期备份设置、写作统计、文件的习惯，那么理论上使用Nightly版本将是十分安全的。**我们由衷感谢每一个使用Nightly，并进行BUG反馈的用户**。

若希望安装Nightly版本，您需要从<https://nightly.zettlr.com/>手动下载。注意，由于Nightly版本每周五自动更新，因此你并不会像常规版本那样收到更新提示。

>**注意**：我们并不保证Nightly版本的稳定性。由于该版本是自动构建的，因此如果我们在自动构建开始之前不小心引入了一个严重的BUG，并在一个小时后对其进行了修复，那么本周的Nithtly将包含该错误。通常最坏的情况下，这些错误会对你的操作系统造成损坏，导致应用程序无法正常启动，在这种情况下，你必须退回到之前的版本。通过使用Nightly版本，我们默认您已经了解并愿意承担这些风险。

另外请注意，我们并不保留任何Nightly之前的版本。Nightly的每周构建都将会取代前一周的内容。如果Nightly无法使用，请随时与我们联系，以便我们在修复错误后手动安排新的构建。

