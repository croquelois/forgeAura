# forgeAura

Add AuraFlow architecture to Forge

## Installation

1) clone `git clone git@github.com:lllyasviel/stable-diffusion-webui-forge.git`
2) go inside `cd stable-diffusion-webui-forge`
3) inside your forge root directory, apply the patch: `git apply forge.patch` it will modify `backend/loader.py`, `backend/nn/t5.py` and `backend/text_processing/t5_engine.py`
4) add `huggingface/AuraFlow` directory inside `backend/huggingface`
5) add `diffusion_engine/auraflow.py` and `diffusion_engine/spiece_tokenizer.py` files inside `backend/diffusion_engine`
6) add `nn/auraflow.py` file inside `backend/nn`

## Result

![forge][forge.png]

![cthulhu][cthulhu.png]

## Todo

- try to get rid of spiecetokenizer, I feel like something in huggingface/transformer can do the same.
- update guess_huggingface to remove loader hacks
- do I really need the attention mask ? is it worth it ?
- test with quantification
- test with VAE + T5 + Model seperated
