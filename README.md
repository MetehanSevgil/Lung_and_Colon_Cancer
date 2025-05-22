# 📊 Derin Öğrenme Modelleri Karşılaştırması

Bu projede; **ResNet50**, **DenseNet121**, **VGG16**, **Xception**, ve **EfficientNetB7** modelleri, farklı görüntü boyutlarında ve farklı donanımlarda eğitilerek test edilmiştir. Her modelin eğitim süresi, doğruluk skorları, F1, precision ve recall gibi metrikleri elde edilmiştir. Ayrıca depolama maliyetini azaltmak ve modelin hafızada kapladığı alanı minimize etmek amacıyla, **hafifletilmiş bir DenseNet121** tabanlı model geliştirilmiştir.

---

## 🧠 Kullanılan Modeller

- ResNet50  
- DenseNet121  
- VGG16  
- Xception  
- EfficientNetB7  
- Lighter DenseNet121

---

## 🖼️ Görüntü Boyutları

- 128×128  
- 256×256  
- 768×768

---

## ⚙️ Donanım Ortamları

| Ortam        | GPU             |
|--------------|-----------------|
| Local        | NVIDIA GTX 1650 TI |
| Google Colab | NVIDIA A100     |

---

## 📊 Performans Sonuçları

| Model              | Img Size | Ortam         | Parametre Sayısı | Model Boyutu | Eğitim Süresi | Test Süresi | Test Acc | F1 Score | Precision | Recall | Model Yükleme |
|--------------------|----------|---------------|------------------|---------------|----------------|-------------|----------|----------|-----------|--------|----------------|
| ResNet50           | 256×256  | Local         | 57.7M            | 220 MB        | 85 dk          | 67 sn       | 0.9986   | 0.9986   | 0.9986    | 0.9986 | 4.11 sn        |
| ResNet50           | 128×128  | Local         | 32.1M            | 122 MB        | 25 dk          | 22 sn       | 0.9974   | 0.9974   | 0.9974    | 0.9974 | 3.74 sn        |
| ResNet50           | 768×768  | Colab         | 330.3M           | 1.23 GB       | 57 dk          | 77 sn       | 0.9988   | 0.9988   | 0.9988    | 0.9988 | 26.24 sn       |
| DenseNet121        | 256×256  | Local         | 40.9M            | 156 MB        | 97 dk          | 34 sn       | 0.9980   | 0.9980   | 0.9980    | 0.9980 | 6.97 sn        |
| DenseNet121        | 128×128  | Local         | 15.5M            | 60 MB         | 26 dk          | 23 sn       | 0.9986   | 0.9986   | 0.9986    | 0.9986 | 6.56 sn        |
| DenseNet121        | 768×768  | Colab         | 311.4M           | 1.16 GB       | 68 dk          | 115 sn      | 0.9998   | 0.9998   | 0.9998    | 0.9998 | 27.87 sn       |
| VGG16              | 256×256  | Local         | 31.6M            | 120 MB        | 130 dk         | 58 sn       | 0.9846   | 0.9846   | 0.9849    | 0.9846 | 1.50 sn        |
| VGG16              | 128×128  | Local         | 18.9M            | 72 MB         | 47 dk          | 63 sn       | 0.9912   | 0.9912   | 0.9912    | 0.9912 | 1.43 sn        |
| VGG16              | 768×768  | Colab         | 166.9M           | 636 MB        | 86 dk          | 58 sn       | 0.9614   | 0.9612   | 0.9653    | 0.9614 | 13.54 sn       |
| Xception           | 256×256  | Local         | 88.5M            | 337 MB        | 133 dk         | 64 sn       | 0.9986   | 0.9986   | 0.9986    | 0.9986 | 4.54 sn        |
| Xception           | 128×128  | Local         | 37.8M            | 144 MB        | 40 dk          | 58 sn       | 0.9960   | 0.9960   | 0.9960    | 0.9960 | 3.17 sn        |
| Xception           | 768×768  | Colab         | 629.6M           | 2.35 GB       | 90 dk          | 74 sn       | 0.9922   | 0.9922   | 0.9923    | 0.9922 | 51.32 sn       |
| EfficientNetB7     | 256×256  | Colab         | 106.7M           | 407 MB        | 29 dk          | 19 sn       | 0.9868   | 0.9868   | 0.9873    | 0.9868 | 12.43 sn       |
| EfficientNetB7     | 128×128  | Local         | 29.4M            | 118 MB        | 41 dk          | 78 sn       | 0.9974   | 0.9974   | 0.9974    | 0.9974 | 3.47 sn        |
| EfficientNetB7     | 768×768  | Colab         | 447.5M           | 1.67 GB       | 181 dk         | 75 sn       | 0.1684   | 0.0744   | 0.0478    | 0.1684 | 36.61 sn       |
| Lighter_DenseNet121| 128×128  | Local         | 1.6M             | 6.41 MB       | 18 dk          | 16 sn       | 0.9986   | 0.9986   | 0.9986    | 0.9986 | 3.39 sn        |

---

## 📚 Gereksinimler

```bash
tensorflow>=2.x
numpy
pandas
scikit-learn
matplotlib


# Relevant Links
- https://arxiv.org/abs/1912.12142v1
- https://github.com/tampapath/lung_colon_image_set
