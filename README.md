dirsearch — bu Python-da yozilgan, tezkor va kuchli web-directory va file discovery (fuzzing) vositasi. Web-pentestingda yashirin papkalar, fayllar, backuplar, admin panellar va boshqa resurslarni topish uchun ishlatiladi.

---

✅ Dirsearch nima qiladi?

Dirsearch saytdagi mavjud bo‘lishi mumkin bo‘lgan quyidagi obyektlarni avtomatik qidiradi:

  - /admin/
  - /backup.zip
  - /login/
  - /test/
  - /api/v1/
  - /robots.txt
  - .php, .html, .js, .bak, .old kabi fayl kengaytmalari

Uning maqsadi yashirin endpointlarni topish, lekin hech qanday ekspluatatsiya yoki hujum amalga oshirmaydi — faqat so‘rovlar yuboradi.

---

▶️ Asosiy ishlatish

Eng oddiy ishlatish varianti:
```
dirsearch -u https://target.com -e php,html
```
Bu degani:
  -u → URL
  -e → qaysi kengaytmalarni qidirish (php, html, js, txt, bak va h.k.)


