 # trex_research
***


## 1.Modern Yazılım Geliştirme Pratikleri
 
 <details> 
<summary>Git nedir? GitHub nedir?</summary>
  GİT:
   <ul>
      <li>Bir versiyon kontrol sistemidir.</li>
      <li>Projenin son haline ulaşmamızı ve projeyi güncel tutmayı sağlar.</li>
      <li>Yazılım geliştirme uygulamasıdır. </li>
     <li>Burada geliştiriciler etkileşim kurar,iletişime geçer ve iş birliği yaparlar.</li>
     <li>Geliştiriciler projeler üzerinde yeni kodlar yazarak yeni şeyler geliştirirler ve bu projeler üzeerinde ki değişiklikleri görebilirler.</li>
     <li>Yerel bir depoda çalışabileceği gibi çevrimiçi veya çevrimdışı uzak depolarda da çalışabilir.</li>
    <li>Geliştirme ekipleri beraber bir proje üzerinde mevcut olan sürümleri engellemeden bir yeni sürüm daha geliştirerek sürümleri yükseltmede geliştirmede yardımcı olur.</li>
</ul>
GitHub:
       <ul>
<li>Bulut tabanlı bir sistem.</li>
<li>Projelerin saklandığı yani depo edildiği bir sunucudur.</li>
</ul>

</details>


<details>
<summary>Temel git komutları:init, clone, add, commit, push, pull, branch, merge</summary>
Git komutu nedir?
<ul>
<li>Dosya kümesi içinde gerçekleştirilen değişiklikleri izlemeyi kolaylaştırır.</li>
<li>Sürüm kontrol sistemine ait araçlar çalıştırılabilir.Dosyaları listeleyebilir ve veriler üzerinde değişiklikler yapılabilir.</li>
</ul>

Git komutları nelerdir?
<ul>
<li>git init:Yeni bir depo açmak için ve hazırlanacak projelerde start vermek için kullanılır.Lokal dosyalarını buraya kaydedebilmeye olanak tanır.</li>
-ÖRNEK KULLANIM-> git init[depo adı]
  
<li>git clone:Uzak bir sunucuda ki projeyi bilgisayara indirebilir, bilgisayarda veya lokal server alanında ki güvenli bir konuma taşıyabilirsin.</li>
  -ÖRNEK KULLANIM-> git clone[url]
                    git clone[url]-b[depo adı]
                    
<li>git add:Bir projeyi ya da proje içinde ki bir dosyayı depo alanına eklemeni sağlar.</li>
  -ÖRNEK KULLANIM-> git add [dosya adı] (Belirtilen dosyayı depoya ekler.)
                    git add *  (Birden fazla ekleme yapar.)
                    
<li>git commit:Bir dosyayı sürüm geçmişine kalıcı olarak kaydeder.Git add komutu ile eklendiğinde diğer dosyalarıda kaydeder.Bu komutla yapılan değişiklikler local repository de görülür.</li>
  -ÖRNEK KULLANIM-> git commit -a
                    git commit -m “[kayıt mesajını yazın]”
                    
<li>git push:Bilgisayarda ve local sunucuda bulunan commitleri uzak depo alanlarına aktarmada kullanılır.</li>
  -ÖRNEK KULLANIM-> git push [değişken adı] master (Belli işlem demetlerini uzak sunucuya gönderir.)
                    git push [variable name] [branch] (Bu komut belirtilen değişkeni uzak depoya gönderir.)
                    git push –all [değişken adı] (Bu komut tüm işlem demetlerini uzak depoya gönderir.)
                    git push [değişken adı] :[branch name]  (Bu komut, uzak depoda özel olarak belirtilen işlem demetini siler.)
                    
<li>git pull:Uzak sunucuda ki değişiklik veya herhangi bir projeyi yerelleştirmek için kullanılır.</li>
  -ÖRNEK KULLANIM-> git pull[Depo Bağlantı Linti]
  
<li>git branch:Geçerli depolarda ki yerel dalları,sınıfları ve bölümleri listelemek için kullanılır.</li>
  -ÖRNEK KULLANIM-> git branch (Tüm bölümleri veya sınıfları listeler.)
                    git branch [bölüm adı] (Yeni bir sınıf veya bölüm ekler.)
                    git branch-b[bölüm adı] (Belirtilen bölüm veya sınıfı siler.)
                    
<li>git merge:Belirtilen uzantıyı veya dalı başka bir uzantı ile birleştirir.</li>
  -ÖRNEK KULLANIM-> git merge [branch adı]
</ul>
</details>


<details>
<summary>Merge conflict nedir, nasıl çözülür?</summary>
<dl>
  <dt>Merge confit neden oluşur?</dt>
      <dd>Bir dosyanın belli bir kısmı iki kişi tarafından değiştirilmeye çalışır ise uygulama hangisini uygulayacağını bilemez ve bu sorun ortaya çıkar.</dd>
     <dt>Nasıl çözülür?</dt>
     <dd>Çakışmalı hatalı dosyayı açıp <<<<<<<, =======, >>>>>>> işaretlerinden uygulama için mantıklı olanı seçeriz gerekirse birleştirebilirizde.En son olarak değişikliği git add ile sahneleyip git commit ile birleştirme tamamlanır.</dd>
       </dl>
     </details>

       
<details>
<summary>CI/CD nedir? Azure DevOps, GitHub Actions ile pipeline örnekleri</summary>
<dl>
    <dt>CI(Continuous Integration):Sürekli entegrasyon</dt>
     <dd>Tüm kod değişikliklerinin paylaşıldığı kaynak deposu.Her değişikliliği kaydettiğimizde veya birleştirdiğimizde otomatik olarak test etmek ve bir derleme başlatma uygulamasıdır.CI sayesinde hatalar,güvenlik sorunları daha kolay tespit edilip geliştirme sürecini çok daha erken bir aşamada düzeltilebilir.</dd><br>
     <dt>CD(Continuous Delivery):Sürekli teslimat</dt>
      <dd>Altyapı sağlama uygulama yayınlama sürecini geliştirmek için CI ile birlikte çalışan bir yazılım geliştirme uygulamasıdır.</dd>
      <br>Sürekli entegrasyon ve sürekli teslimatın birleşimidir.Yeni düzenlenmiş bir kodu committen üretime geçirmek için ihtiyaç duyulan manuel insan müdehalesinin çoğunu veya tamamını otomatikleştirir.CI veya CD den yana aynı zamanda altyapıyıda sağlamayı kapsar.Geliştirme ekipleri kodda değişiklik yapabilir ve  bunlar daha sonra otomatik olarak test edilip dağıtım için gönderilirler.<br>
      <dt>GitHub Actions ile Pipeline örnekleri:</dt>
      <dd>GitHub Actions GitHub üzerinden yapılan projeleri barındıran CI/CD iş akışları kurmaya yarayan bir sistem</dd>
      <dt>Azure DevOps ile Piepline örnekleri:</dt>
      <dd>Microsoft bulut tabanlı YMAL veya görsel olarak oluşturulabilen güçlü bir CI/CD aracıdır.</dd>     

</dl>
  </details>

  <details>
<summary>Ek Maddeler</summary>
<ul>
<li>İhtiyaç Analizi ve Planlama:</li>
Bir yazılım projesinin başlangıcında müşterinin ihtiyaçları ve projenin hedefleri detaylı bir şekilde analiz edilir.
<li>Tasarım:</li>
Tasarım aşamasında projenin mimarisi oluşturacak genel yapı tasarlanır.
<li>Geliştirme:</li>
Gerçek kod yazma aşamasıdır.
<li>Test Etme:</li>
Yazılımın istikrarlı ve hatalardan arındırılmış olması gerekmektedir.
<li>Dağıtım ve Yayınlama:</li>
Test aşamasından başarıyla geçtikten sonra, müşteriye sunulmak üzere son kez hazırlanır.
<li>Bakım ve Güncelleme:</li>
Kullanıcıların geri bildirimine göre yazılımın performansı takip edilip tekrar ele alınır.

</ul>
</details>


## 2.  .Net Ekosistemi
  <details>
  <summary>.NET nedir? Tarihçesi, amacı, neden kullanılır?</summary>
  <dl>
<dt>.NET nedir?</dt>
<dd>Herhangi bir işletim sisteminde yerek olarak çalışabilen masaüstü, web ve mobil uygulamalar oluşturmaya yönelik açık kaynaklı bir platformdur. .Net Core Microsoft tarafından sağlanan bir platformdur.90'lar sonlarında büyük bir değişim geçirmiştir.Bu projenin büyük bir değişim geçirmesini sağlayan ve tercih edilebilir kılan; C#, C++ dahil olmak üzere herhangi bir dilde uygulama yazma imknaı vermesidir.</dd>

<dt>.NET tarihçesi</dt>
<ul>
1.Dönem:.NET Framework
<li>2002->Microsoft, sadece Windows  üzerinde çalışan .NET Frameworkü 1.0 ı duyurdu. </li><br>
<li>2003->.NET Framework 1.1 çıktı ve ASP.NET Web performansı geliştirildi.</li><br>
<li>2005->.NET Framework 2.0 yayınlandı ASP.NET 2.0, Generics ve Windows form özellikleri geldi.</li><br>
<li>2006->.NET Framework yayınlandı.WPF(masaüstü için), WPCF(iletişim), WF(iş akışı)CardSpace eklendi. </li><br>
<li>2007-2008->.Net FRamework 3.5 çıktı.LINQ ve Entity Framework hayatımıza girdi.</li><br>
<li>2010->.NET Framework 4.0 yayınlandı. Prarlel Programming(çok çekşrdekli işlem desteği) ve yeni CLR yayınlandı.</li><br>
<li>2012->.NET Framework4.5 çıktı. </li><br>
<li>2013-2014->.NET Framework hala güçlüydü ama linux ve macOS destekleri yoktu ve kapalı kaynak kodu olduğundan çok büyük bir eksiydi ve bu dönemde açık kaynak kodlu program ihtiyacı son derece arttı.</li><br>

2.Dönem:.Net Core
<li>2014->Microsoft .NET Core'u duyurdu.</li>
<li>2016->.NET Core 1.0 yayınlandı ve ilk sürüm Entity Framework Core, ASP.NET de yayınlandı.</li><br>
<li>2017->.NET Core 2.0 çıktı.API sayısı genişledi, NET Framework ile uyumları arttı.</li><br>
<li>2018->.NET Core 2.1(LTS)duyuruldu performans ve stabilitesi ön plana çıktı.</li><br>
<li>2019->.NET Core 3.0 ve hemen ardından 3.1(LTS) yayınlandı.WPF ve Windows performans desteği eklendi,Blazor(C+ WebAssembly)tanıtıldı.</li><br>
<li>2020->Microsoft "Core" adını bıraktı NET 5 adını aldı. NET Framework, NET Core, Xamarin birleşerek tek  bir NERT platformu oldular. </li><br>

3.Dönem:Modern.NET7/8+:
<li>2021->.NET 6(LTS)en çok kullanılan sürümlerden biri oldu.</li><br>
<li>2022->.NET 7 performans ve bulut odaklı.</li><br>
<li>2023->.NET 8(LTS)MAUI ile mobil ve masaüstü birleşti yapay zeka entegrasyonu başladı.</li><br>
<li>2024->.NET 9 en güncel sürüm ve özellikle bulut tabanlı, modern uygulama odaklı.</li><br>

<dt>Amacı</dt>
<dd>NET Framework'ün yalnızca Windowsa bağlı olması ve kapalı kaynak kodlu yapsından dolayı geliştiricileri kısıtlamasından dolayı ortaya çıkan bir platformdur.O dönemlerde linux macOS gibi platformlara olan ihtiyaç artmıştı.Kısacası .NET Core'un amacı geliştiricilere daha özgür, geniş ve kendilerini yenileyebilecekleri bir alan bir platform sunmaktı.Window,Linux,macOS üzerinde çalışılması ile çapraz platform desteği öne çıktı</dd>

<dt>Neden kullanılır</dt>
<dd>Platform bağımsızlığı,açık kaynak ve topluluk desteği,yüksek performs, modüler yapı,modern uygulama geliştirme,uzun dönem destek(LTS)sürümleri
 sağladığından kullanılmasını en çok ön plana çıkaran ögeler de bunlardır.</dd>
</ul>
</details>
  
   <details>
<summary>.NET Framework, .NET Core ve .NET 7/8+ farkları</summary>
    
<table border="1">
    <body>
        <tr>
            <td>Özellik</td>
            <td>.NET Framework</td>
            <td>.NET Core</td>
            <td>.Net 7/8+</td>
    </td>
        </tr>
     
  <tr>
            <td>Çıkış Yılı</td>
            <td>2002</td>
            <td>2016</td>
            <td>2020</td>
        </tr>
         <tr>
            <td>Platform Desteği</td>
            <td>Windows</td>
            <td>Windows Linux macOS </td>
            <td>Windows Linux macOS</td>
        </tr>
         <tr>
            <td>Kaynak Kodu</td>
            <td>Kapalı</td>
            <td>Açık</td>
            <td>Açık</td>
        </tr>
         <tr>
            <td>Geliştirme Durumu</td>
            <td>Sadece bakım</td>
            <td>NET+5 ile birleşti</td>
            <td>Aktif</td>
        </tr>
         <tr>
            <td>Performans</td>
            <td>Düşük</td>
            <td>Orta</td>
            <td>En Yüksek</td>
        </tr>
         <tr>
            <td>Modern Teknoloji</td>
            <td>Yok</td>
            <td>Kısmen</td>
            <td>MAUI Blazor ML.NET Cloud-native</td>
        </tr>
         <tr>
            <td>Güncelleme</td>
            <td>Yok</td>
            <td>Yok</td>
            <td>Var</td>
        </tr>
         <tr>
            <td>Kullanım Alanları</td>
            <td>Eski Windows uygulamaları </td>
            <td>Çoklu platform uygulamaları web,API,Mikroservis</td>
            <td>Modern çoklu platform uygulamaları Bulut,web API ve dahası</td>
        </tr>
         <tr>
            <td>Desteklediği Araçlar</td>
            <td>Visual Studio</td>
            <td>Visual Studio VS Code ClI</td>
            <td>Visual Studio VS Code CLI </td>
        </tr>
        </body>
        </table>
             </details>

<details>
<summary>Platformlar arası çalışabilir mi? (Windows, Linux, macOS)</summary>
 <dl>
<dd>.NET Core ve NET7/8+ sürümleri hepsinin üzerinde sorunsuz çalışabilir.Uygulamalrın farklı iletişim sistemlerinde aynı şekilde derlenip çalışabilmesini sağlar.Tek bir kod tabanı üstünde konsol,web,masaüstü uygulamalrı ve bulut tabanlı mikroservisleri farklı platformlarda kullanabilirler.</dd>
</dl>
 </details>

<details>
<summary>Async, Await, Task, ConfigureAwait gibi anahtar kavramlar</summary>
 <dl>
<dd><li>Async:Senkron olan yani çağırıldığı şekilde ve birbirlerini beklemeyen fonksiyonları, asenkron hale çevirmemize yarar.</li></dd>
<dd><li>Await:Asenkron bir işlemi beklemek için kullanılır </li></dd>
<dd><li>Task:Bir programın işletim sistemi tarafından çalıştırılırken aldığı isim ya da görev.</li> </dd>
<dd><li>ConfigureAwait:Devam görevini yürütmek için main thread'in kullanıp kullanılmayacağını ayarlar.</li></dd>
 </dl>
 </details>

<details>
<summary>Arrow function (=>) ifadesinin C#’taki yeri</summary>
<li>Tek satırda fonksiyon tanımlama: static int Multiply(int x, int y) => x * y;</li>
<li>Lambda ifadesi: Func<int, int> square = n => n * n;</li>
 </details>

<details>
<summary>Senkron/Asenkron örnek senaryo açıklamaları</summary>
 <dl>
<dt>Senkron</dt>
 <dd>Kuralcı bir yapı ve tek yönlü bir zihin disiplinli bir şekilde sırayla kontrol eder.</dd>
 <dt>Asenkron</dt>
 <dd>Uyarlanabilir, esnek ve çok işe sahip.Bir yapılacaktan başka bir yapılacağa geçer ve en son hepsini derler.Zahmetsiz, hızlı yüklenen bir akış kurar.</dd>
 </dl>
 </details>


 ## 3.Backend Geliştirme Temelleri
 <details>
 <summary>Backend nedir?Fronted ile farkları nelerdir?</summary>
  <dl>
<dt>Backend</dt>
<dd>Bir web sitesi ya da bir mobil uygulamanın arka planında çalışan, kullanıcıya görünmeyen kısımdır.Kullanıcıdan gelen talepleri alır, veritabanı veya sınıcı tarafındandaki işlemleri yapar ve sonucu fronted'e iletir.Kısacası backend sisteminin "motorudru" benzetmesi yapabiliriz.</dd>

<dt>Frontend</dt>
<dd>Web sitesi ya da bir mobil uygulamanın kullanıcının gördüğü ve etkilişimde bulunduğu kısımdır.Tasarım ve arayüzde burada bulunur.HTML, CSS ve JS frontedi oluşturan temek teknolojilerdir. </dd>   
<dt>Aralarında ki farklar nelerdir?</dt>
<dd>Biri arkaplanda çalışan ve kullanıcının görmediği,veritabanı ve sunucu tarafı işlemleri yöneten backend, frontedn ise kullanıcının etkileşimde bulunduğu, kullanıcıya görünen kısımdır.</dd>
  </dl>
 </details>

 <details>
<summary>Web sunucusu nedir? API nedir? API türleri</summary>
<dl>
<dt>Web server nedir?</dt>
 <dd>Genellikle donanım ve yazılımın birlikte çalışmasını ifade eder.Web sunucusu donanımı internete bağlıdır,web ile bağlı diğer cihazlar ile veri alışverişşi yapmasını sağlar.</dd>
 <dt>API:</dt>
 <dd>Bir uygulamanın verilere, sunucu yazılımına veya diğer programlara ulaşabilmek için kullandığı bağlantı arayüzüdür.Bir çok veri web üzerine veya akıllı telefonlar ile API'ler sayesinde kolayca alınabiliyor.Bu da iletşimi hızlandırıyor.</dd>
 
 <dt>API Türleri:</dt>
 <ol>
  
 <li>Kullanım Alanına Göre:</li>

 Web API:İnternet üzerinde HTTP/HTTPS ile çalışan API'ler.<br>
 Library API:Programlama kütüphanelerinin sunduğu API'ler.(örn:Python)<br>
 Operating System API:İletişim sisteminin sunduğu arayüzler.<br>
 Hardware API:Donanım ile yazılım arasındaki işetişimi sağlar.<br>
 
<li>Mimariye Göre:</li>

Rest API:HTTP protokolü ile çalışır.JSON veya XML formatında veri döner.<br>
SOAP API:Daha eski XML tabanlı, katı kurallara sahip.<br>
GraphQL API:Tek bir sorguyla sadecd ihtiyaç duyulan veriyi alma imkanı verir.<br>
gRPC API:Google'ın geliştirdiği, hızlı ve verimli iletişim için kullanılan bir sistemdir.<br>

  <li>Erişim Türüne Göre:</li>
  
  Public(açık)API:Herkesin erişimine açıktır.<br>
  Private(özel)API:Sadece kurum içi yazılımda kullanılır.<br>
  Partner API:Sadece belirli iş ortaklarında açılır.
 
 </ol>
</dl>
 </details>

<details>
<summary>HTTP nedir? HTTP metodları: GET, POST, PUT, DELETE</summary>
<dl>
 <dt>HTTP Nedir?</dt>
 <dd>Bu protokol, bir web tarayıcısı ile bir web sunucusu arasında ki iletişimi sağlar.İstemci(server) ve sunucu(server) arsında ki veri transferini yönetir.Tarayıcının web sitelerini görüntülemesini, dosyaları indirmesini sağlar.</dd>
</dl>

 <dt>HTTP Metotları:</dt>
<ul>
 <li>Get:Belirtilen URL'de ki veriyi almak için kullanılır</li>
 <strong>Örnek:Bir e-ticaret listesinde ürün listesini görmek.</strong><br>
  <br>
 <li>Post:Belşirtilen URL'ye yeni bir kaynak eklemek için kullanılır.Bu metot ile form gönderimi sonocunda veriyi sunucuya ekleyebiliriz.</li>
 <strong>Örnek:Bir siteye kayıt olurken "kaydol" dediğinde.</strong><br>
  <br>
 <li>Put:Belirtilen URL'de var olan bir veriyi güncellemek için kullanılır.Bu metot ile sunucuda var olan bir dosyayı güncelleyebiliriz.</li>
  <strong>Örnek:Profil bilgilerinde "Adını ve Soyadını değiştir" dediğinde.<br></strong>
   <br>
 <li>Delete:Belirtilen URL'de ki dosyayı veya veriyi silmek için kullanılır.</li>
  <strong>Örnek:Sosyal medyada kendi gönderini silmek.</strong><br>
 <br>
</ul>
</details>

<details>
<summary>RESTful servislerinin çalışma mantığı</summary>
<dd>Her şey bir kaynak olarak düşünülür.Kaynaklara URL'ler üzerinden ulaşılır, HTTP metodları ile işlem yapılır, JSON ile veri taşınır ve her istek bağımsızdır.</dd>

<br>
<ol>
 <li>Kaynak(resource)mantığına dayanır;</li>
<ul>
 <li>Rest'te her şey bir kaynak(resource) larak düşünülür.</li>
 <li>Kullanıcılar->Users</li>
 <li>Ürünler->Poducts</li>
 <li>Siparişler->Orders</li>
 <li>Kaynağa erişim için Url(edpoint)kullanılır.</li>
</ul>
<br>

<br>
<li>HTTP metodları ile işlem yapılır;</li>
<ul>
<li>Get->Kaynağı getirir.</li>
<li>Post->Yeni kaynak oluşturulur</li>
<li>Put->Var olan kaynağı günceller</li>
<li>Deleted->Kaynağı siler</li>
</ul>
<br>

<br>
<li>İşletimci(client)-Sunuc(server)bağlantısı;</li>
<ul>
<li>İstemci(web, mobil uygulaması) sadece isteği gönderir</li>
<li>Sunucu(backend) isteği işler ve cevabı gönderir</li>
<li>İkisi birbirinden bağımsız, yani bir android uygulaması ve web sitesi bir Rest servisine bağlanabilir </li>
</ul>
<br>

<br>
<li>Stateless(durumsuz)çalışır;</li>
<ul>
<li>Her istek(request)bağımsızdır</li>
<li>sunucu önceki isteklerini hatırlamaz</li>
<li>Gerekli bilgiler(örnek:kimlik doğrulama tokeni)her istekte tekrar gönderilir</li>
</ul>
<br>

<br>
<li>Veri genelde JSON formatında çalışır;</li>
<ul>
<li>Cevaplar anlaşılır bir formatta döner</li>
</ul>
<br>

<br>
<li>HTTP states kodları kullanılır;</li>
 <ul>
  <li>200->Başarılı</li>
  <li>201->Kaynak oluşturur</li>
  <li>400->Hatalı istek</li>
  <li>401->Yetkisiz</li>
  <li>404->Bulunamadı</li>
  <li>500->Sunucu hatası</li>
  <br>
 </ul>
</ol>
</details>

<details>
<summary>JSON veri formatı ve kullanım amacı</summary>

<dd>Heminsan tarafından okunabilir hem de makine tarafından işlenebilir bir şekilde depolamak ve değiştirmek için kullanılan metin tabanlı bir formattır.Metin tabanlı ve sade yapısı sayesinde verilerin anlaşılmasını kolaylaştırır,ayrıca çoğu programlama dili tarafından desteklendiği için farklı sistemler arasında uyumlu bir veri değişimini mümkün kılar</dd>

<dt>Kullanım amacı:</dt>
<dd>Veri değişimi, kolay okunabilir ve yazılabilir veri, programlama dilleri arasında uyumluluk,API ve weeb servislerinde stanart,veri yapılarının baait temsilini sağlar.</dd>
</details>

<details>
<summary>SOAP ve GraphQL nedir, REST’ten farkları</summary>

<dl>
<dt>SOAP</dt>
<dd>Bilgisayar ağlarında web hizmetlerinin uygulanmasında yapılandırılmış bilgi alışverişi için kullanılan bir protokoldür.</dd>

<dt>GraphQL</dt>
<dd>API'ler için bir sorgu dili ve mevcut verilerle bu sorguları yanıtlamak için bir çalışma ortamıdır.</dd>
</dl>

<h3>SOAP vs GraphQL vs REST Temel Karşılaştırması</h3>

<table border="1">
    <body>
        <tr>
            <td>Özellik</td>
            <td>SOAP</td>
            <td>REST</td>
            <td>GraphQL</td>
    </td>
        </tr>
     
  <tr>
            <td>Türü</td>
            <td>Protokol</td>
            <td>Mimari tarz</td>
            <td>Sorgu dili</td>
        </tr>
        <tr>
            <td>Veri Formatı</td>
            <td>XML</td>
            <td>JSON(en çok kullanılan),XML</td>
            <td>JSON</td>
        </tr>
        <tr>
            <td>Endpoint</td>
            <td>Çok Sayıda</td>
            <td>Birden fazla</td>
            <td>Tek bir tane</td>
        </tr>
        <tr>
           <td>Esneklik</td>
           <td>Düşük</td>
           <td>Orta</td>
           <td>Yüksek</td>
       </tr>
        <tr>
           <td>Performans</td>
           <td>Ağır</td>
           <td>Hafif ve hızlı</td>
           <td>Daha esnek ama backend için yorucu</td>
       </tr>
        <tr>
           <td>Kullanım Alanı</td>
           <td>Bankacılık,kurumsal</td>
           <td>Web servisleri,mobil API</td>
           <td>Modern web ve mobil uygulamalar</td>
        </table>
        </body>
       </tr>
</details>

## 4.ASP.NET

<details>
<summary>•	ASP.NET ve ASP.NET Core nedir? Avantajları, farkları</summary>
<dl>
 <dt>ASp.NET</dt>
 <dd>.NET çerçevesi üzerinde web uygulamaları oluşturmak için açık kaynak bir web çerçevesidir.Yine microsoft tarafından geliştirilmiş ve geliştiricilerin dinamik web uygulamaları, hizmetleri ve siteleri oluşturmasına olanak sağlamak amacı ile yayınlanmıştır.</dd>
<dt>ASP.NET Core</dt>
<dd>Microsoft tarafından geliştirilen açık kaynak kodlu bir yazılım geliştirme platformu. ASP.NET Core, tüm ASP.NET altyapısının yeniden tasarlanarak MVC ve Web API altyapıları ile birleştirilmesini sağlamıştır.</dd>
<dt>ASP.NET ve ASP.NET Core farkları</dt>
<dd>ASP.NET güçlü veri tabanlı entegrasyonu sağlar ve oturum yönetimi, kimlik doğrulama ve güvenlik gibi önemli konuları ele alırken ASP.NET Core daha genel amaçlı uygulamalrın geliştirilmesi için kullanılır.</dd>
<dt>Avantajları</dt>
 <dd>ASP.NET ,Core'a göre daha eski.Açık kaynak kodlu, platform bağımsız, modern yazılım mimarilerine uygun olan ASP.NET Core, ASP.NET ise sadece windown üzerinde çalışan stabil ve kurumsal projelerde kullanılmış bir framework.</dd>
</dl>
</details>

<details>
<summary>MVC nedir, ne için kullanılır?</summary>
 <dl>
<dt>MVC Nedir?</dt>
<dd>Model View Controller'in kısaltılmışıdır.Model,veritabanında verilerin çekilmesine yardımcı olur.View, görünüm katmanıdır.HTML, CSS, JS gibi
 kodların tutulduğu bölümdür.Controller,model ve view arasında kalan katmandır.Kısacası uygulama mantığını,veriyi ve kullanıcı arayüzünü birbirinden ayırarak geliştirmeyi kolaylaştıranbir mimari desenidir.Düzenli kod yazmak,bakımı kolaylaştırmak, tekrar kullanılabilirlik sağlamak ve etst edilebilirliği artırmak için kullanılır.</dd>
  </dl>
</details>

<details>
<summary>Middleware nedir, nasıl çalışır?</summary>
<dl>
<dt>Nedir?</dt>
<dd>Web uygulamalrında istek(request) ve yanıt(respone) arasına giren küçük yazılım bileşenidir. İsteği işler, gerekirse sonraki middlaware'e gönderir veya direkt yanıt döner.</dd>
<dt>Nasıl Çalışır</dt>
<dd>Kullanıcıdan gelen istek ilk middlaware gelir.Middlaware isteği işler sonra kimiddlaware aktarır ya da direkt yanıt döner.Son middlaware yanıtı üretir,yanıtu testten geçirerek kullanıcıya ulaşır. </dd>
</dl>
</details>
































