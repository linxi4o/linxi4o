### 林晓

最近常想，语音修复和听力里最像的一件事，是把“听不清”变成一个可以度量的东西。

我是晓，在清华读研，方向是语音修复：从带噪声、混响或丢包损坏的音频里，把干净的语音恢复出来。这个页面放我当前的实验和半成品想法。

<sup>I’m Xiao, a CS graduate student in Beijing. My main work is speech restoration; this page collects ongoing experiments and half-baked ideas. The detailed profile is in Chinese.</sup>

## 一条我常走的流程

```
degraded speech ──> STFT ──> mask estimation ──> waveform reconstruction ──> restored speech
                        │
                        └─ 最难的一步：怎么定义“干净”
```

拿到一条真实录音，噪声和混响常常叠在一起，有时还有丢包留下的空洞。模型学的是从观测信号 x 映射到干净信号 s，但训练用的配对数据永远是一种近似。我最常纠结的不是模型容量，而是评估：增强后语音更“干净”了，但听感真的更好吗？

## 我习惯怎么合作

我喜欢把实验里的模糊判断写成可复现的小脚本。哪怕只是“这个样本听起来更亮”这种直觉，也会尽量配上频谱图和客观指标，哪怕指标不完全可靠。协作时我会主动同步失败案例——那些修不好的畸形波形成了我理解问题的重要方式。

## 页面之外

读书之外，我喜欢夜跑，沿着学校周围一圈圈地记录配速，像是给今天的想法做一次整理。也冲手冲咖啡，最近在试着把豆子的产地和风味描述当作另一种“术语表”来学。

我想做的研究很简单：让真实场景里的语音恢复更可信，而不是只在干净子集上好看。
