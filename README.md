---
license: apache-2.0
---

# THUDM's chatglm2 6B GGML

These files are GGML format model files for [THUDM's chatglm2 6B](https://huggingface.co/THUDM/chatglm2-6b).

GGML files are for CPU + GPU inference using [chatglm.cpp](https://github.com/li-plus/chatglm.cpp) and xorbits-inference (coming soon).

# Prompt template
**NOTE**: prompt template is not available yet since the system prompt is hard coded in chatglm.cpp for now.

# Provided files

| Name | Quant method | Bits | Size |
|------|--------------|------|------|
| chatglm2-ggml-q4_0.bin | q4_0 | 4 | 3.5 GB  |
| chatglm2-ggml-q4_1.bin | q4_1 | 4 | 3.9 GB  |
| chatglm2-ggml-q5_0.bin | q5_0 | 5 | 4.3 GB  |
| chatglm2-ggml-q5_1.bin | q5_1 | 4 | 4.7 GB  |

# How to run in xorbits-inference
Coming soon.

# Slack
For further support, and discussions on these models and AI in general, join our [slack channel](https://join.slack.com/t/xorbitsio/shared_invite/zt-1o3z9ucdh-RbfhbPVpx7prOVdM1CAuxg)!

# Original model card: THUDM's chatglm2 6B
ChatGLM**2**-6B is the second-generation version of the open-source bilingual (Chinese-English) chat model [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B). It retains the smooth conversation flow and low deployment threshold of the first-generation model, while introducing the following new features:

1. **Stronger Performance**: Based on the development experience of the first-generation ChatGLM model, we have fully upgraded the base model of ChatGLM2-6B. ChatGLM2-6B uses the hybrid objective function of [GLM](https://github.com/THUDM/GLM), and has undergone pre-training with 1.4T bilingual tokens and human preference alignment training. The [evaluation results](README.md#evaluation-results) show that, compared to the first-generation model, ChatGLM2-6B has achieved substantial improvements in performance on datasets like MMLU (+23%), CEval (+33%), GSM8K (+571%), BBH (+60%), showing strong competitiveness among models of the same size.
2. **Longer Context**: Based on [FlashAttention](https://github.com/HazyResearch/flash-attention) technique, we have extended the context length of the base model from 2K in ChatGLM-6B to 32K, and trained with a context length of 8K during the dialogue alignment, allowing for more rounds of dialogue. However, the current version of ChatGLM2-6B has limited understanding of single-round ultra-long documents, which we will focus on optimizing in future iterations.
3. **More Efficient Inference**: Based on [Multi-Query Attention](http://arxiv.org/abs/1911.02150) technique, ChatGLM2-6B has more efficient inference speed and lower GPU memory usage: under the official  implementation, the inference speed has increased by 42% compared to the first generation; under INT4 quantization, the dialogue length supported by 6G GPU memory has increased from 1K to 8K.

For more instructions, including how to run CLI and web demos, and model quantization, please refer to our [Github Repo](https://github.com/THUDM/ChatGLM2-6B).
