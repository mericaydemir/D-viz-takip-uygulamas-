Döviz Kuru Takip Konsol Programı

Bu çalışma, Görsel Programlama dersi kapsamında hazırlanmış; gerçek zamanlı döviz verilerini internet üzerinden alabilen ve bu veriler üzerinde listeleme, filtreleme, sıralama ve istatistiksel analizler yapabilen bir C# Konsol uygulamasıdır.

Proje Detayları

Geliştirici: Meriç Aydemir

Dersin Öğretim Elemanı: Emrah SARIÇİÇEK

Kullanılan Dil: C#

Uygulama Türü: Console Application

Projenin Amacı ve Kapsamı

Bu uygulamanın temel hedefi, Frankfurter FREE API üzerinden güncel döviz kurlarını anlık olarak çekmek ve elde edilen veriler üzerinde kullanıcıya LINQ tabanlı sorgular ile işlem yapma olanağı sunmaktır. Proje, Nesne Yönelimli Programlama (OOP) ilkelerine uygun olarak geliştirilmiş ve katmanlı mimari yaklaşımı dikkate alınarak tasarlanmıştır.

Kullanılan Teknolojiler ve Teknik Altyapı

Proje geliştirme sürecinde aşağıdaki yapı ve teknolojilerden yararlanılmıştır:

HttpClient: API ile iletişim kurmak ve döviz verilerini almak amacıyla kullanılmıştır.

Async / Await: API isteklerinin asenkron çalışmasını sağlayarak uygulamanın akışının kesintiye uğramaması hedeflenmiştir.

LINQ: Döviz verileri üzerinde filtreleme, sıralama ve istatistiksel hesaplamalar (Where, Select, OrderBy, Average, Max, Min) yapmak için tercih edilmiştir.

Newtonsoft.Json: API’den dönen JSON verilerinin C# nesnelerine dönüştürülmesi (Deserialize) için kullanılmıştır.

Try-Catch Yapıları: İnternet bağlantı problemleri ve kullanıcıdan alınan hatalı girişler gibi olası hataların kontrol altına alınması amacıyla eklenmiştir.

Uygulama Fonksiyonları (Menü Seçenekleri)

Uygulama içerisinde kullanıcıya sunulan temel işlemler şunlardır:

Tüm Dövizleri Görüntüleme: API’den alınan güncel döviz kurlarını tablo şeklinde ekrana yazdırır.

Döviz Kodu ile Arama: Girilen döviz koduna (USD, EUR vb.) göre arama yapar; harf duyarlılığı bulunmaz.

Kur Değerine Göre Filtreleme: Kullanıcının belirlediği değerin üzerinde olan dövizleri listeler.

Sıralama İşlemleri: Döviz kurlarını artan veya azalan sıraya göre sıralama imkanı sunar.

İstatistiksel Bilgiler: Toplam döviz adedi, en yüksek ve en düşük kur ile ortalama kur değerlerini hesaplayarak gösterir.

Proje Dosya Yapısı

Proje, Sorumlulukların Ayrılması (Separation of Concerns) prensibine uygun biçimde yapılandırılmıştır:

Program.cs: Uygulamanın başlangıç noktasıdır. Menü sistemi, kullanıcıdan alınan girdiler ve konsol çıktıları burada yönetilir.

DovizService.cs: İş kurallarının yer aldığı katmandır. API bağlantıları ve LINQ işlemleri bu dosyada gerçekleştirilir.

Currency.cs: Uygulamada kullanılan döviz modelini temsil eder.

CurrencyResponse.cs: API’den dönen JSON verisini karşılayan veri transfer sınıfıdır.

Kurulum ve Çalıştırma Adımları

1.Uygulamayı yerel bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

2.Proje dosyalarını bilgisayarınıza indirin veya kopyalayın.

3.Proje dizininde bir terminal penceresi açın.

4.Gerekli JSON kütüphanesini yüklemek için aşağıdaki komutu çalıştırın:
dotnet add package Newtonsoft.Json

5.Uygulamayı derlemek ve çalıştırmak için şu komutu kullanın:
dotnet run

Bu Projede Neler Öğrenildi

Bu proje sayesinde, C# dili kullanılarak gerçek zamanlı veri çeken bir konsol uygulamasının nasıl geliştirileceği öğrenilmiştir. Özellikle harici bir REST API ile bağlantı kurulması, bu API’den gelen verilerin işlenmesi ve kullanıcıya anlamlı şekilde sunulması konusunda pratik kazanılmıştır.

Uygulama geliştirme sürecinde HttpClient kullanılarak API üzerinden veri çekme, Async / Await yapısı ile asenkron programlama mantığını kavrama ve uygulamanın akışını bloklamadan çalıştırma becerisi elde edilmiştir. API’den dönen JSON formatındaki verilerin Newtonsoft.Json kütüphanesi yardımıyla C# nesnelerine dönüştürülmesi konusunda deneyim kazanılmıştır.

Ayrıca LINQ kullanılarak veri listeleme, filtreleme, sıralama ve istatistiksel hesaplamalar yapılmış; bu sayede koleksiyonlar üzerinde etkili ve okunabilir sorgular yazma yetkinliği geliştirilmiştir. Try-Catch blokları ile hata yönetimi sağlanarak kullanıcıdan veya bağlantıdan kaynaklanan hataların nasıl kontrol altına alınacağı öğrenilmiştir.

Proje, Nesne Yönelimli Programlama (OOP) ilkelerine ve katmanlı mimari yaklaşımına uygun şekilde tasarlandığı için, sınıflar arası sorumluluk dağılımı, kodun okunabilirliği ve sürdürülebilirliği konularında önemli kazanımlar sağlamıştır. Genel olarak bu çalışma, gerçek hayatta kullanılan veri servisleri ile çalışan konsol uygulamalarının geliştirilmesi konusunda kapsamlı bir deneyim sunmuştur.
