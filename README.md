# Daleel Thkaa Resources

هذا هو مستودع الموارد الخاص بـ Daleel Thkaa.

الغرض من هذا المستودع هو جمع موارد عربية ومفيدة في مجالات الذكاء الاصطناعي، الوكلاء، الأدوات، المجتمعات، الشروحات، والتقارير، بحيث يمكن مراجعتها ثم نشرها داخل الدليل.

إذا كنت تزور هذا المستودع لأول مرة، فالفكرة بسيطة:

- كل مورد يعيش داخل `resources/`.
- كل مورد يُكتب كملف Markdown مع frontmatter واضح.
- أي مساهمة جديدة تمر عبر مراجعة ثم تظهر داخل Daleel Thkaa بعد النشر.
- القوالب والأمثلة الجاهزة تعيش داخل `templates/` ولا تدخل المزامنة.

## إذا كانت هذه أول مرة تساهم فيها

إذا لم يسبق لك العمل على مستودع GitHub من قبل، فابدأ بهذا المسار البسيط:

1. افتح صفحة المستودع على GitHub.
2. اضغط `Fork` إذا كان المشروع يستقبل المساهمات عبر fork، أو انسخه مباشرة إذا كنت تملك صلاحية الكتابة.
3. نزّل المستودع إلى جهازك باستخدام `git clone`.
4. افتح المجلد على جهازك في VS Code أو أي محرر نصوص مناسب.
5. ادخل إلى مجلد `resources/`.
6. أضف موردًا جديدًا أو عدّل موردًا موجودًا.
7. احفظ التغييرات ثم ارفعها عبر `git add` و `git commit` و `git push`.
8. افتح Pull Request واذكر باختصار ما الذي أضفته أو عدّلته.

إذا لم تكن تعرف هذه الأوامر بعد، فالقسم التالي يعطيك الخطوات بشكل أوضح.

## البدء من الصفر

### 1. تثبيت الأدوات الأساسية

حتى تتمكن من العمل على هذا المستودع، ستحتاج عادة إلى:

- حساب على GitHub
- Git مثبت على جهازك
- محرر نصوص مثل VS Code

إذا لم يكن Git مثبتًا لديك، ثبّته أولًا ثم أكمل الخطوات التالية.

### 2. استنساخ المستودع

افتح الطرفية Terminal أو PowerShell ونفّذ:

```bash
git clone https://github.com/YOUR_ORG/daleel-thkaa-resources.git
cd daleel-thkaa-resources
```

إذا كنت تعمل من fork خاص بك، استبدل الرابط برابط fork الخاص بك.

### 3. افتح المشروع

يمكنك فتح المجلد في VS Code مثلًا بالأمر:

```bash
code .
```

أو افتحه يدويًا من داخل المحرر.

### 4. تعرّف على البنية

هذا المستودع بسيط. أغلب العمل سيكون داخل:

```text
resources/
```

كل تصنيف له مجلد خاص، وداخل كل مورد يوجد مجلد مستقل وملف `resource.md`.

أما إذا كنت تريد الاطلاع على أمثلة جاهزة أو نسخ قالب كبداية، فستجدها داخل:

```text
templates/
```

### 5. اختر بين تعديل مورد موجود أو إضافة مورد جديد

- إذا كنت تريد تعديل مورد موجود: افتح ملفه وعدّل المحتوى مباشرة.
- إذا كنت تريد إضافة مورد جديد: أنشئ مجلدًا جديدًا داخل التصنيف المناسب ثم أضف ملف `resource.md`.

### 6. احفظ تغييراتك وارفعها

بعد الانتهاء:

```bash
git add .
git commit -m "Add new resource"
git push
```

ثم افتح Pull Request من GitHub.

إذا لم تكن متأكدًا من صياغة الرسالة، يكفي وصف بسيط مثل: `Add Arabic AI community resource`.

## ما نوع الموارد الموجودة هنا؟

هذا المستودع مخصص لموارد مثل:

- الأدوات والمنصات
- الشروحات والأدلة
- المدونات والنشرات
- المجتمعات المهنية
- مجموعات البيانات
- البرومبتات
- الأبحاث والتقارير
- الفيديوهات والبودكاست

## بنية المستودع

```text
resources/
	blogs/
		your-resource-slug/
			resource.md
	communities/
		your-community-slug/
			resource.md

templates/
	resources/
		blogs/
			arabic-agent-notes/
				resource.md
		communities/
			arabic-ai-builders/
				resource.md
		tools-platforms/
			serpapi-for-agents/
				resource.md
		tutorials-guides/
			arabic-rag-blueprint/
				resource.md
```

كل مورد عبارة عن ملف Markdown واحد مع frontmatter، ويمكنك وضعه بإحدى الصيغ التالية:

- `resources/<category>/<slug>/resource.md`
- `resources/<category>/<slug>.md`
- `resources/<slug>.md`

لكن الصيغة الموصى بها للمساهمين هي الأولى، لأنها تتيح إضافة صور أو ملفات فرعية لاحقًا دون كسر الهيكل.

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

## كيف يعمل هذا المستودع؟

أي ملف داخل `resources/` يمكن أن يدخل إلى مسار المزامنة، ثم يتحول إلى مسودة داخل النظام قبل النشر اليدوي من لوحة الإدارة.

أما الملفات داخل `templates/` فهي للقراءة والنسخ فقط، ولا تدخل إلى Convex ولا تظهر في الموقع.

هذا يعني أن GitHub هو مكان التحرير والتعاون، بينما التطبيق هو مكان المراجعة والنشر والعرض النهائي.

## قوالب جاهزة غير متزامنة

- [templates/resources/blogs/arabic-agent-notes/resource.md](templates/resources/blogs/arabic-agent-notes/resource.md)
- [templates/resources/communities/arabic-ai-builders/resource.md](templates/resources/communities/arabic-ai-builders/resource.md)
- [templates/resources/tools-platforms/serpapi-for-agents/resource.md](templates/resources/tools-platforms/serpapi-for-agents/resource.md)
- [templates/resources/tutorials-guides/arabic-rag-blueprint/resource.md](templates/resources/tutorials-guides/arabic-rag-blueprint/resource.md)

## ابدأ من هنا إذا كنت مساهمًا

إذا كنت تريد إضافة مورد جديد أو تعديل مورد موجود، راجع [CONTRIBUTING.md](CONTRIBUTING.md).

## ما الذي نبحث عنه في المساهمات؟

نفضّل الموارد التي:

- تضيف قيمة فعلية وعملية
- تخدم المهتمين ببناء أو استخدام AI وAgentic systems
- تملك مصدرًا واضحًا ورابطًا صالحًا
- ليست مجرد صفحة تسويقية ضعيفة المحتوى

## أين أبدأ؟

- إذا كنت تريد الإضافة أو التعديل: راجع [CONTRIBUTING.md](CONTRIBUTING.md)
- إذا كنت تريد فهم شكل الملف نفسه: راجع أحد القوالب داخل `templates/`

## ملفات مرتبطة

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [../GITHUB_INTEGRATION.md](../GITHUB_INTEGRATION.md)
