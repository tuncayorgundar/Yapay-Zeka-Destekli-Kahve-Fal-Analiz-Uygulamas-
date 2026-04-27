# Yapay Zeka Destekli Kahve Falı Analiz Uygulaması

Bu proje, geleneksel kahve falı yorumlama sürecini bilgisayarlı görü ve derin öğrenme teknikleriyle modernize eden uçtan uca bir mobil uygulama çözümüdür.

## 📋 Proje Özeti

Sistem, kullanıcıdan alınan kahve fincanı fotoğraflarını dijital bir analiz sürecinden geçirir. OpenCV ile ön işleme tabi tutulan görüntüler, YOLOv8 nesne tespit modeli ile analiz edilerek fincan içindeki semboller tanımlanır. Tespit edilen semboller, önceden tanımlanmış anlam kümeleriyle eşleştirilerek kullanıcıya kişiselleştirilmiş bir yorum sunulur.

## 🛠 Kullanılan Teknolojiler

  * **Görüntü İşleme:** OpenCV (Python).
  * **Derin Öğrenme:** YOLOv8 (Nesne Tespiti).
  * **Mobil Uygulama:** Flutter & Dart.
  * **Backend & Veri Yönetimi:** Firebase Entegrasyonu ve Python API.

## 🏗 Sistem Mimarisi ve İş Akışı

### 1\. Görüntü Ön İşleme (OpenCV)

Görüntüdeki gürültüleri azaltmak ve sembolleri belirginleştirmek için aşağıdaki teknikler uygulanır:

  * **Gri Tonlama:** Renkli görüntülerin işleme hızını artırmak için dönüştürülmesi.
  * **Gaussian Blur:** Görüntü üzerindeki gürültülerin (noise) azaltılması.
  * **Canny Edge Detection:** Nesne sınırlarının ve kenarların belirlenmesi.
  * **Kontur Analizi:** Belirlenen kenarlar üzerinden sembollerin tekil nesneler olarak ayrıştırılması.

### 2\. Nesne Tespiti (YOLOv8)

Ön işlemeden geçen görüntüler eğitilmiş YOLOv8 modeline aktarılır. Model:

  * Fincan içindeki sembolleri (hayvan, nesne, şekil vb.) yüksek hassasiyetle tespit eder.
  * Tespit edilen her sembolü veri tabanındaki anlam karşılıkları ile eşleştirir.

### 3\. Mobil ve Bulut Entegrasyonu

  * **Flutter:** Kullanıcı dostu arayüz üzerinden fotoğraf alımı ve sonuç gösterimi sağlar.
  * **Firebase:** İşlenen verilerin saklanması ve kullanıcı profillerinin yönetilmesini sağlar.
  * **Python API:** Mobil uygulama ile yapay zeka modeli arasındaki iletişimi kurar.

## 🚀 Temel Özellikler

  * Bilimsel yaklaşımla otomatikleştirilmiş geleneksel fal analizi.
  * Yapay zeka destekli hassas nesne tanıma.
  * Bulut tabanlı veri saklama ve hızlı erişim.
