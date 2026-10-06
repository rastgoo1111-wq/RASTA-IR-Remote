# RASTA Universal Audio IR Remote v9

**یک اپلیکیشن اندروید جامع برای کنترل تجهیزات صوتی قدیمی از طریق Infrared (IR)**

## 📱 دستگاه‌های پشتیبانی‌شده

1. **Onkyo CR-185 / CR-185X** — Remote: RC-332S ✓ **VERIFIED**
2. **Sony CMT-E300HD** — Remote: RM-E02D ⚠ **CANDIDATE (Generic SIRC)**
3. **Victor/JVC NX-TC5-B** — Remote: RM-SNXTC5-S ❓ **UNKNOWN (Discovery Required)**
4. **Pioneer P700 Mini Hi-Fi** — Remote: CU-AP015 ❓ **UNKNOWN (Discovery Required)**

## 🎯 ویژگی‌های اصلی

✅ **IR Transmission واقعی** — ConsumerIrManager API Android  
✅ **چهار دستگاه مختلف** — در چهار تب جداگانه  
✅ **کدهای VERIFIED** — فقط کدهای شناخته‌شده (Onkyo)  
✅ **Code Lab** — تست دستی و کشف کدهای جدید  
✅ **Database JSON** — ذخیره‌سازی و backup/restore  
✅ **بدون اینترنت** — عملکرد کامل بدون شبکه  
✅ **RTL Support** — رابط کاربری فارسی  
✅ **Candidate/Unknown** — کدهای غیرتایید شده به‌صورت شفاف  

## 🔧 سیاست Verification

### ✓ VERIFIED
- کدهای Onkyo از documentation رسمی
- کدهای تایید‌شده توسط کاربر روی دستگاه واقعی

### ⚠ CANDIDATE
- کدهای عمومی SIRC برای Sony (نه مدل‌محور)
- نیاز به تست و تایید

### ❓ UNKNOWN
- کدهای JVC و Pioneer هنوز پیدا نشده‌اند
- استفاده از Code Lab برای کشف

## 📋 نیازمندی‌ها

- **Android**: 6.0+ (API 23+)
- **IR Blaster**: گوشی باید IR transmitter داشته باشد (Xiaomi، Samsung، etc.)
- **Java**: 17+

## 🏗️ Build کردن

### روش 1: GitHub Actions (خودکار)
1. به مخزن GitHub بروید
2. به تب "Actions" بروید
3. "Build APK" workflow را اجرا کنید
4. APK را از Releases دانلود کنید

### روش 2: محلی (Android Studio)

```bash
# Clone کردن
git clone https://github.com/rastgoo1111-wq/RASTA-IR-Remote.git
cd RASTA-IR-Remote

# در Android Studio باز کنید
# Gradle sync کنید
# Build → Build APK را انتخاب کنید

# یا از Terminal:
./gradlew assembleDebug
# APK: app/build/outputs/apk/debug/app-debug.apk
```

## 📦 نصب روی گوشی

```bash
adb install -r app/build/outputs/apk/debug/app-debug.apk
```

یا:
- فایل APK را روی گوشی کپی کنید
- روی گوشی دابل کلیک کنید
- "نصب از منابع نامعلوم" را فعال کنید
- نصب کنید

## 🎮 استفاده

### تب Onkyo
- کلیک مستقیم روی دکمه‌ها
- کدهای تایید شده ارسال می‌شوند

### تب Sony
- کدهای generic SIRC (Candidate)
- تست کنید و VERIFY کنید

### تب JVC
- کدها Unknown هستند
- Code Lab برای تست

### تب Pioneer
- کدها Unknown هستند
- Code Lab برای تست

### Code Lab
1. Protocol انتخاب کنید
2. Carrier و parameters را تنظیم کنید
3. TEST SEND بزنید
4. اگر جواب داد: VERIFY کنید
5. اگر نجواب داد: FAILED کنید

## 💾 Database

- تمام کدهای ذخیره‌شده در JSON
- Export برای backup
- Import برای restore
- Clear برای reset

## ⚠️ مهم

**هیچ کد غیرواقعی به‌عنوان VERIFIED نشان داده نمی‌شود.**

- Sony کدهای مدل‌محور تایید‌شده ندارند
- JVC کدهای مدل‌محور تایید‌شده ندارند
- Pioneer کدهای مدل‌محور تایید‌شده ندارند
- فقط Code Lab برای کشف واقعی استفاده شود

## 📄 License

MIT License

---

**Version**: 9.0  
**Platform**: Android 6.0+ (API 23+)  
**Language**: Java 17 + HTML5/JS
