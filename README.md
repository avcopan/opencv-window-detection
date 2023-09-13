In addition to poetry install:
```
poetry install
```
To install pyTorch without GPU (since I don't have nvidia):
```
poetry source add --priority=explicit pytorch-cpu-src https://download.pytorch.org/whl/cpu
poetry add --source pytorch-cpu-src torch torchvision torchaudio
```

To train the model (using the smallest "nano"-sized model since I don't have an NVidia GPU):
```
yolo task=detect mode=train epochs=100 data=data_custom.yaml model=yolov8n.pt imgsz=640
```