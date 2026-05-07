# Chatterbox House Website Improvement Report

**Overall Rating:** 7.5/10 (DeepSeek) / 7/10 (Sir Willy)
**Date:** May 7, 2026
**Status:** Work in progress

---

## What's Working Well

| Element | Why It's Good |
|---------|---------------|
| Pricing transparency | Every class shows 税抜/税込 pricing. Huge trust builder. |
| Bilingual switching | Clean implementation. Critical for mixed Japanese/international families. |
| Real teacher photos | Actual faces (Tony, Jay, Minako) — not stock images. |
| Small class sizes visible | "定員 2–4名" immediately signals personal attention. |
| Phone number everywhere | Banner, floating buttons, contact section. Phone is king for Japanese clients. |
| Google Map embedded | Essential for "where exactly is this school?" |
| Netlify forms with reCAPTCHA | Good spam protection. |
| Urgency messaging | "人気の時間帯はすぐに埋まります" — smart psychological nudge. |
| Updated copy | No outdated promotions, current 2026 copyright. |

---

## High-Priority Improvements

### 1. Hero Section — Visibility Issue
**Status:** Pending
**Risk:** Low
**Description:** On desktop, the hero background (shop.webp) may be washed out due to gradient overlays. Remove unused `.carousel-slide::before` styles if you're not using the carousel anymore.

### 2. Add Trust Badge Section
**Status:** Pending
**Risk:** Medium
**Description:** After the hero, add a thin strip with trust elements:
- "ネイティブ講師在籍"
- "入会金¥0"
- "兄弟割引あり" (if applicable)

### 3. Student/Parent Testimonials
**Status:** SKIPPED (requires parent permission)
**Reason:** Tony prefers authenticity over fake testimonials.

### 4. Line Official Account Integration
**Status:** Pending
**Risk:** Low
**Description:** Create a free Line Official Account and:
- Replace 📱 footer icon with Line link
- Add "Lineで簡単予約" button alongside phone/email

### 5. Fix Google Maps JS Error
**Status:** ✅ COMPLETED (May 7, 2026)
**Risk:** Very Low
**Description:** Remove unused `initMap()` function and script injection — you're using iframe embed, don't need the API call.
**Commit:** a027be5 - "Remove unused Google Maps API code (using iframe embed instead)"

---

## Medium Priority (Conversion Optimization)

### 6. Make "Special Evening Class" More Discoverable
**Status:** Pending
**Risk:** Low
**Description:** Add a banner above classes section: *"中高生向け・夜7時からの特別クラス — 1回 ¥4,400"*

### 7. Add FAQ Section
**Status:** PENDING CONTENT APPROVAL
**Risk:** Low
**Description:** Japanese clients check FAQs before contacting. Common questions:
- 振替授業はありますか？
- 教材費はかかりますか？
- 兄弟割引は？
- 駐車場はありますか？

### 8. Contact Form — Auto-Reply Confirmation
**Status:** Pending
**Risk:** Low
**Description:** Add success message after submission (redirect to /thank-you or inline "送信しました").

### 9. Fix Footer Social Icons
**Status:** Pending
**Risk:** Low
**Description:** Replace `#` links with real URLs (Line, Facebook, Instagram). If you don't have them, hide the icons.

---

## Low Priority (Polish)

### 10. Mobile Hover States
**Status:** Pending
**Risk:** Very Low
**Description:** Wrap `:hover` styles in `@media (hover: hover)` so they only apply on true hover devices.

### 11. Image Alt Text
**Status:** Pending
**Risk:** Very Low
**Description:** Use descriptive alt attributes: `alt="Tony - British English teacher at Chatterbox House in Neyagawa"`

### 12. Performance
**Status:** Pending
**Risk:** Low
**Description:**
- Add `font-display: swap` to Google Fonts
- Resize images to exact display dimensions (max 1200px wide)
- Enable Netlify asset optimization

---

## Section-by-Section Grades

| Section | DeepSeek | Sir Willy | Notes |
|---------|----------|-----------|-------|
| Hero | B+ | B | Strong CTAs, bilingual. Image could be brighter. |
| About | B+ | B | Good info, real photo. Add "since 2020" badge. |
| Classes & Pricing | A- | A | Excellent transparency. Add FAQ link. |
| Teachers | B | B | Real photos great. Needs testimonials. |
| Contact | B+ | B | Good form, map. Missing Line + success message. |
| Footer | C+ | C | Functional but dead social links. |

---

## Change Log

### May 7, 2026
- ✅ Updated copyright to 2026
- ✅ Removed outdated "8月限定" August special copy
- ✅ Created this improvement report
- ✅ Created site update workflow document

---

## Next Steps

1. Fix Google Maps JS error (remove unused code)
2. Fix footer social icons (remove dead links)
3. Make evening class more discoverable
4. Add FAQ section (pending content approval)
5. Add trust badge section
6. Line Official Account integration
7. Contact form success message
8. Performance optimizations
9. Mobile hover states
10. Image alt text improvements

---

## Notes

- **Testimonials skipped:** Tony prefers authenticity over fake testimonials. Would require parent permission anyway.
- **FAQ content:** Need to ask Tony about specific questions and answers before creating.
- **Line integration:** Need Tony to create Line Official Account first.
- **One change at a time:** Push each change individually, verify, revert if problems arise.
