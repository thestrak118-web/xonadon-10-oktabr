# Xonadon — yakuniy tezlik tekshiruvi

2026-09-23. Joriy content commit: `f543c263feb2ac0028616a24af67049026cd8192`.

Quyidagi natijalar rasmiy Google PageSpeed Insights mobil o‘lchovlaridir. B/C fayllari ularning o‘lchovidan keyin o‘zgarmagan; Git diff orqali tekshirildi. Barcha o‘lchovlarda TBT 0 ms. Bu qayd etilgan sinov natijalari; har bir keyingi o‘lchov uchun kafolat emas.

| Manzil | Performance | Speed Index | LCP | CLS |
|---|---:|---:|---:|---:|
| [/a/](https://pagespeed.web.dev/analysis/https-xonadon-10-oktabr-vercel-app-a/j6qlwkqxin?form_factor=mobile) | 100 | 0.772 s | 1.201 s | 0.00009 |
| [/b/](https://pagespeed.web.dev/analysis/https-xonadon-10-oktabr-vercel-app-b/xyqay3uynq?form_factor=mobile) | 100 | 0.783 s | 1.051 s | 0.01894 |
| [/c/](https://pagespeed.web.dev/analysis/https-xonadon-10-oktabr-vercel-app-c/wuf3rhk9k6?form_factor=mobile) | 100 | 0.776 s | 1.051 s | 0.01657 |
| [/](https://pagespeed.web.dev/analysis/https-xonadon-10-oktabr-vercel-app/x9axrueit1?form_factor=mobile) | 100 | 0.762 s | 1.201 s | 0.00000 |

## Majburiy qoidalar

| Band | Natija |
|---|---|
| 1. Til | Barcha landing va thank-you sahifalari `lang="uz"`. |
| 2. Critical CSS | 375×667 uchun inline subset saqlangan; hero qatlamini chizish optimizatsiyasi shu ekran ichida. |
| 3. CSS ulash | `media="print" onload="this.media='all'"` va `noscript` saqlangan. A’da faqat yuklash ustuvorligi `fetchpriority="high"` bilan oshirilgan. |
| 4. HTML | Matn va forma native HTML; bo‘sh/zaxira bloklar qo‘shilmadi. |
| 5.1. Rasmlar atributlari | Har bir img: `loading="lazy" decoding="async"`, width/height va alt. |
| 5.2–5.3. Format/hajm | Barcha rasmlar AVIF. Uch hero 29,833 / 29,598 / 29,106 B; boshqa rasmlar≤10,000 B. |
| 5.4. Fonlar | Faqat tashqi CSSdan ulanadi; HTTP Link header yuklash ko‘rsatmasi, HTML fon elementi yo‘q. |
| 6. Fontlar | Lokal WOFF2 subset, `font-display:swap`. A’da asl Roboto/Mulish variable400–700 birlashtirildi, o‘lchamlar o‘zgarmadi. Joriy Figma aniqligi uchun asl sans fontlar saqlangan. Helvetica Neue Bold hanuz fallback bilan; bu vizual cheklov yashirilmagan. |
| 7. JS | Barcha scriptlar defer. |
| 8. Pixel | Oxirgi script, defer; ID bo‘shligi sabab Meta so‘rovi yo‘q. |
| 9. Qo‘shimcha CSS | Forma uslubi main.css ichida. Critical/main CSS actual CSSPortal orqali minify qilingan, CSSOM va hash tekshiruvlari o‘tgan. |
| CloudConvert | Oldin strelka shu servisda konvertatsiya qilingan. Limitdan keyin foydalanuvchi lokal AVIFga aniq ruxsat berdi; qolgan rasmlar lokal Pillow AVIFda tayyorlangan. |
| CSSPortal | Haqiqiy servis ishlatildi; oxirgi A CSS ham qayta ishlangan. |
| PageSpeed | Rasmiy PSI, yuqorida har bir hisobot havolasi bor. Performance≥90, SI≤0.8s, LCP1–2s, CLS≤1.5 — to‘rtala manzilda o‘tdi. |

## Funksional va vizual tekshiruv

- 320/375/390/425/1440px:15 holat; gorizontal chiqish va yo‘qolgan rasm yo‘q.
- Fontlar optimizatsiyasidan oldin/keyin15 holatning tekshirilgan blok o‘lchamlari aynan teng.
- 75/75 lokal mock forma sinovi: validatsiya, darhol thank-you, fonda yuborish, xato, retry va server tasdig‘idan keyin tozalash.
- Yangi Apps Script endpointi A/B/C configida ulangan. Haqiqiy lead yuborilmadi.
- Telegram kanali, Pixel ID va taymer muddati hali berilmagan. `01:59` statik Figma namunasi.
- `/` → `/a/`; URL parametrlari va fragment saqlanadi.

