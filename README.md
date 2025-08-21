# Manga & Art Basics Club

Next.js App Router + TypeScript + Supabase tabanlı bir **manga & sanat temel kulübü** resmi web sitesi.

## 🎨 Özellikler

### 🏠 Ana Sayfa
- Kulüp başlığı ve adres bilgisi  
- Üç ana buton: **Eğitimler**, **Yarışmalar**, **Ödev Teslimi**  
- 16:9 afiş alanı  

### 📚 Eğitimler Sayfası
- Dört kategori: **Dijital Sanat**, **Hızlı Karalama**, **Eskiz**, **Renk**  
- Öğretmenler video yükleyebilir  
- Öğrenciler ödev gönderebilir  
- Video oynatma ve dosya yükleme desteği  

### 🏆 Yarışmalar Sayfası
- Yayınlanan yarışmalar listesi  
- Admin & öğretmen yarışma oluşturabilir/düzenleyebilir  
- Ödül ayarları ve yayın durumu yönetimi  

### 👥 Hakkında Sayfası
- Kulüp tanıtım metni  
- Tüm öğretmenler ve adminler listelenir  
- Admin öğretmen isimlerini çevrimiçi düzenleyebilir  

### 🔐 Kimlik Doğrulama
- E-posta & şifre ile kayıt/giriş  
- Magic link ile giriş  
- Rol tabanlı yetkilendirme (**admin/staff/student**)  

### 🛠️ Yönetim Paneli
- Kullanıcı rol yönetimi  
- Eğitim içerik yönetimi  
- Yarışma oluşturma & düzenleme  
- Ödev değerlendirme ve geri bildirim  
- Dosya indirme yönetimi  

---

## ⚙️ Teknoloji Yığını

- **Frontend**: Next.js 15 + TypeScript + Tailwind CSS  
- **Backend**: Supabase (Auth + Database + Storage)  
- **UI**: Radix UI + shadcn/ui  
- **Durum Yönetimi**: React Hooks  
- **Kimlik Doğrulama**: Supabase Auth  
- **Veritabanı**: PostgreSQL + RLS  
- **Dosya Depolama**: Supabase Storage  

---

## 🚀 Hızlı Başlangıç

### 1. Projeyi klonla
```bash
git clone <repository-url>
cd manga-art-club

2. Bağımlılıkları yükle

npm install

3. Ortam değişkenlerini ayarla

.env.example dosyasını .env.local olarak kopyala ve düzenle:

cp env.example .env.local

.env.local içeriği:

NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key
NEXT_PUBLIC_SITE_URL=http://localhost:3000

4. Veritabanı kurulum

Supabase üzerinde şu SQL scriptlerini çalıştır:

1. supabase/schema.sql → tablolar & RLS


2. supabase/storage-policies.sql → depolama politikaları



5. Geliştirme sunucusunu başlat

npm run dev

Sonra http://localhost:3000 adresini ziyaret et.


---

📂 Proje Yapısı

manga-art-club/
├── app/                    # Next.js App Router sayfaları
│   ├── admin/             # Yönetim paneli
│   ├── auth/              # Giriş/Kayıt
│   ├── about/             # Hakkında
│   ├── competitions/      # Yarışmalar
│   ├── tutorials/         # Eğitimler
│   ├── profile/           # Profil
│   └── page.tsx           # Ana sayfa
├── components/             # React bileşenleri
│   ├── ui/                # UI temel bileşenler
│   ├── auth-form.tsx      # Giriş/Kayıt formu
│   └── navbar.tsx         # Navigasyon
├── lib/                    # Yardımcı fonksiyonlar
│   ├── supabase/          # Supabase ayarları
│   └── types.ts           # TypeScript tipleri
├── supabase/               # Veritabanı scriptleri
│   ├── schema.sql         # Tablo yapıları
│   └── storage-policies.sql # Depolama politikaları
└── middleware.ts           # Middleware


---

🗄️ Veritabanı Tasarımı

Ana tablolar

profiles → Kullanıcı profili & rol

tutorials → Eğitim içerikleri

competitions → Yarışmalar

submissions → Ödev teslimleri

reviews → Ödev değerlendirmeleri


Rol tabanlı izinler

Öğrenci: İçerik görüntüleme, ödev teslim etme

Öğretmen: Eğitim yükleme, ödev değerlendirme

Admin: Tüm erişimler



---

☁️ Dağıtım

Vercel ile dağıtım

1. GitHub repo → Vercel bağla


2. Ortam değişkenlerini ekle


3. Deploy et



Diğer platformlar

Next.js destekleyen tüm platformlarda çalışır.


---

🛠️ Geliştirme Rehberi

Yeni özellik eklemek

1. lib/types.ts → yeni tip tanımla


2. Yeni sayfa/component oluştur


3. Navigasyon ve yetkilendirmeyi güncelle



Stil değiştirme

Tailwind CSS kullanılıyor → sınıf tabanlı stil

Veritabanı değişikliği

1. supabase/schema.sql dosyasını düzenle


2. Supabase üzerinde çalıştır


3. İlgili TypeScript tiplerini güncelle




---

🤝 Katkıda Bulunma

Issue ve Pull Request gönderebilirsiniz!


---

📜 Lisans

MIT License

İstersen sana bir de **görsel proje yapısı diyagramı** veya **Türkçe veri tabanı ER diyagramı** hazırlayabilirim, ister misin?

  
