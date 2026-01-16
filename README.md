
--Veri Analizi Portfolyosu

3.PROJE: Türkiye Enerji Verimliliği Analizi ve 2031 Projeksiyonu
Bu çalışma, Türkiye'nin 1990-2022 dönemi verilerini kullanarak enerji verimliliği (Energy Intensity) ile yenilenebilir enerji arzı arasındaki ilişkiyi analiz eden hibrit bir veri bilimi projesidir. Proje, hem geleneksel ekonometrik modelleri hem de modern makine öğrenmesi algoritmalarını içermektedir.

Proje Öne Çıkanlar
Hibrit Metodoloji: Değişkenler arası neden-sonuç ilişkileri için ARDL Sınır Testi, gelecek öngörüleri için Facebook Prophet (Machine Learning) kullanılmıştır.
Çok Dilli Entegrasyon: Veri çekme ve temizleme için SQL, ekonometrik modelleme için R, zaman serisi tahmini için Python dilleri reticulate kütüphanesi ile aynı ortamda koşturulmuştur.
Teknik Problem Çözme: Python-C++ derleyici (Rtools) ve sistem yolu (PATH) optimizasyonları yapılarak sistem mimarisi sorunları aşılmıştır.

Bulgular ve Öngörüler
Ekonometrik Sonuçlar: Bulgular, Türkiye'nin yenilenebilir enerji yatırımlarının enerji yoğunluğunu düşürdüğünü ve enerji verimliliğini istatistiksel olarak anlamlı düzeyde desteklediğini göstermektedir.
2031 Projeksiyonu: Prophet modeliyle yapılan makine öğrenmesi tahmini, mevcut trendin sürmesi durumunda enerji yoğunluğunun 2031 yılında 0.00077 birimine kadar gerileyeceğini işaret etmektedir.

Kullanılan Teknolojiler
Diller: SQL, R, Python
Kütüphaneler: - R: tidyverse, tseries, dynlm, reticulate
Python: pandas, prophet, matplotlib
Araçlar: RStudio, Git/GitHub, Rtools 4.4 (C++ Build Tools)

Dosya Yapısı
energy.Rmd: Analizin tüm kodlarını ve akademik yorumlarını içeren ana dosya.
energy.html: Projenin web tarayıcıda görüntülenebilen profesyonel rapor çıktısı.
energy.tex: Akademik raporun LaTeX formatındaki kaynak dosyası.

Bu depo (repository), veri analitiği yeteneklerimi sergilediğim projeleri içerir. Odak noktası; farklı programlama dillerini (**R, Python, SQL**) entegre ederek gerçek hayat problemlerine optimize çözümler üretmektir.

---

2. PROJE: Tedarik Zincirinde Stok Yönetimine Yönelik Analitik İnceleme
Bu depo (repository), veri analitiği yeteneklerimi sergilediğim projeleri içerir. Odak noktası; farklı programlama dillerini (**R, Python, SQL**) entegre ederek gerçek hayat problemlerine optimize çözümler üretmektir.
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

1. PROJE: Kaynak Tahsisi Analizi (Craven Local Plan)
**Dosya:** `kaynak_tahsisi_analizi.pdf`

Bu çalışma, Craven bölgesindeki arazi kullanım politikalarının veri odaklı değerlendirmesini içerir. Depo (Warehouse) ve konut alanlarının tahsisinde analitik düşünme süreci ve politika odaklı çözümlemeler yapılmıştır..

