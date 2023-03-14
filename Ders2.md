### Değişken tanımlama
değişken tanılarken 3 kurala dikkta etmeliyiz
1. kesinlikle ama kesinlikle değişkenin adının başına rakam gelemez isnisna yok "1isim" gibi fakat "isim1" veya "i1sim" gibi tanımlanan değişkenler bir sorun yaratmaz
2. kesinlikle özel karakter kullanmıyoruz (/,-,*,+,-,%,&,! gibi virgül ve boşluk dahil) tek bir isnisna var izin verilen tel özel karakter alt çizgidir istediğiniz gibi kullana biliriniz "_denem", "de_neme", "deneme_" gibi
3. türkçe karakterler kullanmayın kodunuz çalışacaktır ama kesinmlikle tavsiye etmiyorum (ü,ğ,ç,ö,ş,ı gibi) "üzüm" yerine "uzum" yazarsanız daha sağlıklı olur
4. daha önceden aynı blok içerisinde kullanılan (farklıo veri tiplerinde olsa bile) bir değişken varsa aynı değişkeni tekrar tanımlayamazsınız 
```C#
int a1; // sorun yok
int 1a; //1.kural hatası
string de neme; //2.kural hatası
string bolme/islemi; //2.kural hatası
int a_sayisi; // sorun yok
int a_sayısı; //3.kural hatası
string a1; //4.kural hatası

