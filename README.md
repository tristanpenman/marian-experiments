# Marian Experiments

Python scripts and other resources to run MarianMT models on Rockchip NPU devices.

## Prerequisites

Dependencies can be installed using `pip`:

```
pip install -r requirements.txt
```

This includes dependencies for scripts in submodules too.

## Preflight

The script `preflight.py` can be used to check that your system can run a pretrained model from Hugging Face. You can choose a device (e.g. CUDA) using the `--device <type>` argument, and a specific model using `--model-name <id>`.

For example, to download an English-to-French model and run on a CUDA device:

```
$ python3 preflight.py --device cuda --model-name Helsinki-NLP/opus-mt-en-fr
Using device: cuda
Using model: Helsinki-NLP/opus-mt-en-fr
Enter text to translate (empty line to quit):
> I am a fish
Je suis un poisson
>
```

## ONNX Converter

In the [Marian-ONNX-Converter](./Marian-ONNX-Converter) submodule you will find an ONNX implementation of Marian, with a conversion script.

This allows pretrained models on Hugging Face to be converted to ONNX format.
