# SEO/GTM Portfolio Agent

بورتفوليو ثابت ثنائي اللغة (AR/EN بزر تبديل). البيانات كلها في cases.js.

## لما المستخدم يبعت سكرين شوت:
1. حدد نوعه: GSC / GA4 / Ahrefs / Semrush / HubSpot / Looker. لو أداة غير القائمة دي → اسأل المستخدم الأول إيه الأداة دي قبل ما تكمل، وبعدها سجّل اسمها كما هو في `tools`.
2. استخرج الأرقام الظاهرة فعلاً (clicks, impressions, position, sessions, leads, MQLs, revenue, تواريخ الفترة). **ماتخترعش رقم مش ظاهر في الصورة.** لو الأرقام ناقصة، اسألني.
3. لو الصورة جزء من case موجود (نفس العميل/الفترة) أضفها لنفس الـ case وحدّث الـ metrics بدل ما تكرر.
4. لو case جديد: اسألني سؤالين بس لو مش واضحين: إيه اللي اتعمل (actions)؟ وإيه المشكلة الأصلية؟ وبعدها اكتب الـ case.
5. انسخ الصورة لـ images/ باسم kebab-case (client-tool-metric.png) وصغّرها لعرض 1800px كحد أقصى.
6. اكتب challenge في جملة، وactions كنقاط محددة (فعل + تأثير)، والـ metrics بصيغة before → after مع نسبة التغيير.
7. لو العميل سري، استخدم وصف عام ("SaaS B2B - الشرق الأوسط") ونبهني أغطي أي اسم أو دومين ظاهر في الصورة.
8. بعد كل تعديل: شغّل node -e "require('vm').runInNewContext(require('fs').readFileSync('cases.js','utf8'),{window:{}})" للتأكد إن الملف سليم.
9. لخّص اللي اتضاف في سطرين.

## أسلوب الكتابة
- عربي: بالمصري المهني، أرقام قبل الصفات، بدون مبالغة ("ضاعفنا" بس لو الرقم فعلاً ضعف).
- إنجليزي: Professional concise English, numbers first, no hype ("doubled" only if 2x).
- كل case لازم فيه النسختين: `challenge` + `challenge_en`، و`actions` + `actions_en`، و`client` + `client_en`، وكل metric فيه `label` + `label_en`. لو الإنجليزي ناقص، ترجمه من العربي واسأل المستخدم للمراجعة.
- الأقسام تلقائية حسب `category`: أي case بتصنيف `GTM` يظهر في قسم GTM، وغيره في قسم SEO.