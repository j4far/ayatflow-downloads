# AyatFlow downloads

Files that the free [AyatFlow](https://github.com/j4far) Quran app downloads on first use. This repository holds **only** the speech model. It contains no app code.

## Speech model: `whisper-small-ar-quran-q8_0.bin`

The model that checks Quran recitation **on your phone**, so your voice never leaves the device.

| | |
|---|---|
| File | `whisper-small-ar-quran-q8_0.bin` (in the [model-v1 release](../../releases/tag/model-v1)) |
| Size | 264,464,624 bytes |
| SHA-256 | `c78565da1a3c7747f80ecb744acde6a59c17ca63f47c066cdb434a1b18cdf89c` |
| Format | whisper.cpp "ggml", 8-bit quantised (q8_0) |
| Licence | Apache-2.0 (see `LICENSE` and `NOTICE`) |

### Where it comes from

- Fine-tuned model: [`deepdml/whisper-small-ar-quran-mix-norm`](https://huggingface.co/deepdml/whisper-small-ar-quran-mix-norm) (Apache-2.0), itself a fine-tune of OpenAI's [Whisper small](https://github.com/openai/whisper) (MIT).
- Changes made here: converted to whisper.cpp's ggml format with whisper.cpp's `convert-h5-to-ggml.py` (MIT), using the checkpoint's `max_target_positions` (448) as the decoder context, then quantised to q8_0 with whisper.cpp's `quantize` tool. The model's weights were not retrained.
- The fine-tuned model was trained by its author on public Quran recitation datasets (see its model card).

No warranty. A study aid, not a religious authority.
