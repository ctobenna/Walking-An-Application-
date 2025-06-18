# 🔍 Web Application Manual Analysis Lab – TryHackMe Walkthrough

## 🧠 Objective

The goal of this lab was to manually analyze a web application for security issues using only browser-based tools—without the use of automated scanners or extensions. This is a fundamental skill for any aspiring penetration tester, especially when dealing with real-world black-box assessments.

---

## 🛠️ Tools Used

- **Web Browser Developer Tools**
  - Elements Tab
  - Sources (Debugger)
  - Network Tab

---

## 🔎 What I Did

### 1. Manual Crawling and Source Code Review

- I started by viewing the **page source** to identify hidden content and links not visible in the user interface.
- Manually followed embedded links and references to discover directories and files that were not publicly exposed.
- Discovered a hidden **flag** by navigating through the directory structure hinted at in the source.

### 2. DOM & CSS Manipulation with Inspect Tool

- Inspected the DOM structure to find content visually hidden using CSS.
- Overrode CSS styles directly in the browser to make hidden flags and sections visible.
- Example: Modified a `display: none` or `color: transparent` property to uncover content.

### 3. JavaScript Debugging with Sources Tab

- Used the **Sources tab** to:
  - Trace the behavior of scripts controlling content rendering.
  - Identify a specific script that caused a flash of content to appear and disappear.
  - Paused script execution and altered values to reveal the target flag.

### 4. Monitoring HTTP Requests with Network Tab

- Observed **AJAX/XHR requests** made to the server when interacting with the site.
- Analyzed request/response payloads to view background data transfers.
- Identified dynamically loaded content without full page reloads.

---

## 💡 Key Takeaways

- Web applications often contain overlooked or hidden resources in the code that attackers may exploit.
- Manual testing fosters a deeper understanding of **frontend behavior**, **client-server communication**, and **developer oversights**.
- Browser DevTools alone can be powerful in identifying:
  - Hidden elements
  - Debug information
  - Improperly secured client-side data

---
<p align="center">
  <img src="https://i.imgur.com/krReyQL.png" height="80%" weight="80%" alt="complete Badge on tryhackme">
</p>
    
## 🧑‍💻 Skills Gained

- Manual web crawling
- DOM manipulation
- Real-time code debugging
- Traffic inspection via AJAX
- Practical application of OWASP Top 10 issues like **Security Misconfiguration** and **Sensitive Data Exposure**

---
