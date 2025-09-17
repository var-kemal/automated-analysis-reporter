🎯 Proje Amacı, ticaret borsası'ndan alınan tarımsal ürün verilerini kullanarak karmaşık fiyat ve miktar analiz süreçlerini otomatikleştirmek için geliştirilmiş bir çözümdür. Uygulama, kullanıcıların Excel üzerinden kolayca veri girişi yapmasına olanak tanırken, aylık ve yıllık bazda fiyat ve miktar endekslerini otomatik olarak hesaplar. Elde edilen analiz sonuçları, zengin grafikler ve metinsel yorumlarla desteklenerek kapsamlı Word raporlarına dönüştürülür ve verilerin geçmiş yıllarla karşılaştırmalı olarak incelenmesine olanak tanır.

🚀 Özellikler
- 📂 **Excel Veri Tabanı**: `data.xlsx` dosyasında tüm ürünler saklanır.  
- ✍️ **Veri Girişi Arayüzü**: Kullanıcı yeni veri ekleyebilir, düzenleyebilir veya silebilir.  
- 📑 **Word Raporlama**: Otomatik raporlar grafik ve yorumlarla birlikte oluşturulur.  
- 📈 **Grafiksel Analiz**: Aylık ve yıllık değişim oranları grafiklerle görselleştirilir.  
- 🔎 **Geçmiş Yıl Karşılaştırmaları**: 2015’ten günümüze kadar verilerle analiz yapılır.  
- 📊 **Endeks Hesaplamaları**: Laspeyres fiyat endeksi yöntemi uygulanır.  

🧮 Kullanılan Matematiksel Yöntemler

📌 Laspeyres Fiyat Endeksi 

\mathbit{P}_\mathbit{L}=\ \frac{\sum{(\mathbit{p}_\mathbit{t}\ast\mathbit{q}_\mathbf{0})}}{\sum{(\mathbit{p}_\mathbf{0}\ast\mathbit{q}_\mathbf{0})}}
	\mathbit{p}_\mathbit{t} : Cari Dönem Fiyatı
	\mathbit{p}_\mathbf{0} : Temel Yıl Fiyatı
	\mathbit{q}_\mathbf{0}\ : Temel Yıl İşlem Miktarı

Ek hesaplamalar:

\mathbit{\Delta R}(%)=\frac{\mathbit{P}_\mathbf{1}-\mathbit{P}_\mathbf{0}}{\mathbit{P}_\mathbf{0}}\ \times\ \mathbf{100}
	\mathbit{P}_\mathbf{0} : Eski Değer
	\mathbit{P}_\mathbf{1} : Cari Değer
	∆R : Değişim Oranı





📑 Örnek Rapor Çıktısı (Eylül 2025 – Biber)

📈 Grafikler

	Yıllık Değişim Grafiği
 ![image_alt](https://github.com/var-kemal/automated-analysis-reporter/blob/f51ed5f6cb642c4d08d3e81e0a92d7f73063d734/yearly_plot.png)
 
Eylül ayında yıllık miktar endekslerinde; biber miktar endeksi ortalama civarında. Yıllık fiyat endekslerinde; biber fiyat endeksi ortalama civarında.

	Aylık Değişim Grafiği
 ![image_alt](https://github.com/var-kemal/automated-analysis-reporter/blob/ff8e1d25343c3641dc00b099b8af7668fec7b8c3/monthly_quantity.png)
 
Eylül ayında biber fiyat endeksi yıllık bazda yüzde 3.50 azaldı. Aynı dönemde biberin yıllık işlem miktarı yüzde 6.58 oranında arttı. Bu durum fiyat endeksindeki düşüşte etkili olmuştur.
Eylül ayında, son yedi yılın verileri dikkate alındığında biber satış miktarı ortalama civarında olarak kaydedildi. Biber fiyat seviyesi ortalama civarında olarak gerçekleşti.
Eylül ayında biber işlem miktar endeksi yüzde 24.21 azalırken, işlem fiyat endeksi yüzde 0.62 artış gösterdi; son yedi yılın Eylül ayları dikkate alındığında, işlem miktar endeksi altıncı en büyük azalış; son yedi yılın Eylül ayları dikkate alındığında, işlem fiyat endeksi beşinci en büyük artış olarak kaydedildi.











🧑‍💻 Kullanıcı Senaryosu
	
 	Kullanıcı uygulamayı açar (UrunlerAnalizRapor.exe).
	“Veri Girişi” menüsünden Domates – 2023 – Mart – 25.000.000 kg – 300.000.000 ₺ bilgisi ekler.
	Sistem veriyi data.xlsx içine işler.
	“Rapor Oluştur” seçeneği ile Mart 2023 raporu üretilir.
	Word raporunda:
	Domates için miktar ve fiyat endeksleri
	Mart ayı karşılaştırmaları
	Grafikler ve doğal dil yorumları yer alır.

📑 Uygulamanın Veri İşleme ve Raporlama Süreci
1. Veri Yükleme ve Hazırlık
	Uygulama, temel veri setini Excel (data.xlsx) dosyasından okur.
	Veriler ürün adı, yıl, ay, miktar ve tutar bilgilerini içerir.
	Gerekirse otomatik olarak yeni Excel dosyası oluşturulur.

2. Tablo Üretimi ve Yorumlama 
	Tablo, seçilen ürünlerin endekslerini gösterir:
	Miktar Endeksi:
	Endeks değeri
	Önceki aya göre değişim (%)
	Geçen yılın aynı ayına göre değişim (%)
	Fiyat Endeksi:
	Endeks değeri
	Önceki aya göre değişim (%)
	Geçen yılın aynı ayına göre değişim (%)
	Bu tabloya dayanarak otomatik yorum metinleri üretilir.
	Yorumlar: ürünlerin aylık ve yıllık bazda nasıl değişim gösterdiğini özetler.

3. Grafik Üretimi
Uygulama 2 tür grafik oluşturur:
	Aylık Grafikler
	Son 7 yılın verileri kullanılır
	Miktar endeksi (daire işaretli çizgi)
	Fiyat endeksi (kare işaretli çizgi)
	Güncel yıl kırmızı renkle vurgulanır
	Tablo altına yorum eklenir
	Yıllık Grafikler
	Son 10 yılın aynı ayı karşılaştırılır
	Hem miktar hem fiyat endeksi birlikte gösterilir
	Eğilimler görselleştirilir (artış/azalış trendi)

4. Analiz ve Yorumlar
	Aylık Analiz:
	Seçilen ayın verileri önceki ay ve geçen yıl ile kıyaslanır
	Artış/azalış yüzdesi belirtilir
	Ortalama değerlerin altında/üstünde olup olmadığı vurgulanır
	Yıllık Analiz:
	Uzun vadeli eğilimler değerlendirilir
	Örneğin: “Son 7 yılın Eylül ayları dikkate alındığında, biber miktar endeksi altıncı en büyük azalış olarak kaydedildi.”
Bu sayede rapor, sadece tablo ve grafik değil, aynı zamanda yorumlanmış metinsel özet içerir.

5. Şirkete Sağladığı Avantajlar
	Otomasyon: Manuel rapor hazırlama süresini ortadan kaldırır.
	Hızlı Karar Alma: Yönetim, aylık raporları dakikalar içinde elde eder.
	Standartlaşma: Tüm raporlar aynı formatta, profesyonel görsellikte üretilir.
	Detaylı Analiz: Hem tablo hem grafik hem de metinsel yorumlar sunularak çok yönlü analiz sağlanır.
	Geçmiş Karşılaştırmaları: 7–10 yıllık veri üzerinden trend analizi yapılır.

Kullanılan Kütüphaneler

* **GUI Framework:** * `customtkinter` (Modern ve özelleştirilebilir bir Tkinter uzantısı) 
* **Veri İşleme ve Analizi:** * `pandas` (Veri manipülasyonu ve analizi için) * `numpy` (Sayısal işlemler ve bilimsel hesaplamalar için) 
* **Veri Görselleştirme:** * `matplotlib` (Statik, interaktif ve hareketli görselleştirmeler oluşturmak için) * `seaborn` (Matplotlib üzerine kurulu, istatistiksel grafikler için üst düzey bir arayüz) 
* **Belge İşleme:** * `python-docx` (Microsoft Word .docx dosyalarını oluşturmak ve değiştirmek için) 
* **Excel Dosya İşleme:** * `openpyxl` (Excel .xlsx dosyalarını okumak/yazmak için) 
* **Görsel Yardımcı Programlar:** * `Pillow` (Görüntü işleme yetenekleri için, özellikle GUI öğeleri için faydalı olabilir) 


👤 Geliştirici
Kemal Gvaramadze
	Veri analizi ve yapay zeka alanında çalışmalar
	Python ile masaüstü uygulama geliştirme

* **Yürütülebilir Dosya Oluşturma:** * `pyinstaller` (Python uygulamalarını bağımsız yürütülebilir dosyalar halinde paketlemek için) ---

