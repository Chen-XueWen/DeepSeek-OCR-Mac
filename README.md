# DeepSeek-OCR on Apple Silicon (CPU, Transformers)

## Tested on 
- Use Python 3.12.12
```bash
pip3 install torch torchvision
pip3 install huggingface
```

## Patch the Deepseek-OCR source code:
```bash
.cache/huggingface/modules/transformers_modules/deepseek-ai/DeepSeek-OCR/{uuid}/modeling_deepseekocr.py
```

with "modeling_deepseekocr.py" in this repo or replace all "cuda" with "cpu"

## Run OCR
- Edit `prompt`, `image_file`, and `output_path` in `example.py` if needed.
- Run the sample script: `python example.py`.
- Results (markdown and any images) are written to `output_path`.

## Notes
- Currently CPU-only; MPS acceleration is not supported in this build.
