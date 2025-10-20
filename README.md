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

$$
P_L = \frac{\sum(p_t \cdot q_0)}{\sum(p_0 \cdot q_0)}
$$

Burada:
- **$p_t$**: Cari Dönem Fiyatı
- **$p_0$**: Temel Dönem/Yıl Fiyatı
- **$q_0$**: Temel Dönem/Yıl İşlem Miktarı

Ek hesaplamalar:

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\color{White}\LARGE&space;\Delta&space;R(\%)&space;=&space;\frac{P_1&space;-&space;P_0}{P_0}&space;\times&space;100" alt="Yüzde Değişim Formülü">
</div>

Burada:
- **$P_1$**: Cari (Yeni) Değer
- **$P_0$**: Önceki (Eski) Değer
- **$\Delta R$**: İki değer arasındaki yüzdesel değişim oranı


## 📑 Örnek Rapor (Eylül 2025 – Biber)

### 📈 Grafikler  

**Yıllık Değişim**  
![Yıllık Değişim](https://github.com/var-kemal/automated-analysis-reporter/blob/deb6bffbdc1ad3dc59b8c0a7bc334e7262b2b9a0/yearly_plot.png)  

**Aylık Değişim**  
![Biber Miktar Endeksi Aylık Değişim](https://github.com/var-kemal/automated-analysis-reporter/blob/ff8e1d25343c3641dc00b099b8af7668fec7b8c3/monthly_quantity.png)  
![Biber Fiyat Endeksi Aylık Değişim](https://github.com/var-kemal/automated-analysis-reporter/blob/f814ef557547a9903b80d6ee53c50c6ed9a03888/monthly_amount.png)  

---

### 📌 Yorum (Özet)
- **Fiyat Endeksi:** Yıllık bazda %3.50 azaldı.  
- **Miktar Endeksi:** Yıllık bazda %6.58 arttı → fiyat düşüşünde etkili.  
- **Geçmiş Karşılaştırma:** 7 yıllık ortalamaya göre fiyat ve miktar ortalama civarında.  
- **Eylül 2025:** Miktar endeksi %24.21 azaldı, fiyat endeksi %0.62 arttı.  

---

👤 **Geliştirici:** Kemal Gvaramadze  
📧 **İletişim:** kemalgvaramadze.is@gmail.com
