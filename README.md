<div align="center">

<img src="https://ik.imagekit.io/imgayoub/LOGO/ayoub.pw%20logo%20many%20size/no%20background/android-chrome-512x512.png" width="90" alt="ayoub.pw logo" />

# 📞 CallMe

**اتصال صوتي وفيديو خاص — بينك وبين من تختار**

[![Live](https://img.shields.io/badge/🌐_Live-callme.ayoub.pw-00e5ff?style=for-the-badge&labelColor=060613)](https://callme.ayoub.pw)
[![By](https://img.shields.io/badge/by-ayoub.pw-7c3aed?style=for-the-badge&labelColor=060613)](https://ayoub.pw)
[![Stack](https://img.shields.io/badge/Stack-HTML_+_Supabase_+_Agora-f59e0b?style=for-the-badge&labelColor=060613)](#التقنيات)
[![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge&labelColor=060613)](#)

---

*تطبيق اتصال مباشر خاص — شات نصي، صوت، وفيديو — بدون خوادم، بدون متجر، بدون تعقيد*

</div>

---

## 📋 المحتويات

- [لمحة عن المشروع](#-لمحة-عن-المشروع)
- [المميزات](#-المميزات)
- [التقنيات](#-التقنيات)
- [كيف يعمل](#-كيف-يعمل)
- [طريقة الاستخدام](#-طريقة-الاستخدام)
- [إعداد Supabase](#-إعداد-supabase)
- [إعداد Agora](#-إعداد-agora)
- [النشر](#-النشر)
- [هيكل المشروع](#-هيكل-المشروع)
- [خارطة الطريق](#-خارطة-الطريق)
- [المطوّر](#-المطوّر)

---

## 🌟 لمحة عن المشروع

**CallMe** هو تطبيق اتصال خاص مصمم للتواصل المباشر بين شخصين فقط — بدون حسابات معقدة، بدون قواعد بيانات ثقيلة، وبدون الحاجة لتنزيل أي شيء.

يعمل مباشرة من المتصفح كـ **Progressive Web App (PWA)**، ويدعم ثلاث قنوات تواصل في واجهة واحدة أنيقة:

```
💬  شات نصي فوري    →  Supabase Realtime
📞  مكالمة صوتية    →  Agora RTC
🎥  مكالمة فيديو    →  Agora RTC
```

---

## ✨ المميزات

### 🔴 متاح الآن
| المميزة | التفاصيل |
|---|---|
| 💬 **شات فوري** | رسائل نصية تصل فورياً بدون إعادة تحميل |
| 🟢 **حالة الاتصال** | يظهر متصل / غير متصل في الوقت الفعلي |
| 📞 **مكالمة صوتية** | جودة عالية عبر Agora RTC |
| 🎥 **مكالمة فيديو** | فيديو HD مع عرض محلي في الزاوية |
| 🔇 **كتم الصوت** | تحكم فوري بالميكروفون خلال المكالمة |
| 📵 **إيقاف الكاميرا** | تعطيل الفيديو بضغطة واحدة |
| ⏱️ **مؤقت المكالمة** | يعرض مدة الاتصال لحظة بلحظة |
| 🔔 **إشعار المكالمة** | شاشة قبول / رفض فورية |
| 📱 **PWA** | يُثبَّت على الموبايل كتطبيق أصلي |
| 🌙 **Dark Mode** | واجهة داكنة بتصميم مستقبلي |

### 🔜 قادم قريباً
- 🔐 تشفير الرسائل (E2E)
- 🔔 Push Notifications
- 🎙️ رسائل صوتية
- 📎 مشاركة الملفات
- 📜 تاريخ المحادثات

---

## 🛠️ التقنيات

```
┌─────────────────────────────────────────────────────┐
│                    CallMe Stack                      │
├─────────────────────────────────────────────────────┤
│  Frontend     →  HTML5 + CSS3 + Vanilla JS           │
│  Realtime     →  Supabase Realtime (WebSocket)       │
│  Database     →  Supabase PostgreSQL                 │
│  Video/Audio  →  Agora RTC Web SDK v4.21             │
│  Hosting      →  Cloudflare Pages                    │
│  Domain       →  callme.ayoub.pw                     │
└─────────────────────────────────────────────────────┘
```

| التقنية | الدور | الخطة المجانية |
|---|---|---|
| **Supabase** | قاعدة البيانات + Realtime | 500MB + Realtime مجاني |
| **Agora** | صوت وفيديو P2P | 10,000 دقيقة/شهر مجاناً |
| **Cloudflare** | Hosting + CDN + SSL | مجاني بالكامل |

---

## ⚙️ كيف يعمل

```
الشخص A                   Supabase                  الشخص B
    │                          │                         │
    │── دخول (أون لاين) ───────▶│                         │
    │                          │◀────── دخول (أون لاين) ──│
    │                          │                         │
    │── إرسال رسالة ───────────▶│── إشعار فوري ──────────▶│
    │                          │                         │
    │── طلب مكالمة ────────────▶│── إشعار واردة ─────────▶│
    │                          │◀──── قبول ──────────────│
    │                          │                         │
    │◀══════════ Agora P2P: صوت + فيديو مباشر ══════════▶│
    │                          │                         │
    │── إنهاء المكالمة ─────────▶│── إشعار انتهاء ─────────▶│
```

---

## 🚀 طريقة الاستخدام

### على الموبايل
1. افتح **[callme.ayoub.pw](https://callme.ayoub.pw)** في المتصفح
2. اضغط **"أضف إلى الشاشة الرئيسية"** لتثبيته كتطبيق
3. أدخل اسمك واسم الشخص الثاني
4. ابدأ المحادثة فوراً 🎉

### للاتصال بالصوت أو الفيديو
```
1. تأكد أن الطرف الآخر مفتوح التطبيق (● متصل الآن)
2. اضغط 📞 للصوت  أو  🎥 للفيديو
3. سيظهر إشعار للطرف الآخر
4. بعد القبول — يبدأ الاتصال مباشرة
```

> **ملاحظة:** يجب أن يكون الاسمان متطابقَيْن في الجهازين  
> مثال: الجهاز A يكتب `أيوب` ← → الجهاز B يكتب `أيوب` كاسم الشريك

---

## 🗄️ إعداد Supabase

افتح **SQL Editor** في مشروع Supabase والصق:

```sql
-- جدول الحضور
CREATE TABLE IF NOT EXISTS call_users (
  id         UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  username   TEXT UNIQUE NOT NULL,
  status     TEXT DEFAULT 'offline',
  updated_at TIMESTAMPTZ DEFAULT now()
);

-- جدول إشارات المكالمات
CREATE TABLE IF NOT EXISTS calls (
  id         UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  caller     TEXT NOT NULL,
  callee     TEXT NOT NULL,
  status     TEXT DEFAULT 'pending',
  type       TEXT DEFAULT 'voice',
  room_id    TEXT,
  created_at TIMESTAMPTZ DEFAULT now()
);

-- جدول الرسائل
CREATE TABLE IF NOT EXISTS call_messages (
  id         UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  sender     TEXT NOT NULL,
  receiver   TEXT NOT NULL,
  content    TEXT NOT NULL,
  created_at TIMESTAMPTZ DEFAULT now()
);

-- تفعيل Realtime
ALTER PUBLICATION supabase_realtime ADD TABLE call_users;
ALTER PUBLICATION supabase_realtime ADD TABLE calls;
ALTER PUBLICATION supabase_realtime ADD TABLE call_messages;

-- فتح الصلاحيات (للتطوير)
ALTER TABLE call_users    ENABLE ROW LEVEL SECURITY;
ALTER TABLE calls         ENABLE ROW LEVEL SECURITY;
ALTER TABLE call_messages ENABLE ROW LEVEL SECURITY;

CREATE POLICY "open_all" ON call_users    FOR ALL USING (true) WITH CHECK (true);
CREATE POLICY "open_all" ON calls         FOR ALL USING (true) WITH CHECK (true);
CREATE POLICY "open_all" ON call_messages FOR ALL USING (true) WITH CHECK (true);
```

---

## 🎙️ إعداد Agora

```
1. سجّل في agora.io
2. أنشئ مشروعاً جديداً
3. اذهب إلى:
   Project Management → مشروعك → Security
   → Authentication Mechanism → Testing Mode (No Token)
4. انسخ App ID وضعه في الكود:
   const AGORA_APP_ID = 'your-app-id-here';
```

---

## 🌐 النشر

### على Cloudflare Pages (مُوصى به)
```bash
# 1. ارفع callme.html على GitHub
# 2. اذهب إلى Cloudflare Dashboard
# 3. Pages → Create a project → Connect to GitHub
# 4. اختر الـ repo
# 5. أضف Custom Domain: callme.ayoub.pw
```

### على GitHub Pages
```bash
# 1. أنشئ repo باسم callme
# 2. ارفع callme.html → أعد تسميته index.html
# 3. Settings → Pages → Deploy from main
# 4. الرابط: algoushah.github.io/callme
```

---

## 📁 هيكل المشروع

```
callme/
│
├── index.html          ← التطبيق بالكامل (ملف واحد)
├── README.md           ← هذا الملف
│
└── supabase/
    └── setup.sql       ← SQL لإنشاء الجداول
```

> **فلسفة البناء:** ملف HTML واحد — بدون frameworks، بدون npm، بدون تعقيد.

---

## 🗺️ خارطة الطريق

```
v1.0  ✅  شات + إشارة مكالمة (Supabase Realtime)
v1.1  ✅  صوت وفيديو حقيقي (Agora RTC)
v1.2  🔜  Push Notifications
v1.3  🔜  رسائل صوتية
v1.4  🔜  تشفير E2E
v2.0  🔜  دعم أكثر من شخصين (غرف)
```

---

## 👨‍💻 المطوّر

<div align="center">

<img src="https://ik.imagekit.io/imgayoub/LOGO/ayoub.pw%20logo%20many%20size/no%20background/android-chrome-192x192.png" width="64" alt="ayoub.pw" />

**Ayoub**

[![Website](https://img.shields.io/badge/🌐-ayoub.pw-00e5ff?style=flat-square&labelColor=060613)](https://ayoub.pw)
[![GitHub](https://img.shields.io/badge/GitHub-algoushah-7c3aed?style=flat-square&logo=github&labelColor=060613)](https://github.com/algoushah)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-ayoub--k-0077b5?style=flat-square&logo=linkedin&labelColor=060613)](https://www.linkedin.com/in/ayoub-k)
[![Instagram](https://img.shields.io/badge/Instagram-algoushah-e1306c?style=flat-square&logo=instagram&labelColor=060613)](https://www.instagram.com/algoushah/)

*Vienna, Austria 🇦🇹*

</div>

---

<div align="center">

صُنع بـ ❤️ في فيينا — **[callme.ayoub.pw](https://callme.ayoub.pw)**

<sub>© 2026 ayoub.pw — All rights reserved</sub>

</div>
