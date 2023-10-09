# DÜZCE ÜNİVERSİTESİ TEKNOLOJİ FAKÜLTESİ
## BİLGİSAYAR MÜHENDİSLİĞİ BİTİRME TEZİ PROJE RAPORU

### YUNUS EMRE PALAVAR




#### PANDEMİ DÖNEMİNDE UZAKTAN SENKRON- ASENKRON YÜRÜTÜLEN DERSLERDE KLASİK SINAVLARDA ÖĞRENCİ SINAVLARININ OKUNMASI VE DEĞERLENDİRİLMESİ 

OCAK 2021 

İÇİNDEKİLER DİZİNİ
- Giriş
- Kullanılan Teknolojiler
- 2.1. Python Teknolojileri
- 2.1.1. Python
- 2.1.2. Spyder
- 2.1.3 Pandas kütüphanesi
- 2.1.4. Dataframe
- 2.1.5 Xlsxwriter kütüphanesi
- 2.1.6. Openpyxl
- 2.2. Materyal ve Metot
- 2.2.1. Dataset
- 2.2.2. Database
- 2.2.3. Metot
- SONUÇ
 
ŞEKİLLER DİZİNİ

- Şekil 1:Dataset
- Şekil 2:Database
- Şekil 3:Her Öğrencinin 1 Soru İçin Cevapları
- Şekil 4:Bir Öğrencinin Bir Soru İçin Cevabının Cümlelere Bölünmesi
- Şekil 5:Blok Şema
- Şekil 6:Search Algoritması Akış Diyagramı
- Şekil 7:Cevapların Bulunduğu Ansvers Excel Dosyası
- Şekil 8:Öğrenci İd'leri
- Şekil 9:Öğrenci Numaraları

**GİRİŞ**

İçinde bulunulan covid-19 pandemi süreci dolayısıyla ülkemizde uzaktan eğitime geçiş yapıl-mıştır. Uzaktan eğitim süreci senkron veya asenkron olarak sürdürülmektedir. Öğrencilere yapılan dersler doğrultusunda değerlendirilmeleri için ödev verilmekte veya sınav yapılmaktadır. Bu süreçte sınavlar öğrencilere çevrimiçi veya çevrimdışı olarak sunulmaktadır. Bu makalede ele alınacak projede sınav ve ödev türü klasik hazırlanan açık uçlu cevaplar içeren soru şeklidir. Bu projede öğrencilere yapılan ödev veya sınavların okunmasına ve değerlendirilmesine yönelik bir çalışma yapılmıştır. Bu çalışma da günümüzde gelişen bilgisayar teknolojilerinden faydalanılarak insan iş yükünü hafifletmeyi ve daha tutarlı bir sistemle sınavların okunması amaçlanmıştır. Bu doğrultuda eğitim görevlisinden alınan veriler ile hazırlanan database programa entegre edilerek programın database temelli bir değerlendirme yapması sağlanmıştır. Database eklenen veriler eğitim görevlisi tarafından belirlenen sorulara yönelik cevapları oluşturacak anahtar kelime gruplarıdır. Program bu anahtar kelime gruplarını kullanarak öğrenci cevapları üzerinde arama işlemi yapmaktadır. Arama sonuçlarına göre öğrenci cevaplarının değerlendirmesini yapmaktadır.    
 
**KULLANILAN TEKNOLOJILER**

**2.1. Python Teknolojileri**

Bu makalede ele alınacak olan çalışma python programlama dili ile yazılmıştır. Proje yazımında kullanılan derleyici Spyder programıdır. Çalışmada kullanılan python sürümü 3.7 dir. Python yapıları pandas, xlxswriter, dataframe ve openpyxl' dir.

**2.1.1. Python**

Python, nesne yönelimli, yorumlamalı, birimsel (modüler) ve etkileşimli yüksek seviyeli bir programlama dilidir. 

Girintilere dayalı basit sözdizimi, dilin öğrenilmesini ve akılda kalmasını kolaylaştırır. Bu da ona söz diziminin ayrıntıları ile vakit yitirmeden programlama yapılmaya başlanabilen bir dil olma özelliği kazandırır.

Modüler yapısı, sınıf dizgesini (sistem) ve her türlü veri alanı girişini destekler. Hemen hemen her türlü platformda çalışabilir. (Unix, Linux, Mac, Windows, Amiga, Symbian). Python ile sistem programlama, kullanıcı arabirimi programlama, ağ programlama, web programlama, uygulama ve veritabanı yazılımı programlama gibi birçok alanda yazılım geliştirebilirsiniz. Büyük yazılımların hızlı bir şekilde prototiplerinin üretilmesi ve denenmesi gerektiği durumlarda da C ya da C++ gibi dillere tercih edilir.

Python 1980'lerin sonunda ABC programlama diline alternatif olarak tasarlanmıştı. Python 2.0, ilk kez 2000 yılında yayınlandı. 2008'de yayınlanan Python 3.0, dilin önceki versiyonuyla tam uyumlu değildir ve Python 2.x'te yazılan kodların Python 3.x'te çalışması için değiştirilmesi gerekmektedir. Python 2 versiyonun resmi geliştirilme süreci, dilin son sürümü olan Python 2.7.x serisi versiyonların ardından 1 Ocak 2020 itibarıyla resmi olarak sona erdi. 
Python 2.x geliştirilme desteğinin sona ermesinin ardından, Python dilinin 3.5.x ve sonraki sürümlerinin geliştirilmesi devam etmektedir.

Python'un son derece kolay okunabilir olması düşünülmüştür. Bu yüzden örneğin küme parantezleri yerine girintileme işlemi kullanılır. Hatta bazı durumlarda girintileme işlemine dahi gerek kalmadan kodun ilgili bölümü tek satırda yazılabilir. Böylece Python, program kodunuzu en az çaba ile ve hızlıca yazmanıza imkân tanır. Sade sözdizimi ile diğer programlama dillerinden üstündür.

**2.1.2. Spyder**

Spyder, Python dilinde bilimsel programlama için açık kaynaklı bir çapraz platform entegre geliştirme ortamıdır (IDE). Spyder, bilimsel Python yığınında NumPy, SciPy, Matplotlib, pandalar, IPython, SymPy ve Cython ve diğer açık kaynaklı yazılımlar dahil olmak üzere bir dizi önde gelen paketle entegre olur ve MIT lisansı altında piyasaya sürülür.

İlk olarak 2009 yılında Pierre Raybaut tarafından yaratılan ve geliştirilen Spyder, 2012'den beri bilimsel Python geliştiricileri ve topluluk tarafından sürdürülmekte ve sürekli olarak geliştirilmektedir.

Spyder, birinci ve üçüncü taraf eklentilerle genişletilebilir, veri incelemesi için etkileşimli araçlar için destek içerir ve Python'a özgü kod kalite güvencesi ve Pyflakes, Pylint ve Rope gibi iç gözlem araçlarını yerleştirir. Çapraz platform üzerinden Anaconda, Windows'ta, macOS'ta MacPorts üzerinden ve Arch Linux, Debian, Fedora, Gentoo Linux, openSUSE ve Ubuntu gibi büyük Linux dağıtımlarında kullanılabilir.

**2.1.3 Pandas kütüphanesi**

Pandas, veri işlemesi ve analizi için Python programlama dilinde yazılmış olan bir yazılım kütüphanesidir. Bu kütüphane temel olarak zaman etiketli serileri ve sayısal tabloları işlemek için bir veri yapısı oluşturur ve bu şekilde çeşitli işlemler bu veri yapısı üzerinde gerçekleştirilebilir olur. Yazılım ücretsizdir ve bir çeşit BSD ile lisansına sahiptir. Yazılım ismini bir ekonometri terimi olan veri panelinden almıştır. Bir veri paneli birçok zaman aralığı içinde farklı gözlemlerin işlenebildiği yapıyı tarif eder.

- import pandas as pd

**2.1.4. Dataframe**

Pandas temel olarak makine öğrenmesi uygulamalarında kullanılmaktadır. Bu uygulamalarda en öne çıkan özelliği de veri isketleridir. Pandas ayrıca birçok farklı formattan (csv, excel gibi) veri içe aktarması gerçekleştirebilir. Pandas çok farklı veri işleme yöntemlerini uygulayabilir; örneğin gruplama, ekleme, birleştirme, kaynaştırma, bir araya getirme. Ayrıca bu kütüphane veri temizleme için veri doldurma, değiştirme ve varsayma özelliklerine de sahiptir.

- news_df = pd.DataFrame({'document':ansvers_array_one})

**2.1.5 Xlsxwriter kütüphanesi**

Python xlsxwriter kütüphanesi excel formatlı dosyalara veri aktarılması için kullanılır.

- import xlsxwriter

**2.1.6. Openpyxl**

Bu yapı python ile excel, csv formatlı dosyalardan içeri veri aktarılması için kullanılır.

- from openpyxl import Workbook,load_workbook

**2.2. Materyal ve Metot**

**2.2.1. Dataset**

Bu makalede ele alınan proje için 10 öğrencinin 10 soru için cevaplarından oluşan bir dataset kullanılmıştır.

![](https://i.hizliresim.com/nykc2lz.png)
Şekil 1:Dataset

**2.2.2. Database**

Bu makalede ele alınan proje için hazırlanan database içeriği yetkili eğitim görevlisinin verdiği bilgiler ışığında hazırlanmıştır. Database 10 soru için öğrencilerin cevaplarının değerlendirme kriteri olacak keyword’lerden oluşmaktadır. Her soru için 5 adet keyword bulunmaktadır. Her keyword için bir adet prekeyword ve suffix keyword değeri bulunmaktadır.

 
![](https://i.hizliresim.com/qaoiy2q.png)

Şekil 2:Database

**2.2.3. Metot**

Makalede ele alınan projenin blok şeması şekil-5’te gösterilmektedir. Program çalıştırıldığında önceden hazırlanmış datasette ki verileri okur, sonra ki aşama da program datasette ki verilere veri önişleme işlemlerini uygular, akabinde databasede ki verilere dayanarak search algoritmasını çalıştırılır, search algoritması sonuçları bir diziye eklenir, son olarak dizideki veriler excel belgesine yazdırılır. 

Dataset veri okuma işlemi öğrencilerin sorulara ait cevapların bir diziye alınmasıdır. Her soru için öğrenci cevapları birer diziye alınır. Bu dizilerdeki her bir indeksteki verilere veri önişleme işlemleri yapılır.

 
![](https://i.hizliresim.com/t3wm3ev.png)
Şekil 3:Her Öğrencinin 1 Soru İçin Cevapları

Her öğrencinin cevabı veri ön işleme işlemlerinden sonra bir diziye atılır (Şekil-3). Sonra her öğrencinin cevapları cümlelere ayrılarak her biri bir diziye atılır (Şekil-4). Öğrenci cevapları python split metodu kullanılarak cümlelere ayrıştırılır.

 
![](https://i.hizliresim.com/kptiqqb.png)
Şekil 4:Bir Öğrencinin Bir Soru İçin Cevabının Cümlelere Bölünmesi

Veri önişleme aşamasında yapılan işlemler sırasıyla noktalama işaretlerini, sayıları ve özel karakterleri, alfabe boşlukları hariç her şeyin yerini alacak olan regex replace'i (“[^ a-zA-Z #]”, ”“) tek adımda kaldırmak, ardından genellikle yararlı bilgiler içermediğinden daha kısa kelimeleri kaldırmak, son olarak, büyük / küçük harf duyarlılığını geçersiz kılmak için tüm metni küçük harfe çevirmektir.
 
 
![](https://i.hizliresim.com/rrtgonk.jpg)
Şekil 5:Blok Şema

Bu çalışmada sorumlu eğitim görevlisi tarafından hazırlanan database doğrultusunda öğrencilerin cevaplarından oluşan dataset içerisindeki her hücre verisi taranmıştır. Bu tarama işlemi şekil 6’da akış diyagramı verilen search algoritması tarafından gerçekleştirilmiştir.

 
![](https://i.hizliresim.com/gamgon5.jpg)
Şekil 6:Search Algoritması Akış Diyagramı

Search algoritması her öğrencinin bir adet soru için cevaplarının ilk olarak bir diziye atılması işlemiyle başlar. Her cevap cümlelere ayrıştırılarak yeni dizilere atılır. İç içe dizi yapısı oluşturulur. Öğrencilerin cevaplarının cümlelere ayrıştırılmış hallerinin bulunduğu dizi içerisinde her cümle için keyword parametresi aranır. Keyword parametresinin bulunduğu her cümle için prekeyword parametresi aranır. Keyword ve prekeyword parametrelerinin bulunduğu cümle için suffix keyword parametresi aranır. Bir öğrenci için bu üç koşulu sağlayan başka cümle olup olmadığı kontrol edilir. Öğrenci başka bir cümlede aynı koşulları sağladı ise öğrencinin ilk koşulu sağlayan cümlesi dışındaki bütün koşulu sağlayan diğer cümleler es geçilir. Böylelikle bir öğrencinin bu koşulları tekrar etmesinin önüne geçilir. Öğrenci koşulu sağlar ise puanı bir artırılır.

Search algoritması sonucunda öğrencilerin koşulları sağlayan maksimum bir cümlesi diziye atılmıştır. Bu cümlelere ait indeks değeri yeni bir diziye atılır. Koşulları sağlayan cümlelere ait öğrencilerin puanları bir artırılır. Öğrencilerin puanları cevap excel’in de ilgili hücrelere yazılır(şekil-7).

 
![](https://i.hizliresim.com/43zpiv6.png)
Şekil 7:Cevapların Bulunduğu Ansvers Excel Dosyası

Ansver excel oluşturma işlemi program tarafından gerçekleştirilmektedir. Öğrenci no ve id sütunları datasetten çekilmektedir. (Şekil-8, Şekil-9)

 
![](https://i.hizliresim.com/a6zrbc6.png)
Şekil 8:Öğrenci İd'leri

 
![](https://i.hizliresim.com/17myx9l.png)
Şekil 9:Öğrenci Numaraları

 

**SONUÇ**

İçinde bulunulan Covid-19 pandemi süreci dolayısıyla eğitimin uzaktan senkron veya asenkron olarak sürdürülmesinin öğrenci performansı üzerinde etkileri vardır. Öğrenci performansı ölçüm aracı olarak verilen sınavlar veya ödevlerde öğrencilerin açık uçlu sorulara verdiği cevaplar irdelenmektedir. Bu cevaplar açık uçlu olduğunda sayfalarca doküman ortaya çıkmaktadır. İrdeleme sonucunda öğrencilerden istenilen cevapların verilip verilmediği adaletli ve tarafsız olarak değerlendirilmesi amaçlanmaktadır. Ortada ki insan faktörü ve doküman çokluğundan dolayı bu değerlendirme her zaman yüzde yüz doğru bir sonuç vermemektedir. Bu projede aradaki insan faktörünü ortadan kaldıran bilgisayar teknolojileri kullanılarak bir değerlendirme aracı gerçekleştirilmiştir. Bu araç ile ders eğitim görevlisi tarafından verilen bilgiler ışığında hazırlanan database doğrultusunda sorulara verilen cevaplar irdelenmiş ve değerlendirilmiştir. Bu proje sonucunda insan faktörünün ortadan kaldırılması ile hata payı minimize edilmiştir. Bilgisayar teknolojilerinin kullanılması ile insan iş yükü hafifletilmiş ve zaman kazanımı sağlanmıştır. 



