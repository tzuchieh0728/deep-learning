# deep-learning project

# 行走路線及障礙偵測

---

## 研究介紹

---

我們嘗試以平面照片及連續影片作為輸入，並透過單眼深度估計、各種預訓練模型對障礙物或階梯等進行辨識，於找出可行走的路面後，結合整體計算出最佳的行進路線。

---

## 使用技術、模型及其他程式碼

---

1.DPT-Large (MiDaS 3.0)：建立深度圖(著重分辨障礙物)。

2.MiDaS_small：建立深度圖(著重分辨障礙物)。

3.YOLOv8：障礙物辨識。

4.SegFormer (b0-sized) model fine-tuned on ADE20k：透過語意分割模型找出室內空間的可行走區域遮罩。

5.SegFormer (b2-sized) model fine-tuned on CityScapes：透過語意分割模型找出室外空間(街道)的可行走區域遮罩。

---

## 參考文獻

---

1.https://github.com/ultralytics/ultralytics

2.https://github.com/isl-org/MiDaS

3.https://arxiv.org/abs/1907.01341v3
