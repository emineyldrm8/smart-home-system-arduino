# smart-home-system-arduino-
smart home system arduino
# GİRİŞ
Nesnelerin ˙Interneti (IoT) uygulamalarının yaygınla¸sması
ile insanların nesneler ile olan ileti¸siminin yanı sıra
nesnelerin nesneler ile olan ileti¸simi gün geçtikçe önem
arz etmekte ve bu alandaki çalı¸smalar artmaktadır. Bu
çalı¸smalardan birisi Akıllı Ev Sistemleri’dir.Ev ortamında
gerçekle¸stirilen faaliyetleri kolayla¸stıran, güvenilir bir
ortam saglayan ve insan hayatına konfor, rahatlık veren ev ˘
otomasyonu sistemlerine Akıllı Ev denilmektedir.
Akıllı ev, ev teknolojileri endüstrinin birçok alanında
kullanılan kontrol sistemlerinin gündelik hayata uyarlanması;
ev otomasyonu ise bu teknolojilerin ki¸siye özel ihtiyaç ve
isteklerine uygulanmasıdır. Akıllı ev tanımı, bütün bu
teknolojiler sayesinde ev sakinlerinin ihtiyaçlarına cevap
verebilen, onların hayatlarını kolayla¸stıran ve daha güvenli
daha konforlu ve daha tasarruflu bir ya¸sam sunan evler
için kullanılmaktadır. Akıllı evler, otomatik fonksiyonları
ve sistemleri kullanıcı tarafından uzaktan kontrol edilebilen
cihazları içerirler.
Akıllı ev sistemlerinde bulunabilecek bazı özellikler ¸su
¸sekildedir:
• Otomatik ısı sabitleme,
• Odalarda ı¸sık kontrolü,
• Perdelerin açılıp kapanma kontrolü,
• Garaj kapısı kontrolü,
• Hırsız alarm sistemi,
• Ev ile ilgili bilgilerin telefondan otomatik alınması,
• Otomatik toprak sulama sistemi, vb
# PROJE AMACI VE ISTERLERI
Bu projenin amacı, Arduino üzerinde çalı¸san bir akıllı
ev simülasyonu yapmaktır.Projede Proteus programında
Arduino kartı kullanarak akıllı ev sistemi olu¸sturmanız
beklenmektedir. Sistem içerisinde;
• Yangın alarmı,
• Hareket algılayan ı¸sık sistemi,
• Dijital termometre,
• Kilit sistemi bulunmalıdır.
Projenin isterleri ise a¸sagıda sıralanmı¸stır: ˘
1. Arduino kartı olarak Arduino Mega kullanılmalıdır.
2. Projede yangın sensörü ve buzzer kullanılmalıdır. Yangın
tespit edildiginde alarm çalması sa ˘ glanmalıdır. ˘
3. Projede hareket sensörü ve lamba kullanılmalıdır. Hareket
tespit edildiginde lamba yanması sa ˘ glanmalıdır. ˘
4. Projede sıcaklık sensörü ve LCD ekran kullanılmalıdır.
Algılanan sıcaklıgın devamlı olarak LCD ekranda gösterilmesi saglanmalıdır. Sıcaklık 20 C’nin altına ˘
dü¸stügünde ekrana “Sıcaklık dü¸stü”, 30 C’nin üstüne ˘
çıktıgında “Sıcaklık yükseldi” yazdırılmalıdır ˘
5. Projede tus takımı (keypad), kırmızı ve yesil led
kullanılmalıdır. Keypad ile girilecek 4 haneli bir sifre
belirlenmelidir. ¸Sifre yanlıs girildiginde kırmızı, dogru
girildiginde yesil ledin yanması saglanmalıdır. 
#YÖNTEM
Projemizde Proteus 8 programını kullandık.˙I¸se
Arduino kütüphanelerini protues’a eklemekle
ba¸sladık.Kullanacagımız sensörler için ihtiyaç duydu ˘ gumuz ˘
Hareket sensörü kütüphanesini, yangın sensörü
kütüphanesini ekledik.Daha sonra kodlarımızı yazacagımız ˘
Arduino IDE’sini kurduk.Böylece bilgisayarımız projeye
hazır bir hale gelmi¸s oldu.
Ba¸slangıcı yangın sensörü ile yapmaya karar verdik.Arduino
mega 2560 kartının 2.pinine yangın sensörünü bagladık.Daha ˘
sonra sensörün içerisine yangın alarmı için indirdigimiz ˘
kütüphaneyi hex formatında yükledik.Sensörün kontrolünü
yapabilmek için kodumuzu yazdık.Pin giri¸slerini global
degi¸sken olarak belirleyip e ˘ ger yangın varsa kartın 21. ˘
pinine ekledigimiz buzzer’ın ötmesini, yangın yok ise ˘
normal i¸sleyi¸sine devam etmesini saglayacak kodları yazdık ˘
ve bu kodu aynı ¸sekilde mega 2560 kartının içerisine hex
formatında ekledik.Böylece ilk sensörümüzü gerçeklestirmis
olduk.<br></br>
![image](https://user-images.githubusercontent.com/73225797/221408013-98329d1e-c41a-4f2d-95e2-b0984a65c3e8.png)<br></br>
Yangın sensöründen sonra hareket sensörüne geçis¸ yaptık.Hareket sensörünün giris¸ini kartın 20.pinine bag˘ladık.Daha  sonra  yangın  sensöründe  de  kullandıg˘ımız logicstate’i   kullanarak   0   ve   1   deg˘erlerine   göre   hareket algılandg˘ında    transistör    yardımıyla    kartın    13.    pinine bag˘ladıg˘ımız lambanın yanmasını sag˘layacak, hareket yoksa
lambanın sönük kalmasını devam ettirecek olan kodu
yazıp kartın içerisine ekledik.1 degerinde sistem hareketin ˘
oldugunu görüp lambayı yakacaktır.0 de ˘ gerinde ise lamba ˘
herhangi bir hareket olmadıgından dolayı sönük kalmaya ˘
devam edecektir.Burada transistör yardımıyla bu yapıyı
olu¸sturduk.Böylece ikinci senösrümüzü de gerçekle¸stirmi¸s
olduk
![image](https://user-images.githubusercontent.com/73225797/221408123-a34cd655-94e3-40c1-9545-4e948e9a0b00.png)
![image](https://user-images.githubusercontent.com/73225797/221408137-9c692d8e-e525-4db4-90df-f3d7a98e0048.png)<br></br>
Hareket sensöründen sonra sıcaklık göstergesine
geçtik.Sıcaklık sensörünü kartın A0. pinine bagladık.LCD’yi ˘
ise 6-5-4-3.pinlere bagladık.Biz LCD ekranı evdeki ˘
yangın,hareket,sıcaklık bilgilerini gösterecek ¸sekilde
ayarlamayı dü¸sündük.Bu nedenle Ekranda ilk ba¸sta evin o
anki sıcaklıgı daha sonra yangın veya hareket olup olmadıgı
bilgisi gösteriliyor.Eger sıcaklık 20 derecenin altına düserse
"Sıcalık Dü¸stü ", 30 derecenin üstüne çıkarsa da "Sıcaklık yükseldi" bilgisi veriliyor.Böylece kullanıcı hem evdeki
sıcaklıgı görmüs oluyor hem de diger bilgilere bu ekran aracılığıyla ulaşmış olur.<br></br>
![image](https://user-images.githubusercontent.com/73225797/221408287-55db965a-dc78-422a-9ac0-51f9e2f0f248.png)
![image](https://user-images.githubusercontent.com/73225797/221408299-6f7b926e-2899-4a54-8010-102f0b8f74ff.png)
![image](https://user-images.githubusercontent.com/73225797/221408341-a18ab3f5-194e-443e-8555-fb64c5401554.png)
![image](https://user-images.githubusercontent.com/73225797/221408351-b14963f9-a348-4508-a36d-e8cf8b9bbcdd.png)<br></br>
Son olarak eve giris için kullanılacak olan tu¸s takımnını
karta ekledik.Tus takımı kırmızı ve yesil ledle birlikte
çalı¸smakta.Kullanıcının 3 tane giri¸s hakkı var.Kullanıcı
yanlıs sifre girerse kırmızı led yanıp ekranda "Yanlıs ¸Sifre"
bilgisi veriliyor.Kullancı dogru ¸sifre girdi ˘ ginde Yesil led 
yanıyor ve ekranda "Dogru ¸Sifre" bilgisi veriliyor.Eger
kullanıcı 3 kere yanlı¸s ¸sifre girerse ekranda "Davetsiz
Misafir" yazısı çıkıyor.

# SONUÇ
Sonuç olarak bütün sensörleri ve bu sensörleri çalı¸stırmak için kullandıgımız aletleri kartımıza ba ˘ glamı¸s oluy- ˘
oruz.Sonradan yaptıgımız düzenlemelerle birlikte ¸su sırada ˘
bir uygluma ortaya çıkmı¸s oluyor: 1-Kullanıcı eve giri¸s
yapmak için ¸sifre girer.
2-Dogru ¸sifreyi giren kullanıcı ilk önce evin o anki sıcaklık ˘
degerini görür.
3-Evde yangın olup olmadıgı bilgisini alır. ˘
4-Evde herhangi bir hareket olup olmadıgı bilgisini alır. ˘
5-Sistem üzerinde yapılan degi¸siklikler kullanıcıya LCD ˘
ekran aracılıgıyla haber verilir

# PSEUDO KOD
#include <Keypad.h><br></br>
#include <LiquidCrystal.h><br></br>
const byte ROWS = 4;<br></br>
const byte COLUMNS = 4;<br></br>
char keys[ROWS][COLUMNS] =
{
{’7’,’8’,’9’,’/’},
{’4’,’5’,’6’,’*’},
{’1’,’2’,’3’,’-’},
{’.’,’0’,’=’,’+’}
};<br></br>
byte rowPins[ROWS] = {14,15,16,17};<br></br>
byte columnPins[COLUMNS] = {10,9,8,7};<br></br>
LiquidCrystal lcd(12,11,6,5,4,3);<br></br>
String sifre = "1234";<br></br>
String girilenSifre;<br></br>
int kontrol= 0;<br></br>
int sayac = 0;<br></br>
int deneme = 0;<br></br>
int max_deneme = 3;<br></br>
int kirmiziled=18;<br></br>
int yesilled=19;<br></br>
define FlamePin 2<br></br>
int buzzer2=1;<br></br>
int sicaklikGostergesi = A0;<br></br>
int hareketSensoru = 20;<br></br>
int hareketDedektoru;<br></br>
int lamba = 21;<br></br>
void setup()<br></br>
{<br></br>
Serial.begin(9600);<br></br>
lcd.begin(16, 2);<br></br>
pinMode(kirmiziled, OUTPUT);<br></br>
pinMode(FlamePin, INPUT_PULLUP);<br></br>
digitalWrite(kirmiziled, LOW);<br></br>
Serial.println("enter password");<br></br>
lcd.print("SIFRE GIRINIZ:");<br></br>
float tempVolt;<br></br>
analogReference(INTERNAL1V1);<br></br>
pinMode(lamba, OUTPUT);<br></br>
pinMode(hareketDedektoru, INPUT);<br></br>
}<br></br>
void loop()<br></br>
{<br></br>
char anahtar = keypad.getKey();<br></br>
if (anahtar == ’=’)<br></br>
{<br></br>
Serial.println(girilenSifre);<br></br>
if ( sifre == girilenSifre )<br></br>
lcd.clear();<br></br>
lcd.println("DOGRU SIFRE");<br></br>
lcd.println("TEBRIKLER");<br></br>
digitalWrite(yesilled, HIGH); digitalWrite(yesilled, LOW); kontrol=1;<br></br>
girilenSifre = ""; sayac = 0;<br></br>
}<br></br>
else<br></br>
{<br></br>
Serial.println("YANLIS SIFRE"); deneme = deneme + 1;<br></br>
if (deneme >= max_deneme )<br></br>
{<br></br>
lcd.clear(); lcd.setCursor(0,0);<br></br>
lcd.print("DAVETSIZ MISAFIR");<br></br>
digitalWrite(kirmiziled, HIGH); digitalWrite(kirmiziled, LOW); digitalWrite(buzzer2, HIGH); digitalWrite(buzzer2, LOW); deneme = 0;<br></br>

if(kontrol == 1) sıcaklık kontrol() yangın kontrol() hareket kontrol()<br></br>

































aracılıgıyla ulasmı¸s oluyor.
