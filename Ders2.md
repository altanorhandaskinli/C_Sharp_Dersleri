### Değişken Tanımlama
Değişken tanılarken 3 kurala dikkta etmeliyiz
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
