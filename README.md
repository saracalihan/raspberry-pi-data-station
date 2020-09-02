# MaviDurak-IO/Mentorlük Veri İstasyonu
[MaviDurak-IO](https://kommunity.com/mavidurakio) bünyesinde bulunan mentorlük programı için geliştirilmiş bulunduğu ortamdan veri toplayan, işleyen ve [API](https://github.com/mavidurak/mentor-api)'a HTTP istekleri gönderen bir istasyondur.Yapılan işlemler için gereken verileri, işlenen verilerin çıktılarını ve API'dan gelen geri dönütleri kendi içerisine kaydedebilir ve tekrardan okuyarak farklı işlemler yapabilir yahut uyarı verebilir.

## İçindekiler
- [Veriler]()
  - [Ne tür verileri kullanır?](#ne-tür-verileri-kullanır)
  - [Bu verileri kullanabilmek için hangi sensörler kullanmalıyım?](#bu-verileri-kullanabilmek-için-hangi-sensörler-kullanmalıyım)
  - [İstasyon tarafından üretilen veriler hangi veri tipinde olabilir?](#i̇stasyon-tarafından-üretilen-veriler-hangi-veri-tipinde-olabilir)
- [İndirme]()
  - [Nasıl yüklenir?](#nasıl-yüklenir)
  - [Bağımlılıklar](#bağımlılıklar)
  - [Yazılım ile ilgili detaylar](#yazılım-ile-ilgili-detaylar)
- [Donanım Bağlantıları](#donanım-bağlantıları)

## Ne tür verileri kullanır?
Bu istasyon Raspberry Pi ile kullanılabilen tüm sensörlerle çalışabilir.Ayrıca sensöre ihtiyaç duymadan sanal olarak rastgele veya anlamlı olarak veriler üretebilir.İstasyonda kullanılması planlanan veriler şu türdedir:
+ **Sıcaklık**
+ **Nem oranı**
+ **Işık şiddeti**
+ **Buton(lar)a basılma durumu**
+ **Potansiyometre(ler) çevrilme durumu**
+ **İvme**
+ **Mesafe**
+ **Kızıl ötesi ışık**
+ **Joystick X, Y pozisyonları ve butonuna basılma durumu**
+ **Keyped'den basılan tuşlar**
+ **(Dahili)İstasyonun işlemci sıcaklığı**
* **(Dahili/Opsiyon)Rastgele yahut bir örüntü ile üretilen veriler**
+ **(Dahili/Opsiyon) Görüntü işleme**
+ **(Dahili/Opsiyon) Etraftaki Bluetooth veya Wifi bağlantı noktası sayısı**


## Bu verileri kullanabilmek için hangi sensörler kullanmalıyım?
Tüm kod buradaki donanımlara göre yazılmıştır.Kodda küçük değiştirmeler yaparak kendi donanımlarınız da ekleyebilir veya mevcut donanımları muadilleri ile değiştirebilirsiniz.
+ **DHT11 (Sıcaklık ve Nem)**
+ **5 mm LDR(Işık şiddeti)**
+ **Push Buton(Buton(lar)a basılma durumu)**
+ **10K Potansiyometre - WH148(Potansiyometre(ler) çevrilme durumu)**
+ **ADXL345 3 Eksen İvme Ölçer(ivme)**
+ **HC-SR04 Ultrasonik Mesafe Sensörü(mesafe)**
+ **38 kHz IR Alıcı - AA3P TK19(Kızıl ötesi ışık)**
+ **2 Eksenli Joystick Kartı(Joystick posizyonları ve buton durumu)**
+ **4x4 Membran Tuş Takımı(Keyped'den basılan tuşlar)**
+ **Görüntü işleme için online cam siteleri kullanılabilir veya Raspberry Pi Kamera(Camera) Modülü**
+ **(Dahili) olarak belirtilen veriler için donanıma gerek yoktur çunku bu veriler için gereken donanımlar Raspberry Pi 4B ile halledilebilir.Bu özellikler en son eklenecektir.**


## İstasyon tarafından üretilen veriler hangi veri tipinde olabilir?
İstasyonun anlamlı veya rastgele olarak tüm veri tiplerinde örnekler üretebilir.Bunlar **integer**, **float**, **date**, **boolean**, **char**, **string**, **array** veya özel olarak belirtilebilecek bir **class** olabilir.
 
 ## Nasıl yüklenir?
 İndirmek için:
 ``` 
 git clone asd
 ```
 Kodu Çalıştırmak için:
 ```
 cd raspberry-pi-data-station
 python3 main.py
 ```

## Yazılım ile ilgili detaylar
Kodlama dili olarak Python kullanılmıştır.İlerleyen süreçte C/C++ dili ile de aynı kod yazılacaktır.Opsiyon olarak belirtilen koşullar koda sonradan eklenecektir.


## Bağımlılıklar
Kodun çalışabilmesi için önceden yüklü olması yerekenler.
+ **[Python](https://www.python.org/)**
+ **[pip](https://www.python.org/)**
+ **[Python Requests](https://requests.readthedocs.io/en/master/)**
+ **[Adafruit_Python_DHT kütüphanesi](https://github.com/adafruit/Adafruit_Python_DHT)**
   ### ...
 
## Donanım Bağlantıları
![baglanti.png]( "Bağlantı fritzing dosyaları ve resimleri")
