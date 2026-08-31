# Bancassurance-Analytics-Project
Bütünleşik Finansal Risk Yönetimi: Kredi Skorlama, Aktüeryal Fiyatlama ve Erken Uyarı (Churn) Sistemleri üzerine matematiksel ve istatistiksel modelleme serisi.
# 🏦 Bütünleşik Finansal Risk Analitiği (Bancassurance)

Bu proje, bir müşterinin kredi riskinden başlayıp, sigorta (kasko) fiyatlamasına ve son olarak müşteri kaybı (churn) erken uyarı sistemine kadar uzanan uçtan uca bir makine öğrenmesi ve istatistiksel modelleme serisidir. Standart metriklerin ötesine geçerek, gerçek dünyadaki finansal dengesizlikleri matematiksel bir yaklaşımla çözmeyi hedefler.

## 📌 Proje Modülleri

### 🟢 Modül 1: Kredi Skorlamada Dengesiz Veri Tuzağı (Tamamlandı)
* **Amaç:** Taşıt kredisi başvurularında temerrüt (batık) riskini hesaplamak.
* **Problem:** Batık kredilerin veri setinde yalnızca %8 gibi çok düşük bir oranda olması (Imbalanced Data), modellerin %90'ın üzerinde sahte bir doğruluk (Accuracy) üretmesine neden olur.
* **Matematiksel ve Analitik Çözüm:** 
  * LightGBM algoritması kullanılarak azınlık sınıfı ağırlıklandırıldı (`is_unbalance=True`).
  * Model performansı yanıltıcı Accuracy yerine **PR-AUC** (Precision-Recall Area Under Curve) ve **F1-Score** metrikleri ile değerlendirildi.
  * Standart modellerin kaçırdığı 2726 gerçek batık müşteri tespit edilerek potansiyel finansal zarar engellendi.
* **Kullanılan Veri:** Kaggle - Home Credit Default Risk

### ⚪ Modül 2: Kasko Hasar Maliyeti Tahmini (Geliştiriliyor)
* **Kapsam:** Poisson ve Gamma dağılımları kullanılarak Genelleştirilmiş Doğrusal Modeller (GLM) ile Aktüeryal Saf Prim (Pure Premium) hesaplaması.

### ⚪ Modül 3: Müşteri Kaybı (Churn) Erken Uyarı Sistemi (Yakında)
* **Kapsam:** Müşteri ayrılmadan önceki 30 günlük işlem hareketlerinden çıkarılan kilit risk göstergelerinin analizi.

---
*Not: Bu proje modüller halinde geliştirilmekte olup, kodlar sırasıyla ilgili klasörlere eklenmektedir.*
