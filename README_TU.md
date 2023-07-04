# Textractor

![How it looks](screenshot.png)

[English](README.md) ● [Español](README_ES.md) ● [简体中文](README_SC.md) ● [Русский](README_RU.md) ● [한국어](README_KR.md) ● [ภาษาไทย](README_TH.md) ● [Français](README_FR.md) ● [Italiano](README_IT.md) ● [日本語](README_JP.md) ● [Bahasa Indonesia](README_ID.md) ● [Português](README_PT.md) ● [Deutsch](README_DE.md)

**Textractor** (diğer adıyla NextHooker) Textractor (diğer adıyla NextHooker), [ITHVNR](https://web.archive.org/web/20160202084144/http://www.hongfire.com/forum/showthread.php/438331-ITHVNR-ITH-with-the-VNR-engine). tabanlı Windows 7+ (ve Wine) için açık kaynaklı bir x86/x64 video oyunu metin düzenleyicisidir.<br>
Kullanımı hakkında özet bilgi için eğitim videosunu izleyin.

## İndirme

Textractor'un resmi stabil sürümlerine [buradan](https://github.com/Artikash/Textractor/releases) ulaşabilirsiniz.<br>
ITHVNR'nin son sürümüne [buradan](https://drive.google.com/open?id=13aHF4uIXWn-3YML_k2YCDWhtGgn5-tnO) ulaşabilirsiniz.<br>
Textractor'un en son kaynaktan deneysel derlemeleri (hata ayıklama bilgileriyle birlikte) [burada](https://ci.appveyor.com/project/Artikash/textractor/history) her işin 'Artifacts' bölümünde bulunabilir.

## Özellikller

- Son derece genişletilebilir ve özelleştirilebilir
- Birçok oyun motorunu otomatik bağlama (VNR desteği olmayanlar da dahil!)
- Metni /H "bağlama" kodlarını kullanarak bağlar (çoğu AGTH kodu desteklenir)
- Olası bağlantı kodlarını otomatik arama

## Destek

Hataları, Textractor'un bağlanmakta sorun yaşadığı oyunları, özellik istekleri veya diğer önerilerinizi bana bildirin.<br>
Bağlamakta sorun yaşadığınız oyun varsa, lütfen bana oyunu [Steam](https://steamcommunity.com/profiles/76561198097566313/) üzerinden ücretsiz olarak indirmenin veya hediye etmenin bir yolunu gösterin.

## Uzantılar

Uzantının nasıl oluşturulacağını öğrenmek için [Örnek Uzantı projesi](https://github.com/Artikash/ExampleExtension) adresime bakın.<br>
Uzantı ile yapılabileceklere ilişkin örnekler için uzantılar klasörüne bakın. 

## Katkıda Bulunma

Tüm katkılar takdirle karşılanmaktadır! Kod tabanı hakkında sorularınız varsa akashmozumdar@gmail.com adresinden e-posta gönderebilirsiniz.<br>
Standart istek yapma sürecini kullanmalısınız ( fork, branch, değişiklik yapma, kendi branch'inizden master'ıma PR yapma).<br>
Çeviriye katkıda bulunmak kolaydır: [text.cpp](text.cpp) çevirmeniz gereken tüm metin dizelerini içerir. BENİ OKU veya öğretici video transkriptinin çevirilerini de bekleriz.

## Derleme

Textractor'u derlemeden önce Qt sürüm 5.13'e ve CMake destekli Visual Studio'ya ihtiyacınız var.
Textractor'un kaynağını klonlayıp `git clone https://github.com/Artikash/Textractor.git` ve `git submodule update --init` ile alt modülleri başlatın.
Daha sonra Visual Studio'da kaynak klasörünü açıp derleyebilmeniz gerekir.

## Proje Mimarisi

Ana bilgisayar texthook'u hedef işleme enjekte eder ve 2 boru dosyası aracılığıyla bağlanır.
texthook borunun bağlanmasını bekler, ardından metin çıktısı veren işlevlere (örn. TextOut, GetGlyphOutline) girdilerinin boru ile iletilmesine yardımcı olacak birkaç talimat enjekte eder.<br>
Hook'larla ilgili ek bilgiler, paylaşılan bellek üzerinden değiş tokuş edilir.<br>
Ana bilgisayarın boru yoluyla aldığı metin, GUI'ye geri gönderilmeden önce biraz işlenir.<br>
Son olarak, GUI metni görüntülemeden önce uzantılara gönderir.

## [Geliştiriciler](docs/CREDITS.md)
