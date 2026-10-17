# 📅 ExpCalc Pro — Exact Date Work Experience Calculator

> An exact, day-level work experience calculator that automatically deduplicates overlapping parallel roles to output your true calendar career span for resumes and LinkedIn.

[![Live Demo](https://img.shields.io/badge/Live_Demo-ExpCalc_Pro-3b82f6?style=for-the-badge&logo=githubpages&logoColor=white)](https://lakhamohit.github.io/ExpCalcPro/)
[![License: MIT](https://img.shields.io/badge/License-MIT-emerald?style=for-the-badge)](LICENSE)

---

## 🌟 Overview

When updating resumes or LinkedIn profiles, calculating total years of experience manually often leads to errors. Standard addition fails when you hold **concurrent roles** (e.g., full-time jobs, freelance work, or parallel training positions), leading to double-counting.

**ExpCalc Pro** fixes this by using **interval-merging algorithms** to deduplicate overlapping work timelines, providing exact day-level precision alongside raw cumulative duration.

---

## ✨ Key Features

* **🎯 Exact Day-Level Precision:** Uses standard HTML date pickers to compute calculations down to the specific day.
* **🛡️ Smart Overlap Deduplication:** Automatically merges overlapping intervals so concurrent positions are not double-counted in your total calendar experience.
* **📊 Dual Calculation Modes:**
  * **Unique Timeline Span:** De-duplicated standard resume format (True calendar span).
  * **Cumulative Total:** Sum of all individual job durations logged back-to-back.
* **⚡ Active Role Tracking:** Check "Present" on active roles to automatically calculate tenure up to today's date.
* **📋 1-Click Formatted Snippet:** Instantly copy a pre-formatted text summary ready to paste into CVs, cover letters, or profiles.
* **🌓 Dark / Light Theme Support:** Fully responsive glassmorphism UI built with Tailwind CSS.

---

## 🚀 Live Demo

Access the hosted web application anytime on GitHub Pages:  
👉 **[https://lakhamohit.github.io/ExpCalcPro/](https://lakhamohit.github.io/ExpCalcPro/)**

---

## 🛠️ Tech Stack

* **Frontend:** HTML5, Tailwind CSS
* **Icons:** FontAwesome 6 & Lucide Icons
* **Scripting:** Vanilla JavaScript (ES6+)
* **Hosting:** GitHub Pages

---

## 💻 Local Setup & Installation

Since **ExpCalc Pro** is built with zero external build dependencies, you can run it locally in seconds:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/lakhamohit/ExpCalcPro.git](https://github.com/lakhamohit/ExpCalcPro.git)

---
##  🧮 How It Works (The Math)
  1. Interval Creation: Each work entry is converted into an interval $[T_{\text{start}}, T_{\text{end}}]$ in Unix timestamp milliseconds.
  2. Sorting & Merging: Intervals are sorted by start date and merged if $T_{\text{start, next}} \le T_{\text{end, current}}$.
  3. Calendar Conversion: Unique days are calculated via exact day differences:$$\text{Years} = \lfloor \text{Days} / 365.25 \rfloor$$$$\text{Months} = \lfloor (\text{Days} \pmod{365.25}) / 30.4375 \rfloor$$
