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
