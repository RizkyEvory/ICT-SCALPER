<p align="center">
  <img src="https://img.shields.io/badge/MetaTrader%205-Indicator-blue?style=for-the-badge&logo=meta&logoColor=white" alt="MT5">
  <img src="https://img.shields.io/badge/Version-5.00-success?style=for-the-badge" alt="Version 5.00">
  <img src="https://img.shields.io/badge/ICT%20Methodology-2024-orange?style=for-the-badge" alt="ICT 2024">
</p>

<h1 align="center">M4DI~UciH4 ICT Scalper v5.0</h1>

<p align="center">
  <strong>Premium ICT (Inner Circle Trader) Scalping Indicator</strong><br>
  Order Blocks • Fair Value Gaps • OTE • Liquidity Sweeps • MSS • MMXM • Confluence Engine
</p>

<p align="center">
  <a href="https://github.com/RizkyEvory">🌐 Repository</a> •
  <a href="#features">✨ Features</a> •
  <a href="#installation">📥 Installation</a> •
  <a href="#settings">⚙️ Settings</a> •
  <a href="#how-to-use">🎯 Cara Pakai</a>
</p>

<hr>

## ✨ Fitur Utama

- Deteksi **Order Block** (Bullish & Bearish) dengan strength scoring
- **Fair Value Gap** (FVG) otomatis + auto-delete saat terisi
- **Optimal Trade Entry** (OTE) zone berbasis Fib 50%–61.8%
- **Liquidity Pools** (Equal Highs/Lows, BSL/SSL, Swing levels)
- **Market Structure Shift** (MSS / CHoCH + BOS)
- **Market Maker Model** (MMXM) swing detection
- **Confluence Engine** berbobot (OB + FVG + OTE + MSS + Liquidity)
- Smart entry signal hanya saat **confluence ≥ 70%**
- Dashboard real-time dengan:
  - Market structure & liquidity status
  - Active zones (OB, FVG, OTE)
  - Confluence breakdown
  - Signal status + RR + expiry countdown
  - Performance metrics (hit rate, fill rate, dll)
- Visual rectangle, garis fibo, diamond marker, label informatif
- Alert popup/sound/push saat sinyal confluence tinggi

## 📸 Preview (sangat direkomendasikan ditambahkan)

- Dashboard saat sinyal BUY confluence tinggi (OB + FVG + OTE)
- Multiple Order Blocks + FVG yang belum terisi
- Liquidity sweep + MSS Up (CHoCH bullish)
- OTE zone dengan harga masuk + fib levels terlihat
- Confluence matrix breakdown di dashboard

## 📥 Instalasi

1. Download → `M4DI_UciH4_ICT_Scalper_v5.mq5`
2. Buka MT5 → **File → Open Data Folder**
3. Masuk folder → `MQL5/Indicators`
4. Paste file `.mq5`
5. Restart MT5 atau refresh Navigator (klik kanan → Refresh)
6. Drag ke chart (rekomendasi **M5 – M15**)

## ⚙️ Pengaturan Rekomendasi (Scalping ICT)

| Kelompok                  | Parameter                     | Nilai Umum          | Keterangan                                      |
|---------------------------|-------------------------------|----------------------|--------------------------------------------------|
| ICT Core                  | Enable MMXM / OB / FVG / OTE  | true (semua)        | Nonaktifkan jika ingin ringan                    |
| Order Blocks              | Min Body Ratio                | 0.60–0.70           | Filter candle body kuat                          |
|                           | Lookback Period               | 40–80               | Lebih besar = lebih banyak OB historis           |
|                           | Min Strength                  | 60–75               | Filter OB lemah                                  |
| Fair Value Gaps           | Min Gap Pips                  | 3–6                 | Sesuaikan pair (XAUUSD butuh lebih besar)        |
|                           | Auto Delete when Filled       | true                | Membersihkan chart                               |
| OTE & Fibonacci           | Only 50–62% Zone              | true                | Fokus sweet spot ICT                             |
|                           | Min Zone Pips                 | 5–10                | Filter zona terlalu kecil                        |
| Liquidity                 | Equal HL Tolerance            | 2.5–4.0 pips        | Sensitivitas equal highs/lows                    |
|                           | Min Touches                   | 2–3                 | Berapa kali disentuh baru dianggap pool          |
| Confluence                | Min Confluence Score          | 70–80               | Filter sinyal lemah                              |
|                           | OB / OTE / MSS Weight         | 25 / 30 / 25        | Bobot prioritas (sesuaikan gaya trading)         |
| Entry & Exit              | Risk:Reward Min               | 1.5–2.0             | Minimal RR yang diterima                         |
|                           | SL Buffer Pips                | 1.5–3.0             | Buffer di bawah/atas zona                        |
| Alert                     | Enable Popup / Sound          | true                | Sangat membantu scalping                         |

## 🎯 Cara Membaca & Trading

### 1. Urutan Prioritas Confluence (dari paling kuat)

1. **OTE Zone (50–61.8%)** → sweet spot utama ICT  
2. **Bullish/Bearish Order Block** (strength ≥ 70%)  
3. **FVG yang masih pending** (belum terisi)  
4. **MSS / CHoCH** baru terjadi (shift structure)  
5. **Liquidity sweep** (BSL/SSL baru diambil)

Semakin banyak tanda centang ✓ di dashboard → semakin tinggi probabilitas.

### 2. Sinyal Ideal

| Arah | Kondisi Terbaik                                      | Confluence Biasa | Catatan Penting                           |
|------|-------------------------------------------------------|------------------|--------------------------------------------|
| BUY  | Harga di OTE 50–62% + Bullish OB + FVG + SSL taken   | 78–94%          | Tunggu candle konfirmasi bullish           |
| SELL | Harga di OTE 50–62% + Bearish OB + FVG + BSL taken   | 75–92%          | Hindari jika RR < 1.6                      |

### 3. Panduan Dashboard (singkat)

- **Structure** → BULLISH / BEARISH / MSS UP/DOWN  
- **Liquidity** → berapa pool sudah di-sweep  
- **Next Target** → level liquidity terdekat  
- **OTE Zone** → harga sedang di dalam atau di luar  
- **Confluence** → breakdown OB/FVG/OTE/MSS/LIQ  
- **Signal** → READY = layak entry | WAITING = tunggu  
- **RR & Conf** → minimal 1:1.8 + conf ≥ 75% → go  
- **Metrics** → lihat OB hit rate & FVG fill rate

### 4. Tips Penting ICT Scalping

- Timeframe terbaik: **M5 – M15** (H1 untuk konteks)
- Pair ideal: **XAUUSD, EURUSD, GBPUSD, NAS100, GER40**
- Hindari entry saat **confluence < 70%** atau RR < 1.5
- Perhatikan **expiry signal** (default 30 menit)
- Gunakan **higher timeframe** (H1/H4) untuk bias utama
- Jangan chase setelah liquidity sweep sudah jauh

## ⚠️ Peringatan

- Ini **bukan holy grail** — tetap butuh price action & manajemen risiko
- Indikator ini mengikuti **ICT 2024 methodology** versi umum (bukan copy 1:1 dari mentor tertentu)
- Backtest dan forward test dulu minimal 3–6 bulan
- Risk per trade **maksimal 0.5–1.5%**

## 📜 Lisensi

Distributed under **MIT License**  
Copyright © 2024 M4DI~UciH4 (RizkyEvory)

## 📬 Kontak & Dukungan

GitHub: https://github.com/RizkyEvory  
Silakan buka **Issue** jika menemukan bug atau ingin request fitur.

---

⭐ Jika indikator ini membantu trading ICT Anda, jangan lupa **star** repository ini! ⭐

Semoga entry-entry Anda selalu high-probability & profit konsisten!  
M4DI~UciH4 ICT Scalper Team
