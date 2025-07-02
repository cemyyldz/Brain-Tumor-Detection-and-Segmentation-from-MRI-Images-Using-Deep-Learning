# 🧠 Brain Tumor Detection and Segmentation from MRI Images Using Deep Learning  
### MRI Görüntülerinden Derin Öğrenme ile Beyin Tümörü Tespiti ve Segmentasyonu

## 📌 Proje Hakkında

Bu proje, MRI (Manyetik Rezonans Görüntüleme) verileri üzerinden **beyin tümörlerinin tespiti ve segmentasyonu** işlemlerini gerçekleştirmek amacıyla geliştirilmiştir. Derin öğrenme mimarisi olarak **U-Net** kullanılmış, tıbbi görüntülerin analizi için **SimpleITK**, **NumPy** ve **Keras** kütüphanelerinden yararlanılmıştır.

Projenin amacı, doktorların tanı süreçlerini destekleyebilecek, tümörleri otomatik olarak tespit edip bölütleyebilecek bir sistem sunmaktır.

---

## 🎯 Hedefler

- MRI görüntülerinden beyindeki tümörleri otomatik olarak tespit etmek  
- U-Net mimarisi ile tümör bölgesini segment (mask) olarak çıkarmak  
- Tıbbi görüntüleri işlerken yüksek doğrulukla çalışan, veri odaklı bir model geliştirmek  

---

## 🧪 Kullanılan Teknolojiler ve Kütüphaneler

- Python
- Keras & TensorFlow
- NumPy & Matplotlib
- SimpleITK
- OpenCV
- scikit-learn

---

## 🧬 Kullanılan Veri Kümesi

- **BraTS (Brain Tumor Segmentation Challenge)** veri kümesi kullanılmıştır.  
- MRI görüntüleri ve ilgili maske etiketleri içermektedir.  
- T1, T2, FLAIR gibi MRI modaliteleri bulunmaktadır.  
> 🔒 Not: Veri kümesi, yasal nedenlerle bu repo altında paylaşılmamıştır. [BraTS](https://www.med.upenn.edu/sbia/brats2020/data.html) sitesinden erişebilirsiniz.

## 📊 Model Performansı

Aşağıda üç farklı modelin performans metrikleri gösterilmiştir. Modeller sırasıyla **tam tümör segmentasyonu**, **ödemsiz tümör segmentasyonu** ve **geniş (enhancing tumor)** segmentasyonu hedefiyle eğitilmiştir.

| Model Türü       | Dice Score | F1 Skoru | IoU    | Precision | Recall | Loss   |
|------------------|------------|----------|--------|-----------|--------|--------|
| Model Tam Tümör  | 0.6484     | 0.6538   | 0.5855 | 0.6708    | 0.6622 | 0.3516 |
| Model Ödemsiz    | 0.8246     | 0.8263   | 0.7780 | 0.8393    | 0.8268 | 0.1758 |
| Model Geniş      | 0.7876     | 0.7904   | 0.7022 | 0.8042    | 0.7965 | 0.2119 |

🔹 **Dice Score** ve **IoU** metrikleri, segmentasyon başarısını ölçmekte yaygın olarak kullanılır.  
🔹 Model "Ödemsiz" versiyonda en yüksek başarıyı göstermiştir.


---
