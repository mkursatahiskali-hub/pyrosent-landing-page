\# 🔥 Pyrosent | Ormanların Akıllı Kalkanı



> Yangınları başladığı saniyede tespit eden ve insan onayı beklemeden otonom olarak müdahale eden, \*\*Edge AI\*\* destekli aktif orman yangını koruma sistemi.



!\[Lisans](https://img.shields.io/badge/lisans-MIT-green)

!\[Node](https://img.shields.io/badge/node-%3E%3D16-brightgreen)

!\[Durum](https://img.shields.io/badge/durum-geli%C5%9Ftirme-orange)



\---



\## 📖 Pyrosent Nedir?



Geleneksel orman yangını izleme sistemleri (kameralar, uydular) sadece \*\*gözlem\*\* yapar; tespit ile fiili müdahale arasında insan onayına ve itfaiye ekiplerinin sahaya ulaşmasına bağlı, saatler sürebilen kritik bir boşluk bırakır. Bu süre zarfında küçük bir kıvılcım, büyük bir felakete dönüşebilir.



\*\*Pyrosent\*\*, bu boşluğu ortadan kaldırmak için tasarlanmış uçtan uca otonom bir sistemdir:



1\. \*\*🔍 Tespit (Termal Algılama)\*\* — Yüksek çözünürlüklü (640x512) termal sensörler, ormanlık alanı sürekli tarar ve en ufak ısı değişimini milisaniyeler içinde yakalar.

2\. \*\*🧠 Karar (Edge AI Doğrulaması)\*\* — Donanım üzerinde çalışan yapay zeka, sahte alarmları (hayvan, motor ısısı vb.) filtreleyerek 500ms'den kısa sürede yangın kararını kesinleştirir.

3\. \*\*💧 Müdahale (Aktif Söndürme)\*\* — Motorlu döner nozul sistemi devreye girer ve yerel su rezervi kullanılarak alevlere doğrudan fiziksel müdahale başlatılır.



Sonuç: \*\*tespit ile müdahale arasındaki süre, saatlerden saniyelere iner.\*\*



Sistem ayrıca elektrik şebekesi veya şehir suyu olmayan zorlu arazi koşullarında da çalışacak şekilde \*\*off-grid\*\* (solar + batarya) olarak tasarlanmıştır ve gerektiğinde merkezi kontrol odasından \*\*uzaktan iptal/devralma (override)\*\* imkanı sunar.



Bu repo, Pyrosent'in tanıtım amaçlı \*\*kurumsal web sitesini\*\* ve ziyaretçilerden iletişim talebi alan \*\*basit bir backend API'sini\*\* içerir.



\---



\## 🛠️ Teknoloji Yığını (Tech Stack)



| Katman | Teknoloji |

|---|---|

| \*\*Backend\*\* | \[Node.js](https://nodejs.org/) + \[Express](https://expressjs.com/) |

| \*\*Frontend\*\* | HTML5 + \[Tailwind CSS](https://tailwindcss.com/) (CDN üzerinden) |

| \*\*İkonlar\*\* | \[Lucide Icons](https://lucide.dev/) |

| \*\*Font\*\* | \[Inter](https://fonts.google.com/specimen/Inter) (Google Fonts) |

| \*\*Veri Depolama\*\* | Basit JSON dosyası (`gelen\_mesajlar.json`) |



\---



\## 📂 Proje Yapısı



```

pyrosent-landing-page/

├── app.js                 # Express sunucusu ve API uç noktaları

├── index.html              # Tek sayfalık tanıtım sitesi

├── package.json             # Proje bağımlılıkları ve script'leri

├── gelen\_mesajlar.json       # (Otomatik oluşur) Gelen iletişim formu mesajları

└── README.md

```



\---



\## 🚀 Kurulum (Installation)



Projeyi kendi bilgisayarınızda çalıştırmak için:



\### Gereksinimler



\- \[Node.js](https://nodejs.org/) (v16 veya üzeri önerilir)

\- npm (Node.js ile birlikte gelir)



\### Adımlar



1\. Bu repoyu klonlayın veya indirin:



&#x20;  ```bash

&#x20;  git clone https://github.com/kullanici-adi/pyrosent-landing-page.git

&#x20;  cd pyrosent-landing-page

&#x20;  ```



2\. Bağımlılıkları yükleyin:



&#x20;  ```bash

&#x20;  npm install

&#x20;  ```



3\. Sunucuyu başlatın:



&#x20;  ```bash

&#x20;  npm start

&#x20;  ```



4\. Tarayıcınızda aşağıdaki adresi açın:



&#x20;  ```

&#x20;  http://localhost:3000

&#x20;  ```



> 💡 Sunucu varsayılan olarak \*\*3000\*\* portunda çalışır. Farklı bir port kullanmak isterseniz `PORT` ortam değişkenini ayarlayabilirsiniz:

> ```bash

> PORT=5000 npm start

> ```



\### API Uç Noktası



| Metot | Yol | Açıklama |

|---|---|---|

| `GET` | `/` | Ana sayfayı (`index.html`) sunar |

| `POST` | `/api/iletisim` | İletişim formundan gelen `name`, `email`, `message` alanlarını alır, doğrular ve `gelen\_mesajlar.json` dosyasına kaydeder |



\---



\## 🤝 Katkıda Bulunma (Contributing)



Pyrosent açık kaynak bir projedir ve katkılara açıktır! Destek olmak isterseniz:



1\. Bu repoyu \*\*fork\*\*'layın.

2\. Yeni bir özellik dalı (branch) oluşturun:



&#x20;  ```bash

&#x20;  git checkout -b ozellik/yeni-ozellik-adi

&#x20;  ```



3\. Değişikliklerinizi yapın ve anlamlı bir commit mesajıyla kaydedin:



&#x20;  ```bash

&#x20;  git commit -m "Yeni özellik: ..."

&#x20;  ```



4\. Dalınızı kendi fork'unuza gönderin:



&#x20;  ```bash

&#x20;  git push origin ozellik/yeni-ozellik-adi

&#x20;  ```



5\. Ana repoya bir \*\*Pull Request\*\* açın ve değişikliklerinizi açıklayın.



\### Katkı Kuralları



\- Kod stilini mevcut dosyalarla tutarlı tutun.

\- Yeni özellikler için mümkünse açıklayıcı commit mesajları yazın.

\- Büyük değişiklikler öncesinde bir \*\*Issue\*\* açarak tartışmaya açmanız önerilir.

\- Hata bildirimleri (bug report) için lütfen adım adım nasıl tekrarlanabileceğini belirtin.



\---



\## 📄 Lisans



Bu proje \[MIT Lisansı](LICENSE) ile lisanslanmıştır.



\---



<div align="center">



\*\*Pyrosent Dev Team\*\* tarafından 🔥 ile geliştirilmektedir.



</div>

