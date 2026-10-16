# H Dutch Hero — مشروع Android

هذا المشروع يغلّف **نفس ملف الموقع** `H_Dutch_Hero.html` داخل تطبيق Android باستخدام WebView. لم أعدّل محتوى الدروس؛ نُسخت الصفحة إلى `app/src/main/assets/index.html`.

## بناء ملف APK على الكمبيوتر

1. ثبّت Android Studio من الموقع الرسمي: https://developer.android.com/studio
2. فك ضغط مجلد `H_Dutch_Hero_Android.zip`.
3. افتح Android Studio واختر **Open** ثم اختر مجلد `H_Dutch_Hero_Android`.
4. وافق على تثبيت مكوّنات Android SDK المطلوبة وانتظر انتهاء Gradle Sync.
5. من القائمة اختر **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
6. عند نجاح البناء، يظهر رابط **locate**. عادةً يكون الملف هنا:
   `app/build/outputs/apk/debug/app-debug.apk`
7. انقل APK إلى هاتف Android وافتحه لتثبيته. قد يطلب الهاتف السماح بالتثبيت من مصدر الملف الذي استخدمته.

## ملاحظات مهمة

- هذا مجلد مصدر Android، وليس APK مُجمّعًا.
- حفظ التقدّم يعتمد على `localStorage` داخل WebView.
- النطق عبر Web Speech API قد يعتمد على إصدار Android ومحرك WebView والأصوات المثبتة.
- ميزة التعرّف على الكلام/الميكروفون قد لا تعمل في WebView مع صفحة محلية؛ تحتاج اختبارًا على الجهاز وقد تتطلب تطويرًا إضافيًا.
- لم يتم اختبار APK على جهاز حقيقي، ولم يُبنَ APK في هذه البيئة لعدم توفر Android SDK وGradle.
