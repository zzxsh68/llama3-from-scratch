---
frameworks:
- Pytorch
license: Apache License 2.0
tasks:
- text-generation

#model-type:
##如 gpt、phi、llama、chatglm、baichuan 等
#- gpt

#domain:
##如 nlp、cv、audio、multi-modal
#- nlp

#language:
##语言代码列表 https://help.aliyun.com/document_detail/215387.html?spm=a2c4g.11186623.0.0.9f8d7467kni6Aa
#- cn 

#metrics:
##如 CIDEr、Blue、ROUGE 等
#- CIDEr

#tags:
##各种自定义，包括 pretrained、fine-tuned、instruction-tuned、RL-tuned 等训练方法和其他
#- pretrained

#tools:
##如 vllm、fastchat、llamacpp、AdaSeq 等
#- vllm
---

## 1.简介 (Introduction)

本模型是Meta-Llama-3-8B-Instruct模型的前两层，由于Llama3-8B共有32层，使用CPU加载模型时，16G的内存无法加载模型，故从32层中摘取前两层保存为一个新的模型。

主要用于 [llama3-from-scratch-zh](https://github.com/wdndev/llama3-from-scratch-zh) 和 [llama3-from-scratch](https://github.com/naklecha/llama3-from-scratch) 的学习，方便笔记本用户快速加载模型，运行学习。


This model is the first two layers of the Meta-Llama 3-8B-Instruct model. As Llama3-8B has 32 layers, the model cannot be loaded with 16G of memory when CPU is used to load the model, so remove the first two layers from the 32 layers and store them as a new model.

It is mainly used for [llama3-from-scratch-zh](https://github.com/wdndev/llama3-from-scratch-zh) and [llama3-from-scratch](https://github.com/naklecha/llama3-from-scratch) learning, convenient laptop users fast load model, operation study.

## 2.模型下载 (Model Download)

SDK doenload
```bash
# install ModelScope
pip install modelscope
```
```python
#SDK download model
from modelscope import snapshot_download
model_dir = snapshot_download('wdndev/Meta-Llama-3-8B-Instruct-2layers')
```
Git download model
```
#Git模型下载
git clone https://www.modelscope.cn/wdndev/Meta-Llama-3-8B-Instruct-2layers.git
```

<p style="color: lightgrey;">如果您是本模型的贡献者，我们邀请您根据<a href="https://modelscope.cn/docs/ModelScope%E6%A8%A1%E5%9E%8B%E6%8E%A5%E5%85%A5%E6%B5%81%E7%A8%8B%E6%A6%82%E8%A7%88" style="color: lightgrey; text-decoration: underline;">模型贡献文档</a>，及时完善模型卡片内容。</p>