# VisionTransformer-Comparison

Repository ini berisi implementasi dan perbandingan dua model Vision Transformer ringan, yaitu **ViT-Tiny** dan **DeiT-Tiny**, pada dataset klasifikasi makanan Indonesia.

Project ini dibuat untuk:
- Melatih model ViT dan DeiT yang ringan
- Membandingkan performa kedua model
- Mengukur inference time, parameter, throughput
- Membuat prediksi test set
- Menyediakan visualisasi dan summary hasil

## Struktur Repository

VisionTransformer-Comparison/
├── notebooks/
│   └── vision_transformer_comparison.ipynb
├── src/
├── outputs/
├── data/
├── requirements.txt
└── README.md

## Cara Install
pip install -r requirements.txt


## 🏋 Cara Training
python src/train_vit.py
python src/train_deit.py

## 🧪 Cara Evaluasi
python src/evaluate.py

## 🔮 Cara Prediksi
python src/predict.py
