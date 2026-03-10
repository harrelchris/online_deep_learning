# Online Deep Learning


## Install

```shell
pip install -r homework2/requirements.txt
pip3 install torch torchvision torchaudio

# Verify
python3 -c "import torch; print(f'PyTorch version: {torch.__version__}'); print(f'MPS (GPU) available: {torch.backends.mps.is_available()}')"
```

## Train

```shell
python3 -m homework.train --model_name linear
python3 -m homework.train --model_name mlp
python3 -m homework.train --model_name mlp_deep
python3 -m homework.train --model_name mlp_deep_residual
```

## Grade

```shell
python3 -m grader homework -v
```

If accuracy falls short, try --lr 3e-4 or --num_epoch 100 to squeeze out more performance.

## Bundle

```shell
python3 bundle.py homework ch55526
```
