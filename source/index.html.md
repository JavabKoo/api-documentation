---
title: راهنمای API جواب‌کو

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - javascript

toc_footers:
  - <a href='#'>دریافت کلید توسعه‌دهنده</a>


includes:
  - questions
  - errors

search: true
---

# معرفی

جواب‌کو یک جامعه می‌باشد با هدف بالاتر بردن سطح فرهنگ و دانش فارسی‌زبانان دنیا.

# احراز هویت

وب سرویس جواب‌کو برای احراز هویت از استاندارد
OAuth2.0
استفاده می‌کند.

در هر درخواست باید
Authorization
در هدر به صورت
Bearer
فرستاده شود. درخواست‌هایی که در آنها هدر
Authorization
فرستاده نشود با خطا روبرو می‌شوند.
