


# v. Hafta Ödevleri
### 1. DEVELOPER SUMMIT 2020'deki yazılım konferanslarından ilginizi çekenlerin özetlerini çıkarmaya çalışınız.
#### Türkay Ürkmez
- Yazılım araçları nelerdir ? Nasıl daha temiz kod yazarız ?  
> Yazılımda varlıkların iletişimi temiz mimariyi oluşturur. Temiz kod yazarken belirli bir mimariyle yürütmek, Solid prensiblerini takip etmek, yazılıma ait bağımlılıkları azaltmak ve test edilebilirliği sağlamak önemli noktalardır. 

>Solid Prensipleri ile yazılan kodların en temel özelliği sürdürülebilir olmalarıdır.
> - Single Responsibility Principle : Bir sınıfın, nesnenin yapması gereken tek bir iş olmalıdır.
> - Open/Closed Principle : Bir sınıf ya da fonksiyon davranışını değiştirmemeli fakat yeni özellikler kazanıp gelişebilmelidir. 
> -  Liskov Substitution Principle : Bir nesneyi değiştirsem de sistem çalışmaya devam eder. Bir nesneye göre kod yazılmaz. Veri okunacak XMML- Database den okuyacak. Metoda ne verirsem çalışmalı bu prensip için.
> - Interface Segregation Principle : Arayüzlerin birbirinden ayrı olmasıdır.
> - Dependency Inversion Principle : Dependency inversion prensipin ne olduğudur, dependency injection ise kodun nasıl yazılacağını anlatır. Uygulama yazarken bağımlılıkları tespit edilmelidir. Örneğin uygulama sadece SQL ile çalışır ise "Dependency Inversion" a uygun değildir. Uygulama herhangi bir databasede çalışır ise bağımsızlığa uymaya başlamıştır.

> Bağımsızlık konusunda  "Loosely Coupled"  kavramı daha düşük bağımlılıklar ile daha esnek kod yazmamızı sağlar. 

> Test edilebilir olması önemli noktalardandır. Farklı kullanıcılarda farklı değişkenlerden etkilenerek nelerle karşılaşılacağı öğrenilmelidir. Test edilme örnekleri,
> - Veri kaynağı değişirse,
> - Arayüz değişirse,
> - Performans ihtiyaçları değişirse,
> - Alternetif araçlar ortaya çıkarsa,
> - POC (proof of concept) şeklinde karşımıza çıkabilir.

> Domain Driven Design, kompleks gereksinimlerin var olduğu bir dünyada, sürekli değişen temel business kurallarını birbirine derinlemesine bağlayan bir yazılım geliştirme yaklaşımıdır.
> - Yaygın kullanılan dil ve jargon ortaya koymak ve developerlar ile domain arasında herkesin anlayabileceği bir dil bütünü oluşturmak amacındadır. Ortak bir dil belirlemek test süreçlerini kolaylaştıracağı gibi gereksinimlerin değişmesi durumunda yazılım takımının bu değişiklikleri kolay anlayabilmesini sağlayacaktır.





### 2. SQLite ve LocalDB nedir?

> **SQLite** (Self Contained DB) RDBMS yani ilişkisel veritabanı sağlayan bir yazılım kütüphanesidir. İlişkisel veritabanı, organize edilmiş verilerin tablolarda saklanması ve bu tablolar arasında kurulan bağ ile oluşan veritabanı çeşitidir. 
> Açık kaynak kodlu bir SQLite serverless'tır.
> SQLite’ın çalışması için herhangi bir sunucuya ihtiyacı olmadığı için, kurulum ve ya konfigürasyon adımları yoktur. Platformdan bağımsız şekilde her veritabanı için sadece bir dosya vardır. Bu da veritabanının yedeklenmesini ve kopyalanmasını kolaylaştırır. 
> Geniş yelpazeye yayılmış cihazlarda kullanılabilir. 
> - Gömülü sistemler/IoT cihazlar.
> - Akıllı Ev/Otomobil, G Teknolojileri (Saat,Elbise vb.), Uçaklar, Dronelar, Robotlar, Endüstri
> - Web siteleri, Cache bellek, Veri aktarım dosyası 

>SQLite karşılığı SQL Server, Oracle ya da MySQL olarak düşünülmemelidir. Çünkü bunlar RDBMS değildirler.
>Full featured SQL özelliğini barındırır. SQL standartlarını tam olarak desteklemektedir.
> Transactional  bir yapıdadır. Transaction veri tabanında gerçekleştiren bir grup işlem bütününe verilen addır. ACID prensiplerini uygular. 
 -**A**tomicity (Bütünlük): Atomicity ilkesine göre transactional işlemlerden herhangi biri başarısız olursa tüm işlemler başarısız olarak sayılacaktır.
-**C**onsistency (Tutarlılık): Transaction tam anlamı ile gerçekleşinceye kadar  işlemden etkilenen verilerin değerlerinin bir önceki geçerli değeri vermesidir.
-**I**solation (İzolasyon): Transaction veriler üzerinde çalışırken, işlemlerin dışarıdan ne kadar görünür olabileceği ile ilgili bilgiler içerir. Transaction dışarıdan müdahaleye izin vermemelidir. Yapılan işlemler izole olmalı ve bir transaction bir diğerinden bağımsız olmalıdır.
-**D**urability (Dayanıklılık): Transaction sırasında fiziksel veya işlemsel bir hata olması durumunda sistemin kendisini bir önceki geçerli veri durumuna döndürebilme kabiliyetidir.

> **LocalDB** Microsoft'un SQL Express'in yeni versiyonu olarak piyasaya sunulmuştur. SQL Server™, verilerin güvenle ve bütünlük içerisinde depolanmasını ve aynı anda birden fazla kullanıcı tarafından erişilmesini sağlayan kurumsal çaplı bir ilişkisel veri tabanı yönetim sistemidir (RDBMS). SQL Server, işletmeler için kritik önem taşıyan verileri şifreleme, verilere erişim sağlayan kişileri gözlemleme ve erişim kısıtlamaları tanımlama gibi güvenlik özellikleri sayesinde kullanıcılara kapsamlı bir denetim kapasitesi sunar. Yüksek Kullanılabilirlik (High Availability) ve olağanüstü durum kurtarma özelliklerini tek bir çözümde birleştiren SQL Server, hızlı yük devretme ve yük dengeleme desteği ile aksaklık süresini en aza indirir ve güvenli veri akışının optimize edilmesini sağlar.
> LocalDB ile SQL Server arasında farklılıklar şu şekilde sıralanabilir;
> - LocalDB SQL Server Express Edition'a göre hada az ön koşul ve daha hızlı kurulum seçeneği ortaya koyduğu için daha hafif bir dağıtım seçeneği olarak karşımıza çıkar.
> - LocalDB, SQL Express ile aynı programlanabilirlik özelliklerine sahiptir, ancak bir hizmet olarak değil, uygulamalarla "kullanıcı modunda" çalışır.
> - LocalDB çok kullanıcılı senaryolar için bir sunucu olarak tasarlanmamıştır.
> - SS Management Studio Express, Azure gibi Express araçları LocalDB olmadan da kullanılabilir.


### 3. Lazy Loading kavramı hakkında temel bir araştırma yapınız.
> Lazy Loading Entity frameworkün yazılan LINQ sorgularına bağlı olarak veriyi veri tabanından yüklemek için kullandığı loading yöntemleridir. Lazy Loading, sayfada yer alan bir ögenin ihtiyaç duyulmadığı takdirde çağrılmaması prensibi ile çalışır yani bir nesne örneğinin gerçekten ihtiyaç duyulacağı ana kadar alınmaması ve bekletilmesi amacıyla kullanılır. Bu yöntemde veriler sorguya bağlı olarak çekilir ve veri setinin içindeki tüm dataları yüklemek yerine kullanılacağı an tekrar sorgu atar ve veriyi çeker.
> Lazy loading ile birbiriyle ilişkili olan entityler ihtiyaç oldukça çekilir. Bu da bize içinde bulunduğumuz case’e göre performans açısından yarar sağlayabilir.


#### Kaynaklar:
- [Kaynak 1](https://www.youtube.com/watch?v=GgGoG9_JMv8)
- [Kaynak 2](https://www.karamelek.org/sqlite-nedir-ve-nasil-kullanilir/)
- [Kaynak 3](https://alkanity.com/veri-bilimi/veritabani-kavramlari/normalizasyon-kurallari-acid-prensipleri/)
- [Kaynak 4](https://www.tutorialspoint.com/sqlite/sqlite_overview.htm)
- [Kaynak 5](https://stackoverflow.com/questions/10183379/is-there-a-difference-between-sql-server-express-2012-and-localdb)
- [Kaynak 6](https://www.penta.com.tr/markalar/microsoft/urunler/microsoft-sql-server/microsoft-sql-server-nedir/)
- [Kaynak 7](https://medium.com/@e.karabudak7/lazy-loading-vs-eager-loading-67d09c6a251)
- [Kaynak 8](https://medium.com/kariyertech/domain-driven-design-643c02168ecc)
