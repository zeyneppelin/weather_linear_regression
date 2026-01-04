 weather_linear_regression
 Hava Durumu Sıcaklık Tahmini (Linear Regression)

 Proje Amacı
Bu projede amaç, geçmiş hava durumu verilerini kullanarak Temperature (C) (sıcaklık) değerini tahmin eden bir makine öğrenmesi regresyon modeli oluşturmaktır.

Bu çalışma, ham veriden başlayarak **veri temizleme**, **kategorik dönüşümler**, **ölçekleme**, **modelleme** ve **değerlendirme** adımlarını içeren **uçtan uca bir makine öğrenmesi pipeline’ı** sunmaktadır.


Veri Seti
- Dosya adı: weatherHistory.csv
- Hedef değişken (tahmin edilen):Temperature (C)


Yapılan Adımlar
 1. Veri Yükleme
CSV dosyası okunarak veri seti incelenmiştir.  
Verinin boyutu, kolonları ve temel yapısı kontrol edilmiştir.

2. Veri Temizleme
- Formatted Date kolonu datetime formatına çevrilmiştir.
- Loud Cover kolonu sabit değer içerdiği için veri setinden çıkarılmıştır.
- Eksik değerler kontrol edilmiş ve gerekli durumlarda veri setinden temizlenmiştir.

Amaç: 
Modelin hatalı, eksik veya anlamsız verilerden etkilenmesini önlemek.

 3. Kategorik Verilerin Sayısallaştırılması
Aşağıdaki kategorik kolonlar **Label Encoding** yöntemi ile sayısal hale getirilmiştir:
- Summary
- Precip Type
- Daily Summary

Amaç:
Makine öğrenmesi modelinin metin tabanlı verileri sayısal olarak işleyebilmesini sağlamak.

 4. Feature ve Target Ayrımı
- Hedef değişken (y): Temperature (C)
- Bağımsız değişkenler (X): Diğer tüm kolonlar
- Formatted Date kolonu modele doğrudan verilmemiştir.

 5. Train / Test Ayrımı
Veri seti:
- %80 eğitim (train)
- %20 test
olacak şekilde ikiye ayrılmıştır.

Amaç:  
Modelin ezber yapmadan, daha önce görmediği veriler üzerinde performansının ölçülmesini sağlamak.

 6. Ölçekleme (StandardScaler)
Sayısal değişkenler **StandardScaler** kullanılarak ölçeklendirilmiştir.

Amaç:
- Büyük ölçekli değişkenlerin modeli domine etmesini önlemek  
- Lineer regresyon modelinin daha sağlıklı öğrenmesini sağlamak


 7. Modelleme (Linear Regression)
- Linear Regression modeli eğitilmiştir.
- Test verisi üzerinde tahminler alınmıştır.

 8. Model Değerlendirme
Model performansı aşağıdaki metriklerle değerlendirilmiştir:
- R² Score
- Mean Squared Error (MSE)

Ayrıca:
- Gerçek değerler ile tahmin edilen değerler karşılaştırılarak görsel bir grafik oluşturulmuştur.



