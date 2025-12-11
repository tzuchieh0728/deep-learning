# deep-learning project

# 行走路線及障礙偵測


## 研究介紹

我們嘗試以平面照片及連續影片作為輸入，並透過單眼深度估計、各種預訓練模型對障礙物或階梯等進行辨識，於找出可行走的路面後，結合整體計算出最佳的行進路線。

## 使用技術、模型及其他程式碼

1.DPT-Large (MiDaS 3.0)：建立深度圖(著重分辨障礙物)。

2.MiDaS_small：建立深度圖(著重分辨障礙物)。

3.YOLOv8：障礙物辨識。

4.SegFormer (b0-sized) model fine-tuned on ADE20k：透過語意分割模型找出室內空間的可行走區域遮罩。

5.SegFormer (b2-sized) model fine-tuned on CityScapes：透過語意分割模型找出室外空間(街道)的可行走區域遮罩。

## 參考文獻與外部連結

1.[YOLO](https://github.com/ultralytics/ultralytics)

2.[MiDaS](https://github.com/isl-org/MiDaS)

3.[Towards Robust Monocular Depth Estimation: Mixing Datasets for Zero-shot Cross-dataset Transfer](https://arxiv.org/abs/1907.01341v3)

4.[Flexible camera calibration by viewing a plane from unknown orientation](https://www.researchgate.net/publication/3816565_Flexible_camera_calibration_by_viewing_a_plane_from_unknown_orientation)

5.[Bhavana, N., Kodabagi, M. M., Kumar, B. M., Ajay, P., Muthukumaran, N., & Ahilan, A. (2024). POT-YOLO: Real-time road potholes detection using edge segmentation-based YOLO V8 network. IEEE Sensors Journal, 24(15), 24802-24809.、Karthika, B., Dharssinee, M., Reshma, V., Venkatesan, R.,](https://www.researchgate.net/publication/381034963_POT-YOLO_Real-Time_Road_Potholes_Detection_using_Edge_Segmentation_based_Yolo_V8_Network)

6.[Sujarani, R. (2024, June). Object detection using yolo-v8. In 2024 15th International Conference on Computing Communication and Networking Technologies (ICCCNT)](https://www.researchgate.net/publication/385535267_Object_Detection_Using_YOLO-V8)

7.[Mulajkar, R., & Yede, S. (2024, April). YOLO version v1 to v8 comprehensive review. In 2024 International Conference on Inventive Computation Technologies (ICICT) (pp. 472-478). IEEE.](https://www.researchgate.net/publication/381264145_YOLO_Version_v1_to_v8_Comprehensive_Review)

## 如何使用

1.透過pip安裝下列檔案
```python
!pip install ultralytics torch torchvision
```

2.下載並於google colab開啟程式碼檔案

3.單圖片分析：於base code區塊開頭將`img_path`修改成自己的圖片路徑，進行單圖片分析。

```python
img_path  = "YOUR_IMG_PATH"
```

4.影片分析：於影片測試的第二區塊，將`input_video`修改成自己的圖片連結，進行影片分析。

```python
input_video  = "YOUR_VIDEO_PATH"
output_video = "YOUR_RESULT_VIDEO_PATH"
```
5. Gradio畫面展示: 執行Gradio即時呈現區塊，點擊下方輸出格的網址，模擬手機即時生成導引影片的功能
```
* Running on public URL: https://a2d7755fb3bffe8616.gradio.live
```
