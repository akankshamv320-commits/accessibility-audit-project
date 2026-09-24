# Accessibility Audit Report

1. Introduction

An accessibility audit was carried out on the W3C Before/After Demo website to identify common accessibility problems that may affect users with disabilities.
The audit mainly focused on Lighthouse accessibility checks and basic keyboard navigation.

2. Website Audited

**Website:** W3C Before/After Demo – Before Page

**URL:** https://www.w3.org/WAI/demos/bad/before/home.html

**Tool Used:** Google Chrome Lighthouse

**Accessibility Score:** 50/100

3. Audit Method

The following methods were used during the audit:

- Lighthouse accessibility audit
- Keyboard-only navigation
- Checking the visibility and order of keyboard focus
- Reviewing the accessibility errors reported by Lighthouse

Five main accessibility issues were identified from the Lighthouse report.

4. Accessibility Issues Found

4.1 Images Without Alternative Text

**WCAG Reference:** 1.1.1 – Non-text Content

**Priority:** High

Lighthouse reported that some image elements do not have an `alt` attribute. The expanded Lighthouse result also showed multiple affected image elements.
This can cause problems for screen-reader users because the purpose or information contained in an image may not be available to them.

**Suggested Fix:**  
Add suitable `alt` text to informative images. Decorative images can use an empty `alt` attribute.

---

4.2 Select Elements Without Labels

**WCAG Reference:** 3.3.2 – Labels or Instructions

**Priority:** High

Lighthouse reported that some select elements do not have associated label elements.

Without a proper label, users using assistive technologies may not clearly understand what the selection control is for.

**Suggested Fix:**  
Add a proper `<label>` and associate it with the corresponding select element.

---

4.3 Links Without a Discernible Name

**WCAG Reference:** 2.4.4 – Link Purpose (In Context)

**Priority:** High

Lighthouse reported that some links do not have a discernible name.

This can make it difficult for screen-reader users to understand the purpose of a link.

**Suggested Fix:**  
Provide meaningful visible link text or another suitable accessible name.

---

4.4 Insufficient Color Contrast

**WCAG Reference:** 1.4.3 – Contrast (Minimum)

**Priority:** Medium

Lighthouse reported that some foreground and background color combinations do not have sufficient contrast.

Low contrast can make text difficult to read, especially for users with low vision.

**Suggested Fix:**  
Change the foreground or background colors so that the required WCAG contrast level is achieved.

---

4.5 Missing Language Attribute

**WCAG Reference:** 3.1.1 – Language of Page

**Priority:** Medium

Lighthouse reported that the `<html>` element does not have a `lang` attribute.

The language attribute helps browsers and assistive technologies understand the default language of the page.

**Suggested Fix:**  
Add the appropriate language attribute to the HTML element, for example:

`<html lang="en">`

5. Keyboard Navigation

A basic keyboard-only check was also carried out.

The main observations were:

- Interactive elements could be reached using the Tab key.
- The focus order was generally logical.
- Focus was visible, but the focus indicator was quite faint.
- The language selection control could be opened using the keyboard.
- Pressing Escape did not close the control.
- Focus could still move to the next element, so no keyboard trap was observed.

6. Priority of Issues

The issues were given a priority based on their possible effect on users.

**High Priority**
- Images without alternative text
- Select elements without labels
- Links without a discernible name

**Medium Priority**
- Insufficient color contrast
- Missing language attribute

7. Conclusion

The audit identified five accessibility problems on the W3C Before/After Demo page.
The main problems were related to images, form controls, links, color contrast, and page language. Fixing these issues would improve the accessibility and usability of the page for users who depend on assistive technologies.
