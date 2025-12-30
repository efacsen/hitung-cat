# HitungCat.com - Product Vision Document

## Ringkasan Eksekutif

**HitungCat.com** adalah aplikasi web gratis yang membantu masyarakat Indonesia menghitung kebutuhan cat secara akurat untuk proyek renovasi rumah. Aplikasi ini menjembatani kesenjangan pengetahuan antara pemilik rumah dan dunia konstruksi, mencegah pemborosan material, dan membangun kepercayaan dalam proses renovasi.

---

## 1. Masalah yang Diselesaikan

### 1.1 Knowledge Gap (Kesenjangan Pengetahuan)

Mayoritas pemilik rumah di Indonesia tidak memiliki pengetahuan dasar tentang material bangunan:

| Masalah | Dampak |
|---------|--------|
| **Tidak tahu daya sebar cat** | 1 Liter cat ≈ 10m² adalah pengetahuan yang jarang dimiliki orang awam |
| **Bingung dengan satuan** | "Galon" (2.5L/5kg) vs "Pail" (20L/25kg) membingungkan |
| **Tidak bisa menghitung luas** | Menghitung m² tembok dikurangi pintu/jendela butuh matematika |

### 1.2 Trust Deficit (Defisit Kepercayaan)

```
Pemilik Rumah ←──[TIDAK PERCAYA]──→ Tukang/Mandor
```

- Pemilik rumah takut di-"mark up" dalam daftar material
- Tukang/Mandor tidak punya alat untuk membuktikan transparansi
- Tidak ada pihak netral yang bisa jadi rujukan

### 1.3 Kesalahan Aplikasi

| Kesalahan Umum | Konsekuensi |
|----------------|-------------|
| Cat langsung di acian baru tanpa primer | Cat mengelupas dalam 6-12 bulan |
| Cat biasa di tembok lembab | Jamur dan cat terkelupas |
| Beli cat terlalu sedikit | Pekerjaan terhenti, warna beda batch |
| Beli cat terlalu banyak | Uang terbuang, limbah kimia |

---

## 2. Solusi: HitungCat.com

### 2.1 Konsep Inti

> **"Dari ukuran ruangan → langsung tahu harus beli apa"**

Bukan hanya menampilkan "Anda butuh 13.5 Liter" (yang membingungkan), tapi langsung memberikan **daftar belanja** yang actionable:

```
┌─────────────────────────────────────────┐
│  HASIL PERHITUNGAN                      │
│                                         │
│  Untuk ruangan 4m x 5m x 3m, Anda perlu:│
│                                         │
│  ✓ Cat Dasar (Primer)                   │
│    → 1 Galon (2.5L) Alkali Primer       │
│                                         │
│  ✓ Cat Finish (2 lapis)                 │
│    → 1 Pail (20L) + 1 Galon (2.5L)      │
│                                         │
│  [📱 Kirim ke WA Toko]                  │
└─────────────────────────────────────────┘
```

### 2.2 Fitur Utama

#### A. Kalkulator Cerdas
- Input sederhana: Panjang × Lebar × Tinggi ruangan
- Otomatis kurangi area pintu & jendela standar
- Pilihan kondisi tembok (baru/lama/lembab)
- Hasil dalam format kemasan yang dijual di toko

#### B. Rekomendasi Kontekstual
- Tembok acian baru → Rekomendasikan primer
- Tembok lembab → Rekomendasikan cat anti bocor
- Ganti warna gelap ke terang → Rekomendasikan cat dasar putih

#### C. Mode Pengguna
| Mode | Target User | Wastage Buffer |
|------|-------------|----------------|
| **Mode Hemat** | DIY / Pemilik rumah yang mengawasi | 5% |
| **Mode Mandor** | Kontraktor / Borongan | 15-20% |

#### D. Integrasi WhatsApp
Tombol "Kirim ke WA Toko" menghasilkan pesan siap kirim:
```
Pak, saya mau beli:
- 1 Pail Dulux Catylac Putih
- 1 Galon Alkali Primer
Ada stok? Bisa diantar ke [alamat]?
```

---

## 3. Target Pengguna

### 3.1 Persona Primer: Pemilik Rumah DIY

**"Pak Budi" (35-50 tahun)**
- Baru beli rumah atau mau renovasi
- Ingin hemat dengan cat sendiri atau awasi tukang
- Googling: *"cara hitung kebutuhan cat tembok"*
- Pain point: Takut beli kebanyakan/kekurangan

**Value Proposition:**
> *"Berhenti menebak. Berhenti buang uang untuk sisa cat. Beli tepat sesuai kebutuhan dalam hitungan detik."*

### 3.2 Persona Sekunder: Mandor/Kontraktor Kecil

**"Pak Joko" (30-45 tahun)**
- Handle 2-5 proyek renovasi per bulan
- Butuh buat RAB cepat dan transparan
- Pain point: Klien sering curiga dengan daftar material

**Value Proposition:**
> *"Tampil profesional di depan klien. Buat daftar material instan yang transparan dan membangun kepercayaan."*

### 3.3 Persona Tersier: Toko Bangunan

**"Toko Bangunan Makmur Jaya"**
- Ingin traffic dan customer baru
- Pain point: Bersaing dengan marketplace online

**Value Proposition:**
> *"Dapat leads berkualitas dari customer yang sudah tahu mau beli apa."*

---

## 4. Diferensiasi Kompetitif

### 4.1 Kenapa Bukan Google/Kalkulator Biasa?

| Solusi Existing | Masalah |
|-----------------|---------|
| Google "rumus cat tembok" | Harus hitung manual, tidak ada konteks Indonesia |
| Kalkulator di website cat | Bias ke produk sendiri, tidak netral |
| Tanya tukang | Trust issue, mungkin di-markup |
| Kalkulator generik | Tidak paham format "Galon/Pail" Indonesia |

### 4.2 Keunggulan HitungCat.com

1. **Netral** - Tidak terafiliasi dengan brand cat tertentu
2. **Lokal** - Paham format kemasan Indonesia (Galon 2.5L, Pail 20L)
3. **Kontekstual** - Tahu kondisi tembok Indonesia (acian, lembab, dll)
4. **Actionable** - Output = daftar belanja, bukan angka abstrak
5. **Mobile-First** - Didesain untuk HP dengan koneksi 4G

---

## 5. Model Bisnis

### 5.1 Revenue Streams

```
┌─────────────────────────────────────────────────────────┐
│                    REVENUE MODEL                        │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  FASE 1: TRAFFIC & TRUST (Tahun 1)                     │
│  └─ Fokus: SEO, user acquisition, data collection      │
│  └─ Revenue: Minimal (Google AdSense)                  │
│                                                         │
│  FASE 2: MONETIZATION (Tahun 2+)                       │
│  ├─ Affiliate Tokopedia/Shopee (5-10% komisi)          │
│  ├─ Partnership Toko Bangunan (listing fee)            │
│  ├─ Brand Partnership (featured recommendation)        │
│  └─ Premium Features (PDF report, multi-room)          │
│                                                         │
│  FASE 3: ECOSYSTEM (Tahun 3+)                          │
│  ├─ Marketplace "Bursa Sisa Cat"                       │
│  ├─ Lead generation untuk kontraktor                   │
│  └─ Data insights untuk brand cat                      │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

### 5.2 Strategi Akuisisi User

#### A. SEO (Organik)
Target keywords:
- "cara hitung cat tembok" (high intent)
- "1 galon cat untuk berapa meter" (informational)
- "rumus kebutuhan cat dinding" (transactional)
- "kalkulator cat gratis" (direct)

#### B. Hyper-Local SEO
Landing pages programmatic:
- `/kalkulator-cat-jakarta`
- `/toko-cat-bandung`
- `/hitung-cat-surabaya`

#### C. WhatsApp Virality
Setiap user yang share ke toko = eksposur gratis ke pemilik toko

---

## 6. Fitur Roadmap

### MVP (Minimum Viable Product)

| Fitur | Prioritas | Status |
|-------|-----------|--------|
| Kalkulator 1 ruangan | P0 | 🔲 Planned |
| Input: P × L × T | P0 | 🔲 Planned |
| Pilihan kondisi tembok | P0 | 🔲 Planned |
| Output: Galon/Pail | P0 | 🔲 Planned |
| Rekomendasi primer | P0 | 🔲 Planned |
| Mode Hemat/Mandor | P1 | 🔲 Planned |
| Tombol WA Share | P1 | 🔲 Planned |
| Mobile responsive | P0 | 🔲 Planned |

### Post-MVP

| Fitur | Prioritas | Deskripsi |
|-------|-----------|-----------|
| Multi-room calculator | P2 | Hitung seluruh rumah sekaligus |
| Estimasi harga | P2 | Integrasi harga real-time |
| PDF Report | P2 | Download RAB untuk klien |
| Bursa Sisa Cat | P3 | Marketplace cat bekas |
| Direktori Toko | P3 | Database toko bangunan lokal |
| Account system | P3 | Simpan history perhitungan |

### User Account & Saved Calculations

Fitur login untuk menyimpan history perhitungan dan data proyek.

```
┌─────────────────────────────────────────────────────────────────┐
│                    USER ACCOUNT BENEFITS                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  👤 UNTUK PEMILIK RUMAH                                         │
│  ├─ Simpan perhitungan untuk dibandingkan nanti                │
│  ├─ Track progress renovasi per ruangan                        │
│  ├─ Akses history dari device manapun                          │
│  └─ Tidak perlu hitung ulang jika lupa                         │
│                                                                 │
│  👷 UNTUK MANDOR/KONTRAKTOR                                     │
│  ├─ Simpan RAB per klien/proyek                                │
│  ├─ Duplicate & modify perhitungan sebelumnya                  │
│  ├─ Professional portfolio of past projects                    │
│  └─ Quick reference untuk estimasi proyek baru                 │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

#### Login Options (Prioritas)

| Method | Effort | User Base di Indonesia | Priority |
|--------|--------|------------------------|----------|
| **Google OAuth** | Low | 150+ juta users | P0 |
| **WhatsApp OTP** | Medium | 112+ juta users | P0 |
| **TikTok OAuth** | Medium | 125+ juta users (growing fast) | P1 |
| **Facebook OAuth** | Low | 119+ juta users | P1 |
| **Instagram OAuth** | Low | 89+ juta users | P2 |
| **Twitter/X OAuth** | Low | 24+ juta users | P3 |
| Email + Password | Medium | Fallback option | P3 |

```
┌─────────────────────────────────────────────────────────────────┐
│                    SOCIAL LOGIN STRATEGY                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  🎯 TARGET DEMOGRAPHIC → LOGIN PREFERENCE                       │
│                                                                 │
│  Gen Z (18-25)        →  TikTok, Instagram                     │
│  Millennials (26-40)  →  Google, WhatsApp, Facebook            │
│  Gen X (40+)          →  WhatsApp, Google                      │
│                                                                 │
│  📱 MOBILE-FIRST PRIORITY                                       │
│  WhatsApp & TikTok = highest mobile engagement di Indonesia    │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

#### Social Login Implementation

| Platform | SDK/API | Docs |
|----------|---------|------|
| Google | Firebase Auth / NextAuth.js | https://next-auth.js.org |
| TikTok | TikTok Login Kit | https://developers.tiktok.com |
| Facebook | Facebook Login | https://developers.facebook.com |
| Instagram | Facebook Login (same SDK) | Via Facebook Developer |
| WhatsApp | Twilio / Fonnte (lokal) | https://fonnte.com |
| Twitter/X | Twitter OAuth 2.0 | https://developer.twitter.com |

#### Recommended Auth Stack

```
NextAuth.js (or Supabase Auth)
├── Built-in providers: Google, Facebook, Twitter
├── Custom provider: TikTok, WhatsApp OTP
└── Fallback: Email magic link (passwordless)
```

#### Privacy & Data Collection

| Data | Collected | Purpose |
|------|-----------|---------|
| Name | Yes | Personalization |
| Email/Phone | Yes | Account recovery, notifications |
| Profile Photo | Optional | Avatar display |
| Social Posts | **NO** | Tidak perlu akses konten |
| Friends List | **NO** | Tidak perlu data sosial |

> **Prinsip:** Minta permission seminimal mungkin. User trust = conversion.

#### Saved Calculation Data Model

```
User
├── id
├── name
├── email / phone
├── created_at
│
└── Projects[]
    ├── id
    ├── name ("Renovasi Rumah Jl. Melati")
    ├── created_at
    │
    └── Calculations[]
        ├── id
        ├── room_name ("Kamar Tidur Utama")
        ├── dimensions (p, l, t)
        ├── wall_condition
        ├── result (primer, cat finish, total)
        ├── notes
        └── created_at
```

#### User Journey dengan Account

```
TANPA LOGIN                         DENGAN LOGIN
─────────────                       ─────────────
Hitung → Result → Gone              Hitung → Save → Access Forever
                                              ↓
                                    Dashboard dengan semua proyek
                                              ↓
                                    Share link ke tukang/toko
                                              ↓
                                    Compare revisi perhitungan
```

#### Monetization Angle

| Tier | Limit | Harga |
|------|-------|-------|
| **Free** | 5 saved calculations | Rp 0 |
| **Pro** | Unlimited + PDF export + Priority support | Rp 25.000/bulan |
| **Business** | Team access + Client management + Branding | Rp 100.000/bulan |

### Feature Voting System

Prioritas fitur post-MVP akan ditentukan oleh **voting pengguna**, bukan asumsi internal.

```
┌─────────────────────────────────────────────────────────┐
│              USER-DRIVEN DEVELOPMENT                    │
├─────────────────────────────────────────────────────────┤
│                                                         │
│   ┌─────────────┐    ┌─────────────┐    ┌───────────┐  │
│   │   SUGGEST   │ →  │    VOTE     │ →  │   BUILD   │  │
│   │   Feature   │    │  (Upvote)   │    │  Top Voted│  │
│   └─────────────┘    └─────────────┘    └───────────┘  │
│                                                         │
│   Anyone can        Everyone can       We prioritize   │
│   submit ideas      vote on ideas      by vote count   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Lihat detail:** `FEATURE_VOTING.md`

---

## 7. Metrik Keberhasilan

### 7.1 Utility Metrics
| Metrik | Target MVP | Target 6 Bulan |
|--------|------------|----------------|
| Perhitungan per hari | 50 | 500 |
| Unique users per bulan | 1,000 | 10,000 |
| Bounce rate | < 60% | < 40% |
| Time on site | > 2 menit | > 3 menit |

### 7.2 Engagement Metrics
| Metrik | Target |
|--------|--------|
| WA Share CTR | > 10% |
| Return users | > 20% |
| Calculation completion rate | > 70% |

### 7.3 Business Metrics (Post-MVP)
| Metrik | Target |
|--------|--------|
| Affiliate conversion | > 2% |
| Partner store signups | 50 toko |
| Monthly revenue | Break-even |

---

## 8. Tech Stack (Rekomendasi)

| Layer | Technology | Alasan |
|-------|------------|--------|
| **Frontend** | Next.js 14 | SSR untuk SEO, React ecosystem |
| **Styling** | Tailwind CSS | Rapid development, mobile-first |
| **Hosting** | Vercel | Edge network, performa di SEA |
| **Analytics** | Plausible/Umami | Privacy-friendly, GDPR compliant |
| **Database** | Supabase (jika perlu) | PostgreSQL + Auth gratis |

### Prinsip Teknis
- **Mobile-first**: 80% traffic dari HP
- **Fast loading**: Target < 3 detik di 4G
- **Offline-capable**: PWA untuk area sinyal lemah
- **SEO-optimized**: Static generation untuk landing pages

---

## 9. Risiko & Mitigasi

| Risiko | Kemungkinan | Dampak | Mitigasi |
|--------|-------------|--------|----------|
| Akurasi koefisien salah | Medium | High | Riset lapangan ekstensif, feedback loop |
| Kompetitor besar (brand cat) | Medium | Medium | Fokus netralitas, trust positioning |
| Low traffic | Medium | High | Investasi SEO dari awal |
| User tidak share ke WA | Low | Medium | A/B test CTA, incentive program |

---

## 10. Tim & Resources

### Kebutuhan Minimum
| Role | Responsibility | Status |
|------|----------------|--------|
| Product Owner | Vision, prioritas, user research | ✅ Filled |
| Full-stack Developer | Build & maintain aplikasi | 🔲 Needed |
| UI/UX Designer | Mobile-first design | 🔲 Needed (bisa outsource) |
| Content/SEO | Artikel, landing pages | 🔲 Needed (bisa part-time) |

### Budget Estimasi (MVP)
| Item | Estimasi |
|------|----------|
| Domain (hitungcat.com) | Rp 150.000/tahun |
| Hosting (Vercel free tier) | Rp 0 |
| Design assets | Rp 500.000 - 2.000.000 |
| Development | Rp 0 (jika build sendiri) |
| **Total MVP** | **< Rp 2.500.000** |

---

## 11. Call to Action

### Immediate Next Steps

1. **Riset Lapangan** ← *Saat ini*
   - Interview 3-5 tukang/mandor
   - Validasi koefisien daya sebar
   - Lihat: `INTERVIEW_GUIDE.md`

2. **Finalisasi Spesifikasi**
   - User flow diagram
   - Data model
   - API design (jika ada backend)

3. **Design & Prototype**
   - Wireframe mobile
   - UI mockup
   - User testing

4. **Development**
   - Setup project
   - Core calculator logic
   - Frontend implementation

5. **Soft Launch**
   - Deploy MVP
   - Gather feedback
   - Iterate

---

*Dokumen ini adalah living document yang akan di-update seiring perkembangan proyek.*

**Versi:** 1.0
**Terakhir diupdate:** November 2025
**Author:** Tim HitungCat.com
