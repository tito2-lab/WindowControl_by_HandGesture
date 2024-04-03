# Window Select by Hand Gesture on Windows
手のハンドサインをWeb CamでキャプチャしてWindows上に開いているWindowをキーボードとマウスなしで選択します。Hand GestureのモデルをOpenVINOで軽量化したモデルを利用して、NPUで動作をさせることにより利用するリソースも軽減させます。
Select Window on Windows by Web Cam captruing hand gestures, using hand gesture model on OpenVINO and offloading task to NPU for reducing running cost. 

# Available Hand Gestures


# Recommended Settings
- Python v3.10
- Windows 11
- Intel(r) Core(TM) Ultra if running on NPU (Intel(r) AI Boost)

# Setup
1. Install Python on your windows (set path for python execution file) 
2. open cmd and make virtual environment and activate
```
python -m venv handgestenv
handgestenv\Scripts\activate
```
3. Install libraries and run on Jupyter
```
pip install -r requirements.txt
jupyter lab WindowSelectHandGesture.ipnb
```

# Reference
- Yolov8x Tuned to Hand Gestures (HF) : [lewiswatson/yolov8x-tuned-hand-gestures](https://huggingface.co/lewiswatson/yolov8x-tuned-hand-gestures)
- Convert and Optimize YOLOv8 real-time object detection with OpenVINO™ (GitHub): [notebooks/yolov8-optimization/yolov8-object-detection.ipynb](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/yolov8-optimization/yolov8-object-detection.ipynb)
