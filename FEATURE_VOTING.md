# HitungCat.com - Feature Voting System

## Filosofi

> **"Build what users want, not what we assume they need."**

Daripada menebak fitur mana yang penting, kita biarkan pengguna yang menentukan. Sistem voting memastikan development effort kita tepat sasaran.

---

## 1. Konsep Sistem

### 1.1 User Flow

```
┌──────────────────────────────────────────────────────────────────┐
│                        FEATURE VOTING FLOW                        │
└──────────────────────────────────────────────────────────────────┘

     User selesai             Muncul prompt              User bisa:
     hitung cat          "Ada fitur yang kamu
         │                    inginkan?"                 ┌─────────┐
         │                        │                      │ SUGGEST │
         ▼                        ▼                      │ fitur   │
    ┌─────────┐            ┌─────────────┐              │ baru    │
    │ RESULT  │ ────────── │  FEEDBACK   │ ───────────► └────┬────┘
    │  PAGE   │            │   PROMPT    │                   │
    └─────────┘            └─────────────┘              ┌────▼────┐
                                  │                      │  VOTE   │
                                  │                      │ fitur   │
                                  ▼                      │ existing│
                           ┌─────────────┐              └────┬────┘
                           │  FEATURE    │                   │
                           │   BOARD     │ ◄─────────────────┘
                           │  (Public)   │
                           └─────────────┘
                                  │
                                  ▼
                           Sorted by votes
                           (highest first)
```

### 1.2 Prinsip Utama

| Prinsip | Implementasi |
|---------|--------------|
| **Terbuka** | Siapapun bisa suggest tanpa login |
| **Transparan** | Semua orang bisa lihat votes & status |
| **Demokratis** | 1 user = 1 vote per fitur |
| **Accountable** | Kita commit untuk build top-voted features |

---

## 2. Komponen Sistem

### 2.1 Feature Submission

**Data yang dikumpulkan:**

| Field | Required | Contoh |
|-------|----------|--------|
| Judul Fitur | Ya | "Kalkulator untuk plafon/ceiling" |
| Deskripsi | Ya | "Biar bisa hitung cat plafon terpisah dari tembok" |
| Kategori | Ya | Calculator / Tools / Marketplace / Other |
| Nama/Alias | Tidak | "Budi" (opsional untuk kredit) |
| Email | Tidak | Untuk notifikasi jika dibangun |

**Kategori Fitur:**

```
📊 Calculator     - Fitur perhitungan baru
🛠️ Tools         - Alat bantu tambahan
🏪 Marketplace   - Jual/beli, direktori toko
📱 Experience    - UI/UX improvements
📚 Education     - Konten edukasi, tutorial
🔗 Integration   - Integrasi platform lain
```

### 2.2 Voting Mechanism

**Anti-spam measures:**
- Rate limiting (max 10 votes per session)
- Cookie/localStorage tracking (no login required)
- Optional: Simple captcha untuk submissions

**Vote options:**
```
┌─────────────────────────────────────────────┐
│  🔼  Kalkulator Multi-Ruangan               │
│ 127  Hitung kebutuhan cat seluruh rumah    │
│      sekaligus dalam satu form              │
│                                             │
│  📊 Calculator    🟢 Under Consideration    │
└─────────────────────────────────────────────┘
```

### 2.3 Status Labels

| Status | Arti | Color |
|--------|------|-------|
| `Under Consideration` | Sedang dipertimbangkan | 🟡 Yellow |
| `Planned` | Akan dibangun | 🔵 Blue |
| `In Progress` | Sedang dikerjakan | 🟠 Orange |
| `Completed` | Sudah live | 🟢 Green |
| `Not Now` | Ditunda/tidak prioritas | ⚪ Gray |

---

## 3. Implementasi Options

### Option A: Third-Party Tools (Recommended for MVP)

#### Canny.io
- **Pros:** Feature-rich, beautiful UI, roadmap public
- **Cons:** Paid ($400/mo), mungkin overkill
- **Link:** canny.io

#### Nolt.io
- **Pros:** Simple, affordable ($25/mo), clean UI
- **Cons:** Limited customization
- **Link:** nolt.io

#### Frill.co
- **Pros:** Free tier available, good for startups
- **Cons:** Branding on free tier
- **Link:** frill.co

#### Upvoty
- **Pros:** Affordable ($15/mo), roadmap feature
- **Cons:** Less polished UI
- **Link:** upvoty.com

### Option B: Free Alternatives

#### GitHub Discussions
- **Pros:** Free, developer-friendly, integrated with repo
- **Cons:** Technical audience only, not user-friendly untuk orang awam

#### Notion Public Page
- **Pros:** Free, flexible, easy to setup
- **Cons:** Manual vote counting, no native upvote

#### Google Form + Sheets
- **Pros:** Free, familiar
- **Cons:** Not real-time, no public voting visibility

### Option C: Build Custom (Post-MVP)

Jika traffic sudah cukup, bisa build sendiri:

```
Tech Stack:
- Supabase (DB + Auth)
- Next.js API routes
- Simple upvote component

Tables:
- features (id, title, description, category, votes, status)
- votes (id, feature_id, session_id, created_at)
```

### Rekomendasi

| Fase | Solusi | Alasan |
|------|--------|--------|
| **MVP** | Nolt.io atau Frill.co | Cepat setup, affordable, professional |
| **Growth** | Custom build | Full control, no monthly fee |

---

## 4. Seed Features (Initial List)

Untuk launch, kita pre-populate dengan fitur-fitur yang sudah terpikirkan:

| Fitur | Kategori | Status |
|-------|----------|--------|
| Kalkulator multi-ruangan | Calculator | Under Consideration |
| Estimasi harga real-time | Calculator | Under Consideration |
| Download PDF RAB | Tools | Under Consideration |
| Kalkulator plafon/ceiling | Calculator | Under Consideration |
| Kalkulator eksterior | Calculator | Under Consideration |
| Perbandingan merk cat | Tools | Under Consideration |
| Direktori toko bangunan | Marketplace | Under Consideration |
| Bursa sisa cat | Marketplace | Under Consideration |
| Tutorial video pengecatan | Education | Under Consideration |
| Kalkulator plamir/dempul | Calculator | Under Consideration |
| Mode gelap (dark mode) | Experience | Under Consideration |
| Simpan history perhitungan | Experience | Under Consideration |
| Share result ke Instagram | Integration | Under Consideration |
| Integrasi Tokopedia cart | Integration | Under Consideration |
| Kalkulator waterproofing | Calculator | Under Consideration |

---

## 5. Communication Strategy

### 5.1 Placement di Website

```
┌─────────────────────────────────────────────┐
│             HITUNGCAT.COM                   │
├─────────────────────────────────────────────┤
│                                             │
│  [🧮 Calculator]  [📋 Roadmap]  [💡 Vote]   │
│                                             │
│  ┌─────────────────────────────────────┐   │
│  │                                     │   │
│  │         CALCULATOR AREA             │   │
│  │                                     │   │
│  └─────────────────────────────────────┘   │
│                                             │
│  ┌─────────────────────────────────────┐   │
│  │  💡 Punya ide fitur?                │   │
│  │     [Vote & Suggest Fitur Baru →]   │   │
│  └─────────────────────────────────────┘   │
│                                             │
└─────────────────────────────────────────────┘
```

### 5.2 Post-Calculation Prompt

Setelah user selesai hitung, tampilkan:

```
┌─────────────────────────────────────────────┐
│  ✅ Hasil perhitungan kamu sudah siap!      │
│                                             │
│  Bantu kami jadi lebih baik:                │
│                                             │
│  [⭐ Vote Fitur Baru]   [📝 Kasih Feedback] │
│                                             │
└─────────────────────────────────────────────┘
```

### 5.3 Monthly Update

Commit untuk transparency:

```
📢 UPDATE BULANAN - Desember 2025

Top 3 Fitur Paling Banyak Di-vote:
1. 🥇 Kalkulator Multi-Ruangan (234 votes) → IN PROGRESS
2. 🥈 Estimasi Harga Real-time (189 votes) → PLANNED
3. 🥉 Download PDF RAB (156 votes) → UNDER CONSIDERATION

Terima kasih sudah voting! 🙏
```

---

## 6. Success Metrics

| Metrik | Target |
|--------|--------|
| Total feature submissions | 50+ dalam 3 bulan pertama |
| Total votes | 500+ dalam 3 bulan pertama |
| Avg votes per feature | 10+ |
| Features completed from votes | 3+ dalam 6 bulan |
| User satisfaction (completed features) | Survey score > 4/5 |

---

## 7. Governance

### Kapan Fitur Akan Dibangun?

Tidak semua top-voted akan otomatis dibangun. Pertimbangan:

| Faktor | Bobot |
|--------|-------|
| Jumlah votes | 40% |
| Effort/complexity | 25% |
| Strategic alignment | 20% |
| Revenue potential | 15% |

### Kapan Fitur Ditolak?

- Tidak align dengan core mission
- Technically not feasible
- Legal/compliance issues
- Duplicate dengan fitur existing

**Transparansi:** Jika ditolak, jelaskan alasannya di status dengan komentar.

---

## 8. Implementation Checklist

### MVP Launch

- [ ] Pilih platform (Nolt/Frill/Custom)
- [ ] Setup board dengan branding HitungCat
- [ ] Add seed features (15 items)
- [ ] Embed/link di website
- [ ] Add post-calculation prompt
- [ ] Test submission flow
- [ ] Test voting flow

### Ongoing

- [ ] Review submissions weekly
- [ ] Update status labels
- [ ] Monthly transparency update
- [ ] Celebrate completed features
- [ ] Archive stale/duplicate features

---

*Dokumen ini adalah bagian dari product documentation HitungCat.com*

**Versi:** 1.0
**Terakhir diupdate:** November 2025
