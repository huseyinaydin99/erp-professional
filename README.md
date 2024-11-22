### Java ve Angular ile Geliştirdiğim ERP Projesi
Bu proje, modern iş süreçlerini dijitalleştiren, kullanıcı dostu bir deneyim sunan ve güçlü bir altyapıya sahip bir ERP çözümü olarak tarafımdan tasarlanmış ve geliştirilmiştir. Backend tarafında Java kullanılırken, frontend kısmı Angular ile modern web standartlarına uygun bir şekilde oluşturulmuştur. Projenin tüm modülleri, ihtiyaçlara göre özelleştirilmiş ve genişletilebilir bir yapıya sahiptir.
![Ekran görüntüsü 2024-11-22 172312](https://github.com/user-attachments/assets/faa705d7-72b0-409e-97f4-62e1e88c3291)
![Ekran görüntüsü 2024-11-22 171826](https://github.com/user-attachments/assets/3943c87b-7bfc-4494-b55d-cdaf61a2b2fa)

#### Kullandığım Teknolojiler
Backend ve proje altyapısında kullandığım başlıca teknolojiler ve kütüphaneler şunlardır:

- Java (Benim sevgilim. Java, ERP projemde güçlü, taşınabilir ve ölçeklenebilir bir altyapı sunarak, sistemin verimli çalışmasını sağlıyor. Ayrıca, geniş kütüphane desteği ve sağlam framework'leri ile projemde hızlı geliştirme ve sürdürülebilir kod yapısı oluşturuyorum).
- Spring Security (ERP projemde Crypto modülünü, kullanıcı şifrelerini güvenli bir şekilde şifrelemek için kullanıyorum. Bu modül, veri güvenliğini artırarak kullanıcı bilgilerini korumama yardımcı oluyor. SQL Injection gibi saldıralar olurda veritabanı okunursa okunan şifrelerin hash'li ve salt'lı olmasını sağlıyor böylelikle ele geçen şifreler işe yaramaz)
- Jersey (ERP projemde Jersey, RESTful web servisleri oluşturmak ve dış sistemlerle veri alışverişi sağlamak için kullanıyorum. Jersey, hızlı ve ölçeklenebilir bir servis yapısı sunarak API geliştirme sürecini kolaylaştırıyor).
- Gson (JSON işlemleri için Entity'den JSON'a JSON'dan Entity'e dönüşüm için).
- Maven bağımlılık yönetimi, proje standartizasyonu ve paketleme için.
- JavaMail (ERP projemde JavaMail'i, kullanıcı kayıt onayı ve şifre sıfırlama gibi e-posta bildirimlerini göndermek için kullanıyorum. Ayrıca, sistemdeki önemli işlemlerle ilgili yöneticilere otomatik bildirimler göndermek amacıyla da entegre ettim. JavaMail, e-posta iletişimini güvenli ve verimli bir şekilde yönetmeme yardımcı oluyor).
- CORS Filter (Cross-Origin kaynak paylaşımı yönetimi istemci sunucu arası istek iletimi).
- JAXB (XML işlemleri için, Java POJO'ları ile XML'leri birbirine bağlayabilmek adına).
- HttpClient ve HttpMime (ERP projemde HttpClient'i, dış servislerle API iletişimini sağlamak için kullanıyorum. HttpMime ise dosya yükleme ve indirme işlemlerini yönetmek için projemde yer alıyor).
- MySQL (Projemde MySQL'i kullanma amacım, veritabanı yönetimi için güçlü, güvenilir ve açık kaynaklı bir çözüm sunmaktı. MySQL'in verimli sorgulama yapısı, büyük veri setlerini hızla işleme ve analiz etme imkanı sundu, bu da ERP sistemimin performansını artırdı. Ayrıca, SQL dilinin yaygın kullanımı sayesinde veritabanı sorguları yazmak ve yönetmek oldukça kolay hale geldi. MySQL'in ölçeklenebilir yapısı, işletmemin büyümesiyle birlikte veritabanımın da sorunsuz bir şekilde büyümesine olanak tanıdı).

#### 1. Kullanıcı Kaydı ve Giriş İşlemleri
Kullanıcı yönetimi sistemin temel taşıdır. Kullanıcıların sisteme kayıt olabilmeleri, güvenli bir şekilde giriş yapabilmeleri için gereken tüm süreçleri baştan sona geliştirdim.

##### Kullanıcı Kaydı:
Kullanıcılar, ad, soyad, e-posta ve şifre gibi bilgilerle sisteme kayıt olurlar. Kayıt işlemi sırasında şifreler Spring Security kullanılarak hash edilir ve güvenli bir şekilde veritabanında saklanır.
![Ekran görüntüsü 2024-11-22 123828](https://github.com/user-attachments/assets/97348f59-be35-44a8-9978-4c4fbed9785a)

##### E-Posta Onayı:
Kullanıcı kaydının tamamlanabilmesi için e-posta adresine onay bağlantısı gönderilir. Bu işlemde JavaMail API'sini kullandım.

##### Login ve Şifremi Unuttum:
Kullanıcılar e-posta ve şifreleriyle giriş yapabilir, şifrelerini unuttuklarında şifre sıfırlama bağlantısı alabilirler.
![Ekran görüntüsü 2024-11-22 125036](https://github.com/user-attachments/assets/6e01139e-d6a1-4e1d-99e0-a2b40ab678ee)

#### 2. Ana Sayfa İstatistikleri
Sistemin kullanımıyla ilgili özet bilgilerin görselleştirildiği bir modül geliştirdim.

##### İstatistik Gösterimi:
Ana sayfa, toplam kullanıcı, aktif işlemler, aylık satış miktarı gibi bilgileri bar grafikler ve tablolarla görselleştirir.
![Ekran görüntüsü 2024-11-22 171826](https://github.com/user-attachments/assets/8e6fd3fc-5f25-4fc3-b0a1-8e75771dc71b)

##### RESTful API Entegrasyonu:
Backend’den Angular’a veri aktarmak için REST API kullandım.
![Ekran görüntüsü 2024-11-22 174833](https://github.com/user-attachments/assets/2cff65c6-53f9-434e-86ef-1ef323dff091)

#### 3. Cari İşlemleri
Müşteri ve tedarikçi ilişkilerini yönetmek için kapsamlı bir modül geliştirdim.

##### Cari Hesap Ekleme:
Yeni müşteri ve tedarikçiler eklenebilir.
![Ekran görüntüsü 2024-11-22 164830](https://github.com/user-attachments/assets/d9934e7c-5c3b-44fd-8e1b-3d6c799481a7)

##### Hesap Hareketleri:
Alacak ve borç bakiyeleri detaylı olarak takip edilebilir.
![Ekran görüntüsü 2024-11-22 164917](https://github.com/user-attachments/assets/23d8573d-3ebc-4c21-8c89-fff4e058a210)
![Ekran görüntüsü 2024-11-22 165305](https://github.com/user-attachments/assets/23daab81-49ae-4188-951e-fa5b0a7a0c7d)

##### Filtreleme ve Raporlama:
Veriler, tarihe ve işlem türüne göre filtrelenebilir.
![Ekran görüntüsü 2024-11-22 164840](https://github.com/user-attachments/assets/fbd1a6e9-5945-450e-a31b-3cc9db0ee628)

#### 4. Kasa İşlemleri
Finansal hareketlerin merkezi olan kasa yönetimi modülünü geliştirdim.

##### Hesaplar ve Masraf Kalemleri:
Kasa hesapları ayrı ayrı takip edilebilir. Ayrıca masraf kalemleri oluşturularak detaylı raporlar hazırlanabilir.
![Ekran görüntüsü 2024-11-22 165530](https://github.com/user-attachments/assets/ada4a3bb-746f-4a22-bd43-ec4ff5891600)
![Ekran görüntüsü 2024-11-22 165701](https://github.com/user-attachments/assets/c0fcd6d8-3ca2-41c0-b980-d1e45737cbec)

##### Hareket Yönetimi:
Gelir-gider işlemleri eklenebilir, düzenlenebilir ve silinebilir.
![Ekran görüntüsü 2024-11-22 165556](https://github.com/user-attachments/assets/2340829d-26fe-4d57-a8c9-98d912ba0252)
![Ekran görüntüsü 2024-11-22 165611](https://github.com/user-attachments/assets/93077ba5-4507-4cb2-851d-294950fa424f)

#### 5. Stok İşlemleri
Stok yönetimi, ürün ve depo düzenlemelerini içeren kapsamlı bir modül geliştirdim.

##### Depo Yönetimi:
Birden fazla depo oluşturulabilir ve ürünler bu depolar arasında aktarılabilir.
![Ekran görüntüsü 2024-11-22 165733](https://github.com/user-attachments/assets/07937bcf-2a27-441d-a171-a54118d3ae2c)

##### Kategori ve Ürün Yönetimi:
Ürünler kategorilere göre sınıflandırılabilir ve stok seviyeleri güncellenebilir.
![Ekran görüntüsü 2024-11-22 170150](https://github.com/user-attachments/assets/2a6dfcf6-b311-4dc3-8542-d10c5e1a16c7)

#### 6. Fatura İşlemleri
Satış ve alış süreçlerini kolaylaştırmak için bir fatura yönetimi modülü geliştirdim.
![Ekran görüntüsü 2024-11-22 170427](https://github.com/user-attachments/assets/b92e5d7a-2e01-4402-a941-60e4f94a9b76)

##### Alış ve Satış Faturaları:
Faturalar, detaylı ürün bilgileri ve toplam tutar hesaplamalarıyla oluşturulur.
![Ekran görüntüsü 2024-11-22 170413](https://github.com/user-attachments/assets/f6a079bb-2d18-4934-acf8-7d4374a3be8c)
![Ekran görüntüsü 2024-11-22 171123](https://github.com/user-attachments/assets/c43a1c6e-acd5-4a84-93b0-90db4a847c9e)

##### PDF Raporlama:
Faturalar, müşteri veya tedarikçilere gönderilmek üzere PDF formatında indirilebilir.
![Ekran görüntüsü 2024-11-22 170449](https://github.com/user-attachments/assets/883704fd-b786-4f3d-99c3-f2cae2bb92c5)

#### 7. Kullanıcı Profil Ayarları
Kullanıcılar, profillerini özelleştirebilir ve kişisel bilgilerini güncelleyebilir.

##### Profil Güncelleme:
Kullanıcı adı, e-posta gibi bilgileri düzenleme imkanı sundum ve kritik işlemler için kullanıcı seviyesinde yetkilendirme geliştirdim.
![Ekran görüntüsü 2024-11-22 172419](https://github.com/user-attachments/assets/5ae25ce1-f93e-4af6-8006-cbcc169ac60b)

##### Şifre Değiştirme:
Kullanıcılar, mevcut şifrelerini doğruladıktan sonra yeni bir şifre belirleyebilir.

##### Rol Yönetimi:
Yönetici, kullanıcı gibi roller atanabilir ve yetkiler dinamik olarak belirlenebilir.

#### 8. E-Posta Bildirim Ayarları
Sistem içi bildirimlerin e-posta ile kullanıcıya iletildiği bir modül oluşturdum.

##### Bildirim Türleri:
Belirli işlemler tamamlandığında bildirimler otomatik olarak e-posta ile gönderilir.

##### SMTP Konfigürasyonu:
JavaMail ile SMTP ayarlarını özelleştirilebilir bir şekilde yapılandırdım.
![Ekran görüntüsü 2024-11-22 170648](https://github.com/user-attachments/assets/df5ad426-b5b6-47ac-9d5d-45f74ac54af8)

#### 9. MySQL Database ve Diagramı:
MySQL, ERP projemde veritabanı yönetimini sağlamak için güvenilir, ölçeklenebilir ve hızlı sorgulama özellikleri sunarak verilerin düzenli bir şekilde depolanmasına olanak tanıyor.
![Ekran görüntüsü 2024-11-22 174905](https://github.com/user-attachments/assets/bbcf0eb2-15ad-4ae6-9db2-c73d9a04b80c)
![Ekran görüntüsü 2024-11-22 181132](https://github.com/user-attachments/assets/a2a3bdb8-2f0a-41e1-be5f-cd49a09f5d08)


#### Sonuç
ERP projem modern iş süreçlerini dijitalleştiren ve kolaylaştıran güçlü bir ERP çözümüdür. 

<hr />

#### ERP Nedir?

ERP, yani Kurumsal Kaynak Planlama, bir işletmenin tüm süreçlerini tek bir sistem altında toplayarak daha düzenli, kontrollü ve verimli bir şekilde yönetmesini sağlayan bir yazılım çözümüdür. Örneğin, bir şirketi düşünelim; satış, stok yönetimi, muhasebe, insan kaynakları gibi farklı departmanlar var ve bu departmanların hepsi birbirine bağlı çalışmak zorunda. Eğer bu süreçler ayrı sistemlerle yönetilirse bilgi kaybı, iletişim kopukluğu ya da verimsizlik yaşanabilir. İşte ERP, tüm bu sorunları ortadan kaldırıyor. Şirketin satış yaptığı bir ürünün stok bilgisi, faturası ve ödemesi anlık olarak herkesin erişebileceği şekilde güncelleniyor. Böylece işler hem daha hızlı hem de daha doğru bir şekilde ilerliyor. ERP, adeta bir şirketin sinir sistemi gibi çalışıyor ve tüm departmanların aynı platformda birbirine bağlı olmasını sağlıyor. Özellikle büyümek isteyen ya da karmaşık süreçleri olan firmalar için bu sistem vazgeçilmez bir araç.
![erp](https://github.com/user-attachments/assets/fb939878-8940-46bc-95e3-72439299a049)
