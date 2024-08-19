## 说明
为了减少启动时候动态加载模型带来的时间损耗，
在构建镜像之前，请先将模型下载到 CosyVoice-300M/pretrained_models 目录下，包含三个模型
```
# git模型下载，请确保已安装git lfs
cd CosyVoice-300M
mkdir -p pretrained_models
git clone https://www.modelscope.cn/speech_tts/CosyVoice-300M.git pretrained_models/CosyVoice-300M
git clone https://www.modelscope.cn/speech_tts/CosyVoice-300M-SFT.git pretrained_models/CosyVoice-300M-SFT
git clone https://www.modelscope.cn/speech_tts/CosyVoice-300M-Instruct.git pretrained_models/CosyVoice-300M-Instruct
git clone https://www.modelscope.cn/speech_tts/speech_kantts_ttsfrd.git pretrained_models/speech_kantts_ttsfrd
```