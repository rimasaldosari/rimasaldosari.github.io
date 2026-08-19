# ريماس الدوسري — بورتفوليو شخصي | Rimas Aldosari — Personal Portfolio

> **Personal Portfolio Site** — طالبة علوم حاسب متخصصة في الذكاء الاصطناعي ووكلاء الذكاء الاصطناعي | CS Student specializing in AI Agents & Generative AI

🔗 **Live Site:** [rimasaldosari.github.io](https://rimasaldosari.github.io)

---

## Table of Contents | جدول المحتويات

1. [Executive Summary | ملخص تنفيذي](#1-executive-summary--ملخص-تنفيذي)
2. [Problem Statement | بيان المشكلة](#2-problem-statement--بيان-المشكلة)
3. [Solution Overview | نظرة على الحل](#3-solution-overview--نظرة-على-الحل)
4. [Site Architecture | هيكل الموقع](#4-site-architecture--هيكل-الموقع)
5. [Design System | نظام التصميم](#5-design-system--نظام-التصميم)
6. [Tech Stack & Project Structure | التقنيات وبنية المشروع](#6-tech-stack--project-structure--التقنيات-وبنية-المشروع)
7. [Featured Projects | المشاريع البارزة](#7-featured-projects--المشاريع-البارزة)
8. [Visitor Journey | رحلة الزائر](#8-visitor-journey--رحلة-الزائر)
9. [Performance & Accessibility | الأداء وإمكانية الوصول](#9-performance--accessibility--الأداء-وإمكانية-الوصول)
10. [Running Locally & Deployment | التشغيل والنشر](#10-running-locally--deployment--التشغيل-والنشر)
11. [Contact | التواصل](#11-contact--التواصل)
12. [Appendix | الملحق](#12-appendix--الملحق)

---

## 1. Executive Summary | ملخص تنفيذي

**البورتفوليو** هو الموقع الشخصي لـ **ريماس الدوسري**، طالبة علوم حاسب متخصصة في الذكاء الاصطناعي والنماذج التوليدية ووكلاء الذكاء الاصطناعي (AI Agents). يعمل الموقع كواجهة تعريفية احترافية تجمع نبذة شخصية، أبرز المشاريع التقنية، ووسيلة تواصل مباشرة — مبني بالكامل بتقنيات ويب أساسية (HTML/CSS/JS) دون أي إطار عمل (Framework)، ومستضاف مجانًا عبر GitHub Pages.

**RAFID Portfolio** is the personal website of **Rimas Aldosari**, a Computer Science student specializing in AI, generative models, and AI agents. The site serves as a professional introduction hub combining a personal bio, featured technical projects, and a direct contact channel — built entirely with core web technologies (HTML/CSS/JS), with no framework dependency, and hosted for free via GitHub Pages.

---

## 2. Problem Statement | بيان المشكلة

الطلاب والمطورون الناشئون في مجال الذكاء الاصطناعي يحتاجون منصة واحدة موثوقة تعرض أعمالهم بشكل احترافي أمام: المُوظِّفين، لجان الهاكاثونات، وفرق التدريب. الاعتماد فقط على ملف السيرة الذاتية (CV) أو حساب GitHub المتفرق لا يعطي انطباعًا بصريًا قويًا ولا يبرز السياق الكامل للمشاريع (المشكلة، الحل، التقنيات).

Early-career AI students and developers need a single, trustworthy platform to present their work professionally to employers, hackathon judges, and training programs. Relying solely on a CV or a scattered GitHub profile fails to give a strong visual impression or convey the full context of a project (problem, solution, tech stack).

---

## 3. Solution Overview | نظرة على الحل

موقع صفحة واحدة (Single Page) ثنائي اللغة (عربي RTL بشكل أساسي)، يعرض:
- نبذة شخصية موجزة ومركّزة
- بطاقات مشاريع تفاعلية مع الوسوم التقنية وروابط GitHub مباشرة
- خلفية متحركة (Canvas Animation) تعكس طابع "الشبكات العصبية" بصريًا لتعزيز الهوية التقنية
- قسم تواصل مباشر (بريد، لينكد إن، GitHub) بدون الحاجة لنموذج خلفي (Backend Form)

A single-page, bilingual (primarily Arabic RTL) site that presents:
- A concise personal bio
- Interactive project cards with tech tags and direct GitHub links
- An animated neural-network-style canvas background reinforcing the technical identity
- A direct contact section (email, LinkedIn, GitHub) with no backend form required

---

## 4. Site Architecture | هيكل الموقع

الموقع **ثابت بالكامل (Static)** — لا يوجد خادم خلفي (Backend) ولا قاعدة بيانات، وهذا مقصود لأن طبيعة المحتوى (بورتفوليو شخصي) لا تتطلب تخزين بيانات ديناميكية:

```
Browser (Visitor)
      │
      ▼
GitHub Pages (Static Hosting)
      │
      ▼
index.html  ──▶  assets/css/style.css   (التنسيق)
      │      ──▶  assets/js/main.js      (السلوك: reveal + canvas + copy email)
      │      ──▶  assets/images/*.jpg    (الوسائط)
      ▼
Google Fonts (Tajawal, JetBrains Mono) — عبر CDN خارجي
```

**لماذا لا يوجد Backend أو API؟**
لأن الموقع لا يحتاج تسجيل دخول، ولا تخزين بيانات مستخدمين، ولا معالجة طلبات — كل التفاعل (البريد، الروابط) يتم عبر بروتوكولات المتصفح القياسية (`mailto:`, `target="_blank"`) أو JavaScript من جهة العميل فقط (Client-side).

*Site is fully static — no backend server or database, as the personal-portfolio content type doesn't require dynamic data storage. No login, no user data, no request processing; all interaction (email, links) happens via standard browser protocols or client-side JavaScript only.*

---

## 5. Design System | نظام التصميم

| العنصر | القيمة |
|---|---|
| الخط الأساسي | Tajawal (عربي) |
| الخط الثانوي | JetBrains Mono (للوسوم والأكواد) |
| لون الخلفية | `#0A0C12` (Ink) |
| لون التمييز | `#8C7CFF` (Violet) |
| لون ثانوي | `#D2A85C` (Gold) |
| نمط CSS | Utility-first مكتوب يدويًا (بدون Tailwind CDN) |
| الاتجاه | RTL (`dir="rtl"`) |
| الاستجابة | Mobile-first مع نقاط توقف عند 768px و1024px |

---

## 6. Tech Stack & Project Structure | التقنيات وبنية المشروع

**Tech Stack:**
- HTML5 (Semantic, RTL)
- CSS3 (Custom utility classes, no build step)
- Vanilla JavaScript (IntersectionObserver للـ scroll reveal، Canvas API للخلفية المتحركة)
- Google Fonts (Tajawal, JetBrains Mono)
- GitHub Pages (الاستضافة)

```
.
├── index.html                        # الصفحة كاملة (HTML + CSS + JS مدمجين)
├── assets/
│   └── images/
│       ├── ai-agent-builder.jpg
│       └── rafid-app-screenshots.jpg
├── README.md
├── LICENSE
└── .gitignore
```

> **ملاحظة:** الـ CSS وJavaScript مدمجين داخل `index.html` نفسه (بدل ملفات منفصلة) لتبسيط الرفع والصيانة عبر واجهة GitHub مباشرة — الصور فقط خارجية لأنها الأثقل حجمًا.

---

## 7. Featured Projects | المشاريع البارزة

| المشروع | الوصف | التقنيات |
|---|---|---|
| [رافد (Rafid)](https://github.com/rimasaldosari/Rafid) | مساعد مالي ذكي مدمج داخل تطبيق البنك، يقيّم جاهزية التمويل لأصحاب المنشآت الصغيرة والمتوسطة — Amad 2026 Hackathon | Fintech, AI Scoring, UX |
| [بوصلة الهاكثونات](https://github.com/rimasaldosari/Future-Makers-Gate) | منصة تفاعلية لاكتشاف الهاكثونات والمعسكرات في السعودية، مع مولّد أفكار مدعوم بالذكاء الاصطناعي | Streamlit, Python, AI |
| [محاكاة إدارة الحشود 2034](https://github.com/rimasaldosari/crowd-management-2034) | نظام محاكاة ذكي لإدارة الحشود، طُوّر ضمن هاكاثون Mega Future بمناسبة كأس العالم 2034 | AI Simulation, Crowd Management |

<p align="center">
  <img src="assets/images/ai-agent-builder.jpg" width="480" alt="محرر بناء وكيل ذكاء اصطناعي">
  <br><em>محرر بناء وكيل الذكاء الاصطناعي — عقدة AI Agent متصلة بذاكرة، نموذج، وأدوات بحث</em>
</p>

<p align="center">
  <img src="assets/images/rafid-app-screenshots.jpg" width="480" alt="لقطات شاشة لتطبيق رافد">
  <br><em>لقطات من تطبيق رافد: تسجيل الدخول، الرئيسية، ودرجة الجاهزية الائتمانية</em>
</p>

---

## 8. Visitor Journey | رحلة الزائر

1. **الوصول** → الزائر يصل عبر رابط مباشر أو محرك بحث
2. **الانطباع الأول (Hero)** → اسم، تخصص، وخلفية بصرية متحركة تعكس الهوية التقنية
3. **نبذة عني** → فهم سريع للخلفية الأكاديمية والاهتمامات
4. **المشاريع** → استعراض الأعمال الفعلية مع إمكانية الانتقال المباشر لكود كل مشروع على GitHub
5. **التواصل** → دعوة واضحة لإجراء (Call-to-Action) عبر البريد أو لينكد إن

---

## 9. Performance & Accessibility | الأداء وإمكانية الوصول

- ✅ لا مكتبات خارجية ثقيلة (بدون React/Vue/Tailwind CDN) → تحميل سريع
- ✅ الصور مستقلة عن الكود (وليست Base64) → تحميل متوازٍ وتخزين مؤقت (Caching) أفضل
- ✅ `prefers-reduced-motion` مدعوم → تعطيل الحركة لمن يفضّل ذلك
- ✅ تباين ألوان (Contrast) مناسب على الخلفية الداكنة
- ✅ عناصر تفاعلية مع `focus-visible` واضح لمستخدمي لوحة المفاتيح
- ⚠️ لا يوجد اختبار تلقائي (Automated Testing) — الموقع بسيط وثابت بما لا يستدعي ذلك حاليًا

---

## 10. Running Locally & Deployment | التشغيل والنشر

لا حاجة لأدوات بناء (Build Tools) — الموقع HTML/CSS/JS ثابت بالكامل.

```bash
git clone https://github.com/rimasaldosari/rimasaldosari.github.io.git
cd rimasaldosari.github.io
python3 -m http.server 8000
# افتحي المتصفح على http://localhost:8000
```

**النشر (Deployment):** يتم تلقائيًا عبر **GitHub Pages** من فرع `main` في هذا المستودع — أي تعديل يُدفع (push) للفرع الرئيسي يظهر مباشرة على الموقع المباشر خلال دقائق.

---

## 11. Contact | التواصل

- 📧 Email: [remas142909@gmail.com](mailto:remas142909@gmail.com)
- 💼 LinkedIn: [rimas-aldosari](https://www.linkedin.com/in/rimas-aldosari-656a23375)
- 🐙 GitHub: [@rimasaldosari](https://github.com/rimasaldosari)

---

## 12. Appendix | الملحق

### الرخصة | License
هذا المشروع مرخّص تحت [رخصة MIT](LICENSE).

### ملاحظات تقنية | Technical Notes
- تم استخراج الصور من صيغة Base64 المدمجة سابقًا داخل HTML إلى ملفات مستقلة في `assets/images/` لتحسين الأداء وسهولة الصيانة.
- الـ CSS وJavaScript مدمجين عمدًا داخل `index.html` (وليسا في ملفات منفصلة) لتبسيط رفع المشروع وتعديله عبر واجهة GitHub مباشرة، مع تفادي مشاكل الروابط النسبية بين الملفات.

### الفريق | Team
- **ريماس الدوسري** — تصميم، تطوير، ومحتوى كامل الموقع
