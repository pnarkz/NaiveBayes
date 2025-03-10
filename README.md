Naive Bayes ile İkili Sınıflandırma

Bu proje, Naive Bayes yöntemini kullanarak ikili sınıflandırma gerçekleştirmektedir. Hem Scikit-learn GaussianNB modeli hem de Python ile sıfırdan yazılmış bir Gaussian Naive Bayes modeli kullanılarak sonuçlar karşılaştırılmıştır.

📌 Proje İçeriği

Bu proje, diabetes.csv veri seti üzerinde çalışmaktadır ve aşağıdaki aşamaları içermektedir:

Veri Ön İşleme:

Eksik veriler doldurulmuştur.

Özellikler bağımsız değişkenler (X) ve bağımlı değişken (y) olarak ayrılmıştır.

Veri, eğitim (%80) ve test (%20) olmak üzere ikiye bölünmüştür.

Scikit-learn GaussianNB Modeli:

Scikit-learn kütüphanesi kullanılarak GaussianNB modeli eğitilmiştir.

Modelin eğitim ve test süresi ölçülmüştür.

Karmaşıklık matrisi ile modelin performansı değerlendirilmiştir.

Özel GaussianNB Modeli:

Gaussian Naive Bayes modeli sıfırdan Python ile yazılmıştır.

Aynı veri seti ile eğitilip test edilmiştir.

Eğitim ve test süreleri ölçülmüştür.

Karmaşıklık matrisi kullanılarak modelin performansı analiz edilmiştir.

Model Karşılaştırması:
Her iki modelin doğruluk oranları, eğitim ve test süreleri karşılaştırılmıştır.
Sonuçlar görselleştirilerek analiz edilmiştir.

Proje Yapısı
1.naiveBayes/
│── gaussianNB_scikit.ipynb   # Scikit-learn modeli içeren notebook
│── gaussianNB_custom.ipynb   # Özel yazılmış Naive Bayes modeli içeren notebook
│── diabetes.csv              # Kullanılan veri seti
│── README.md                 # Proje açıklaması ve sonuç değerlendirmesi
│── requirements.txt          # Gerekli kütüphaneler

🔍 Sonuç ve Değerlendirme

Her iki modelin karşılaştırması aşağıdaki açılardan yapılmıştır:

Karmaşıklık Matrisi: Modelin sınıflandırma başarısı görselleştirilmiştir.

Doğruluk Oranı: Her iki modelin doğruluk oranı hesaplanmıştır.

Eğitim ve Test Süreleri: Modellerin eğitim ve tahmin süreleri ölçülerek karşılaştırılmıştır.

Genellikle Scikit-learn modeli daha optimize ve hızlı çalışırken, özel olarak yazılan modelde performans düşüklüğü gözlemlenebilir. Bunun sebebi, kütüphanelerin optimize edilmiş matematiksel işlemler kullanmasıdır.

Daha detaylı analiz ve görselleştirmeler için ilgili notebook dosyalarına göz atabilirsiniz.# NaiveBayes
