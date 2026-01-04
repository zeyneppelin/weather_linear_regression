- weather_linear_regression
- Hava Durumu Sıcaklık Tahmini (Linear Regression)

- Proje Amacı
Bu projede amaç, geçmiş hava durumu verilerini kullanarak Temperature (C) (sıcaklık) değerini tahmin eden bir makine öğrenmesi regresyon modeli** oluşturmaktır.

Bu çalışma, ham veriden başlayarak veri temizleme, feature engineering, modelleme ve değerlendirme adımlarını içeren uçtan uca bir makine öğrenmesi pipeline’ıdır.

-Veri Seti
- Dosya adı: `weatherHistory.csv`
- Hedef değişken (tahmin edilen): `Temperature (C)`

-Yapılan Adımlar
 1. Veri Yükleme
CSV dosyası okunarak veri seti incelenmiştir.
Verinin boyutu, kolonları ve temel yapısı kontrol edilmiştir.

2. Veri Temizleme
- Formatted Date kolonu datetime formatına çevrilmiştir.
- Loud Cover kolonu sabit değer içerdiği için veri setinden çıkarılmıştır.
- Eksik değerler kontrol edilmiş ve gerekli durumlarda temizlenmiştir.
Amaç: Modelin hatalı veya anlamsız verilerden etkilenmesini önlemek.

3. Kategorik Verilerin Sayısallaştırılması
Aşağıdaki kategorik kolonlar sayısal hale getirilmiştir:
- Summary
- Precip Type
- Daily Summary

Bu işlem Label Encoding yöntemi ile yapılmıştır.

Amaç: Makine öğrenmesi modelinin metin verilerini anlayabilmesi.

 4. Feature ve Target Ayrımı
- Hedef değişken (y): Temperature (C)
- Bağımsız değişkenler (X): Diğer tüm kolonlar
- Formatted Date kolonu modele doğrudan verilmemiştir.

 5. Train / Test Ayrımı
Veri seti:
- %80 eğitim (train)
- %20 test

olarak ikiye ayrılmıştır.

Amaç: Modelin ezber yapmadığından emin olmak.

 6. Ölçekleme (StandardScaler)
Sayısal değişkenler StandardScaler ile ölçeklendirilmiştir.

Amaç:
- Büyük sayılı kolonların modeli domine etmesini önlemek
- Lineer regresyonun daha sağlıklı öğrenmesini sağlamak

 7. Modelleme (Linear Regression)
- Linear Regression modeli eğitilmiştir.
- Test verisi üzerinde tahminler alınmıştır.

 8. Model Değerlendirme
Model performansı şu metriklerle değerlendirilmiştir:
- R² Score
- Mean Squared Error (MSE)

Ayrıca:
- Gerçek değerler ile tahmin edilen değerler karşılaştırılarak
  görsel bir grafik oluşturulmuştur.

## Sonuç
Bu proje, temel bir regresyon problemi için temiz ve anlaşılır bir makine öğrenmesi yaklaşımı sunmaktadır.
Aynı yapı, farklı veri setleri için de kolayca uyarlanabilir.

