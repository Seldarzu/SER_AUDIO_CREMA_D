# Ses Tabanlı Konuşma Duygu Tanıma (SER)

Bu repository, **CREMA-D veri seti** kullanılarak gerçekleştirilen
**ses tabanlı konuşma duygu tanıma (Speech Emotion Recognition)** çalışmalarını içermektedir.

Amaç, farklı **veri bölme protokollerinin** ve **ses modelleme yaklaşımlarının**
duygu tanıma performansı üzerindeki etkisini sistematik olarak incelemektir.

---

## 🎯 Proje Amaçları
- Konuşma/ses sinyallerinden duygu tahmini yapmak
- Random split ve speaker-independent split yaklaşımlarını karşılaştırmak
- Klasik ve derin öğrenme tabanlı ses modellerini değerlendirmek
- Akademik olarak şeffaf ve tekrar üretilebilir sonuçlar sunmak

---

## 🧠 Kullanılan Ses Modelleme Yaklaşımları

### 1️⃣ MFCC Tabanlı Modeller
- Mel-Frequency Cepstral Coefficients (MFCC)
- Yorumlanabilir ve temiz pipeline’lar
- Güçlü baseline ve nihai sonuçlar için kullanılmıştır

### 2️⃣ Wav2Vec2 Tabanlı Modeller
- Ön-eğitimli (self-supervised) konuşma temsilleri
- FAST ve FULL eğitim stratejileri
- Hiperparametrelerin sistematik olarak test edilmesi

---

## 🔀 Veri Bölme Protokolleri

### 🔹 Speaker-Independent Split
**`AUDIO_03_modeling_SER_speaker_independent_v01.ipynb`**

- Eğitim ve test setlerinde aynı konuşmacılar yer almaz
- Speaker leakage engellenir
- Gerçekçi ve zorlayıcı bir değerlendirme sağlar
- Akademik olarak tercih edilen protokoldür

---

### 🔹 Random Split
**`AUDIO_03_modeling_SER_random_split_v01.ipynb`**

- Veri rastgele bölünür
- Aynı konuşmacı train ve test setinde yer alabilir
- Performans genellikle daha yüksek çıkar
- Karşılaştırma amacıyla tutulmuştur

Bu iki yaklaşım, **metodolojik farkların açıkça gösterilmesi** amacıyla birlikte sunulmaktadır.

---

## 📂 Notebook Açıklamaları

### `AUDIO_00_raw_CREMA-D_dataset_sanity_v01.ipynb`
- CREMA-D veri setinin incelenmesi
- Ham ses verileri üzerinde kontroller
- İlk keşifsel analizler

---

### `AUDIO_03_modeling_SER_speaker_independent_v01.ipynb`
- Nihai speaker-independent SER modeli
- Ana referans notebook

---

### `AUDIO_03_modeling_SER_random_split_v01.ipynb`
- Random split ile SER modelleme
- Baseline karşılaştırma notebook’u

---

### `AUDIO_04_experiments_CREMA-D_wav2vec2_gridsearch_v01.ipynb`
- Wav2Vec2 tabanlı kapsamlı deneyler
- FAST / FULL eğitim modları
- Hiperparametre taramaları

---

### `AUDIO_05_final_audio_emotion_results_v01.ipynb`
- Nihai MFCC tabanlı sonuçlar
- Temiz eğitim ve değerlendirme akışı
- Performans metrikleri

---

## 📦 Model Dosyaları
GitHub dosya boyutu kısıtları nedeniyle eğitilmiş model dosyaları
(`.pt` / `.pth`) repository içerisinde yer almamaktadır.

---

## 👩‍💻 Hazırlayan
**Arzu Selda Avcı**  
Bilgisayar Mühendisliği – Derin Öğrenme / Konuşma Duygu Tanıma
