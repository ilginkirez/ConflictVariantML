# ConflictVariantML

**Resolving Conflicting Genetic Variants Through Machine Learning-Based Classification**

---

## 🧬 Proje Hakkında
Bu proje, **genetik varyantlardaki çelişkili sınıflandırmaları çözmek** amacıyla makine öğrenmesi ve derin öğrenme yöntemlerini kullanır.  
Özellikle ClinVar veri setindeki varyantlar üzerinde, **patojenik ve benign varyantları doğru şekilde ayırt etmek** hedeflenmiştir.  

**Amaç:**  
- Genetik varyantların doğru sınıflandırılmasını sağlamak  
- Klinik karar destek sistemlerinde doğruluğu artırmak  
- Sınıf dengesizliği problemlerini ele almak  

---

## 📊 Kullanılan Modeller ve Yöntemler

### Geleneksel Makine Öğrenmesi:
- **Random Forest** – Tabular veri ve gürültüye dayanıklı  
- **CatBoost** – Kategorik veriler ve sınıf dengesizliği için optimize  
- **Gradient Boosting Classifier** – Karmaşık ilişkileri modelleme  
- **Logistic Regression, Naive Bayes, KNN** – Karşılaştırma amaçlı  

### Derin Öğrenme:
- **CNN** – Sıralı/genetik verilerde pattern tespiti  
- **GRU** – Uzun bağımlılıkları yakalamak için  
- **DNN** – Yüksek boyutlu veri için karmaşık ilişkiler  

### Veri İşleme ve Dengeleme:
- **Stratified Sampling** – Sınıf oranlarını koruma  
- **SMOTE** – Azınlık sınıfını artırma  
- **Özellik Seçimi** – Yüksek korelasyonlu değişkenleri azaltma  

---

## 📈 Deneysel Sonuçlar

| Model | Accuracy | F1-Score | Precision | Recall (Pathogenic) |
|-------|----------|----------|-----------|-------------------|
| Random Forest | 0.8010 | 0.7751 | 0.7650 | 0.3500 |
| CatBoost | 0.7990 | 0.7616 | 0.7994 | 0.7477 |
| Gradient Boosting | 0.7767 | 0.7456 | 0.7550 | 0.2900 |
| CNN | 0.7648 | 0.7400 | 0.7550 | 0.3200 |
| GRU | 0.7627 | 0.7350 | 0.7450 | 0.3100 |
| DNN | 0.7569 | 0.7200 | 0.7350 | 0.3000 |

**Öne çıkan model:**  
- **CatBoost**, yüksek recall ve precision ile patojenik varyantları tespit etmede en iyi performansı göstermiştir ve çok hızlı çalışır (0.0007 s/sample).  

---

## 🗂 Veri Seti
- **Kaynak:** [Kaggle – Conflicting ClinVar Variants](https://www.kaggle.com/datasets/kevinarvai/clinvar-conflicting)  
- **Toplam Örnek:** 65,188  
  - Benign: 48,754 (%74.8)  
  - Pathogenic: 16,434 (%25.2)  
- **Özellikler:** kromozom numarası, alleller, gen simgesi, fonksiyonel skorlar (CADD, SIFT, PolyPhen), klinik önem  

---
## 🔮 Gelecek Çalışmalar

Sistematik hiperparametre optimizasyonu (Bayesian Optimization / Optuna)

Model ensemble teknikleri ile daha yüksek performans

Transfer learning ve biyolojik ön bilgi entegrasyonu

Klinik karar destek sistemine gerçek zamanlı entegrasyon

---

## 🚀 Kullanım

1. Depoyu klonlayın:
```bash
git clone https://github.com/ilginkirez/ConflictVariantML.git
cd ConflictVariantML

2. Gerekli paketleri yükleyin:
pip install -r requirements.txt

3. Jupyter Notebook'u başlatın:
jupyter notebook

4. ML_Conflicting_Variants.ipynb dosyasını açın ve çalıştırın.


