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
