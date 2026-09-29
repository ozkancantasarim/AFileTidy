# AFileTidy — Automatic File Organizer

Windows 10/11 için dosya türlerine göre klasörleme aracı. PSD, görsel, vektör, belge, tablo, font, Photoshop fırçası, video, ses, arşiv ve başka türleri ayırır.

## Özellikler

- İşlem öncesi dosya türü ve boyutu önizlemesi; her dosya için seçim kutusu ve Tümünü seç kontrolü
- İsteğe bağlı alt klasör taraması
- İç içe boş klasörleri alttan üste temizleme
- Aynı adlı dosyaları `(2)`, `(3)` ekleyerek koruma; üzerine yazmama
- Taşıma ve geri alma ilerlemesi
- Son işlemi geri alma; silinen boş klasörleri gerektiğinde yeniden oluşturma
- Açık/koyu tema ve Türkçe/İngilizce arayüz

Önizlemede işareti kaldırılan dosyalar taşınmaz. Tümünü seç kutusuyla liste topluca açılıp kapatılabilir. Klasör sütunundaki hedef yolun tamamı üzerine gelindiğinde görünür.

Alt klasörler seçilmezse yalnızca seçilen klasörün en üst düzeyindeki dosyalar işlenir. Alt klasörler seçilirse içerideki dosyalar ana klasörün altındaki tür klasörlerine taşınır. Bu modda ana klasördeki önceden oluşturulmuş tür klasörleri tekrar taranmaz; yeni dosyaların bulunduğu diğer klasörler taranır. Boş klasör temizliği yalnızca bu modda çalışır. Seçilen ağacın bütün alt klasörleri alttan üste kontrol edilir; iç içe boş klasörler de silinir. Dolu klasörler, bağlantı klasörleri, seçilen ana klasör ve `.Klasorleyici` kayıt klasörü korunur. Taşınacak dosya olmasa bile bu modda boş klasörleri temizlemek mümkündür. Diskin kök dizini seçilemez.

## İndir ve çalıştır

Windows 10/11 için hazır **AFileTidy.exe** dosyasını [Releases](https://github.com/ozkancantasarim/AFileTidy/releases/latest) sayfasından indirin ve çalıştırın. Kaynak kodu indirmeniz veya EXE derlemeniz gerekmez. İlk sürüm yayımlanana kadar Releases bağlantısında indirme görünmez.

Uygulama dosyaları seçtiğiniz klasör içinde düzenler. İlk kullanımda küçük bir deneme klasörüyle önizlemeyi kontrol edin. İmzalanmamış EXE dosyaları için Windows güvenlik uyarısı gösterebilir.

### Geliştiriciler için kaynak koddan derleme

Kaynak koddan EXE üretmek isteyenler Windows üzerinde `EXE_OLUSTUR.cmd` dosyasını çalıştırabilir. Sonuç `dist/AFileTidy.exe` olur. GitHub Actions da aynı derleme betiğini Windows üzerinde çalıştırır. PowerShell 5.1 ile `AFileTidy.ps1` doğrudan açılabilir.

## Geri alma ve veri güvenliği

Her işlemde seçilen klasörde `.Klasorleyici/son-islem.json` kaydı tutulur. Yeni işlem yapıldığında önceki kayıt `.Klasorleyici/gecmis` altında saklanır; önceki taşıma olduğu gibi kalır. **Son İşlemi Geri Al** yalnızca en son yapılan taşıma işlemini geri alır. Bir önceki işlemin dosyaları yeniden taşınmaz. Geri alma, başka bir dosyanın üzerine yazmaz; çakışmaları atlar. Dosyaları aynı disk ağacı içinde taşımak boş disk alanı oluşturmaz. Önemli verilerde önce küçük bir klasörde deneyin.

## Lisans

MIT. Bkz. [LICENSE](LICENSE).

## Marka

Logo `assets/AFileTidy.png` dosyasında şeffaf PNG, Windows simgesi `assets/AFileTidy.ico` dosyasındadır. Arayüzde geliştirici adı `ozkancantasarim` olarak görünür.
