# 🛠 Build Guide — AIHawk Job Application Agent

[English](#english) · [فارسی](#فارسی) · [العربية](#العربية) · [README](./README.md)

> **Verified status:** Extensible automation agent; provider plugins are not included

## English

### 1. Prerequisites

- Python, Selenium, undetected-chromedriver
- LangChain
- OpenAI, Anthropic, Gemini, Hugging Face, Ollama
- pdfminer.six, ReportLab

Use an isolated environment or container. Prefer the committed lockfile over unconstrained upgrades.

### 2. Environment variables and services

- Selected LLM API key
- Browser/profile configuration

Store secrets outside Git. Use least-privilege accounts and separate development, staging and production values.

### 3. Development setup

```bash
python -m venv .venv
```

```bash
source .venv/bin/activate
```

```bash
pip install -r requirements.txt
```

- Copy sample configuration and add selected provider credentials

- Run the documented entry point

### 4. Production build

- No compiled build

### 5. Tests and validation

- pytest -q

### 6. Known blockers and cautions

- Provider plugins were removed
- Automation must comply with platform terms

### 7. Release checklist

- Build from a clean checkout with the lockfile.
- Record runtime versions and the final artifact checksum.
- Run dependency, license and secret scanning.
- Confirm that uploaded files, fixtures and logs contain no confidential data.
- Apply migrations with a backup and tested rollback path.
- Use read-only or least-privilege credentials where possible.
- Add health checks, monitoring, backups and rollback instructions.
- Review domain obligations for medical, biometric, hiring, financial or cryptocurrency systems.

### 8. Troubleshooting

1. Confirm the current directory and runtime versions.
2. Check ports, database/queue availability and model files.
3. Inspect logs without printing tokens or passwords.
4. Reproduce from a clean virtual environment or container.
5. Do not delete lockfiles or force-upgrade packages until the original build is reproduced.
6. For repositories marked incomplete or recovery-only, complete the stated remediation before deployment.

---

## فارسی

### پیش‌نیاز و محیط

فناوری‌های بخش انگلیسی بالا پیش‌نیازهای مرجع پروژه هستند. محیط مجازی یا کانتینر جداگانه بسازید، Lockfile را حفظ کنید و کلید واقعی را داخل Git قرار ندهید.

### راه‌اندازی توسعه

دستورات بخش **Development setup** را به‌ترتیب اجرا کنید. قبل از هر دستور، مسیر جاری ترمینال، نسخه Runtime و فعال‌بودن سرویس‌های وابسته را کنترل کنید.

### Build و تست

- دستورات **Production build** را از Checkout تمیز اجرا کنید.
- تست‌ها و چک‌لیست **Tests and validation** را انجام دهید.
- نسخه ابزارها، هش خروجی و تنظیمات استقرار را ثبت کنید.
- در مخزن ناقص، ابتدا مانع مستندشده را برطرف کنید و نتیجه را دوباره اعتبارسنجی کنید.

### چک‌لیست انتشار

- اسکن Dependency، License و Secret انجام شود.
- داده شخصی، فایل آپلودی، Log و Fixture بررسی شود.
- Migration همراه Backup و Rollback آزمایش‌شده باشد.
- دسترسی‌ها حداقلی و استقرار نخست در محیط غیرعملیاتی باشد.
- مانیتورینگ، Health Check و Backup آماده باشد.

---

## العربية

### المتطلبات والبيئة

التقنيات المذكورة في القسم الإنجليزي هي المتطلبات المرجعية. استخدم بيئة معزولة أو حاوية، حافظ على ملفات القفل، ولا تضع مفاتيح حقيقية داخل Git.

### إعداد التطوير

نفذ أوامر **Development setup** بالترتيب، وتأكد من المسار وإصدارات التشغيل والخدمات التابعة قبل كل خطوة.

### البناء والاختبار

- نفذ **Production build** من نسخة نظيفة.
- شغّل **Tests and validation**.
- سجل إصدارات الأدوات وبصمة الملف الناتج وإعدادات النشر.
- في المستودعات غير المكتملة عالج العائق الموثق قبل النشر.

### قائمة الإصدار

- افحص التبعيات والتراخيص والأسرار.
- راجع البيانات الشخصية والملفات والسجلات.
- اختبر الترحيلات مع نسخة احتياطية وخطة تراجع.
- استخدم أقل صلاحيات وابدأ ببيئة غير إنتاجية.
- جهز المراقبة وفحوص الصحة والنسخ الاحتياطية.
