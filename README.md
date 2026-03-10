# Online Deep Learning


## Install

```shell
pip install -r homework2/requirements.txt

# MacOS
pip3 install torch torchvision torchaudio

# Windows
pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu128

# Verify
python3 -c "import torch; print(f'PyTorch version: {torch.__version__}'); print(f'MPS (GPU) available: {torch.backends.mps.is_available()}')"
```

## Download Data

```shell
# MacOS
curl -L -O https://www.cs.utexas.edu/~bzhou/dl_class/classification_data.zip && unzip classification_data.zip && rm classification_data.zip

# Windows
$url = "https://www.cs.utexas.edu/~bzhou/dl_class/classification_data.zip"; $file = "classification_data.zip"; Invoke-WebRequest -Uri $url -OutFile $file; Expand-Archive -Path $file -DestinationPath "."; Remove-Item -Path $file
```

https://www.cs.utexas.edu/~bzhou/dl_class/classification_data.zip

Put in `homework2/homework`

## Train

```shell
python3 -m homework.train --model_name linear
python3 -m homework.train --model_name mlp --num_epoch 75
python3 -m homework.train --model_name mlp_deep --num_epoch 100
python3 -m homework.train --model_name mlp_deep_residual --num_epoch 100
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
