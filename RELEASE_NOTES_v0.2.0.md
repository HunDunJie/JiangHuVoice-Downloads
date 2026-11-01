# JiangHuVoice Reader 0.2.0 Windows 测试版

这是首个可安装的 Windows 发行版。它只有一个 Reader，Basic 和 Standard
是可独立安装、卸载和升级的本地引擎/模型包。

## 推荐安装方式

下载 `JiangHuVoice-Setup-0.2.0-x64.exe` 与 `SHA256SUMS.txt`，核对 SHA-256
后运行安装器。Reader Core 必装；Basic 可选且使用 CPU；Standard 可选，
需要 NVIDIA GPU/CUDA。也可以只安装 Core，以后再从 Reader 的语音包管理器
下载 Basic 或 Standard。

安装器尚未购买代码签名证书，Windows 可能显示未知发布者警告。请只从本
Release 下载，并核对哈希。

## 已验证功能

- 从参考音频转写并创建可复用声音数据；
- Basic 与 Standard 真实本地合成；
- 按动态总时长预生成连续朗读窗口；
- 暂停、继续、停止、上一句、下一句；
- 快速连续双击时旧会话失效，只播放最后位置；
- 已生成窗口中间跳转无需重新生成；
- Basic/Standard 独立安装、卸载与恢复；
- 文档、声音档案和缓存均保存在本机。

## 重要说明

公开资产不包含任何克隆声音、参考录音、用户数据库或内部测试数据。请仅使用
你有权使用的参考声音。Standard 包较大，分成 9 个可独立校验的 ZIP 分卷，
Reader 会自动下载并整体安装，不需要手工解压。

本版本包含第三方开源组件与模型，具体许可和署名见
`THIRD_PARTY_NOTICES.md`。完整文件哈希见 `SHA256SUMS.txt`。
