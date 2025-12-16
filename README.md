# Genetik Algoritma ile Nakliye Rotası Optimizasyonu


**Hazırlayan:** Ömer TAŞKIN
**Öğrenci No:** 2212721023
**github linki** https://github.com/omertkn1/nakliye-rotasi-optimizasyon


## Proje Açıklaması

Bu proje, bir lojistik firmasının rota seçimi sırasında yakıt tüketimi ve süreyi optimize etmesi için genetik algoritma kullanmaktadır. Senaryo 3'e göre geliştirilmiştir.

## Problem Tanımı

### Amaç Fonksiyonu
$$y = -2x_1 - 3x_2 + 0.1x_1x_2$$

Bu fonksiyon negatif toplam maliyeti temsil eder. Maksimize etmek istiyoruz (yani maliyeti minimize etmek).

### Değişkenler
- **x₁**: Ortalama hız (km/h) → [40, 100]
- **x₂**: Araç yük kapasitesi (ton) → [2, 10]

### Kısıtlar
- $x_1 \times x_2 \leq 700$ (Motor gücü limiti)
- $x_1 \geq 60$ (Minimum hız şartı)

## Kurulum

### Gereksinimler
Bu projeyi çalıştırmak için aşağıdaki Python kütüphanelerine ihtiyacınız vardır:

```bash
pip install numpy matplotlib
```

### Dosya Yapısı
```
NakliyeOptimizasyon/
├── genetikAlgoritma_optimizasyon.ipynb  # Ana Jupyter notebook
└── README.md                              # Bu dosya
```

## Çalışma Adımları

1. **Kütüphaneleri İçe Aktarın**: İlk hücrede gerekli kütüphaneler yüklenir.

2. **Problem Parametrelerini Tanımlayın**: Değişken sınırları ve kısıtlar tanımlanır.

3. **Amaç Fonksiyonu ve Kısıt Kontrolü**: Amaç fonksiyonu ve kısıt kontrol fonksiyonları tanımlanır.

4. **Genetik Algoritma Parametreleri**: Popülasyon boyutu, nesil sayısı, çaprazlama ve mutasyon oranları ayarlanır.

5. **Birey ve Popülasyon Tanımları**: Her birey iki gen içerir (x1: hız, x2: yük kapasitesi).

6. **Seçilim Mekanizması**: Turnuva seçilimi uygulanır.

7. **Çaprazlama (Crossover)**: Aritmetik çaprazlama ile yeni bireyler oluşturulur.

8. **Mutasyon**: Rastgele gen değişiklikleri uygulanır.

9. **Elitizm**: En iyi bireyler korunur.

10. **Genetik Algoritma Ana Döngüsü**: Algoritma çalıştırılır ve sonuçlar elde edilir.

11. **Görselleştirme**: Sonuçlar grafiklerle görselleştirilir.

12. **Analiz ve Yorum**: Sonuçlar analiz edilir ve yorumlanır.

## Kullanım

1. Jupyter Notebook'u başlatın:
   ```bash
   jupyter notebook genetikAlgoritma_optimizasyon.ipynb
   ```

2. Tüm hücreleri sırayla çalıştırın (Cell → Run All veya Shift+Enter ile her hücreyi tek tek çalıştırın).

3. Sonuçları inceleyin:
   - Fitness değerlerinin evrimi
   - Değişkenlerin evrimi
   - Çözüm yolunun görselleştirilmesi
   - Detaylı analiz ve yorumlar

## Genetik Algoritma Bileşenleri

### 1. Popülasyon Tanımı
- Her birey iki gen içerir: x1 (hız) ve x2 (yük kapasitesi)
- Popülasyon boyutu: 50 birey

### 2. Fitness Fonksiyonu
- Amaç fonksiyonu değeri kullanılır
- Kısıt ihlalleri için ceza verilir (-10000)

### 3. Seçilim Mekanizması
- **Turnuva Seçilimi**: Rastgele seçilen bireyler arasından en iyisi seçilir
- Turnuva boyutu: 3

### 4. Çaprazlama (Crossover)
- **Aritmetik Çaprazlama**: Ebeveynlerin özelliklerini birleştirir
- Çaprazlama oranı: 0.8

### 5. Mutasyon
- Rastgele gen değişiklikleri uygulanır
- Mutasyon oranı: 0.1
- Genetik çeşitliliği artırır ve yerel optimumlardan kaçınmayı sağlar

### 6. Elitizm
- Her nesilde en iyi 2 birey korunur
- Çözüm kalitesini garanti eder

## Parametreler

- **Popülasyon Boyutu**: 50
- **Maksimum Nesil**: 100
- **Çaprazlama Oranı**: 0.8
- **Mutasyon Oranı**: 0.1
- **Turnuva Boyutu**: 3
- **Elitizm Sayısı**: 2

## Sonuçlar

Genetik algoritma, verilen kısıtlar altında amaç fonksiyonunu optimize eder. Algoritma çalıştırıldığında:

- En iyi çözüm değerleri (x1, x2)
- Amaç fonksiyonu değeri
- Kısıt kontrolü sonuçları
- Fitness değerlerinin evrimi
- Değişkenlerin evrimi
gösterilir.

## Notlar

- Kod Türkçe açıklamalarla yazılmıştır
- Her adımda detaylı markdown açıklamaları bulunmaktadır
- Kısıtlar otomatik olarak kontrol edilir ve sağlanır
- Görselleştirmeler algoritmanın çalışmasını anlamayı kolaylaştırır

## Lisans

Bu proje eğitim amaçlıdır.


