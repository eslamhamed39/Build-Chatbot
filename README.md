# تشغيل Chatbot Backend بعد الـ Build

## 1. تثبيت الحزم

```bash
npm install
```

## 2. تجهيز ملف البيئة

انسخ ملف الإعدادات وعدّل القيم حسب السيرفر:

```bash
cp .env.example .env
```

أهم القيم داخل `.env`:

```env
PORT=8080
DB_FILE=./chatbot.db
CORS_ORIGIN=https://your-frontend-domain.com
SYNC_KEY=your_secret_key_min_32_chars_here_change_me
```


## 3. تشغيل نسخة الـ Build

```bash
npm run start:dist
```

## 4. التأكد أن السيرفر يعمل

افتح الرابط التالي:

```bash
http://localhost:8080/health
```

إذا تم تغيير `PORT` في `.env`، استخدم نفس رقم البورت الجديد.

## ملاحظات مهمة

- يجب وجود قاعدة البيانات أو تحديد مسارها في `DB_FILE`.
- لتشغيل الشات بوت من الفرونت، تأكد أن `CORS_ORIGIN` يحتوي على رابط موقعك.
