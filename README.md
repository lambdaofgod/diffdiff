# diffdiff

## Tools for diffing huggingface diffuser models

### Usage

- guidance scale
- negative prompt

* Supported `<PROMPTS>` 
- a list of prompts separated by "|"
- path to text file, each line is a prompt

* `<SAVE_DIR>`

* `<CONFIG>`
- a string that can be interpreted as Python dictionary
- a path to config file


#### Configuration

See [stable diffusion pipeline documentation](https://github.com/huggingface/diffusers/blob/main/src/diffusers/pipelines/stable_diffusion/pipeline_stable_diffusion.py#L431)

```
python -m diffdiff --prompts <PROMPTS> --save_dir <SAVE_DIR> --config <CONFIG>
```
