# JiangHuVoice Reader Downloads

这里是 JiangHuVoice Reader 的公开下载说明仓库。源码保存在独立的 [JiangHuVoice 仓库](https://github.com/HunDunJie/JiangHuVoice)中；本仓库不包含程序源码、模型、声音档案或用户数据。

> 迁移状态（2026-11-01）：本次只迁移仓库和下载说明，未迁移历史 Release 附件。新账号尚未发布安装包、更新清单及语音模型；以下安装步骤需等待后续正式发布。仓库内保留的版本说明是迁移前的历史记录，不代表新账号已提供对应下载。

## 安装

1. 打开右侧 [Releases](https://github.com/HunDunJie/JiangHuVoice-Downloads/releases)。
2. 下载最新的 `JiangHuVoice-Setup-<版本>-x64.exe` 和 `SHA256SUMS.txt`。
3. 校验 SHA-256 后运行安装器，选择安装目录。
4. Reader Core 必装；Basic 是 CPU 档，可选；Standard 需要受支持的 NVIDIA GPU/CUDA，也可稍后在 Reader 中安装。
5. 第一次使用时，用你自己有权使用的参考录音创建声音。公开安装包不附带克隆声音。

从0.2.1开始，安装器会随Basic/Standard勾选状态实时显示下载量、安装完成占用和安装峰值，并在继续前检查目标盘空间。Reader主界面可以手动检查Reader更新；模型包管理页可以手动检查Basic/Standard更新。两者都不会在启动时静默下载或静默升级。0.2.2进一步为Reader安装器和大型语音包增加持久断点续传与自动重试；网络中断后会保留已下载部分，重新安装时从断点继续。0.2.3修复同一安装会话释放空间后仍误报不足、安装语音包弹出控制台、在线目录短流失败、声音最终名称未保存，以及Markdown排版正文被误报为“没有清晰人声”等现场问题。0.2.4统一把声音创建转写显示和保存为简体，增加参考录音质量报告，并修正短句边界、闭引号、跨句响度、Standard隐藏减速和二次切句造成的节奏不一致。0.2.5为Standard增加计算平滑，在保持生成PCM不变和低缓冲自动恢复全速的前提下，降低显卡功耗、时钟与风扇突然爬升。

当前为未代码签名的测试版。Windows 可能显示来源警告；请只从本仓库 Release 下载并核对哈希。

## 组件

- Reader Core：界面、文档、播放、双击定位、声音创建、FFmpeg 和本地转写。
- Basic：MOSS-TTS-Nano CPU 本地语音包。
- Standard：GPT-SoVITS GPU 本地语音包。
- Advanced：尚未发布，不提供空壳或模拟实现。

安装和卸载 Basic/Standard 不会删除声音档案与文档。卸载 Reader 默认保留 `data` 用户数据目录。

## 隐私与声音权利

朗读、声音创建、转写和缓存均在本机完成。用户应确保对上传的参考音频及生成声音拥有必要权利。本发布不包含任何内部测试声音或其他克隆声音。
