# 故障处理

和其它软件一样，Zettlr可能会在某处出现一些问题。本页面包含有关如何解决这些问题的说明。我们现在有四年的问题处理经验，因此，在大多数情况下，下面列出的方案可以解决您遇到的问题。

> 在Discord、Reddit、QQ或GitHub上提出问题之前，请您首先尝试此处本页的步骤，并参考常见问题解答（FAQ）。您问题的提出与解决便是我们更新的最大动力！

## 1. 尝试关闭并重启Zettlr

这可能听起来微不足道，但通常情况下，关闭并重启Zettlr（或是重启电脑）可以解决你所遇到绝大多数问题。

> 当你总是遇到同一个问题，并且该问题*往往*是在你执行特定操作后才出现时，你可能发现了一个我们从未发现的**BUG**。当且仅当这种情况下,请毫不犹豫地在GitHub上创建一个issue，并为我们提供一个关于如何重现该问题最简方法。之后，我们将想办法修复它。

## 2. 重新安装最新版本

当我们发现一个问题时,通常会第一时间修复它,并在一段时间后发布新版本。所以请确保您的Zettlr总是更新到最新版本，（因为旧版本确实有bug）！

## 3. Zettlr设置初始化

我们已经多次接到反馈——应用程序**似乎**出现如无法启动等问题。在这种情况下，清除缓存通常会有所帮助——这与Zettlr所使用的Electron框架有关。它会生成自己的缓存文件，但是我们没有任何控制的手段，只能靠删除这些缓存文件来解决该问题。

同时，由于Zettlr维护本地设置和元数据(如用户自定义的标签、工作空间位置、设置)，因而在某些情况下，您可能需要重置、读取或修改此数据(例如，您的安装已损坏，抑或是您意外加载了错误的工作区等等)。这些数据位于应用程序数据的存储路径中，其位置取决于您的操作系统：

* **Windows:** `C:\Users\<your username>\AppData\Roaming\Zettlr` (请注意， AppData 是一个隐藏文件夹, 你需要改变资源管理器的设置来显示它)
* **macOS:** `/Users/<your username>/Library/Application Support/Zettlr` (打开Finder窗口，按住“Alt”，同时打开“Go”菜单，然后点击出现的“Library”条目)
* **Linux:** `/home/<your username>/.config/Zettlr` (注意 `.config` 是一个隐藏文件夹，你需要使用命令行打开它)

如果您希望重置您的Zettlr，请遵循以下步骤：

1. 确保Zettlr已经**彻底**关闭(在某些错误情况下，将出现一个“僵尸”进程，您可以从任务管理器或活动监视器中将其关闭)
2. 确保有选择地备份以下文件：

   * `stats.json` (你的写作统计数据)
   * `config.json` (应用设置 —— 包括您的工作区位置以及打开文件列表)
   * `custom.css` (您的私人定制 CSS （如果有的话）)
   * `tags.json` (您的彩色编码标签)
   * `targets.json` (您的写作不表)
   * `user.dic` (您的私人词典)
3. 选择并删除该目录下的所有内容
4. 重新启动应用程序（这些文件将被重新创建）

## 4. 向社区求助

如果上述步骤都没有帮助，您可以向社区进行咨询。我们在 [Zettlr Reddit](https://www.reddit.com/r/Zettlr) 和 [Discord](https://discord.com/invite/PcfS3DM9Xj) 上的社区都很活跃，你可以任选其一进行求助。

## 5. 创建一个Github Issue

如果社区也无法解决你的问题，或者经过讨论后你们发现该问题似乎由程序Bug造成，请在Github上常见一个Issue。请您尽可能地对您所遇到的问题进行更加详细的描述，以便我们能更加顺利地解决该问题。

> 如果您在GitHub上创建了一个Issue，请确保您收到我们的通知。开发者总是在第一时间会对您的Issue提出一些相关问题。您的答复越快，我们就能更加全面地了解并解决问题。如果无人回答，可能表示我们并不确定如何帮助您。在这种情况下，请您对问题进行重新表述，或是添加其他有用的信息。

## 6. 将Zettlr回退到较早版本

有时侯，创建一个Issue并等待其解决可能会阻碍你的工作效率。一些用户决定将Zettlr回退到以前的版本，直到我们能够解决该Issue。在这一节中，我们将为您提供一些建议，告诉你在这种情况下什么可能是重要的，以及这样做可能会出什么问题。

虽然我们的主页只显示最新的稳定版本，但即使是远古版本，您也可以在我们的 [GitHub发布页面](https://github.com/Zettlr/Zettlr/releases)上轻松找到。通常，您无需做任何准备工作，只需运行相应版本的安装程序，即可安装任何版本的Zettlr。实际上，安装程序总是首先删除所有已安装的程序，然后再安装您下载的对应版本。因而将被替换的只是你的Zettlr程序，而非数据(记住：不是数据)。

也就是说，有时，我们会在更新期间更新配置(这只能单向工作)。因此，如果您恰好回退到该版本，您的配置可能会损坏。在这种情况下，您只需要关闭应用程序(如果它没有崩溃)，删除`config.json`文件(见上文)，然后再次启动Zettlr即可。**切记，在回退到较早的版本之前，请始终备份您的数据!!!**
