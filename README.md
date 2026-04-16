# 🎓 QuizHub — بوابة الكويزات التفاعلية

## 📁 هيكل المجلدات

```
quizhub/
├── index.html          ← الموقع الرئيسي (لا تعدله)
├── subjects.json       ← قائمة المواد والمحاضرات (هنا تتحكم في كل شيء)
├── README.md           ← التعليمات دي
└── quizzes/
    ├── Dialysis_quiz.html
    ├── quiz2.html
    └── ...
```

---

## ✅ كيف ترفع الموقع على GitHub Pages (مجاني)

### الخطوة 1 — إنشاء حساب
اذهب إلى [github.com](https://github.com) وسجّل حساباً مجانياً

### الخطوة 2 — إنشاء Repository
- اضغط على **＋** ثم **New repository**
- اسمه: `quizhub`
- اختر **Public**
- اضغط **Create repository**

### الخطوة 3 — رفع الملفات
- اضغط **uploading an existing file**
- ارفع كل الملفات والمجلد `quizzes` كاملاً
- اضغط **Commit changes**

### الخطوة 4 — تفعيل GitHub Pages
- اذهب إلى **Settings** في الـ Repository
- من القائمة الجانبية اختر **Pages**
- في **Source** اختر: `Deploy from a branch`
- في **Branch** اختر: `main` ثم `/ (root)`
- اضغط **Save**
- انتظر دقيقة، لينكك هيكون:
  👉 `https://YOUR_USERNAME.github.io/quizhub`

---

## ➕ كيف تضيف مادة جديدة

افتح ملف `subjects.json` وأضف كائن جديد في المصفوفة:

```json
{
  "id": "anatomy",
  "name": "Anatomy",
  "nameAr": "التشريح",
  "emoji": "🦴",
  "color": "#10b981",
  "lectures": [
    {
      "id": "lecture1",
      "name": "Lecture 1",
      "nameAr": "المحاضرة الأولى",
      "file": "quizzes/anatomy_lec1.html",
      "questions": 40
    }
  ]
}
```

ثم ارفع ملف الكويز في مجلد `quizzes/`

---

## ➕ كيف تضيف محاضرة لمادة موجودة

في `subjects.json` أضف عنصر جديد داخل مصفوفة `lectures`:

```json
{
  "id": "dialysis2",
  "name": "Dialysis Quiz 2",
  "nameAr": "كويز الديلاليز 2",
  "file": "quizzes/Dialysis_quiz2.html",
  "questions": 50
}
```

---

## 🔄 كيف تحدث الموقع بعد الإضافة

1. افتح الـ Repository على GitHub
2. ارفع الملفات الجديدة
3. الموقع يتحدث تلقائياً خلال 1-2 دقيقة
