# DeepSeek-R1 蒸留/量子化モデル、Github Copilot 回答比較
## 結果
GithubCopilot Claude 3.5 Sonnet が一番  





|       |Name                                               |Dockerの質問   |UMLの質問  |LLMの質問  |
|---    |---                                                |---            |---        |---        |
|Local  |bartowski/DeepSeek-R1-Distill-Qwen-14B-GGUF:Q5_K_L |10.99  |採用  |
|Local  |bartowski/DeepSeek-R1-Distill-Qwen-32B-GGUF:IQ2_S  |10.39  |  |
|Local  |(ollama)deepseek-r1:14b                            |9.00  |おそらくQ4_K_M    |
|Github |Claude 3.5 Sonnet                                  ||
|Github |GPT4o                                              ||
|Github |o1 mini                                            ||
|Github |o1 preview                                         ||

## 質問文と回答
### Dockerの質問
<details><summary>質問</summary>

```
The following is the Docker command.
---
docker run -d --gpus=all -v ollama:/root/. docker run -d --gpus=all -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
---
docker run -d --gpus=all -v Replace this command with Dockerfile and Dockercompose.
```
</details>

