# diffdiff

## Tools for diffing huggingface diffuser models

## Usage

### Fast example

Generate images with different models

```
python -m diffdiff generate \
    --versions "CompVis/stable-diffusion-v1-4 stabilityai/stable-diffusion-2" \
    --prompts "Xenomorph birthday party & Escher style pencil drawing of octopus bicycle"
    --save_dir weird_images
```

Run Gradio UI to compare images

```
python -m diffdiff ui --save_dir weird_images
```

### Generation

```
python -m diffdiff generate
    --prompts <PROMPTS> \
    --versions <VERSIONS> \
    --config <CONFIG> \
    --save_dir <SAVE_DIR> \
    --sep <SEP>
```

* Supported `<PROMPTS>` 
  - a list of prompts separated by `<SEP>`
  - path to text file, each line is a prompt

* `<VERSIONS>="CompVis/stable-diffusion-v1-4"`

Model versions (separated with space) to run, at minimum one version. 

* `<CONFIG>`
  - a string that can be interpreted as Python dictionary
  - a path to config file

* `<SAVE_DIR>=images`
Directory where we will save images

* `<SEP>="&"`

Separator to delineate prompts. 

### Configuration

See [stable diffusion pipeline documentation](https://github.com/huggingface/diffusers/blob/main/src/diffusers/pipelines/stable_diffusion/pipeline_stable_diffusion.py#L431)
