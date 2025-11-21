# Perbandingan Model Vision Transformer untuk Klasifikasi Makanan Indonesia

Proyek ini mengimplementasikan dan membandingkan dua model Vision Transformer (ViT) untuk tugas klasifikasi gambar makanan Indonesia. Eksperimen ini bertujuan untuk menganalisis performa dan efisiensi komputasi dari model ViT dan DeiT pada dataset makanan tradisional Indonesia.

## 📊 Dataset
Dataset terdiri dari 5 kelas makanan Indonesia dengan distribusi yang seimbang. Setiap kelas merepresentasikan makanan khas Indonesia yang berbeda.

## 🤖 Model yang Dibandingkan
- **Vision Transformer (ViT-Tiny)**: Arsitektur transformer murni untuk visi
- **Data-efficient Image Transformer (DeiT-Tiny)**: ViT dengan knowledge distillation untuk efisiensi data

## 📈 Metrik Evaluasi
Proyek ini mengukur:
- Akurasi, Precision, Recall, dan F1-Score
- Jumlah parameter dan ukuran model
- Waktu inferensi dan throughput
- Analisis trade-off antara akurasi dan efisiensi

## 🏗️ Model Architectures

### Vision Transformer (ViT-Tiny)
- **Input**: Image patches 16x16 pixels
- **Embedding Dimension**: 192
- **Transformer Layers**: 12
- **Attention Heads**: 3
- **Parameters**: ~5.5 juta
- **Kelebihan**: Arsitektur pure transformer, skalabilitas baik

### DeiT-Tiny 
- **Input**: Image patches 16x16 pixels  
- **Embedding Dimension**: 192
- **Transformer Layers**: 12
- **Attention Heads**: 3
- **Parameters**: ~5.5 juta
- **Kelebihan**: Knowledge distillation, lebih efisien data

## 🔬 Metodologi Eksperimen

### Preprocessing
- Resize image: 224x224 pixels
- Normalization: ImageNet mean & std
- **Tanpa augmentasi** (sesuai requirement)

### Training Configuration
- **Optimizer**: AdamW dengan weight decay
- **Learning Rate**: 1e-4
- **Batch Size**: 8-16 (disesuaikan kemampuan hardware)
- **Epochs**: 5
- **Loss Function**: CrossEntropyLoss
- **Strategy**: Transfer learning dengan fine-tuning

### Evaluation Protocol
- **Train/Validation Split**: 80/20 stratified split
- **Metrics Calculation**: Sklearn classification report
- **Inference Timing**: Warm-up + multiple runs untuk akurasi
- **Hardware**: CPU/GPU dengan spesifikasi tercatat

## 📈 Hasil Eksperimen

### Performa Klasifikasi
| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| ViT-Tiny | 0.3500 | 0.3450 | 0.3500 | 0.3400 |
| DeiT-Tiny | 0.3750 | 0.3700 | 0.3750 | 0.3650 |

### Efisiensi Komputasi
| Model | Total Params | Trainable | Inference Time | Throughput |
|-------|--------------|-----------|----------------|------------|
| ViT-Tiny | 5.5M | 3,845 | 15.2 ms | 65.7 img/s |
| DeiT-Tiny | 5.5M | 3,845 | 14.8 ms | 67.6 img/s |

### Analisis Visual
- Learning curves (train/val loss & accuracy)
- Confusion matrices per model
- Perbandingan inference time
- Trade-off analysis visualization

## 📞 Contact

- **Author**:ALDI SANJAYA
- **NIM**: 122140150
- **Email**: aldi.122140150@student.itera.ac.id
- **Institution**: Institut Teknologi Sumatera (ITERA)

## ❓ Getting Help
- Buka [Issues](https://github.com/ALDISANJAYA121/VisionTransformer-Comparison/issues) untuk bug reports
- Check [Wiki](https://github.com/ALDISANJAYA121/VisionTransformer-Comparison/wiki) untuk dokumentasi lengkap
