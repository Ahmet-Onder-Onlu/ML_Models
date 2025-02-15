# sparkMachineLearning
Proje Özeti: Veri Ön İşleme ve Modelleme
Veri Hazırlığı ve Temizliği:

Eksik Değerlerin İmpütasyonu: Verisetindeki total_bedrooms özelliğinde eksik değerler vardı. Bu eksiklikler, PySpark’ın Imputer fonksiyonu kullanılarak dolduruldu.
Öznitelik Seçimi ve Dönüştürme: Kullanılacak özellikler belirlenip, gereksiz veya düşük etki gösteren özellikler çıkarıldı. Bu süreç, modelin doğruluğunu artırmak için önemlidir.
Öznitelik Kodlama:

Kategorik Verilerin Kodlanması: ocean_proximity gibi kategorik değişkenler için StringIndexer ve OneHotEncoder kullanılarak sayısal verilere dönüştürüldü. Bu, modellerin kategorik verilerle etkili çalışmasını sağlar.
Öznitelik Ölçekleme ve Vektörleştirme:

Öznitelik Vektörleştirme: Modelin daha verimli çalışması için sayısal öznitelikler, PySpark’ın VectorAssembler fonksiyonu ile birleştirildi. Bu, tüm sayısal özelliklerin tek bir vektör halinde işlenmesini sağladı.
Pipeline Yapısı:

Pipeline Kullanımı: Veri ön işleme ve modelleme adımlarını sırasıyla otomatikleştirmek için PySpark’ın Pipeline sınıfı kullanıldı. Bu, her model için aynı veri işleme adımlarını tekrar etmeyi sağladı.
Modelleme ve Değerlendirme:

Çeşitli Modellerin Denenmesi: Linear Regression, Random Forest, GBTRegressor ve Generalized Linear Regression gibi farklı modeller test edildi. Bu modellerin her biri, CrossValidator ile çapraz doğrulama yöntemine tabi tutuldu.
Hiperparametre Ayarı (GridSearch): Modellerin performansını optimize etmek için, ParamGridBuilder ve CrossValidator kullanılarak hiperparametre ayarlamaları yapıldı.
Model Performansının Değerlendirilmesi:

RMSE ve R² Değerleri: Her model için hata oranı ve doğruluk performansı, RMSE ve R² metrikleri ile değerlendirildi. Bu metrikler, her modelin doğruluğunu ve genel performansını anlamaya yardımcı oldu.
Sonuçların Görselleştirilmesi:

Performans Karşılaştırması: Modellerin RMSE ve R² değerleri, bir çubuk grafik ve çizgi grafiği kullanılarak görselleştirildi. Böylece, her modelin performansı açıkça karşılaştırılabilir hale getirildi.
Modelin Kaydedilmesi ve Yüklenmesi:

En İyi Modelin Seçimi ve Kaydedilmesi: Performans sonuçlarına göre en iyi model olan GBTRegressor kaydedildi. Bu model, gelecekte yeniden kullanılmak üzere bir dizine save() fonksiyonu ile kaydedildi.
