### Değişken Tanımlama
Değişken tanımlarken başına veri tipini yazmalıyız
değişken tanılarken 3 kurala dikkta etmeliyiz
1. Kesinlikle ama kesinlikle değişkenin adının başına rakam gelemez isnisna yok "1isim" gibi fakat "isim1" veya "i1sim" gibi tanımlanan değişkenler bir sorun yaratmaz
2. Kesinlikle özel karakter kullanmıyoruz (/,-,*,+,-,%,&,! gibi virgül ve boşluk dahil) tek bir isnisna var izin verilen tel özel karakter alt çizgidir istediğiniz gibi kullana biliriniz "_denem", "de_neme", "deneme_" gibi
3. Türkçe karakterler kullanmayın kodunuz çalışacaktır ama kesinmlikle tavsiye etmiyorum (ü,ğ,ç,ö,ş,ı gibi) "üzüm" yerine "uzum" yazarsanız daha sağlıklı olur
4. Daha önceden aynı blok içerisinde kullanılan (farklı veri tiplerinde olsa bile) bir değişken varsa aynı değişkeni tekrar tanımlayamazsınız 
```C#
int a1; // sorun yok
int 1a; //1.kural hatası
int de neme; //2.kural hatası
string bolme.islemi; //2.kural hatası
int a_sayisi; // sorun yok
int a_sayısı; //3.kural hatası
string a1; //4.kural hatası
```

### Ana (Sık Kullanılan) Veri Tipleri
Sayısal,Metin ve Boolen olmak üzere 3 tanedir

1.Sayısal veri tipleri "int" anahtar kelimesi ile tanımlana bilir tabiki sadece "int" ile sınırlı değil "float","double","long","short" gibi farklı türlerde var ama onlar bir sonraki dersin konusu sadece bu derslik "int" veri tipini bilseniz yeter bu veri tipini tam sayılarda kullanırız

```C#

int sayilar;

```

2.Metin veri tipleri "string" anahtar kelimesi ile tanımlana bilir tabiki sadece "string" ile sınırlı değil "char" vs gibi çok sayıda türlere sahip "string" veri tipini tırnak içine yazdığımız bir veriyi atayacağımız değişken için kullanabiliriz

```C#

string metinler;

```

3.Boolen veri tipi bu tek veri tipidir benzeri yada yernine kullanıla bilecek başka bir veri tipi yok "bool" anahtar kelimesi ile tanımlanır sadece "true" ve "false" değerlerini tutar başka değer alamaz

```C#

bool dogru_yanlis;

```

### Değişkene Değer Atama
Değişkene değer atarken "=" operatörünü kullanırız ve 2 şeye dikkat etmeliyiz
1.Değişenin veri tipi "int" veri tipindeki "a" değişkenine sadece sayı ataya biliriz

```C#

int a;

a="merhaba";//hatalı atama "merhaba" bir string dir ama "a" değişkeni ise "int"

a=5;//doğru bir atama

```

2.Eşittirin sağı veya solu her zaman değişken "=" oparetörünün soluna atanacak değer sağına yazılır aksi durumda hata alırız

```C#

string b;

"merhaba" = b //1.kurala uygun ama 2.kuralda hata var bu yüzden yanlış atama

b="merhaba"//doğru bir atama

```

### Consola Veri Yazdırma
Consola yazı,sayı yada bir şeyler yazdırırken "Console" sınıfının içindeki "Write" veya "WriteLine" gömülü fonksiyonlarını kullanırız fonksiyon ve sınıf kavramına yabancısımız ileride işleyeceğiz şimdilik sadece böyle olduklarını bilin 
peki "Write" ile "WriteLine" arasında ne fark var arasındaki far şu "Write" kullanarak consola ekranına yine yazdırma işlemi yaparız ama yazıyı yazdıktan sonra imleç yazının bittiği yerde kalır yani "Write" komutunu kullandıktan sonra her hangibi bir komutla tekrar bir şey yazdırdığımızda yan yana yazar 
"WriteLine" ise yazdırma işleminden sonra imleci bir alt satıra gönderir yani "WriteLine" ile yazdırma işleminden sonra bir kere daha yazdırma işlemi yapacak olursak alt alta yazacaktır
```C#
Console.Write("merhaba");
Console.Write("dünya"); //çıktısı "merhabadünya" olucak

Console.WriteLine("merhaba");
Console.Write("dünya"); // çıktısı:
/*
merhaba
dünya
*/
//şeklinde olucak

Console.WriteLine("merhaba");
Console.Write("dünya");
Console.Write("nasılsın");// çıktısı
/*
merhaba
dünyanasılsın
*/
//şeklinde olucak imleç merhabadan sonra aşşağı inecek ama "dünya" yazarken "Write" kullandığımız için "dünya" ve "nasılsın" birleşik yazılacak
```

### Consolu Açık Tutma
Ekrana yazdırma işlemini Visual Sutudio da çalıştırdıysanız consol açılıp kapanmıştır videoda olduğu gibi bunu sebebi şu aslında kodunuz doğru ve çalışıyor ama ekrana yazdırdıktan sonra beklemesini söylemediğimiz sürece beklemez yazdırıd sonrada kapatır bilgisayara söylemedn yapmasını bekleyemeyiz.
Peki nasıl beklemesini söyleye biliriz yine "Console" sınıfı içinde bulunan "Read","ReadLine","ReadKey" gömülü fonksiyonlarını kullanarak beklemesini sağlaya biliriz
Not: "Read","ReadLine","ReadKey" gömülü fonksiyonları sadece ekranda Consolu açık tutmak için kullanılmıyor ileri derslerimizde asıl kullanım amaçlarını görüceğiz zaten form uygulamalarına geçtiğimizde consol olmayacağı için bunları kullanmamız gerekmicek ama o zamana kadar daha çok kullanacağız bunları

```C#

Console.Write("Merhaba Dünya!");

Console.Read();//enter tuşuna basana kadar açık kalır

```

```C#

Console.Write("Merhaba Dünya!");

Console.ReadLine();//enter tuşuna basana kadar açık kalır

```

```C#

Console.Write("Merhaba Dünya!");

Console.ReadKey();//bir tuşuna basana kadar açık kalır

```

### Yorum Satırları 
Şu anda veya yakın zamanda çok büyük projeler yapmicaz fakat eğer gerçekten 1.000, 1.500 satır koddan oluşan projeler yaptığınızda akşam yatıp sabah devam etmek için tekrar projnizi açtığınızda monitörle uzun uzun dakikalarca bakışmamanız için kodunuzdaki sınıfların, fonksiyonalrın, değişkenlerin nerde, ne zaman, ne için kullanıldığını yazmank için kullanabilirsiniz tabiki siz derseniz ben sınıflarımı,fonksiyonlarımı,değişkenlerimi güzel güzel kurallara uygun anlaşılır isimlendirdim kodumu okunaklı kısa öz yazdım isterseniz kullanmaya bilirsiniz size kalmış bir şey
bilgisayar yorum satırını okumaz bir kodu yorum satrı olarka yazarsanız çalışmadığını görür sünüz 
```C#

//Console.Write("Merhaba Dünya!");

//Console.ReadKey();

```
yukarıdaki örnekte olduğu gibi "//" koyarak sadece "//" koyulan satırı yorum satırı yapa bilirsiniz
ama eğer bir kaç satırı aynı anda yorum satırı yapmak isterseniz
```C#
/*
Console.Write("Merhaba Dünya!");

Console.ReadKey();//bir tuşuna basana kadar açık kalır
*/
```
yukarıdaki örnek gibi "/*" ile yorum satırının başlangıcını "*/" ilede bitişini belirleye bilirsiniz
