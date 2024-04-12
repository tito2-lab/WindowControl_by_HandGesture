# Window Select by Hand Gesture on Windows
手のハンドサインをWeb CamでキャプチャしてWindows上に開いているWindowをキーボードとマウスなしで選択します。[Hand Gestureを学習させたYOLOv8のモデル](https://huggingface.co/lewiswatson/yolov8x-tuned-hand-gestures)をOpenVINOで軽量化したモデルを利用して、NPUで動作をさせることにより利用するリソースも軽減させます。
Select Window on Windows by Web Cam captruing hand gestures, using hand gesture model on OpenVINO and offloading task to NPU for reducing running cost. 

# Recommended Settings
- Python v3.10
- Windows 11
- Intel(r) Core(TM) Ultra if running on NPU (Intel(r) AI Boost)
- Intel(r) NPU driver 32.0.100.2267 or later

# Available Hand Gestures

[lewiswatson/yolov8x-tuned-hand-gestures](https://huggingface.co/lewiswatson/yolov8x-tuned-hand-gestures) のモデルをベースとしています。このモデルはアルファベットのハンドジェスチャーを入力されたイメージから検知、認識をおこないます。そのうち "H", "S", "T", "V", "W", "O" の文字のジェスチャーを利用してWindowsのコントロールに使っています。

This script is baded on [lewiswatson/yolov8x-tuned-hand-gestures](https://huggingface.co/lewiswatson/yolov8x-tuned-hand-gestures) model. This model can detect alphabets hand gestures from input image. This scipt uses "H", "S", "T", "V", "W" and "O" charactors from these gestures. (Actually these gestrues can be detected more accurately). 


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
jupyter lab hand_gesture.ipnb
```

# Reference
- Yolov8x Tuned to Hand Gestures (HF) : [lewiswatson/yolov8x-tuned-hand-gestures](https://huggingface.co/lewiswatson/yolov8x-tuned-hand-gestures)
- Convert and Optimize YOLOv8 real-time object detection with OpenVINO™ (GitHub): [notebooks/yolov8-optimization/yolov8-object-detection.ipynb](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/yolov8-optimization/yolov8-object-detection.ipynb)
- Hand Gesture Image: [https://www.freepik.com/free-vector/hand-gesture-language-alphabet_2776330.htm#from_view=detail_alsolike](https://www.freepik.com/free-vector/hand-gesture-language-alphabet_2776330.htm#from_view=detail_alsolike)
