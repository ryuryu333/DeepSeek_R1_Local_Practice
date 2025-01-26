# DeepSeek-R1 蒸留/量子化モデル、Github Copilot 回答比較
## 結果
GithubCopilot Claude 3.5 Sonnet が一番  
質問に対して期待する回答の要素を書き出し、いくつ一致しているかで点数化  

|        | Name                                               | Dockerの質問 | UMLの質問 | LLMの質問 |
| ------ | -------------------------------------------------- | ------------ | --------- | --------- |
| Local  | bartowski/DeepSeek-R1-Distill-Qwen-14B-GGUF:Q5_K_L | 0            | 0         | 0         |
| Local  | bartowski/DeepSeek-R1-Distill-Qwen-32B-GGUF:IQ2_S  | 2            | 2         | 0         |
| Github | Claude 3.5 Sonnet                                  | 4            | 4         | 2         |
| Github | GPT4o                                              | 3            | 3         | 0         |
| Github | o1 mini                                            | 3            | 3         | 2         |
| Github | o1 preview                                         | 3            | 3         | 0         |

## 質問文と回答
### Docker
#### 質問
<details><summary>Dockerの質問</summary>

```
The following is the Docker command.
---
docker run -d --gpus=all -v ollama:/root/. docker run -d --gpus=all -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
---
Replace this command with Dockerfile and Dockercompose.
```
</details>

#### 回答
Claude 3.5 Sonnet が頭ひとつ飛び抜けて良い  
次点はo1系列  

|        | Name                                               | ollama/ollamaイメージを使用している | GPU使用の箇所が有効な書き方か | 名前付きボリュームを定義している | Dockerfileでポート番号を指定している | 元コマンドに無い不要な要素が含まれていない |
| ------ | -------------------------------------------------- | ----------------------------------- | ----------------------------- | -------------------------------- | ------------------------------------ | ------------------------------------------ |
| Local  | bartowski/DeepSeek-R1-Distill-Qwen-14B-GGUF:Q5_K_L | x                                   | x                             | x                                | x                                    | x                                          |
| Local  | bartowski/DeepSeek-R1-Distill-Qwen-32B-GGUF:IQ2_S  | ok                                  | x                             | x                                | ok                                   | x                                          |
| Github | Claude 3.5 Sonnet                                  | x                                   | ok                            | ok                               | ok                                   | ok                                         |
| Github | GPT4o                                              | ok                                  | x                             | ok                               | x                                    | ok                                         |
| Github | o1 mini                                            | ok                                  | x                             | ok                               | x                                    | ok                                         |
| Github | o1 preview                                         | ok                                  | x                             | ok                               | x                                    | ok                                         |

※Version記載は非推奨だが、情報が古いのか全ての回答で記載あり、表に含めず  

### UML
#### 質問
<details><summary>UMLの質問</summary>

```
I am looking foard docker icon for UML. Please serch from this github repository. https://github.com/tupadr3/plantuml-icon-font-sprites
```
</details>

#### 回答
Claude 3.5 Sonnet が頭ひとつ飛び抜けて良い  

|        | Name                                               | Dockerアイコンを見つける方法を示せる | 引用サイトにDockerアイコンが含まれていると判断できる | Dockerアイコンの保存場所を示せる |
| ------ | -------------------------------------------------- | ------------------------------------ | ---------------------------------------------------- | -------------------------------- |
| Local  | bartowski/DeepSeek-R1-Distill-Qwen-14B-GGUF:Q5_K_L | x                                    | x                                                    | x                                |
| Local  | bartowski/DeepSeek-R1-Distill-Qwen-32B-GGUF:IQ2_S  | ok                                   | x                                                    | x                                |
| Github | Claude 3.5 Sonnet                                  | ok                                   | ok                                                   | ok                               |
| Github | GPT4o                                              | x                                    | x                                                    | x                                |
| Github | o1 mini                                            | x                                    | x                                                    | x                                |
| Github | o1 preview                                         | x                                    | x                                                    | x                                |

### LLM
#### 質問
<details><summary>LLMの質問</summary>

```
I would like to discuss which LLM I should choose. My PC has 12GB of VRAM. The following two URLs describe different LLM models.
---
https://huggingface.co/bartowski/DeepSeek-R1-Distill-Qwen-14B-GGUF
https://huggingface.co/bartowski/DeepSeek-R1-Distill-Qwen-32B-GGUF
---
Each model is quantized in a different way. Please compare the models and narrow down which model will work with my PC's GPU. Then select the model that you think performs better. When thinking about it, please get the information detailed in the URL I just mentioned before you start selecting a model.
```
</details>

#### 回答
Claude 3.5 Sonnet が頭ひとつ飛び抜けて良い  

|        | Name                                               | 蒸留/量子化を含むモデルを提案出来ている | 指定した性能のモデルを提案出来ている |
| ------ | -------------------------------------------------- | --------------------------------------- | ------------------------------------ |
| Local  | bartowski/DeepSeek-R1-Distill-Qwen-14B-GGUF:Q5_K_L | x                                       | x                                    |
| Local  | bartowski/DeepSeek-R1-Distill-Qwen-32B-GGUF:IQ2_S  | x                                       | x                                    |
| Github | Claude 3.5 Sonnet                                  | ok                                      | ok                                   | ok                               
| Github | GPT4o                                              | x                                       | x                                    | x                                
| Github | o1 mini                                            | ok                                      | ok                                   | x                                
| Github | o1 preview                                         | x                                       | x                                    | x                                

