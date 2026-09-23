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

Har bir variantning `js/config.js` faylida shu loyihaning Apps Script endpointi, Telegram kanali va zarur bo‘lsa Pixel ID hamda taymer muddati belgilanadi. Hozir qiymatlar bo‘sh. Backend bo‘lmasa ariza qabul qilinmaydi. Sozlangach valid ism/telefon thank-you sahifasiga darhol o‘tadi, yuborish fonda ishlaydi; xatoda qayta yuborish mumkin.

## Tekshiruv va qolgan ishlar

15 responsive holat, 48 matn/raqam va 75 lokal mock forma tekshiruvi o‘tgan. Haqiqiy lead yuborish hali sinalmagan.

Bu yakuniy optimallashtirilgan production nusxasi emas: rasmlarning bir qismi hali PNG, CloudConvert limiti sabab AVIF va hajm talablari yakunlanmagan. Helvetica Neue Bold o‘rnida fallback bor. Official PageSpeed o‘lchanmagan: Performance 90+, Speed Index ≤0.8 s, LCP 1–2 s va CLS talablari tasdiqlanmagan.
