# Otobus Bilgileri ve Seferleri Projesi

## Proje Tanımı
Bu proje, otobus bilgilerini ve sefer detaylarını yönetmek için geliştirilmiştir. İki adet Z'li Tablo kullanılarak otobus bilgileri ve sefer detayları tutulmaktadır. Bu tablolar `ZIS_BUSINFO` ve `ZIS_TRIPDETAIL` olarak adlandırılmıştır.

## Proje Dosya Yapısı

Proje, karmaşıklığı azaltmak ve düzeni sağlamak için üç ana dosyaya ayrılmıştır. Bunlar `MainProject`, `FunctionInclude`, ve `DataInclude` dosyalarıdır.

### 1. MainProject
Ana projenin bulunduğu dosyadır. TabStrip ekranlarının oluşturulması ve gerekli fonksiyonların çağrılması burada yer almaktadır.

### 2. FunctionInclude
Proje içinde kullanılan fonksiyonların bulunduğu dosyadır. Ana projeden çağrılarak kullanılmaktadır.

### 3. DataInclude
Veri tanımlamalarının yapıldığı dosyadır. Fonksiyonlarda kullanılan tablo structure yapılarının tanımlandığı dosyadır.

## Proje Kullanım

**Tab Ekranları :** 
Ana projede bulunan tab ekranları üzerinden otobus bilgilerini ve sefer detaylarını yönetebilirsiniz.

- **Tab1:**
  İki tablonun key alanları yer alan Selection Screen ekranı içerir. Bu ekrandan girilen değerlere göre tabloda kayıtlı olan verilerin filtrelenip ALV raporuna basılması sağlanır.
  
- **Tab2:** 
  Kullanıcıdan Excel dosyası seçilmesi sağlayacak ekrandır. Kullanıcının Excel dosyasını seçmesini sağlar. Seçilen Excel dosyasındaki verileri okuyarak ekranda ALV raporuna basılmasını sağlayan ekrandır.

**ALV Rapor :**
ALV raporu Gui status'ünde 5 adet buton yer almaktadır. Bunlar sırası ile &BACK, &SAVE, &BUSINFO, &TRIP, &EXCEL butonlarıdır.

- İrem Saral

