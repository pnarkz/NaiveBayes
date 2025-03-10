# Naive Bayes ile İkili Sınıflandırma

Bu proje, Naive Bayes yöntemini kullanarak ikili sınıflandırma gerçekleştirmektedir. Hem **Scikit-learn GaussianNB modeli** hem de **Python ile sıfırdan yazılmış bir Gaussian Naive Bayes modeli** kullanılarak sonuçlar karşılaştırılmıştır.

##  Proje İçeriği
Bu proje, **diabetes.csv** veri seti üzerinde çalışmaktadır ve aşağıdaki aşamaları içermektedir:

1. **Veri Ön İşleme:**
   - Eksik veriler doldurulmuştur.
   - Özellikler bağımsız değişkenler (X) ve bağımlı değişken (y) olarak ayrılmıştır.
   - Veri, eğitim (%80) ve test (%20) olmak üzere ikiye bölünmüştür.

2. **Scikit-learn GaussianNB Modeli:**
   - Scikit-learn kütüphanesi kullanılarak GaussianNB modeli eğitilmiştir.
   - Modelin eğitim ve test süresi ölçülmüştür.
   - Karmaşıklık matrisi ile modelin performansı değerlendirilmiştir.

3. **Özel GaussianNB Modeli:**
   - Gaussian Naive Bayes modeli sıfırdan Python ile yazılmıştır.
   - Aynı veri seti ile eğitilip test edilmiştir.
   - Eğitim ve test süreleri ölçülmüştür.
   - Karmaşıklık matrisi kullanılarak modelin performansı analiz edilmiştir.

4. **Model Karşılaştırması:**
   - Her iki modelin doğruluk oranları, eğitim ve test süreleri karşılaştırılmıştır.
   - Sonuçlar görselleştirilerek analiz edilmiştir.

##  Proje Yapısı
```
1.naiveBayes/
│── gaussianNB_scikit.ipynb   # Scikit-learn modeli içeren notebook
│── gaussianNB_custom.ipynb   # Özel yazılmış Naive Bayes modeli içeren notebook
│── diabetes.csv              # Kullanılan veri seti
│── README.md                 # Proje açıklaması ve sonuç değerlendirmesi
│── requirements.txt          # Gerekli kütüphaneler
```

##  Veri Seti Hakkında
Kullanılan **diabetes.csv** veri seti, genellikle **Pima Indians Diabetes Database (PIDD)** olarak bilinir. **Tip-2 diyabet teşhisini** tahmin etmek amacıyla oluşturulmuştur ve **Pima Kızılderilileri** topluluğuna ait bireylerin sağlık verilerini içermektedir.

###  **Veri Seti Özellikleri**
| **Özellik**            | **Açıklama** |
|------------------------|-------------|
| **Pregnancies**        | Kişinin hamilelik sayısı |
| **Glucose**           | Kan şekeri (plazma glikoz) seviyesi (mg/dL) |
| **BloodPressure**      | Diyastolik kan basıncı (mm Hg) |
| **SkinThickness**      | Deri kıvrım kalınlığı (mm) |
| **Insulin**           | Serum insülin seviyesi (2 saatlik test sonucu) |
| **BMI**               | Vücut Kitle İndeksi (BMI) |
| **DiabetesPedigreeFunction** | Ailede diyabet görülme olasılığı (genetik risk faktörü) |
| **Age**               | Kişinin yaşı (yıl) |
| **Outcome**           | Diyabet durumu (0: Sağlıklı, 1: Diyabet) |

- **1000'den fazla örnek** içeren tabular veri setidir.
- **Bağımsız değişkenler** sürekli değerler içerdiği için **Gaussian Naive Bayes modeli için uygundur.**
- **Eksik veriler**, sürekli değişkenlerde ortalama ile doldurulmuştur.

##  Neden Gaussian Naive Bayes Seçildi?
**Gaussian Naive Bayes modeli**, sürekli veriler üzerinde etkili olan bir istatistiksel sınıflandırma yöntemidir. **Bu veri setinde tüm bağımsız değişkenler sayısal ve süreklidir (Glucose, BMI, Blood Pressure vb.), bu yüzden Gaussian modeli uygundur.**

- **GaussianNB, verilerin normal dağılıma sahip olduğunu varsayar.**
- **Hızlı ve hesaplama açısından verimlidir**, büyük veri setlerinde bile hızlı bir şekilde eğitilip tahmin yapabilir.
- **Basit ama güçlü bir modeldir**, küçük veri setlerinde bile genellikle iyi sonuçlar verir.
- **Eksik veri ve düşük boyutlu veri kümeleriyle çalışmada etkilidir.**

Alternatif olarak **Bernoulli Naive Bayes** veya **Multinomial Naive Bayes** gibi modeller de kullanılabilirdi ancak:
- **Bernoulli Naive Bayes** genellikle **ikili (binary) özellikler** ile çalışır.
- **Multinomial Naive Bayes** genellikle **metin madenciliği ve kategorik veriler** için uygundur.
- **Bu veri setindeki tüm özellikler sürekli olduğu için Gaussian Naive Bayes en iyi seçimdir.**

##  Sonuç ve Değerlendirme
Her iki modelin karşılaştırması aşağıdaki açılardan yapılmıştır:

- **Karmaşıklık Matrisi:** Modelin sınıflandırma başarısı görselleştirilmiştir.
- **Doğruluk Oranı:** Her iki modelin doğruluk oranı hesaplanmıştır.
- **Eğitim ve Test Süreleri:** Modellerin eğitim ve tahmin süreleri ölçülerek karşılaştırılmıştır.

Genellikle **Scikit-learn modeli** daha optimize ve hızlı çalışırken, özel olarak yazılan modelde performans düşüklüğü gözlemlenebilir. Bunun sebebi, kütüphanelerin optimize edilmiş matematiksel işlemler kullanmasıdır.

Daha detaylı analiz ve görselleştirmeler için ilgili notebook dosyalarına göz atabilirsiniz.


