### Razor Pages nedir? ###

Razor Pages, asp.net core 2 ile birlikte gelen yeni bir özellik. Daha önce kullandığımız asp.net web forms çatısına yaklaşım olarak benzemekle birlikte klasik asp.net webforms'u kullanmadan asp.net mvc üzerine geliştirilmiştir. Razor Pages, sayfa bazlı senaryolar için bildiğimiz mvc (model view controller)'a göre daha kolay uygulama geliştirmeyi sağlayan bir platformdur. Frontend çatılarda kullanılan yaklaşım olan mvvm (model view view model) yapısına benzeşen çift yönlü bağlantı özelliğini desteklemektedir.

### Console Application Nedir? ###

Visual Studio ile yeni proje oluştururken bize "Windows Forms Application" ve "Console Application" gibi seçenekler sunulur. Bunlar arasındaki fark nedir?
Windows Forms Application yani Windows Uygulamaları günümüzde iyice yaygınlaşmış olup, programcıya hazır nesneler sunan (textBox, comboBox, RadioButton...) ve grafik arayüzüne sahip bir programlama dilidir. Console ise grafiksel olmayan bir kullanıcı arayüzüne sahiptir. Kullanıcıdan bilgi alma ve gösterme işlemleri siyah bir ekranda gerçekleşir. Visual C# veya Visual VB dillerinde kullanabildiğimiz hazır nesneler Console Uygulamalarında yoktur. Programcı kendisi kod yazarak bu nesnelere benzer yapılar oluşturabilir ancak bu herkesin yapabileceği bir şey değildir. Günümüzde Windows uygulamaları daha yaygın olarak kullanılmaktadır. Console uygulamaları ise bazı okullarda programcılığa giriş amacıyla kullanılabilmektedir.

### Serialize nedir? ###

Serialization işlemi, bir nesneyi, depolamak veya serileştirmek amacıyla istenen formata dönüştürme işlemidir. Bir nesnedeki verinin bir yerde depolaması veya ağ ortamında bir yerden bir yere gönderilmesi gerektiği durumlarda uygun formata dönüştürülmesi işlemine serileştirme denir. Serileştirilen nesneler veritabanı, hafıza veya dosya gibi ortamlarda saklanabilirler.

### Deserialize nedir? ###

Deserialization ise serileştirilmiş biçimdeki verilerin tekrar nesnelere dönüştürülmesi işlemidir. 
Serialization işleminin tam tersi bir durum sözkonusudur burada.

### MVC (Model-View-Controller) nedir? ###

**Model** - Kullanıcaya göstermek ve manipule etmesini sağlamak istediğimiz verileri içeren nesnelerdir.

**View** - Kullanıcıya Model'i gösterdiğimiz ve Model üzerinde çeşitli manipulasyonlara izin verdiğimiz yer, 
Web olsun, windows olsun fark etmez, amaç kullanıcıya birşeyler göstermek ve inputlar almaktır.

**Controller** - Kullanıcıdan gelen inputları karşılar, ayrıca UI ile ilgili bütün akışı yönetir ve kararları verir. Controller View hakkında hiç birşey bilmez ama View Controller'ı bilir. Görüldüğü üzere Controller ile View arasında 1-n bir ilişki var yani bir Controller birden fazla View tarafından kullanılabilir. Controller kullanıcıdan gelen inputlar doğrultusunda Model üzerinde değişikleri yapar, Model değiştiğini View'e notify eder yani View ile Model arasında Observer ilişkisi var. View, Model'e register olur, görüldüğü üzere bir model'e birden fazla View register olabilir. Aralarında ki observer ilişkisi sayesinde, Model'deki herangi bir değişiklik ona register olmuş bütün View'lere yansır.

### MVP (Model-View-Present) nedir? ### 

MVP Pattern'i aslında MVC'den evrilmiş bir pattern, sadece bağımlılıklar değişiyor ve Controller'ın yerine Prenseter (ki bu durumda kendisine hala Controller denebiliyor) geliyor. Görüldüğü üzere burada inputları direk View karşılıyor, modern programlama ortamlarının mantığına daha uygun. View Presenter'ını biliyor, Presenter ise View'i bir interface aracılığıyla biliyor aralarında bir abstraction var. Ayrıca MVC'nin aksine View ile Presenter arasında 1–1 ilişki var. Presenter Model'i manipule ediyor, Model'in değişikleri Presenter'a notify etme durumu birazcık tartışmalı, etmeyedebilir, Presenter ilgili değişikliği yapıp, View'i kendisi güncelleyebilir. Zaten buradaki en büyük fark MVC'nin aksine Presenter'ın View'i bir interface aracılığıyla kendisinin güncellemesi, View burada Presenter'a interface aracılığıyla istediği bilgiyi açabilir, ister Textbox'ın Text'i olsun ister Buton'ın Enabled'ı olsun. Presenter View'in nasıl bir View, Web mi? Windows mu? olduğuyla ilgilenmiyor, sadece data akışıyla ilgili ne yapması gerektiğini, View'den gelen etkileşimleri nasıl karşılaması gerektiğini ve View'de nasıl değişikler yapması gerektğini biliyor. Yani Prensenter'ımız burada karar mekanizaması rölünü üstleniyor.

### MVVM (Model-View-ViewModel) Nedir? ###

MVVM bir projenin "sorumlulukların ayrıştırılması" esasına göre geliştirilmesi temeline dayanan bir tasarım kalıbı sunmaktadır. Sorumlulukların ayrıştırılması, yani meslek hayatımızda kullandığımız karşılığıyla Separation of Concerns(SoC). MVVM bir yazılımı Model, View ve ViewModel adında üç farklı yapıda geliştirmemizi tavsiye etmektedir. Bu üç yapıyla ilgili kısa açıklamalara az sonra değineceğiz. İlk olarak 2005 yılında John Gossman tarafından decoupling problemini çözmek için ortaya atılan MVVM deseni aslında Martin Fowler'ın Presentation Model deseninin WPF ve Silverlight platformları için özelleştirilmiş halidir. Belki bazılarımızın kulağına yeni gelen bu tasarım deseninin aslında 10 seneye yakın bir geçmişi bulunmakta. Özellikle ülkemizde bu tarz gelişmelere biraz geç adapte olduğumuzu düşünürsek, MVVM'in sektörümüz için taze bir konu olduğunu söyleyebiliriz. MVVM'in Temel Yapı Taşları MVVM, Model, View ve ViewModel olmak üzere üç temel yapıdan oluşmaktadır. Kısaca bu yapıların neler olduğuna değinecek olursak:
**Model** - Veritabanından, web servislerinden ya da herhangi bir veri kaynağından gelen verilerimizi temsil etmek için kullanılan POCO ya da entity sınıflarından oluşmaktadır. Ayrıca veri tutarlığını ve doğruluğunu kontrol eden iş kuralları da burada yer almaktadır.
**View** - Bu kısım verilerimizi son kullanıcılara aktardığımız görsel arayüzdür. Son kullanıcı ile uygulama arasında bir köprü görevi görür.
**ViewModel** - ViewModel ise görsel arayüz ile model arasında köprü görevi görmektedir, yani Model'i View'a bağlayan yapıdır. View ile Model arasında doğrudan bir etkileşim yoktur. View, ilgili işlemleri ViewModel üzerinden yapmaktadır. ViewModel'ın View'a direkt erişimi yoktur ve View ile ilgili hiçbir şey bilmez.

### MVU (Model-View-Update) – How Does It Work? ###

MVU (also known as The Elm Architecture) seems to be one of those things which are a mystery to most of us. Until all of a sudden, we understand it and never wanna miss it again. It's not all that complicated. https://thomasbandt.com/model-view-update
