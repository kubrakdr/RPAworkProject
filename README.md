süreç çalıştığında tanımlanan bir mail adresine gelen mailleri okuyacak.
Bu maillerde istenilen formata uygun olanlar için web tarayıcısı üzerinden arama yapacak.
Arama sonuçlarını mail yollayan kişeye mail atacak. Bu işlemlerden herhangi birinde 
hata alınırsa mail yollayan kişiye atılan mail ile birlikte alınan hatayı yollayacak ve bir sonraki işleme devam edecek.

Hata Mail Formatı:
Başlık: {Mail Başlık} Hatası
İçerik: 
Merhaba,

Gönderdiğiniz mail’de hata alındı. Lütfen düzeltme yapıp tekrar gönderin.
Hata Detayı: {Hata Mesajı}

İyi çalışmalar
_________________________________________________________________________________

1. Adım:
 Sürecin mail okuma ile başlayacak. (Outlook'tan okuma olabilir)
Mail başlık’ından hangi arama motorunda arama işlemi yapılacağı belirlenecek. Varsayılan 3 (Bing, Yandex, Google) adet arama motoru üzerinde arama işlemi yapılacak.
Mail başlığı formatı “{Arama Motoru} Arama” formatında olmalıdır. Bu formata uygun değilse kayıt mail okunduya çekilecek ve bir sonraki maile geçilecek. 
Örnek: Google Arama 
Arama parametresi mail içeriğinden alınacak. Mail içeriğindeki veri belirtilen arama motorunda aranacak. Mail içeriği formatı “Arama Parametresi: {Aranacak Veri}” formatında olmalıdır. İçerik formatı uygun değilse kayıt mail okunduya çekilecek ve bir sonraki maile geçilecek. 
Örnek: Arama Parametresi: RPA

2. Adım
 Mail okuması başarılı ise belirtilen arama motorunda istenilen metin aranır ve ilk 5 satırın arama başlığı ve varsa detayı excel'e eklenerek maili atan kullanıcıya gönderilir.
 Excel Formatı: (excel adı: arama sonucu.xlsx)
 Başlık - Detay
Web sayfasını okurken oluşan her hangi bir hata gene kullanıcıya mail dönülecek
Hatasız tamamlanması durumunda excel dosyası kullanıcıya mail olarak atılacaktır.
Örnek Mail:
 Subject: {Arama Veri} Arama sonucu
 Body: 
Merhaba,
{Arama Motor} arama sonucunuz ektedir.
İyi çalışmalar

NOT: Beklenen durumlar haricinde de tüm hatalar maili atan kullanıcıya dönülmeli.
