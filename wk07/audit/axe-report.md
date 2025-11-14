# axe DevTools Audit Report — Week 7

**Date**: [YYYY-MM-DD]
**URL**: http://localhost:8080/tasks
**Tool**: axe DevTools 4.x
**Scope**: Full page scan (add form + task list)

---

## Summary
- **Critical**: 1
- **Serious**: 4
- **Moderate**: 0
- **Minor**: 0
- **Total**: 5 issues

---

## Critical Issues

### Issue 1: Image lacking alternative text (critical)
**Element**: `<img src="/static/img/icon.png" width="16" height="16">`
**Rule**: `non-text content` (WCAG 2.1, 2.2)
**Description**: Ensure <img> elements have alternative text or a role of none or presentation.
**Impact**: Screen readers can't describe the image without alternative text.
**Fix**: Add alt attribute to image.
**Status**: 

---

## Serious Issues

### Issue 2: Links lack discernible text (Serious)
**Element**: `<a href="/about"></a>`
**Rule**: `label` (WCAG 1.3.1, 4.1.2)
**Description**: Link elements are inaccessible to screen readers.
**Impact**: Screen readers don't describe the link.
**Fix**: Add image attribute to link.
**Status**: 

### Issue 3: Insufficient color contrast (Serious)
**Element**: `<<button type="submit">Add Task</button>`
**Rule**: `color-contrast` (WCAG 1.4.3)
**Description**: Text color #6c757d on background color #0172ad = 1.11 (fails AA 4.5:1)
**Impact**: People with low vision struggle to read button text.
**Fix**: Change button color to #495057 (darker gray, 7:1 contrast).
**Status**: 

### Issue 4: Insufficient color contrast (Serious)
**Element**: `<button type="submit" aria-label="Delete task: Test Task">Delete</button>`
**Rule**: `color-contrast` (WCAG 1.4.3)
**Description**: Text color #6c757d on background color #0172ad = 1.11 (fails AA 4.5:1)
**Impact**: People with low vision struggle to read button text.
**Fix**: Change button color to #495057 (darker gray, 7:1 contrast).
**Status**: 

### Issue 5: Insufficient color contrast (Serious)
**Element**: `<button type="submit" aria-label="Delete task: Kotlin 2.2.21 Works">Delete</button>`
**Rule**: `color-contrast` (WCAG 1.4.3)
**Description**: Text color #6c757d on background color #0172ad = 1.11 (fails AA 4.5:1)
**Impact**: People with low vision struggle to read button text.
**Fix**: Change button color to #495057 (darker gray, 7:1 contrast).
**Status**: 


---

## Moderate Issues

---

## Minor Issues

---

## Actions
1. **(Issue 1)**: Add alt attribute
2. **(Issue 2)**: Add title attribute
3. **(Issue 3-5)**: Fix contrast ratio → Add to backlog

---

**Next step**: Manual testing to catch issues axe misses (focus order, SR announcements, keyboard traps).
