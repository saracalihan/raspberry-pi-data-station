# MaviDurak-IO/Mentorlük Veri İstasyonu
MaviDurak-IO bünyesinde bulunan mentorlük programı için geliştirilmiş bulunduğu ortamdan veri toplayan, işleyen ve [API](https://github.com/mavidurak/mentor-api)'a HTTP istekleri gönderen bir istasyondur.Yapılan işlemler için gereken verileri, işlenen verilerin çıktılarını ve API'dan gelen geri dönütleri kendi içerisindeki veri tabanına kaydedebilir ve tekrardan okuyarak farklı işlemler yapabilir.

---

## Ne tür verileri kullanır?
Bu istasyon Raspberry Pi ile kullanılabilen tüm sensörlerle çalışabilir.Ayrıca sensöre ihtiyaç duymadan sanal olarak üretilen rastgele veya düzenli olarak veriler üretebilir.İstasyonda kullanılması planlanan veriler şu türdedir:
+ ### Sıcaklık
+ ### Nem oranı
+ ### Işık yoğunluğu
+ ### Buton(lar)a basılma durumu
+ ### Potansiyometre(ler) çevrilme durumu
+ ### İvme
+ ### Mesafe
+ ### Kızıl ötesi ışık
+ ### Joystick X, Y pozisyonları ve butonuna basılma durumu
+ ### Keyped'dan basılan tuşlar
+ ### İstasyonun işlemci sıcaklığı
* ### Rastgele yahut bir örüntü ile üretilen veriler
+ ### (Opsiyon) Görüntü işleme
+ ### (Opsiyon) Etraftaki Bluetooth veya Wifi bağlantı noktası sayısı

---

## Bu verileri kullanabilmek için hangi sensörler kullanmalıyım?
Tüm kod buradaki donanımlara göre yazılmıştır.Kodda küçük değiştirmeler yaparak kendi donanımlarınız da ekleyebilir veya mevsut donanımları muadilleri ile değiştirebilirsiniz.
+ ### DHT11 (Sıcaklık ve Nem)
+ ### 5 mm LDR(Işık Yoğunluğu)
+ ### Push Buton(Buton(lar)a basılma durumu)
+ ### 10K Potansiyometre - WH148(Potansiyometre(ler) çevrilme durumu)
+ ### ADXL345 3 Eksen İvme Ölçer(ivme)
+ ### HC-SR04 Ultrasonik Mesafe Sensörü(mesafe)
+ ### 38 kHz IR Alıcı - AA3P TK19(Kızıl ötesi ışık)
+ ### 2 Eksenli Joystick Kartı(Joystick posizyonları ve buton durumu)
+ ### 4x4 Membran Tuş Takımı(Keyped'dan basılan tuşlar)
+ ### Görüntü işleme için online cam siteleri kullanılabilir veya 
+ ### (Opsiyon) olarak belirtilen veriler için donanıma gerek yoktur çunku bu veriler için gereken donanımlar Raspberry Pi 4B içerisinde bulunur.

---

## İstasyon tarafından üretilen veriler hangi veri tipinde olabilir?
İstasyonun anlamlı veya rastgele olarak tüm veri tiplerinde örnekler üretebilir.Bunlar **intager**, **float**, **date**, **boolean**, **char**, **string**, **array** veya özel olarak belirtilebilecek bir **class** olabilir.
 
---

## Yazılım ile ilgili detaylar
Kodlama dili olarak Python kullanılmıştır.İlerleyen süreçte C/C++ dili ile de aynı kod yazılacaktır.Opsiyon olarak belirtilen koşullar koda sonradan eklenecektir.

---

## Bağlılıklar
+ ### [Python](https://www.python.org/)
+ ### [pip](https://www.python.org/)
+ ### [Python Requests](https://requests.readthedocs.io/en/master/)
+ ### [Adafruit_Python_DHT kütüphanesi](https://github.com/adafruit/Adafruit_Python_DHT)
 ...
 
 
