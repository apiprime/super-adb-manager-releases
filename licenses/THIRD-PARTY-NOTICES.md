# Üçüncü Taraf Bileşenler ve Lisanslar
# Third-Party Components and Licenses

**Super ADB Manager** — ApiPrime® Software Technologies

Super ADB Manager, aşağıdaki açık kaynaklı bileşenleri **değiştirilmemiş hâlde**
uygulama paketi (`.app`) içinde dağıtır. Her bileşen kendi lisansı altındadır.
Bu dosya, o lisansların gerektirdiği atıf ve bilgilendirme yükümlülüğünü yerine getirir.

Super ADB Manager'ın kendi kaynak kodu ApiPrime® Software Technologies'e aittir ve
bu bileşenlerden bağımsızdır: uygulamanın kendi ikili dosyası (`scrcpySC`) aşağıdaki
GPL/LGPL lisanslı kitaplıklara bağlanmaz (link etmez); bu kitaplıklar yalnızca
uygulamayla birlikte dağıtılan bağımsız programların (`scrcpy`, `samtp`) çalışması
için pakette bulunur.

---

## Bileşenler

| Bileşen | Sürüm | Lisans | Kaynak |
|---------|-------|--------|--------|
| **scrcpy** (+ `scrcpy-server`) | 3.3.4 | Apache-2.0 | https://github.com/Genymobile/scrcpy |
| **adb** (Android Debug Bridge, AOSP) | 1.0.41 | Apache-2.0 | https://android.googlesource.com/platform/packages/modules/adb |
| **FFmpeg** (`libavcodec`, `libavformat`, `libavutil`, `libswresample`) | 8.x | **GPL-2.0-or-later** (GPL yapılandırmasıyla derlenmiştir) | https://ffmpeg.org/download.html · https://git.ffmpeg.org/ffmpeg.git |
| **x264** | 165 | **GPL-2.0-or-later** | https://www.videolan.org/developers/x264.html |
| **x265** | 216 | **GPL-2.0-or-later** | https://bitbucket.org/multicoreware/x265_git |
| **LAME** (`libmp3lame`) | 3.100 | LGPL-2.1-or-later | https://lame.sourceforge.io/ |
| **libusb** | 1.0 | LGPL-2.1-or-later | https://libusb.info/ |
| **libmtp** | 1.1.23 | LGPL-2.1-or-later | https://libmtp.sourceforge.net/ |
| **SDL2** | 2.x | Zlib | https://www.libsdl.org/ |
| **dav1d** | 1.x | BSD-2-Clause | https://code.videolan.org/videolan/dav1d |
| **libvpx** | 1.x | BSD-3-Clause | https://chromium.googlesource.com/webm/libvpx |
| **Opus** | 1.x | BSD-3-Clause | https://opus-codec.org/ |
| **SVT-AV1** (`libSvtAv1Enc`) | 4.1.0 | BSD-3-Clause-Clear + AOM Patent License 1.0 | https://gitlab.com/AOMediaCodec/SVT-AV1 |
| **OpenSSL** (`libcrypto`, `libssl`) | 3.x | Apache-2.0 | https://www.openssl.org/source/ |

Lisans tam metinleri bu klasördedir:
`GPL-2.0.txt` · `LGPL-2.1.txt` · `Apache-2.0.txt`

BSD-2-Clause, BSD-3-Clause ve Zlib lisanslı bileşenler için lisans metni ilgili
projenin yukarıdaki kaynak adresinde yer alır ve telif hakkı bildirimleri korunmuştur.

---

## GPL / LGPL — Kaynak Kodu Teklifi (Written Offer)

FFmpeg, x264 ve x265 bileşenleri **GPL-2.0-or-later**; LAME, libusb ve libmtp
bileşenleri **LGPL-2.1-or-later** lisanslıdır. Bu lisanslar, ikili (binary) dağıtımla
birlikte ilgili kaynak koda erişim sağlanmasını gerektirir.

Bu bileşenler **hiçbir değişiklik yapılmadan**, Homebrew (https://brew.sh) üzerinden
derlenmiş hâlleriyle dağıtılmaktadır. Karşılık gelen kaynak kodlarına yukarıdaki
tabloda verilen resmî adreslerden ulaşabilirsiniz.

Ayrıca **GPL-2.0 §3(b) ve LGPL-2.1 §6 uyarınca**: bu dağıtımı aldığınız tarihten
itibaren **en az üç yıl boyunca**, bu bileşenlerin dağıtılan sürümlerine karşılık
gelen tam kaynak kodunu, yalnızca fiziksel dağıtım maliyetini karşılayacak bir ücret
karşılığında (ya da tercih ederseniz elektronik olarak ücretsiz) size iletmeyi
teklif ediyoruz.

**Talep için:** info@apiprime.com — konu satırına "Super ADB Manager — GPL source request"
yazmanız ve uygulama sürümünü belirtmeniz yeterlidir.

---

## Notlar

- LGPL lisanslı kitaplıklar dinamik olarak (`.dylib`) bağlanır ve
  `Contents/Resources/libs/` klasöründe ayrı dosyalar hâlinde bulunur; bu sayede
  LGPL-2.1 §6'nın gerektirdiği şekilde değiştirilmiş sürümlerle değiştirilebilirler.
- `samtp`, Super ADB Manager'ın MTP desteği için yazdığı küçük bir yardımcı programdır;
  libmtp (LGPL-2.1+) kitaplığını dinamik olarak kullanır.
- Android, Google LLC'nin tescilli markasıdır. Bu uygulama Google ile
  bağlantılı değildir ve Google tarafından desteklenmemektedir.
