# Prolab2 2. Proje

# EN AZ SAYIDA BANKNOT PARA ÜSTÜ VERME

# 1. ÖZET
“En az sayıda bankot para üstü verme ” adlı projemizde otomatik araç yıkama makinesinin minimum sayıda para üstü vererek çalışması beklenmektedir. Bunun için öncelikle Text.txt adlı dosyadan kasadaki para miktarı okunur. Yıkama makinesine kullanıcı işlem yapmak için para yüklemesi yapar. Sonrasında yapılacak işlemler seçilir. Yapılan işlemler hatasız bir şekilde gerçekleşirse para üstü verilir. Hatalı işlem yapılırsa ekranda hata mesajı gösterilir.
# 2. GİRİŞ
Projemizde text.txt uzantılı dosyadan okuma yaparak kasadaki para miktarını tutarız. Ardından kullanıcıdan işlem yapması için ‘Proteus 8’ adlı programda butonları kullandırarak işlem yaptırtırız. Kullanıcının girdiği bilgilere göre işlemler yaptırıp ekrana yazılar yazdırırız.
Kullanıcının elinde olmadan paranın kasaya sıkışması durumunda işlem iptal edilir.Kullanıcı istemesi durumunda başa dönebilir yada işlemlerini bitirebilir.


# 3. Yöntem
Program C programlama dilinde yazılmış olup,geliştirme ortamı olarak “Arduino IDE” kullanılmıştır. Simülasyon için “Proteus 8” sanal ortamı kullanılmıştır. Projemizde ilk olarak yol haritamızı çıkardık. Ardından projenin isterleri doğrultusunda araştırmalar yaptık.
##Kullandığımız fonksiyonlar :
### dosya_oku():
Bu fonksiyonda SD karttan alınan veriler kasadaki para adeti ve işlemlerin özellikleri olarak tutulur.
### reset(): 
Uygulama veya kullanıcı kaynaklı hata oluştuğunda işlem yapılan bilgilerin eski haline getirilmesinde kullanılır.
### para_yukleme():
Kullanıcıdan alınan nakit miktarı tutulur.
### islem_secimi():
Kullanıcının seçim yaptığı işlemler tutulur.

## Kullandığımız kütüphaneler:

#include <SPI.h> 

#include <SD.h>

# 4. Deneysel Sonuçlar
- Arduino kartın proteus üzerinden kullanılmasını araştırdık.
- Buton ve ledlerin kullanılmasını araştırdık.
- Dosya okuma yaparken .txt den okuma işleminde sıkıntı yaşadık. Projenin isterleri arasındaki txt okuma işlemi için araştırma yaptık.
Sonucunda Proteus ortamı üzerinde bir SD kart kullnanıp ,bu kartın içindeki txt den veri aldık.
- Para üstü verirken sıkıntılar yaşadık. Bunu çözmek için kod üzerinde bazı denemeler yaptık.


# 5. Pseudo(sözde) Kod
1- Program çalıştırıldı.

2- dosya_oku() fonksiyonu çalıştırıldı.

3- Sd kartın içinde Text.txt içindeki bilgiler alındı.

4- Kasadaki para sayısı para_adet [] adlı integer diziye aktarıldı. 

5-İşlem özellikleri hizmet isimli struct dizide tutuldu.

6-dosya_oku() fonksiyonundan çıkılır.

7-Kullanıcıdan para girişi istenir.

8- para_yukleme() fonksiyonu çağırılır.

9- Para yüklemesi yapılır ve yüklenen paralar para_yuklenen[] dizisinde tutulur. 

10-Para yükleme işlemi bitirilir ve işlem seçilmesi istenir.

11- islem_sec() fonksiyonu çağırılır.

12- İşlem özellikleri işlem_istenen[] adlı dizide tutulur hizmetin toplam adetinden düşülür.

13-Eğer seçim yanlış yapılırsa işlemler Reset butonuna basılarak iptal edilebilir.

14- Para üstü hesaplaması yapılır.

15- Kasada yeterli miktarda para olup olmadığına bakılır. 

16-Para sıkışma durumuna bakılır.

17- Hata kontrolü yapılır.

18- Eğer hata varsa uyarı mesajı yazdırılır ve işlem iptal ettirilir. 

19-Hata yoksa para üstü hesaplaması yazdırılır.

20-İsteğe bağlı reset tuşuna basılarak işlem yapılabilir.

# 6. Ekran Çıktıları

![image](https://user-images.githubusercontent.com/58952369/180403063-a665b438-9060-4614-8823-68f010e65261.png)

![image](https://user-images.githubusercontent.com/58952369/180403265-0cb4feb8-ee75-403e-8de2-5e4743a5d1ce.png)

![image](https://user-images.githubusercontent.com/58952369/180403336-e923b697-40da-43bf-8a4d-8001d66c65c1.png)

![image](https://user-images.githubusercontent.com/58952369/180403477-aeaf1ead-b55a-4545-828e-6454c30e4b67.png)

![image](https://user-images.githubusercontent.com/58952369/180403503-5b3e9dbe-be8c-4300-b9ac-615a21e1dc2c.png)

![image](https://user-images.githubusercontent.com/58952369/180403517-59482daf-c3b4-4262-8bbc-03b1418c5ebe.png)



# 7. Kaynakça

https://www.arduino.cc/en/tutorial/sketch

http://edestek2.kocaeli.edu.tr/course/view.php?id=10

https://stackoverflow.com/
