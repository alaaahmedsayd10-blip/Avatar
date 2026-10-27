# Avatar — عالمي الافتراضي

جهزت مسار نشر من GitHub Pages حتى لا تحتاج إلى إعداد Cloudflare أو إضافة أسرار Cloudflare.

## نشر نسخة اللعبة

1. افتح تبويب **Actions** في المستودع.
2. اختر **Publish Avatar on GitHub Pages**.
3. اضغط **Run workflow** إذا ظهر الزر، أو انتظر تشغيله تلقائيًا بعد تحديث ملف اللعبة.
4. بعد نجاح مرحلتي Build وDeploy، افتح **Settings → Pages**؛ سيعرض GitHub رابط اللعبة المنشورة.

ملف اللعبة الأصلي محفوظ داخل `my-virtual-world_v10_cloudflare_online.zip`، ويستخرج مسار النشر ملفات الواجهة والصور من داخله.

## مهم بخصوص اللعب الجماعي

نشر GitHub Pages يستضيف ملفات الواجهة فقط؛ لا يشغّل WebSocket أو خادم اللعبة. المشروع الحالي ما زال يستخدم اتصال Cloudflare القديم للّعب الجماعي، لذلك لا أعتبر النشر وحده تفعيلًا للأونلاين.

لتحويل الاتصال إلى Playroom Kit، يلزم `gameId` خاص بمشروعك من [Playroom Dev Portal](https://dev.joinplayroom.com/). بعد إنشاء المشروع، أرسل قيمة `gameId` فقط (ليست كلمة مرور أو مفتاحًا سريًا) حتى نربط حركة اللاعبين بالغرفة المشتركة. تظل Supabase مسؤولة عن الحسابات.

## الملفات

- `my-virtual-world_v10_cloudflare_online.zip`: نسخة المشروع المرفوعة.
- `.github/workflows/pages.yml`: نشر ملفات اللعبة عبر GitHub Pages.
- `.github/workflows/deploy-avatar.yml`: مسار Cloudflare القديم، لم يعد مطلوبًا لنشر ملفات الواجهة.
