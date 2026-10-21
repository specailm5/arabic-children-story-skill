# مهارة أدب الطفل واليافعين
### (Arabic Children & YA Literature Skill)

<p align="center">
  <a href="https://github.com/specailm5/arabic-children-story-skill/blob/master/LICENSE"><img alt="License" src="https://img.shields.io/github/license/specailm5/arabic-children-story-skill?style=flat-square"></a>
  <a href="https://github.com/specailm5/arabic-children-story-skill/commits/master"><img alt="Last commit" src="https://img.shields.io/github/last-commit/specailm5/arabic-children-story-skill?style=flat-square"></a>
  <a href="https://specailm5.github.io/arabic-children-story-skill/"><img alt="Docs" src="https://img.shields.io/badge/docs-live-brightgreen?style=flat-square"></a>
  <img alt="Agent Skills" src="https://img.shields.io/badge/Agent%20Skills-compatible-5B21B6?style=flat-square">
</p>

**Arabic children's literature skill for AI agents** — matches content, language, length and format to the age stage; builds story, rhythm and refrain; integrates values without preaching; controls vocabulary and sentence length: `«كان ياما كان… ولد صادق»` ← `«وجد سامر محفظة. نظر حوله. لا أحد.»`. Works with Claude Code, Codex, Antigravity and VS Code agent harnesses.

🔗 **الموقع المرجعي (المراحل والقصة واللغة والنماذج): [specailm5.github.io/arabic-children-story-skill](https://specailm5.github.io/arabic-children-story-skill/)**

> مهارة برمجية ولغوية لنماذج الذكاء الاصطناعي والمحررات الذكية (Codex، Claude Code، Antigravity IDE، VS Code Agent Harness) لكتابة أدب الطفل العربي وتحريره وتشخيصه، استناداً إلى **«أدب الأطفال: علم وفن»** لأحمد نجيب، و**«أدب الطفل العربي»** لحسن شحاته، و**«أدب الأطفال»** لأنس داود.

---

## 📖 ما هي المهارة؟

أكثر ما يُكتب للطفل إما يُصغّره إلى حدّ الإسفاف، أو يُلقّنه إلى حدّ الملل. والنتيجة نصوص لا يحبها الطفل، ولا يثق بها المربي.

تُمكِّنُ هذه المهارةُ الوكيلَ الذكيَّ من:

1. **تحديد المرحلة العمرية** قبل الكتابة، وضبط الموضوع والطول والإخراج.
2. **تطبيق الانقرائية:** اللغة، والمضمون، والإخراج.
3. **بناء الحكاية:** بطل في عمر القارئ، مشكلة واضحة، ثلاث محاولات، حل من الطفل.
4. **ضبط اللغة:** مفردات محسوسة، جمل قصيرة، تكرار مقصود.
5. **كتابة الأنشودة** على إيقاع مناسب، مع مراجعة الوزن.
6. **إخفاء القيمة في الفعل** بدل الوعظ.
7. **تقييم النص** في ثمانية محاور، مع سلم خطورة.

**القواعد الأربع:**
> **اعرف عمر القارئ. لا تُبسّط إلى الإسفاف. لا تَعِظ إلى الملل. واجعل القيمة تُرى.**

---

## 📂 بنية المهارة ومكوناتها

<pre dir="rtl"><code>
arabic-children-story-skill/
│
├── skills/arabic-children-story-skill/          # المهارة (تركيب Agent Skills القياسي)
│   ├── SKILL.md                           # الدليل الأساسي: من العمر إلى النص
│   ├── references/                        # المراجع التفصيلية
│   │   ├── stages.md                      # المراحل العمرية
│   │   ├── story.md                       # البطل، المشكلة، التكرار، الحل
│   │   ├── language_rhythm.md             # المفردات، الجمل، الأنشودة
│   │   └── media_values.md                # الوسيط، الصورة، القيم، الحساسية
│   └── examples/                          # النماذج والتمارين
│       ├── before_after_children_story.md  # قصة كاملة قبل/بعد
│       └── children_workshop.md            # عشرة تمارين
│
├── docs/                                  # الموقع المرجعي (GitHub Pages)
│
├── .agents/skills/arabic-children-story-skill/  # مسار Codex و Antigravity
│
└── .claude/skills/arabic-children-story-skill/  # مسار Claude Code
</code></pre>

---

## 🚀 طرق التثبيت والاستخدام (Installation Guide)

تُثبَّتُ المهارةُ إما في مشروعٍ بعينه (**محلياً**)، وإما **عامةً (Global)** لتعمل في كافة المشاريع.

---

### أولاً: التثبيت بأمر واحد عبر `npx` (الطريقة الأسرع — موصى به)

```bash
npx skills add specailm5/arabic-children-story-skill -g -y
```

ولاختيار بيئات بعينها أو التثبيت داخل مشروع محدد:

```bash
npx skills add specailm5/arabic-children-story-skill -a claude-code -a codex
npx skills add specailm5/arabic-children-story-skill --skill arabic-children-story-skill -g -y
```

---

### ثانياً: التثبيت العام لبيئة Claude Code و Codex و Antigravity (يدوياً)

#### لنظام Windows (PowerShell):

```powershell
# مصدر المهارة داخل المستودع
$src = "skills\arabic-children-story-skill"

# 1. تثبيت لبيئة Claude Code
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\arabic-children-story-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.claude\skills\arabic-children-story-skill\"

# 2. تثبيت لبيئة Codex و Agent Skills العامة
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills\arabic-children-story-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.agents\skills\arabic-children-story-skill\"

# 3. تثبيت لبيئة Google Antigravity / Gemini
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\arabic-children-story-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.gemini\config\skills\arabic-children-story-skill\"
```

#### لنظام macOS / Linux (Bash):

```bash
src=skills/arabic-children-story-skill

# 1. لبيئة Claude Code
mkdir -p ~/.claude/skills/arabic-children-story-skill
cp -r "$src/." ~/.claude/skills/arabic-children-story-skill/

# 2. لبيئة Codex و Agent Harness
mkdir -p ~/.agents/skills/arabic-children-story-skill
cp -r "$src/." ~/.agents/skills/arabic-children-story-skill/

# 3. لبيئة Antigravity / Gemini
mkdir -p ~/.gemini/config/skills/arabic-children-story-skill
cp -r "$src/." ~/.gemini/config/skills/arabic-children-story-skill/
```

---

### ثالثاً: التثبيت المحلي داخل مشروع محدد (VS Code Workspace Harness)

```powershell
New-Item -ItemType Directory -Force -Path ".agents\skills\arabic-children-story-skill"
Copy-Item -Recurse -Force "path\to\skills\arabic-children-story-skill\*" ".agents\skills\arabic-children-story-skill\"
```

---

### رابعاً: الاستخدام اليدوي (Direct System Prompt / Custom Instructions)

* افتح ملف [`skills/arabic-children-story-skill/SKILL.md`](skills/arabic-children-story-skill/SKILL.md) وانسخ محتواه وضعه في خانة **التعليمات المخصصة (Custom Instructions)** أو **System Prompt**.

---

## ⚡ كيف تعمل المهارة؟

### سبعة أسئلة قبل الكتابة

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">السؤال</th>
<th align="right">لماذا؟</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>ما العمر؟</strong></td>
<td>٠–٣ / ٣–٦ / ٦–٩ / ٩–١٢ / ١٢–١٥ / يافعين</td>
</tr>
<tr>
<td><strong>ما الوسيط؟</strong></td>
<td>كتاب / أنشودة / مسرح / إذاعة / فيديو</td>
</tr>
<tr>
<td><strong>من يقرأ؟</strong></td>
<td>الطفل / الكبير له / معاً</td>
</tr>
<tr>
<td><strong>ما النوع؟</strong></td>
<td>واقعي / خيالي / علمي / تراثي</td>
</tr>
<tr>
<td><strong>ما الغاية؟</strong></td>
<td>متعة / تعليم / قيمة / مهارة</td>
</tr>
<tr>
<td><strong>ما اللغة؟</strong></td>
<td>فصحى مبسطة / مشكولة / عامية</td>
</tr>
<tr>
<td><strong>ما الحساسية؟</strong></td>
<td>خوف / عنف / موت / دين</td>
</tr>
</tbody>
</table>
<br clear="all">

### المراحل في سطر

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">المرحلة</th>
<th align="right">الموضوع</th>
<th align="right">الطول</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>٠–٣</strong></td>
<td>محسوسات</td>
<td>١٠–٥٠ كلمة</td>
</tr>
<tr>
<td><strong>٣–٦</strong></td>
<td>حكاية متكررة</td>
<td>١٠٠–٣٠٠</td>
</tr>
<tr>
<td><strong>٦–٩</strong></td>
<td>مشكلة وحل</td>
<td>٣٠٠–١٠٠٠</td>
</tr>
<tr>
<td><strong>٩–١٢</strong></td>
<td>مغامرة/علم</td>
<td>١٠٠٠–٥٠٠٠</td>
</tr>
<tr>
<td><strong>١٢–١٥</strong></td>
<td>تأمل/صراع</td>
<td>٥٠٠٠–٢٠٠٠٠</td>
</tr>
<tr>
<td><strong>يافعون</strong></td>
<td>هوية</td>
<td>رواية</td>
</tr>
</tbody>
</table>
<br clear="all">

### مسار العمل

<pre dir="rtl"><code>
① العمر والوسيط
        ↓
② الفكرة والحكاية
        ↓
③ الشخصية والمشكلة
        ↓
④ التكرار والحل
        ↓
⑤ اللغة والإيقاع
        ↓
⑥ القيمة بلا وعظ
        ↓
⑦ الصورة والإخراج
        ↓
⑧ القراءة على طفل
</code></pre>

### قبل/بعد

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">قبل</th>
<th align="right">بعد</th>
<th align="right">السبب</th>
</tr>
</thead>
<tbody>
<tr>
<td>«كان ياما كان… ولد صادق»</td>
<td>«وجد سامر محفظة»</td>
<td>بداية من الحدث</td>
</tr>
<tr>
<td>«يجب أن يكون صادقاً»</td>
<td>«وضعها في جيبه. ثم أخرجها»</td>
<td>قيمة تُرى</td>
</tr>
<tr>
<td>الشرطة تحل</td>
<td>الطفل يعيدها</td>
<td>الطفل بطل</td>
</tr>
<tr>
<td>«تعلم أن الصدق…»</td>
<td>«لم يحلم بشيء»</td>
<td>نهاية بصورة</td>
</tr>
</tbody>
</table>
<br clear="all">

---

## 📚 المراجع والاعتماد

* **«أدب الأطفال: علم وفن»** — أحمد نجيب — دراسات في أدب الأطفال:
  <https://archive.org/details/20200602_20200602_1551>
* **«أدب الطفل العربي»** — حسن شحاته — الدار المصرية اللبنانية، القاهرة:
  <https://archive.org/details/20200602_20200602_1551>
* **«أدب الأطفال»** (الشعر والأنشودة) — أنس داود:
  <https://archive.org/details/20200602_20200602_1551>

> **إقرار بالفضل:** هذه المهارة صياغة تعليمية مستقلة لمبادئ الكتب الثلاثة، مع نقل اقتباسات محدودة بإسنادها إلى صفحاتها. ولا يتضمّن المستودع نسخاً كاملة من الكتب، ولا يُغني عن الرجوع إلى الأصل.

---

## ⚠️ حدود المسؤولية

- المهارة **لكتابة أدب الطفل وتحريره**، لا لاستنساخ شخصيات محمية.
- لا تُخيف الطفل بلا سبب، ولا تُقدّم عنفاً مجانياً.
- لا تُقدّم تمييزاً على أساس جنس/لون/دين/إعاقة.
- لا تُفتِ في الدين، ولا تُلقّن قيمة بلا حكاية.
- المستخدم مسؤول عن مراجعة النص النهائي، وحقوق الرسام والمؤلف.

---

## 🤝 المساهمة

نرحب بالمساهمات التي تحسّن المادة أو التحرير أو التوثيق. اقرأ [CONTRIBUTING.md](CONTRIBUTING.md) قبل فتح طلب سحب، والتزم بـ[قواعد السلوك](CODE_OF_CONDUCT.md).

## 🛡️ الأمان

إن وجدت مشكلة أمنية، فلا تفتح قضية عامة؛ راجع [SECURITY.md](SECURITY.md).

## 📄 سجل التغييرات

راجع [CHANGELOG.md](CHANGELOG.md) لمعرفة ما أُضيف في كل إصدار.

## 📬 الدعم

للأسئلة والاقتراحات: [افتح قضية](https://github.com/specailm5/arabic-children-story-skill/issues).

---

## 📜 الترخيص (License)

هذه المهارة مفتوحة المصدر تحت رخصة [MIT](LICENSE)، ومتاحة للاستخدام الشخصي والتجاري والبحثي لدعم اللغة العربية.
