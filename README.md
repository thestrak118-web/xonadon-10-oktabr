# Xonadon — 10-oktabr

Uchta mustaqil landing sahifa. Joriy dizayn va forma nusxasi.

- `/` → `/a/` (parametr va fragment saqlanadi)
- `/a/` — asosiy oq-oltin sayt
- `/b/` — oq-ko‘k sayt
- `/c/` — to‘q ko‘k sayt

## Ishga tushirish

`python3 -m http.server 8000` va `http://localhost:8000/`.
Statik hostingda build komandasi kerak emas, publish papkasi repozitoriy ildizi.
Har bir variant o‘z assetlari bilan alohida ishlaydi.

## Forma

Har bir variantning `js/config.js` faylida shu loyihaning Apps Script endpointi, Telegram kanali va zarur bo‘lsa Pixel ID hamda taymer muddati belgilanadi. Apps Script endpointi ulangan; Telegram, Pixel va taymer muddati hali berilmagan. Sozlangach valid ism/telefon thank-you sahifasiga darhol o‘tadi, yuborish fonda ishlaydi; xatoda qayta yuborish mumkin.

## PageSpeed va tekshiruv

| Manzil | Performance | Speed Index | LCP | CLS |
|---|---:|---:|---:|---:|
| [/a/](https://pagespeed.web.dev/analysis/https-xonadon-10-oktabr-vercel-app-a/j6qlwkqxin?form_factor=mobile) | 100 | 0.772 s | 1.201 s | 0.00009 |
| [/b/](https://pagespeed.web.dev/analysis/https-xonadon-10-oktabr-vercel-app-b/xyqay3uynq?form_factor=mobile) | 100 | 0.783 s | 1.051 s | 0.01894 |
| [/c/](https://pagespeed.web.dev/analysis/https-xonadon-10-oktabr-vercel-app-c/wuf3rhk9k6?form_factor=mobile) | 100 | 0.776 s | 1.051 s | 0.01657 |
| [/](https://pagespeed.web.dev/analysis/https-xonadon-10-oktabr-vercel-app/x9axrueit1?form_factor=mobile) | 100 | 0.762 s | 1.201 s | 0.00000 |

Barcha natijalar rasmiy PSI mobil sinovidan; joriy o‘lchovlar, keyingi natijalar kafolati emas. Barcha rasmlar AVIF: fonlar≤30KB, boshqalar≤10KB.15 responsive holat va75mock forma sinovi o‘tdi. [Bandma-band tekshiruv](TEKSHIRUV.md).

Apps Script ulangan, haqiqiy lead yuborish hali tekshirilmagan. Telegram, Pixel va taymer muddati kutilmoqda. Helvetica Neue Bold asl fayli yo‘qligi sabab tegishli joylar fallback bilan.
