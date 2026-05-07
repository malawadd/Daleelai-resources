# Daleelai Resources

هذا المستودع هو مصدر الموارد التي تظهر داخل منصة دليل AI.

فكرته بسيطة: نضيف الموارد هنا بصيغة Markdown منظمة، ثم تُسحب إلى النظام كمحتوى قابل للمراجعة قبل النشر داخل المنصة.

## ما الذي يوجد هنا؟

- موارد عربية أو مفيدة للجمهور العربي في مجالات الذكاء الاصطناعي.
- أدوات ومنصات ووكلاء وشروحات ومدونات ومجتمعات وتقارير وقنوات ومصادر مرجعية.
- قوالب جاهزة داخل `templates/` تساعد على إضافة موارد جديدة بسرعة.

## كيف يعمل المستودع؟

1. تتم إضافة أو تعديل الموارد داخل `resources/`.
2. تُسحب هذه الملفات إلى النظام عبر المزامنة.
3. تظهر كمسودات داخل لوحة الإدارة.
4. يراجعها الفريق ثم ينشرها داخل الدليل.

باختصار:

- `resources/` = محتوى فعلي يدخل إلى مسار المزامنة.
- `templates/` = أمثلة وقوالب للنسخ فقط، ولا تُعامل كمحتوى نهائي.

## بنية المستودع

```text
resources/
  <category>/
    <slug>/
      resource.md

templates/
  resources/
    <category>/
      <example-slug>/
        resource.md
```

الصيغة المفضلة لكل مورد هي:

```text
resources/<category>/<slug>/resource.md
```

## التصنيفات المعتمدة

- `general`
- `agents`
- `frameworks`
- `tools-platforms`
- `tutorials-guides`
- `blogs`
- `communities`
- `newsletters`
- `datasets`
- `prompts`
- `research-reports`
- `videos-podcasts`

## ما الذي نبحث عنه في الموارد؟

نفضّل الموارد التي:

- تضيف قيمة عملية واضحة.
- تخدم المستخدم العربي أو العاملين في السوق العربي.
- تملك مصدرًا واضحًا ويمكن التحقق منه.
- تقدم محتوى حقيقيًا، لا مجرد صفحة تسويقية فارغة.

ونرحب خصوصًا بموارد مثل:

- الأدوات والمنصات
- الوكلاء والمشاريع المفتوحة
- الشروحات والأدلة العملية
- المجتمعات العربية أو الإقليمية
- المدونات والنشرات
- الأبحاث والتقارير
- القنوات والفيديوهات والبودكاست

## قبل أن تساهم

إذا كنت تريد إضافة مورد جديد أو تعديل مورد موجود:

1. راجع [CONTRIBUTING.md](CONTRIBUTING.md).
2. اختر التصنيف المناسب.
3. انسخ قالبًا قريبًا من `templates/resources/` إن احتجت.
4. أضف المورد داخل `resources/`.
5. التزم بصياغة عربية واضحة في المحتوى.

## ما الذي ستجده في دليل المساهمة؟

ملف [CONTRIBUTING.md](CONTRIBUTING.md) يحتوي على التفاصيل العملية، ومنها:

- طريقة إنشاء مورد جديد
- قواعد تسمية `slug`
- شكل الـ frontmatter
- معنى الحقول مثل `whyItMattersTitle` و`whyItMattersPoints`
- أسلوب الكتابة المناسب
- قائمة مراجعة قبل فتح Pull Request

## أمثلة جاهزة

- [templates/resources/blogs/arabic-agent-notes/resource.md](templates/resources/blogs/arabic-agent-notes/resource.md)
- [templates/resources/communities/arabic-ai-builders/resource.md](templates/resources/communities/arabic-ai-builders/resource.md)
- [templates/resources/tools-platforms/serpapi-for-agents/resource.md](templates/resources/tools-platforms/serpapi-for-agents/resource.md)
- [templates/resources/tutorials-guides/arabic-rag-blueprint/resource.md](templates/resources/tutorials-guides/arabic-rag-blueprint/resource.md)

## ملاحظات مهمة

- اكتب اسم الحقول كما هي بالإنجليزية، مثل `pricing` و`platform` و`sourceLabel`.
- يمكن أن تكون قيم هذه الحقول بالعربية إذا كان ذلك أنسب للدليل.
- اجعل `whyItMattersTitle` عنوانًا قصيرًا يجيب مباشرة عن سؤال: لماذا يهم هذا المورد؟
- اجعل النقاط داخل `whyItMattersPoints` تبرر هذا العنوان، لا أن تعيد صياغته فقط.

## روابط مرتبطة

- [CONTRIBUTING.md](CONTRIBUTING.md)
