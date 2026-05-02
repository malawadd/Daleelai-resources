# دليل المساهمة في مستودع موارد Daleel Thkaa

هذا الملف يشرح للمساهمين كيف يضيفون موارد جديدة إلى الدليل، وكيف يعدّلون الموارد الحالية، وما الذي يجب التأكد منه قبل فتح Pull Request.

## الهدف من هذا المستودع

هذا المستودع هو مصدر الموارد التي تظهر داخل Daleel Thkaa. كل ملف تتم إضافته هنا يمكن أن يدخل إلى النظام عبر المزامنة، ثم يظهر كمسودة داخل لوحة الإدارة قبل النشر.

بمعنى عملي:

1. المساهم يضيف أو يعدّل موردًا في GitHub.
2. النظام يسحب التغييرات من `resources/`.
3. يظهر المورد كمسودة داخل لوحة الإدارة.
4. يراجعه المشرف ثم ينشره ليظهر في الدليل العام.

## ما الذي يمكن المساهمة به؟

نرحب بإضافة موارد مثل:

- أدوات ومنصات AI وAgentic.
- شروحات وأدلة عملية.
- مجتمعات عربية أو إقليمية مفيدة.
- مدونات ونشرات موثوقة.
- مكتبات برومبتات أو مجموعات بيانات أو تقارير مفيدة.

نفضل الموارد التي:

- تضيف قيمة عملية فعلية.
- تخدم جمهورًا عربيًا أو تفيد العاملين في السوق العربي.
- تكون واضحة المصدر وحديثة نسبيًا.
- لا تكون مجرد إعلان تسويقي فارغ.

## بنية المجلدات المعتمدة

الصيغة الموصى بها لكل مورد هي:

```text
resources/<category>/<slug>/resource.md
```

مثال:

```text
resources/blogs/your-resource-slug/resource.md
```

هذه الصيغة هي الأفضل لأنها تتيح لاحقًا إضافة ملفات مساندة داخل نفس المجلد إذا احتجنا لذلك.

الصيغ الأخرى التي يفهمها النظام حاليًا:

- `resources/<category>/<slug>.md`
- `resources/<slug>.md`

لكن لا تستخدمها إلا إذا كان هناك سبب واضح.

إذا كنت تريد نقطة بداية سريعة، انسخ أحد الملفات الموجودة داخل `templates/resources/` ثم انقله إلى `resources/` بعد تعديل الاسم والمحتوى والبيانات الوصفية.

## التصنيفات المتاحة حاليًا

اختر تصنيفًا واحدًا أساسيًا للمورد من هذه القائمة:

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

إذا كان المورد يمكن أن يقع في أكثر من تصنيف، اختر التصنيف الأوضح ثم استخدم `tags` لتوضيح بقية التفاصيل.

## كيف تضيف موردًا جديدًا

1. اختر التصنيف المناسب.
2. أنشئ مجلدًا جديدًا باسم slug واضح وصغير.
3. أضف ملفًا باسم `resource.md`.
4. اكتب frontmatter كاملًا في أعلى الملف.
5. أضف وصفًا عربيًا واضحًا داخل جسم الملف.
6. افتح Pull Request مع شرح مختصر لما أضفته.

## قواعد تسمية الـ slug

يفضل أن يكون الـ slug:

- باللغة الإنجليزية أو transliteration بسيطة.
- بحروف صغيرة فقط.
- مفصولًا بشرطات `-`.
- قصيرًا وواضحًا.

مثال جيد:

```text
your-resource-slug
```

مثال غير جيد:

```text
My Amazing Arabic Resource Final Version 2
```

## القالب الموصى به للملف

انسخ هذا القالب وعدّله:

```md
---
title: "اسم المورد"
description: "وصف مختصر وواضح يشرح لماذا هذا المورد مهم."
category: "tools-platforms"
tags:
  - "arabic"
  - "agents"
  - "tool"
contentType: "reference"
language: "Arabic"
pricing: "Free"
platform: "GitHub"
sourceLabel: "Official Source"
sourceUrl: "https://example.com"
featured: false
createdAt: "2026-05-02"
whyItMattersTitle: "عنوان مختصر يوضح سبب أهمية المورد"
whyItMattersPoints:
  - title: "سبب أول"
    description: "جملة قصيرة تشرح قيمة واضحة ومباشرة."
  - title: "سبب ثان"
    description: "جملة قصيرة تشرح زاوية أخرى من أهمية المورد."
  - title: "سبب ثالث"
    description: "جملة قصيرة تشرح لماذا قد يعود المستخدم لهذا المورد."
---

## لماذا هذا المورد مهم؟

اشرح القيمة الفعلية للمورد في فقرتين أو ثلاث فقرات قصيرة.

## ماذا سيجد المستخدم داخله؟

- نقطة أولى
- نقطة ثانية
- نقطة ثالثة
```

## شرح الحقول المهمة

- `title`: اسم المورد كما سيظهر للمستخدم.
- `description`: وصف مختصر يظهر في البطاقة وصفحة المورد.
- `category`: تصنيف واحد من القائمة المعتمدة.
- `tags`: وسوم تسهّل البحث والفهم السريع.
- `contentType`: واحدة من `guide` أو `toolkit` أو `reference` أو `dataset` أو `community`.
- `language`: `Arabic` أو `Arabic + English`.
- `pricing`: `Free` أو `Free + Paid`.
- `platform`: نوع المنصة مثل `Blog` أو `Docs` أو `GitHub` أو `API` أو `Discord`.
- `sourceLabel`: الاسم المختصر الذي سيظهر بجانب رابط المصدر.
- `sourceUrl`: الرابط الأصلي للمورد، ويجب أن يكون صحيحًا ومباشرًا قدر الإمكان.
- `featured`: اجعلها `false` بشكل افتراضي. فريق الإدارة يقرر ما إذا كان المورد مميزًا.
- `createdAt`: تاريخ بصيغة `YYYY-MM-DD`.
- `whyItMattersTitle`: عنوان قصير يظهر فوق نقاط تشرح باختصار لماذا هذا المورد مهم.
- `whyItMattersPoints`: ثلاث نقاط مختصرة، كل نقطة تحتوي `title` و`description` وتلخص القيمة العملية للمورد بسرعة.

## ماذا نكتب داخل جسم المورد؟

بعد الـ frontmatter، اكتب محتوى مفيدًا يجيب بوضوح عن الأسئلة التالية:

- لماذا هذا المورد يستحق الإضافة؟
- لمن يناسب؟
- ما الذي سيستفيده القارئ أو المستخدم منه؟
- هل هناك ملاحظات مهمة قبل استخدامه؟

يفضل أن يكون النص:

- واضحًا ومباشرًا.
- قصيرًا نسبيًا.
- مبنيًا على قيمة فعلية لا على تسويق.

## كتل Markdoc المدعومة

إذا احتجت، يمكنك استخدام هذه الكتل داخل محتوى المورد:

- `callout`
- `accordion`
- `tabs` و `tab`
- `video`
- `slides`

مثال:

```md
{% callout title="ملاحظة مهمة" tone="tip" %}
هذا المورد مناسب أكثر لمن لديه أساس أولي في المجال.
{% /callout %}
```

## قبل فتح Pull Request

راجع هذه القائمة:

- هل الملف موجود داخل `resources/`؟
- هل اسم المجلد والـ slug واضحان؟
- هل `category` من القائمة المعتمدة؟
- هل `sourceUrl` صالح ويعمل؟
- هل `description` قصيرة وواضحة؟
- هل `tags` مفيدة فعلًا؟
- هل المحتوى يشرح القيمة الحقيقية للمورد؟
- هل تجنبت التكرار مع مورد موجود سابقًا؟

## كيف نراجع المساهمات؟

عادة ننظر إلى هذه الأمور عند المراجعة:

- جودة المورد نفسه.
- وضوح الوصف.
- ملاءمة التصنيف.
- صحة الرابط والمصدر.
- ما إذا كان المورد يضيف شيئًا جديدًا للدليل.

قد نطلب تعديلًا بسيطًا على:

- التصنيف
- الوسوم
- الصياغة
- عنوان المورد أو وصفه

## أمثلة عملية داخل هذا المستودع

يمكنك الاستفادة من هذه الأمثلة قبل إنشاء موردك:

- [templates/resources/blogs/arabic-agent-notes/resource.md](templates/resources/blogs/arabic-agent-notes/resource.md)
- [templates/resources/communities/arabic-ai-builders/resource.md](templates/resources/communities/arabic-ai-builders/resource.md)
- [templates/resources/tools-platforms/serpapi-for-agents/resource.md](templates/resources/tools-platforms/serpapi-for-agents/resource.md)
- [templates/resources/tutorials-guides/arabic-rag-blueprint/resource.md](templates/resources/tutorials-guides/arabic-rag-blueprint/resource.md)

## ملفات مفيدة مرتبطة

- [README.md](README.md)
- [../GITHUB_INTEGRATION.md](../GITHUB_INTEGRATION.md)
- [../CONTENT_AUTHORING_GUIDE.md](../CONTENT_AUTHORING_GUIDE.md)
