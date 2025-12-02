# shayla-marketplace (MVP) — OTP auth + scaffold

هدف: اسکافلد وب‌اپ (Next.js frontend + Express backend) با احراز هویت شماره تلفن (OTP) و پشتیبانی از Twilio.

ویژگی‌های اولیه:
- ورود با شماره تلفن و کد OTP
- پشتیبانی از Twilio (SMS واقعی) یا حالت Mock (پیام در console لاگ می‌شود)
- ساختار ساده برای توسعهٔ سریع MVP

نصب و اجرا محلی:
1. clone repo
2. cp .env.example .env و متغیرها را تنظیم کنید (TWILIO_* در صورت نیاز)
3. نصب وابستگی‌ها: yarn install
4. اجرای محلی: yarn dev
   - این پروژه به طور همزمان سرور backend (Express) و frontend (Next.js) را اجرا می‌کند.

اگر فایل‌های secrets را به GitHub اضافه کردید (TWILIO_SID, TWILIO_TOKEN, TWILIO_FROM, JWT_SECRET, DATABASE_URL) و سپس CI یا deploy می‌کنید، SMS واقعی کار خواهد کرد.

فایل‌های مهم:
- backend/index.js
- backend/otp.js
- frontend/components/Login.jsx
- .env.example