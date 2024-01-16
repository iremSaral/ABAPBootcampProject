# Otobus Bilgileri ve Seferleri Projesi

## Proje Tanımı
Bu proje, otobus bilgilerini ve sefer detaylarını yönetmek için geliştirilmiştir. İki adet Z'li Tablo kullanılarak otobus bilgileri ve sefer detayları tutulmaktadır. Bu tablolar `ZIS_BUSINFO` ve `ZIS_TRIPDETAIL` olarak adlandırılmıştır.

## Proje Dosya Yapısı

Proje, karmaşıklığı azaltmak ve düzeni sağlamak için üç ana dosyaya ayrılmıştır. Bunlar `Main Code`, `Include Function`, ve `Include Data` dosyalarıdır.

### 1. MainProject
Ana projenin bulunduğu dosyadır. TabStrip ekranlarının oluşturulması ve gerekli fonksiyonların çağrılması burada yer almaktadır.

### 2. FunctionInclude
Proje içinde kullanılan fonksiyonların bulunduğu dosyadır. Ana projeden çağrılarak kullanılmaktadır.

### 3. DataInclude
Veri tanımlamalarının yapıldığı dosyadır. Fonksiyonlarda kullanılan tablo, structure yapılarının tanımlandığı dosyadır.

## Proje Kullanımı

**Tab Ekranları :** 
Ana projede bulunan tab ekranları üzerinden otobus bilgilerini ve sefer detaylarını yönetebilirsiniz.

- **Tab1:**
  İki tablonun key alanları yer alan Selection Screen ekranı içerir. Bu ekrandan girilen değerlere göre tabloda kayıtlı olan verilerin filtrelenip ALV raporuna basılması sağlanır. Ekranda herhangi bir filtreleme yapılmamış değer girilmemiş ise uygulama çalıştığında ekranda veri girilmesi için uyarı mesajı verir. 

  Tab1 ekranı selection screen görüntüsü

  ![Tab1 ekranı selection screen görüntüsü](https://github.com/iremSaral/ABAPBootcampProject/assets/92708146/947fe3ba-cb5e-4e16-8019-6fec0db76fe0)

  Selection Screen sonucu ALV Rapor Örneği

  ![tab1alv](https://github.com/iremSaral/ABAPBootcampProject/assets/92708146/5c892b4d-c7dc-45e2-8139-2434aeb72293)
  

- **Tab2:** 
  Kullanıcıdan Excel dosyası seçilmesini sağlayacak ekrandır. Kullanıcının Excel dosyasını seçmesini sağlar. Seçilen Excel dosyasındaki verileri okuyarak ekranda ALV raporuna basılmasını sağlayan ekrandır. Eğer ki excel dosyası seçilmemiş ise uygulama ALV çıktısı üretmez, ekranda dosya yüklenmesi için uyarı mesajı gösterir.

Tab2 ekranı file upload görüntüsü

![Tab2](https://github.com/iremSaral/ABAPBootcampProject/assets/92708146/bfced3cf-e586-48fc-8bf4-0ccbe61a99a9)

File Upload ALV Rapor Örneği

![tab2alv](https://github.com/iremSaral/ABAPBootcampProject/assets/92708146/475c8ad0-3cdf-4b12-9d73-7e6c5f355bb0)


**ALV Rapor :**
ALV raporu Gui status'ünde 5 adet buton yer almaktadır. Bunlar sırası ile &BACK, &SAVE, &BUSINFO, &TRIP, &EXCEL butonlarıdır.

![Picture1](https://github.com/iremSaral/ABAPBootcampProject/assets/92708146/09653ccd-49ee-43d2-a2d6-467d0b905014)


- **&BACK :**
ALV Raporundan tab ekranına geri dönmek için koyulmuştur. F2 kısa yolu ile kullanılır.

- **&SAVE :** 
Excel’den veri okunduğu zaman aktif olarak çalışır. Excel verilerinin Z’li tablolara kaydedilmesini sağlayan fonksiyonu çağırmaktadır. Shift+F1 kısa yolu ile erişilebilir.

- **&BUSINFO :**
Header Tablomun SM30 bakım ekranının çağırılması için koyulmuştur. ‘ZIS_HEADER’ TCode’ una tanımlı bakım ekranını çağırır. F5 kısa yolu ile erişim sağlanabilir. Bakım ekranı Şekil 9.’daki gibidir.

- **&TRIP :**
İtem Tablomun SM30 bakım ekranının çağırılması için koyulmuştur. ‘ZIS_ITEM’ TCode’ una tanımlı bakım ekranını çağırır. Shift+F5 kısa yolu ile erişim sağlanabilir. Bakım ekranı Şekil 10.’da verilmiştir. 

- **&EXCEL :** 
Excel dosyasından veri yüklenirken seçilen excel dosyası ile tablolarımın arasındaki oluşabilecek uyumsuzluğu engellemek için konulmuştur. Olması gereken Excel formatının bilgisayara kaydedilmesi sağlanır. Uygulama Excel formatı Şekil 11.’de verilmiştir. 
