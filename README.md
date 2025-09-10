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
<ul>
  <li>Merge confit neden oluşur?</li>
      Bir dosyanın belli bir kısmı iki kişi tarafından değiştirilmeye çalışır ise uygulama hangisini uygulayacağını bilemez ve bu sorun ortaya çıkar.
     <li>Nasıl çözülür?</li>
     Çakışmalı hatalı dosyayı açıp <<<<<<<, =======, >>>>>>> işaretlerinden uygulama için mantıklı olanı seçeriz gerekirse birleştirebilirizde.En son olarak değişikliği git add ile sahneleyip git commit ile birleştirme tamamlanır.
       </ul>
     </details>

       
<details>
<summary>CI/CD nedir? Azure DevOps, GitHub Actions ile pipeline örnekleri</summary>
<ul>
    <li>CI(Continuous Integration):Sürekli entegrasyon</li>
     Tüm kod değişikliklerinin paylaşıldığı kaynak deposu.Her değişikliliği kaydettiğimizde veya birleştirdiğimizde otomatik olarak test etmek ve bir derleme başlatma uygulamasıdır.CI sayesinde hatalar,güvenlik sorunları daha kolay tespit edilip geliştirme sürecini çok daha erken bir aşamada düzeltilebilir.<br>
     <li>CD(Continuous Delivery):Sürekli teslimat</li>
      Altyapı sağlama uygulama yayınlama sürecini geliştirmek için CI ile birlikte çalışan bir yazılım geliştirme uygulamasıdır.
      <br>Sürekli entegrasyon ve sürekli teslimatın birleşimidir.Yeni düzenlenmiş bir kodu committen üretime geçirmek için ihtiyaç duyulan manuel insan müdehalesinin çoğunu veya tamamını otomatikleştirir.CI veya CD den yana aynı zamanda altyapıyıda sağlamayı kapsar.Geliştirme ekipleri kodda değişiklik yapabilir ve  bunlar daha sonra otomatik olarak test edilip dağıtım için gönderilirler.<br>
      <li>GitHub Actions ile Pipeline örnekleri:</li>
      GitHub Actions GitHub üzerinden yapılan projeleri barındıran CI/CD iş akışları kurmaya yarayan bir sistem
      <li>Azure DevOps ile Piepline örnekleri:</li>
      Microsoft bulut tabanlı YMAL veya görsel olarak oluşturulabilen güçlü bir CI/CD aracıdır.     



</ul>
  </details>


  





    
  </details>


  
   

</details>
