# JS-DOM
JS-DOM-NOTES

## Methods

1-) document.doctype : Belge döküman türü referansını elde etmek için kullanılır. Eğer ki belgenin doctypeını öğrenmek istiyorsak bu methodu kullanmamız yeterli olacaktır.

      let name = document.doctype.name;
        console.log(name); --> HTML
     
2-) document.documentElement : HTML tagının referansını element nesnesi halinde elde etmek için kullanılır.

      let name = document.documentElement;
        console.log(name);

        let name2 = document.documentElement.nodeName;
        console.log(name2); --> HTML

3-) implementation : Belge ile ilgili DOM implementatşon arayüzünden türetilmiş bir DOM implementation nesnesi referansını bool veri türünde elde etmek için kullanılır.

      let process = document.implementation;
      document.getElementById("res").innerHTML = process.hasFeature("HTML", "1.0");

4-) document.body :  body : Belge içerisindeki body tagının referansını elde etmek için kullanılır.

       let body = document.body;
       console.log(body);

5-)head :  head : Belge içerisindeki head tagının referansını elde etmek için kullanılır.
      
        let head = document.head;
        console.log(head);
      
6-)characterSet : Belgenin karakter kodlamasının referansını elde etmek için kullanılır.
      
      let res = document.characterSet;
      console.log(res);
      
7-)document.inputEncoding : Belgenin karakter kodlamasının referansını elde etmek için kullanılır.

      let res = document.inputEncoding;
      console.log(res); --> UTF-8
      
8-) document.title : Belge içerisindeki title tagının referansını almak için kullanılır.

       let title = document.title;
       console.log(title);
       
9-)  document.compatMode :Belgenin tarayıcı tarafından hangi modda çalıştırıldığının referansını elde etmek için kullanılır.

       --> BackCompat : tuhaf veya rastlantı modu. birşeylerde problem var demektir 
       --> CSS1compat : standar/normal mod. bunu alırsak problem yok demektir
      
       let res = document.compatMode;
       console.log(res);

10-) document.documentMode : Belgeyi oluşturmak için tarayıcı tarafından kullanılan modun referansını elde etmek için kullanılır. sadece (Internet Explorer) için geliştirilmiş           bir methodtur.

        let res = document.documentMode;
        console.log(res);

11-) document.defaultView : Belgenin window referansını elde etmek için kullanılır.

         let res = document.defaultView;
        console.log(res);

12-)document.documentURI : Belge sayfasının URI(uniform resource indentifier) adresi referansının elde etmek için kullanılır.
      (Dosyanın çalıştığı yolu almak istiyorsak bunu kullan.)
      
      let res = document.documentURI;
      console.log(res); --> index.html:24 http://127.0.0.1:5500/index.html gibi.

13-) document.location : document.location : Belge url(uniform resource locator) adresi referansını elde etmek için ve ayarlamak için kullanılır.
      
         let res = document.location;
        console.log(res);

        //// 
        let resHref = res.href;
        console.log(resHref);

        /*ayarlam işlemi */
        //let islem = document.location.href = "https://www.google.com.tr"; bunu açarsan google gider :D

        /*mail gönderimi için */
        //let islem2 = document.location.href = "mailto:ahmetsuhanoka0@gmail.com";

        //Döküman içerisinde hareketlilik sağlamak kullanılabilir.(kaydırma istenilen yere gitme fln.)
            
14-)document.baseURI :  Belgenin mutlak url(uniform resource locator) adresi referansını elde etmek için kullanılır.
      
        let res = document.baseURI;
        console.log(res);

15-)document.URL : Belgenin tam url(uniform resource locator) adresi referansını elde etmek için kullanılır.

       let res = document.URL;
        console.log(res);

16-) document.domain : Belgenin domain adı referansını elde etmek için kullanılır.

         let res = document.domain;
        console.log(res);

17-) document.lastModified : Belgenin en son güncelleme tarihini ve saatinin referansını elde etmek için kullanılır.
      
18-)  document.readyState : Belge içeriğinin tarayıcı tarafından yüklenme durumu değeri referansını elde etmek için kullanılır.

         return value :
         -complete
         -loading
         
19-) document.designMode : Belgenin çalışma anında düzenlenebilir olup olmadığı referansını elde etmek için kullanılır.

       on --> dönerse belge düzenlenebilir demek.
       off --> dönerse düzenlenemez demektir.
       inherit --> dönerse düzenlenemez. 

20-)document.hasFocus() : Belge odağının olup olmadığı referansını elde etmek için kullanılır. BOOL veri tipi döner. Örneğin başka bir yer tıkladığımda false döner.
      sayfa odağı içerisinde tru döner. !!!

       let res = document.hasFocus();
        console.log(res);

21-) document.activeElement : Belge içerisindeki seçili veya odaklanılmış elemanın referansını elde etmek için kullanılır.

      const body = document.querySelector("body");

        const findActiveElement = () => {
            let res = document.activeElement;
            console.log(res);

        }
        const writeActiveElementName = () => {
            let res = document.activeElement.tagName;
            console.log(res);
        }
        body.addEventListener("click", findActiveElement);
        body.addEventListener("click", writeActiveElementName);

22-) document.anchors : Bu method kaldırılmaya çalışıyor ve tavsiye edilmiyor. kullanma!
     detaylı bilgi için <a  href="https://developer.mozilla.org/en-US/docs/Web/API/Document/anchors">TIKLA</a>
     
23-)document.links : document.links : Belge içerisindeki tüm linklerin referanslarını elde etmek için kullanılır. Referanslar birden fazla ise herbir link referansı döngü ile         elde edilebilir.

      let allLinks = document.links; // let allLinks = document.getElemenByTagName("a");

24-) document.scripts : Belge içerisindeki script tagına sahip olan tüm elemnaların referanslarını elde etmek için kullanılır.

      let scripts = document.scripts; 

25-) document.embeds :Belge içerisindeki embed veya object tagına sahip tüm elemanların referansını elde etmke için kullanılır.Embed HTML tarafında çok
     kullanılmamalı(img/iframe/video/audio) tagları kullanılmalı.
     
     let embeds= document.embeds;

26-) document.forms :Belge içerisindeki form tagına sahip tüm elemanların referanslarını elde etmek için kullanılır. Eğer birden fazla ise döngü ile herbirine tek tek
     ulaşılabilir.
     
      let forms = document.forms;
      
27-) document.images : Belge içerisindeki img tagına sahip tüm elemanların referanslarını elde etmek için kullanılır. Eğer birden fazla ise döngü ile herbirine tek tek 
     ulaşılabilir. 
      
      var imagesCollection = document.images;

28-)navigator.plugins : Tarayıcıdaki tüm eklentilerin referansını elde etmek için kullanılır. Eklenti referansları birden fazla ise her bir eklenti döngü ile elde edilebilir.
      
      let pluginsColletion = navigator.plugins;

29-) document.createAttribute() : Belge içerisinde istenilen elemena yeni bir nitelik Node u oluşturuyor ve bu oluşturduğu Nodu Node Object olarak geri dönüyor. 

   document.setAttributeNode : createAttribute() metodu ile oluşturulan özellik nodunu node nesnesine uygular.
   
    //butone tıklandığında seçilen h1 tagının color:red olacak :)
      const header1 = document.getElementById("header1");
        const button = document.getElementById("button1");
        button.addEventListener("click", function() {
            header1.setAttributeNode(att);
        });
        let att = document.createAttribute("style");
        att.value = "color:red;";

30-) document.createElement() : Belge içerisinde yeni bir HTML Node oluşturur ve oluşturduğu bu node'u bir NOde object oalrak geri döndürür.

   createTextNode() : document.createElement() methodu ile oluşturulan HTML elemanına metin nodu oluşturur ve oluşturduğu bu Node'u Node Object olarak geri döndürür.
   
   appendChild() : Bir nodu belirtilecek olan herhangi bir elemanın içerisine en sonda olmak üzere eklemek için kullanılır. 
   
        let body = document.querySelector("body");
        let div = document.createElement("div");
        let textNode = document.createTextNode("Ahmet Suhan OKA");
        div.appendChild(textNode);
        body.appendChild(div);

31-) document.createComment(): Belge içerisine yeni bir açıklama Node'u oluşturur ve oluşturduğu bu Node'u bir Node object olarak geriye döndürür.

      const areaDiv = document.querySelector("#area");
        let comment = document.createComment("Comment ekledim :)");
        areaDiv.appendChild(comment);
        
32-) addeventListener("eventAdi",function) : Belgeye Event Listener eklemek için kullanılır yani olay ekleriz. İşaretşlenen veya dinlenen olay belgede gerçekleştirilecek olur 
      ise belirtilecek olan fonksiyon veya fonksiyonlar çalışır.
      
      resultArea.addEventListener("mouseover", ornek1);
       resultArea.addEventListener("click", function(){});


33-) removeEventListener("eventAdi",function) : Belgeye addEventListener ile eklenmiş olan event'tı silmek için kullanılır.

      kaldırılacakEleman.removeEventListener("eventAdi",kaldırılacakFonksiyonAdi);
      
34-) dir : Belge içerisindeki metinlerin yazılış yönü referansını elde etmek için kullanılır. Ayrıca Belge içerisindeki metinlerin yazılış yönünün atamasını ayarlamak için de
     kullanılır.
     
        1-)ltr --> left to right
        2-)rtl --> right to left
     
        let area3 = document.getElementById("area3")
        console.log(area3.dir); --> rtl
        area3.dir = "ltr";
        console.log(area3.dir); --> ltr

35-) open() : Belge içerisinden yeni bir HTML çıktı akışı açmak için kullanılır.

   close() : Open metodu ile açılan HTML çıktı akışını kapatmak/sonlandırmak için kullanılır.
   
       Parametreler: 
        1-) Dosyanın Mime türü
        2-) Geçmiş aktarımı
        
         function ornek1() {

            let islen = window.open(); // yeni sayfada açmak için
            islem.document.open("text/html", "replace"); //geçmiş hatırlanır
            islem.document.write("burası yeni");
            islem.document.close();
        }
        
36-) document.styleSheets :Belge üzerinde etkisi olan tüm stil sayfalarının nesne referansını elde etmek için kullanılır. Eğer stil sayfası referansları birden fazla ise her
     style sayfası referansı döngü ile elde edilebilir.
     
      let styleSheets = document.styleSheets;

37-) document.adoptNode() : Belge içerisine başka bir belgeden node eklemek için kullanılır. Ekelenecek olan Node un varsa tüm alt node'larıda işleme dahil edilerek ilgili tüm
      nodlar diğer belgeden kaldırılır. 

38-) document.importNode() : Belge içerisine başka bir belgeden node eklemek için kullanılır. Eklenecek olan node un varsa tüm alt node ları da eklenir.

39-) document.normalize() : Belge içerisindeki boş text node larını kaldırarak bitişik düğüme katılmasını sağlar.

40-) document.cookie : 

       Cookie Yapısı :
        1-)Çerez ADI : 
        2-):erez değeri: 
        3-)Ceçer yaşam süresi
        4-)Path
        cookie adı = Cookie değeri; Cooki yaşam süresi ; Path

41-) Atribute üzeinde --> lenght() : Belge içerisindeki HTML elemanına eklenmiş olan attribute lerin sayısını elde etmek için kullanılır.
      
      let asdDivAttributeLength = asdDiv.attributes.length;

42-) attributes[index].name : Belge içerisindeki HTML elemanına eklenmiş olan attribute adı referansını elde etmek için kullanılır. HTML elemanı içerisindek, çzellik sayısı birden fazla ise her
      bir özellik adı referansı döngü ile elde edilebilir.
      
            const asdDiv = document.getElementById("asd");
            let asdDivAttrName = asdDiv.attributes[0].name;
            console.log(asdDivAttrName);
            console.log(asdDiv.getAttributeNames());
            

43-) attributes[index].value : Belge içerisindeki HTML elemanına eklenmiş olan attribute değerinin referansını elde etmek için kullanılır. HTML elemenanı içerisindeki attribute 
      sayısı birden fazl ise her bir attribute değeri döngü ile elde edilebilir.
      
          let asdDiv = document.getElementById("asd");
            for(let i = 0 ; i< asdDiv.attributes.length; i++){
                console.log(asdDiv.attributes[i].value);
            }  

44-)  attributes[index].specified : Belge içerisindeki HTML elemanına Her hangi bir attribute nin klenip eklenmediğini referansını bool veri türünde elde etmek için  kullanılır.

            let asdDiv = document.getElementById("asd");
            console.log(asdDiv.attributes[0].specified);
            console.log(asdDiv.attributes.item(1).specified);
            let res = asdDiv.getAttributeNode("id").specified;
            console.log(res);
            let res2 = asdDiv.getAttributeNode("class").specified;
            console.log(res2);

45-)
     
   
      
