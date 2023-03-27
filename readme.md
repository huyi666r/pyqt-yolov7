### 主要参考https://gitcode.net/mirrors/javacr/pyqt5-yolov5，实现yolov7模型训练权重的pyqt5可视化推理界面

**功能：**

1. 模型选择
2. 输入选择(本地文件、摄像头、RTSP)；在检测RTSP视频流的时候，尽量不要启用帧间延时，否则会出现很高的延时，用yolo5x模型时，rtsp会很卡，建议抽帧检测, 把main.py中的133-135行注释取消
```python
                    # jump_count += 1
                    # if jump_count % 5 != 0:
                    #     continue
```

3. IoU调整
4. 置信度调整
5. 帧间延时调整
6. 播放/暂停/结束
7. 统计检测结果（显示边框时，支持中文标签）


**使用：**
```bash
# conda创建python虚拟环境
conda create -n yolov7_pyqt5 python=3.8
# 激活环境
conda activate yolov7_pyqt5
# 到项目根目录下
cd ./
# 安装依赖文件
pip install -r requirements.txt
# 将下载好的模型放在pt文件夹下
# 运行main.py
python main.py
```
运行*main.py*开启检测界面后**会自动检测已有模型**。ui文件也已上传，可以按照自己的想法更改ui界面。
