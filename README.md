### Java ve Angular ile Geliştirdiğim ERP Projesi
Bu proje, modern iş süreçlerini dijitalleştiren, kullanıcı dostu bir deneyim sunan ve güçlü bir altyapıya sahip bir ERP çözümü olarak tarafımdan tasarlanmış ve geliştirilmiştir. Backend tarafında Java kullanılırken, frontend kısmı Angular ile modern web standartlarına uygun bir şekilde oluşturulmuştur. Projenin tüm modülleri, ihtiyaçlara göre özelleştirilmiş ve genişletilebilir bir yapıya sahiptir.

#### Kullandığım Teknolojiler
Backend ve proje altyapısında kullandığım başlıca teknolojiler ve kütüphaneler şunlardır:

Java
Spring Security (Crypto modülü ile şifreleme)
Jersey (RESTful web hizmetleri için)
Gson (JSON işlemleri için)
MySQL (veri tabanı)
Maven bağımlılık yönetimi
JavaMail (e-posta işlemleri için)
CORS Filter (Cross-Origin kaynak paylaşımı yönetimi)
JAXB (XML işlemleri için)
HttpClient ve HttpMime (HTTP istekleri için)

#### 1. Kullanıcı Kaydı ve Giriş İşlemleri
Kullanıcı yönetimi sistemin temel taşıdır. Kullanıcıların sisteme kayıt olabilmeleri, güvenli bir şekilde giriş yapabilmeleri için gereken tüm süreçleri baştan sona geliştirdim.

##### Kullanıcı Kaydı:
Kullanıcılar, ad, soyad, e-posta ve şifre gibi bilgilerle sisteme kayıt olurlar. Kayıt işlemi sırasında şifreler Spring Security kullanılarak hash edilir ve güvenli bir şekilde veritabanında saklanır.

##### E-Posta Onayı:
Kullanıcı kaydının tamamlanabilmesi için e-posta adresine onay bağlantısı gönderilir. Bu işlemde JavaMail API'sini kullandım.

##### Login ve Şifremi Unuttum:
Kullanıcılar e-posta ve şifreleriyle giriş yapabilir, şifrelerini unuttuklarında şifre sıfırlama bağlantısı alabilirler.

#### 2. Ana Sayfa İstatistikleri
Sistemin kullanımıyla ilgili özet bilgilerin görselleştirildiği bir modül geliştirdim.

##### İstatistik Gösterimi:
Ana sayfa, toplam kullanıcı, aktif işlemler, aylık satış miktarı gibi bilgileri bar grafikler ve tablolarla görselleştirir.

##### RESTful API Entegrasyonu:
Backend’den Angular’a veri aktarmak için REST API kullandım.

#### 3. Cari İşlemleri
Müşteri ve tedarikçi ilişkilerini yönetmek için kapsamlı bir modül geliştirdim.

##### Cari Hesap Ekleme:
Yeni müşteri ve tedarikçiler eklenebilir.

##### Hesap Hareketleri:
Alacak ve borç bakiyeleri detaylı olarak takip edilebilir.

##### Filtreleme ve Raporlama:
Veriler, tarihe ve işlem türüne göre filtrelenebilir.

#### 4. Kasa İşlemleri
Finansal hareketlerin merkezi olan kasa yönetimi modülünü geliştirdim.

##### Hesaplar ve Masraf Kalemleri:
Kasa hesapları ayrı ayrı takip edilebilir. Ayrıca masraf kalemleri oluşturularak detaylı raporlar hazırlanabilir.

##### Hareket Yönetimi:
Gelir-gider işlemleri eklenebilir, düzenlenebilir ve silinebilir.

#### 5. Stok İşlemleri
Stok yönetimi, ürün ve depo düzenlemelerini içeren kapsamlı bir modül geliştirdim.

##### Depo Yönetimi:
Birden fazla depo oluşturulabilir ve ürünler bu depolar arasında aktarılabilir.

##### Kategori ve Ürün Yönetimi:
Ürünler kategorilere göre sınıflandırılabilir ve stok seviyeleri güncellenebilir.

#### 6. Fatura İşlemleri
Satış ve alış süreçlerini kolaylaştırmak için bir fatura yönetimi modülü geliştirdim.

##### Alış ve Satış Faturaları:
Faturalar, detaylı ürün bilgileri ve toplam tutar hesaplamalarıyla oluşturulur.

##### PDF Raporlama:
Faturalar, müşteri veya tedarikçilere gönderilmek üzere PDF formatında indirilebilir.

#### 7. Kullanıcı Profil Ayarları
Kullanıcılar, profillerini özelleştirebilir ve kişisel bilgilerini güncelleyebilir.

##### Profil Güncelleme:
Kullanıcı adı, e-posta gibi bilgileri düzenleme imkanı sundum.

##### Şifre Değiştirme:
Kullanıcılar, mevcut şifrelerini doğruladıktan sonra yeni bir şifre belirleyebilir.

#### 8. Yetkilendirme İşlemleri
Kritik işlemler için kullanıcı seviyesinde yetkilendirme geliştirdim.

##### Kasa ve Depo Yetkileri:
Belirli kullanıcılara sadece belirli kasalara ve depolara erişim yetkisi tanımlanabilir.

##### Rol Yönetimi:
Yönetici, kullanıcı gibi roller atanabilir ve yetkiler dinamik olarak belirlenebilir.

#### 9. E-Posta Bildirim Ayarları
Sistem içi bildirimlerin e-posta ile kullanıcıya iletildiği bir modül oluşturdum.

##### Bildirim Türleri:
Yeni bir kullanıcı eklendiğinde veya belirli işlemler tamamlandığında bildirimler otomatik olarak gönderilir.
##### SMTP Konfigürasyonu:
JavaMail ile SMTP ayarlarını özelleştirilebilir bir şekilde yapılandırdım.

#### Sonuç
Bu proje, modern iş süreçlerini dijitalleştiren ve kolaylaştıran güçlü bir ERP çözümüdür. 

#### ERP Nedir?

ERP, yani Kurumsal Kaynak Planlama, bir işletmenin tüm süreçlerini tek bir sistem altında toplayarak daha düzenli, kontrollü ve verimli bir şekilde yönetmesini sağlayan bir yazılım çözümüdür. Örneğin, bir şirketi düşünelim; satış, stok yönetimi, muhasebe, insan kaynakları gibi farklı departmanlar var ve bu departmanların hepsi birbirine bağlı çalışmak zorunda. Eğer bu süreçler ayrı sistemlerle yönetilirse bilgi kaybı, iletişim kopukluğu ya da verimsizlik yaşanabilir. İşte ERP, tüm bu sorunları ortadan kaldırıyor. Şirketin satış yaptığı bir ürünün stok bilgisi, faturası ve ödemesi anlık olarak herkesin erişebileceği şekilde güncelleniyor. Böylece işler hem daha hızlı hem de daha doğru bir şekilde ilerliyor. ERP, adeta bir şirketin sinir sistemi gibi çalışıyor ve tüm departmanların aynı platformda birbirine bağlı olmasını sağlıyor. Özellikle büyümek isteyen ya da karmaşık süreçleri olan firmalar için bu sistem vazgeçilmez bir araç.