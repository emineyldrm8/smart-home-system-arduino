# smart-home-system-arduino-
smart home system arduino
# GİRİŞ
Nesnelerin ˙Interneti (IoT) uygulamalarının yaygınlaşması
ile insanların nesneler ile olan iletişiminin yanı sıra
nesnelerin nesneler ile olan iletişimi gün geçtikçe önem
arz etmekte ve bu alandaki çalışmalar artmaktadır. Bu
çalışmalardan birisi Akıllı Ev Sistemleri’dir.Ev ortamında
gerçekleştirilen faaliyetleri kolaylaştıran, güvenilir bir
ortam saglayan ve insan hayatına konfor, rahatlık veren ev
otomasyonu sistemlerine Akıllı Ev denilmektedir.
Akıllı ev, ev teknolojileri endüstrinin birçok alanında
kullanılan kontrol sistemlerinin gündelik hayata uyarlanması;
ev otomasyonu ise bu teknolojilerin kişiye özel ihtiyaç ve
isteklerine uygulanmasıdır. Akıllı ev tanımı, bütün bu
teknolojiler sayesinde ev sakinlerinin ihtiyaçlarına cevap
verebilen, onların hayatlarını kolaylaştıran ve daha güvenli
daha konforlu ve daha tasarruflu bir yaşam sunan evler
için kullanılmaktadır. Akıllı evler, otomatik fonksiyonları
ve sistemleri kullanıcı tarafından uzaktan kontrol edilebilen
cihazları içerirler.
Akıllı ev sistemlerinde bulunabilecek bazı özellikler şu
şekildedir:<br></br>
• Otomatik ısı sabitleme,<br></br>
• Odalarda ı¸sık kontrolü,<br></br>
• Perdelerin açılıp kapanma kontrolü,<br></br>
• Garaj kapısı kontrolü,<br></br>
• Hırsız alarm sistemi,<br></br>
• Ev ile ilgili bilgilerin telefondan otomatik alınması,<br></br>
• Otomatik toprak sulama sistemi, vb
# PROJE AMACI VE İSTERLERİ
Bu projenin amacı, Arduino üzerinde çalışan bir akıllı
ev simülasyonu yapmaktır.Projede Proteus programında
Arduino kartı kullanarak akıllı ev sistemi oluşturmanız
beklenmektedir. Sistem içerisinde;<br></br>
• Yangın alarmı,<br></br>
• Hareket algılayan ı¸sık sistemi,<br></br>
• Dijital termometre,<br></br>
• Kilit sistemi bulunmalıdır.<br></br>
Projenin isterleri ise aşagıda sıralanmıştır:<br></br>
1. Arduino kartı olarak Arduino Mega kullanılmalıdır.<br></br>
2. Projede yangın sensörü ve buzzer kullanılmalıdır. Yangın tespit edildiginde alarm çalması sağlanmalıdır.<br></br>
3. Projede hareket sensörü ve lamba kullanılmalıdır. Hareket tespit edildiginde lamba yanması sağlanmalıdır.<br></br>
4. Projede sıcaklık sensörü ve LCD ekran kullanılmalıdır.<br></br>
Algılanan sıcaklıgın devamlı olarak LCD ekranda gösterilmesi saglanmalıdır. Sıcaklık 20 C’nin altına düştügünde ekrana “Sıcaklık düştü”, 30 C’nin üstüne
çıktıgında “Sıcaklık yükseldi” yazdırılmalıdır.<br></br>
5. Projede tus takımı (keypad), kırmızı ve yesil led
kullanılmalıdır. Keypad ile girilecek 4 haneli bir sifre
belirlenmelidir.Şifre yanlıs girildiginde kırmızı, doğru
girildiginde yeşil ledin yanması saglanmalıdır. 
# YÖNTEM
Projem için Proteus 8 programını kullandım.İşe
Arduino kütüphanelerini Protues’a eklemekle
başladım.Kullanacağım sensörler için ihtiyaç duyduğum
hareket sensörü kütüphanesini, yangın sensörü
kütüphanesini ekledim.Daha sonra kodları yazacağım
Arduino IDE’sini kurdum.Böylece bilgisayarım projeye
hazır bir hale gelmiş oldu.
Başlangıcı yangın sensörü ile yapmaya karar verdim.Arduino
Mega 2560 kartının 2.pinine yangın sensörünü bagladım.Daha
sonra sensörün içerisine yangın alarmı için indirdigimiz 
kütüphaneyi hex formatında yükledim.Sensörün kontrolünü
yapabilmek için kodumuzu yazdım.Pin girişlerini global
degişken olarak belirleyip eğer yangın varsa kartın 21. 
pinine eklediğim buzzerın ötmesini, yangın yok ise
normal işleyişine devam etmesini sağlayacak kodları yazdım
ve bu kodu aynı şekilde   Mega 2560 kartının içerisine hex
formatında ekledim.Böylece ilk sensörü gerçeklestirmiş
oldum.<br></br>
![image](https://user-images.githubusercontent.com/73225797/221408013-98329d1e-c41a-4f2d-95e2-b0984a65c3e8.png)<br></br>
Yangın sensöründen sonra hareket sensörüne geçiş yaptım.Hareket sensörünün girişini kartın 20.pinine bağladım.Daha  sonra  yangın  sensöründe  de  kullandığım logicstate’i   kullanarak   0   ve   1   değerlerine   göre   hareket algılandığında    transistör    yardımıyla    kartın    13.    pinine bağladığımız lambanın yanmasını sağlayacak, hareket yoksa
lambanın sönük kalmasını devam ettirecek olan kodu
yazıp kartın içerisine ekledim.1 değerinde sistem hareketin 
olduğunu görüp lambayı yakacaktır.0 değerinde ise lamba
herhangi bir hareket olmadığından dolayı sönük kalmaya 
devam edecektir.Burada transistör yardımıyla bu yapıyı
oluşturdum.Böylece ikinci sensörü de gerçekleştirmiş
oldum.
![image](https://user-images.githubusercontent.com/73225797/221408123-a34cd655-94e3-40c1-9545-4e948e9a0b00.png)
![image](https://user-images.githubusercontent.com/73225797/221408137-9c692d8e-e525-4db4-90df-f3d7a98e0048.png)<br></br>
Hareket sensöründen sonra sıcaklık göstergesine
geçtim.Sıcaklık sensörünü kartın A0. pinine bagladım.LCD’yi 
ise 6-5-4-3.pinlere bağladım.Biz LCD ekranı evdeki 
yangın,hareket,sıcaklık bilgilerini gösterecek şekilde
ayarlamayı düşündüm.Bu nedenle Ekranda ilk başta evin o
anki sıcaklığı daha sonra yangın veya hareket olup olmadığı
bilgisi gösteriliyor.Eğer sıcaklık 20 derecenin altına düşerse
"Sıcalık Düştü ", 30 derecenin üstüne çıkarsa da "Sıcaklık yükseldi" bilgisi veriliyor.Böylece kullanıcı hem evdeki
sıcaklığı görmüs oluyor hem de diger bilgilere bu ekran aracılığıyla ulaşmış olur.<br></br>
![image](https://user-images.githubusercontent.com/73225797/221408287-55db965a-dc78-422a-9ac0-51f9e2f0f248.png)
![image](https://user-images.githubusercontent.com/73225797/221408299-6f7b926e-2899-4a54-8010-102f0b8f74ff.png)
![image](https://user-images.githubusercontent.com/73225797/221408341-a18ab3f5-194e-443e-8555-fb64c5401554.png)
![image](https://user-images.githubusercontent.com/73225797/221408351-b14963f9-a348-4508-a36d-e8cf8b9bbcdd.png)<br></br>
Son olarak eve giriş için kullanılacak olan tuş takımını
karta ekledim.Tuş takımı kırmızı ve yeşil ledle birlikte
çalışmakta.Kullanıcının 3 tane giriş hakkı var.Kullanıcı
yanlış şifre girerse kırmızı led yanıp ekranda "Yanlış Şifre"
bilgisi veriliyor.Kullanıcı dogru şifre girdiğinde Yeşil Led 
yanıyor ve ekranda "Doğru Şifre" bilgisi veriliyor.Eger
kullanıcı 3 kere yanlış ¸şifre girerse ekranda "Davetsiz
Misafir" yazısı çıkıyor.

# SONUÇ
Sonuç olarak bütün sensörleri ve bu sensörleri çalıştırmak için kullandığımız aletleri kartımıza bağlamış oluyoruz.Sonradan yaptıgımız düzenlemelerle birlikte şu
sırada 
bir uygluma ortaya çıkmış oluyor: 
1-Kullanıcı eve giriş yapmak için sifre girer.<br></br>
2-Dogru şifreyi giren kullanıcı ilk önce evin o anki sıcaklık
değerini görür.<br></br>
3-Evde yangın olup olmadığı bilgisini alır.<br></br>
4-Evde herhangi bir hareket olup olmadığı bilgisini alır. <br></br>
5-Sistem üzerinde yapılan değişiklikler kullanıcıya LCD ekran aracılıgıyla haber verilir.<br></br>

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
