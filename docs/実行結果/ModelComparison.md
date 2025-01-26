# LLMモデルのダウンロード・読み込み
ollama server からダウンロード  
```
ollama run name
```
huggingface からダウンロード  
```
ollama run hf.co/hoge/fugaGGUF:IQ4_K_M
```
## オプション  
出力速度等を表示  
```
ollama run name --verbose
```

# モデル一覧
|Name  |サイズ GB  |備考  |
|---|---|---|
|bartowski/DeepSeek-R1-Distill-Qwen-14B-GGUF:Q5_K_L  |10.99  |採用  |
|bartowski/DeepSeek-R1-Distill-Qwen-32B-GGUF:IQ2_S  |10.39  |  |
|deepseek-r1:14b  |9.00  |おそらくQ4_K_M  |

# 選択理由
RTX4070 VRAM 12GB  
モデルサイズがVRAMを超えるとメインメモリにロードされ、処理速度が遅くなる  
VRAM - 1GB のモデルを選択  
Q2だと性能低下の影響が多いと思われるので、Q4以上を選択  
