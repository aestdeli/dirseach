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
  - -u → URL
  - -e → qaysi kengaytmalarni qidirish (php, html, js, txt, bak va h.k.)

---

📌 Eng muhim parametrlari (tushuntiraman)
1) -u

URL manzil:
```-u https://site.com```

2) -w

Custom wordlist:
```-w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt```

3) -e

Kengaytmalar:
```-e php,js,txt```

4) -o

Natijalarni faylga saqlash:
```-o results.txt```

5) -r

Recurse scan (topilgan papkalarning ichiga ham kirish):
```-r```

6) --threads

Ko‘p ip ishlatish (tezlashtiradi):
```--threads 20 ```

7) --timeout

So‘rovlar uchun timeout:
```--timeout 5```

8) --exclude-status

Keraksiz kodlarni chiqarib tashlash:
```--exclude-status 404,403```

9) --proxy

Masalan, Burp bilan ishlatishda:
```--proxy http://127.0.0.1:8080```

---

🔍 Misol: oddiy scan
```dirsearch -u https://example.com -e php,html -t 20```

🔍 Misol: har bir topilgan papkaga kirib tekshirish
```dirsearch -u https://example.com -w common.txt -r ```

🔍 Misol: natijalarni faylga yozish
```dirsearch -u https://example.com -e php -o result.txt```

🧠 Dirsearchning afzalliklari

✔ Python-da yozilgan — juda moslashuvchan
✔ Tez (ko‘p iplar bilan)
✔ Katta wordlist qo‘llaydi
✔ Proxy (Burp) orqali trafikni ko‘rish mumkin
✔ JSON, text, CSV output chiqaradi

---












