
--Veri Analizi Portfolyosu: Tedarik Zinciri & Kaynak Yönetimi

Bu depo (repository), veri analitiği yeteneklerimi sergilediğim projeleri içerir. Odak noktası; farklı programlama dillerini (**R, Python, SQL**) entegre ederek gerçek hayat problemlerine optimize çözümler üretmektir.

---

1️. PROJE: Tedarik Zincirinde Stok Yönetimine Yönelik Analitik İnceleme
**Kullanılan Teknolojiler:** `R Markdown` • `Python (Seaborn)` • `SQL (SQLite)`

--Projenin Amacı:
Bu proje, sadece bir veri analizi değil, **üç farklı teknolojinin tek bir raporda (Interoperability) konuşturulduğu** bir optimizasyon çalışmasıdır.

* **SQL:** Büyük veri setini filtrelemek ve tedarikçi bazında gruplamak (Aggregation) için kullanıldı.
* **R:** İstatistiksel modelleme (Regresyon Analizi) ve veri manipülasyonu için kullanıldı.
* **Python:** Elde edilen sonuçların görselleştirilmesi (Bubble Chart) ve grafik kütüphanelerinin R ortamında çalıştırılması için kullanıldı.

--Temel Çıkarım (Sonuç)
Analiz sonucunda; ciro lideri olan bazı tedarikçilerin (**Örn: E&J Gallo**), yüksek transfer sayıları yüzünden şirkete gizli lojistik maliyet yarattığı tespit edilmiştir. Çözüm olarak, verimli çalışan (**Örn: Republic National**) tedarikçilerin dağıtım modellerinin örnek alınması önerilmiştir.

<img width="1471" height="549" alt="Ekran görüntüsü 2026-01-06 231810" src="https://github.com/user-attachments/assets/d58b06f0-002e-4bdb-934d-b6dcfc42d1ef" />

Veri biliminde bir model kurmak yeterli değildir; o modelin matematiksel varsayımları karşıladığından emin olunmalıdır. R ile oluşturulan bu tanısal grafikler (Diagnostic Plots), kurduğumuz regresyon modelinin tutarlılığını test etmektedir. Özellikle Normal Q-Q grafiğindeki doğrusallık, hata terimlerinin (residuals) normal dağıldığını; Residuals vs Fitted grafiği ise varyansın homojenliğini kanıtlamaktadır. Bu teknik doğrulama, 'transfer sayısının satış üzerindeki etkisinin' tesadüfi olmadığını, modelin istatistiksel olarak güvenilir ve gürbüz (robust) bir yapıya sahip olduğunu doğrular.

<img width="667" height="503" alt="Ekran görüntüsü 2026-01-06 231757" src="https://github.com/user-attachments/assets/6724e7d7-b46e-4c25-9bed-2d1a0a3c358a" />
Python (Seaborn) kütüphanesinin görselleştirme yetenekleri kullanılarak oluşturulan bu analiz, tedarikçileri 'Satış Performansı' ve 'Operasyonel Lojistik Yükü' ekseninde segmentlere ayırır. Balon büyüklükleri işlem hacmini temsil ederken; sağ tarafta kümelenen tedarikçilerin yüksek ciro sağlamalarına rağmen, aşırı transfer sayılarıyla (x-ekseni) şirkete gizli bir lojistik maliyet yüklediği görülmektedir. Buna karşın sol üst kadrandaki 'Yıldız Bölge', minimum lojistik eforla maksimum satışın yakalandığı optimum verimlilik alanını temsil eder ve stratejik planlama için hedef model olarak belirlenmiştir.

*(Detaylı kodlar ve analiz adımları için yukarıdaki `tedarik_zinciri_optimizasyonu.Rmd` dosyasına bakabilirsiniz.)*

2️. PROJE: Kaynak Tahsisi Analizi (Craven Local Plan)
**Dosya:** `kaynak_tahsisi_analizi.pdf`

Bu çalışma, Craven bölgesindeki arazi kullanım politikalarının veri odaklı değerlendirmesini içerir. Depo (Warehouse) ve konut alanlarının tahsisinde analitik düşünme süreci ve politika odaklı çözümlemeler yapılmıştır..

