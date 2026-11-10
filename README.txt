طريقة الحصول على APK بدون تثبيت أي شيء (عبر GitHub):
1) أنشئ حساباً مجانياً على github.com ثم مستودعاً جديداً (New repository).
2) ارفع محتويات هذا المجلد كما هي (www, package.json, capacitor.config.json, .github).
   مهم: مجلد .github مخفي، تأكد أنه رُفع.
3) افتح تبويب Actions -> Build APK -> Run workflow (أو يبدأ تلقائياً بعد الرفع).
4) بعد ~5 دقائق افتح التشغيل المكتمل ونزّل الملف من Artifacts: TimetableApp-apk.
5) فك الضغط وانقل app-debug.apk إلى الهاتف وثبّته (فعّل "التثبيت من مصادر غير معروفة").

أو محلياً: تحتاج Node 20 و JDK 17 و Android Studio، ثم:
  npm install && npx cap add android && npx cap sync android
  npx cap open android   (ثم Build > Build APK)
