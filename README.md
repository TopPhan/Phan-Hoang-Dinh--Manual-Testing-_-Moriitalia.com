📄 Project: Manual Testing – https://moriitalia.com  
📅 Execution Period: September 28, 2025 – October 17, 2025

👤 Tester: Hoàng Đỉnh

A manual testing project targeting [Moriitalia.com](https://moriitalia.com) — a Vietnamese e-commerce website selling kitchen and lifestyle products. Covers **Black Box Functional Testing** and **Smoke Testing** across 10 core modules, with complete test case documentation, defect logging, and a final summary report.

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Testing Methodology](#-testing-methodology)
- [Project Structure](#-project-structure)
- [Test Coverage by Module](#-test-coverage-by-module)
- [Defect Summary](#-defect-summary)
- [Key Defects Found](#-key-defects-found)
- [Test Results & Quality Assessment](#-test-results--quality-assessment)
- [Planning](#-planning)
- [Deliverables](#-deliverables)

---

## 🌿 Project Overview

This project performs a comprehensive **manual functional test** of the Moriitalia.com e-commerce platform, covering all critical user journeys from account registration through to order placement. The goal was to identify bugs, measure test coverage, and provide a quality assessment before release.

| Metric | Target | Achieved |
|---|---|---|
| 🧪 Total Test Cases Written | — | **216** |
| ▶️ Test Cases Executed | ≥ 90% | **166** (76.9%) |
| ✅ Test Cases Passed | ≥ 85% | **142** (85.5%) |
| ❌ Test Cases Failed | — | **24** |
| 🐛 Total Bugs Logged | — | **24** |
| 🔴 Critical / Fatal Bugs | — | **5** |
| 📅 Execution Period | — | **Sep 28 – Oct 17, 2025** |
| 👤 Tester | — | **Hoàng Đỉnh** |

### 🎯 Project Goals

- Perform black box functional testing on all core e-commerce features of Moriitalia.com.
- Ensure core functionalities behave correctly according to end-user requirements.
- Identify and log all defects with full reproduction steps, severity, and priority.
- Deliver a final Summary Report with quality assessment and release recommendation.

---

## 🧪 Testing Methodology

| Attribute | Value |
|---|---|
| Testing Type | Functional Testing + Smoke Testing |
| Technique | Black Box Testing |
| Execution Method | Manual Testing |
| Testing Level | System Test |
| Tool Used | Excel (test cases & defect log) |
| Environment | Live website — [https://moriitalia.com](https://moriitalia.com) |

---

## 🧱 Project Structure

```
Phan-Hoang-Dinh--Manual-Testing-_-Moriitalia.com/
│
├── Functional Testing - Moriitalia.com.xlsx   # Full test case suite for all 10 modules
├── Smoke Testing - Moriitalia.com.xlsx        # Critical path smoke test cases
├── Defect Log.xlsx                            # All 24 bugs logged with full details
├── Sumary Report.xlsx                         # Final report: coverage, pass/fail, defect rates
│
└── Screenshots/
    ├── Functional Testing/                    # Evidence screenshots for functional test results
    │  
    └── Smoke Testing/                         # Evidence screenshots for smoke test results
        ├──
```

---

## 📊 Test Coverage by Module

The table below shows the complete test results per module, computed from `Sumary Report.xlsx`:

| Module | Pass | Fail | NT | N/A | Total TCs | Test Coverage | Pass Rate | Defect Rate |
|---|---|---|---|---|---|---|---|---|
| 🏠 Homepage | 12 | 0 | 0 | 0 | 12 | **100%** | 100% | **0%** |
| 🔍 Search Items | 17 | 5 | 0 | 1 | 23 | **96%** | 77% | 23% |
| 📦 Product Detail | 10 | 6 | 1 | 12 | 29 | **55%** | 63% | **38%** |
| 🛒 Shopping Cart | 28 | 2 | 4 | 0 | 34 | **88%** | 93% | 7% |
| 💳 Payment | 0 | 0 | 0 | 0 | 0 | **0%** | — | — |
| 📋 Order Manage | 5 | 2 | 0 | 25 | 32 | **22%** | 71% | **29%** |
| 📝 Register | 16 | 4 | 4 | 0 | 24 | **83%** | 80% | 20% |
| 🔑 Sign-in | 20 | 3 | 0 | 2 | 25 | **92%** | 87% | 13% |
| 🔒 Forgot Password | 12 | 0 | 0 | 0 | 12 | **100%** | 100% | **0%** |
| 🔐 Change Password | 22 | 2 | 0 | 1 | 25 | **96%** | 92% | 8% |

> **NT** = Not Tested · **N/A** = Not Applicable

### Coverage Visual

```
Homepage         ████████████████████  100%  ✅
Forgot Password  ████████████████████  100%  ✅
Change Password  ███████████████████▌   96%  ✅
Search Items     ███████████████████▌   96%  ✅
Sign-in          ██████████████████▌    92%  ✅
Shopping Cart    █████████████████▌     88%  ✅
Register         ████████████████▌      83%  ⚠️
Product Detail   ███████████            55%  ⚠️
Order Manage     ████▌                  22%  🔴
Payment          ░░░░░░░░░░░░░░░░░░░░    0%  🔴 (No test cases)
```

---

## 🐛 Defect Summary

### Bugs by Severity

| Severity | Count | Modules Affected |
|---|---|---|
| 🔴 Fatal | 5 | Register, Sign-in, Product Detail, Shopping Cart, Order Payment |
| 🟠 Serious | 2 | Search Items, Product Detail |
| 🟡 Medium | 13 | Sign-in, Change Password, Search Items, Product Detail, Order Payment |
| 🟢 Cosmetic | 7 | Register, Product Detail, Shopping Cart, Smoke (Login/Registration) |

### Bugs by Status

| Status | Count |
|---|---|
| 🔵 Assigned (to DEV/BA) | 18 |
| 🟡 Opened (pending triage) | 9 |
| ✅ Fixed | 3 |

### Bugs by Module

```
Product Detail    ████████████████  11 bugs (most affected)
Sign-in           ████               4 bugs
Register          ███                3 bugs
Order Payment     ███                3 bugs  (from Smoke Test)
Search Items      ██                 2 bugs (in log; more in TCs)
Shopping Cart     ██                 2 bugs
Change Password   ██                 2 bugs
```

---

## 🔍 Key Defects Found

### 🔴 Fatal Bugs (Immediate Action Required)

| Defect ID | Module | Title | Priority |
|---|---|---|---|
| `[Register-9]` | Register | System allows account creation with an existing email by appending `+1` (e.g., `user+1@domain.com`) — **security bypass** | High |
| `[Register-15]` | Register | Password field accepts leading/trailing spaces — allows weak passwords to bypass validation | High |
| `[Sign-in-17]` | Sign-in | No error message or account lockout after 5 consecutive failed login attempts — **brute-force vulnerability** | Immediately |
| `[Product Detail-18]` | Product Detail | No restriction on order quantity — users can add 50+ units with no warning or validation | High |
| `[Shopping Cart-34]` | Shopping Cart | Shipping cost is not recalculated when quantity increases — always shows 0đ regardless of total order value | Immediately |

### 🟠 Serious Bugs

| Defect ID | Module | Title |
|---|---|---|
| `[Search Items-8]` | Search Items | Search button is completely disabled when the browser window is resized — broken search functionality |
| `[Product Detail-1]` | Product Detail | Multiple missing features: Feedback/Reviews, Promotion Status, Policy & Support, Product Suggestions |

### ✅ Bugs Fixed During Testing

| Defect ID | Module | Fix Applied |
|---|---|---|
| `[Sign-in-3]` | Sign-in | Developer added show/hide password icon (👁️) |
| `[Sign-in-7]` | Sign-in | Developer added "Remember Me" checkbox |
| `[Sign-in-14]` | Sign-in | Developer implemented "Remember Me" session persistence |

---

## 📈 Test Results & Quality Assessment

### Overall Quality Verdict

> ⚠️ **The website is NOT ready for deployment.** Core functionalities are unstable, and several critical/fatal bugs have been identified that directly impact security and the purchasing experience.

### Highlights

**🔴 High Risk Areas:**
- **Product Detail (38% Defect Rate)** — highest defect concentration. Multiple missing features (reviews, promotions, policy, suggestions) and a fatal quantity validation bug.
- **Order Manage (29% Defect Rate, 22% Coverage)** — extremely low test coverage. Many scenarios couldn't be tested due to incomplete functionality.
- **Payment (0% Coverage)** — the payment module has **zero test cases** and zero coverage. This is the single highest risk factor for production readiness.

**✅ Stable Areas:**
- **Homepage** — 100% coverage, 0% defect rate. Fully functional and stable.
- **Forgot Password** — 100% coverage, 0% defect rate. End-to-end flow working correctly.
- **Change Password** — 96% coverage, 92% pass rate. Minor cosmetic issues only.
- **Shopping Cart** — 88% coverage, 93% pass rate. Mostly stable except for the shipping cost calculation bug.

### Summary Metrics

```
Test Execution Progress
───────────────────────────────────────────────────────
Total Written:   216  ████████████████████████████████  100%
Executed:        166  ████████████████████████▌          77%
Passed:          142  █████████████████████▌             85.5% of executed
Failed:           24  ████                               14.5% of executed

Defect Breakdown
───────────────────────────────────────────────────────
Fatal:     5   🔴🔴🔴🔴🔴
Serious:   2   🟠🟠
Medium:   13   🟡🟡🟡🟡🟡🟡🟡🟡🟡🟡🟡🟡🟡
Cosmetic:  7   🟢🟢🟢🟢🟢🟢🟢
```

---

## 📅 Planning

```
Stage 1 (Sep 28 – Oct 3) — Analysis & Test Case Design
├── Functional analysis of all 10 modules on Moriitalia.com
├── Define test objectives, scope, and entry/exit criteria
├── Write 216 test cases across Functional and Smoke Testing workbooks
└── Prepare Defect Log template and Summary Report structure

Stage 2 (Oct 5 – Oct 10) — Test Execution & Defect Logging
├── Execute all test cases manually on the live website
├── Log 24 defects into Defect Log.xlsx with full reproduction steps
├── Capture screenshots for all Fail / N/A test results
├── Perform Smoke Testing to verify critical path stability
└── Assign severity, priority, and assignee for each defect

Stage 3 (Oct 12 – Oct 17) — Reporting & Quality Assessment
├── Consolidate all execution results into Summary Report
├── Calculate test coverage, pass rate, and defect rate per module
├── Analyze defects by severity and module impact
├── Write personal quality assessment and release recommendation
└── Organize all project files, screenshots, and deliverables
```

---

## 📁 Deliverables

| File | Description |
|---|---|
| `Functional Testing - Moriitalia.com.xlsx` | Complete test case suite for all 10 functional modules with steps, expected/actual results, and status |
| `Smoke Testing - Moriitalia.com.xlsx` | Critical path smoke test cases covering registration, login, and order payment |
| `Defect Log.xlsx` | 24 bugs fully documented: ID, module, title, reproduction steps, severity, priority, status, assignee, and corrective action |
| `Sumary Report.xlsx` | Final report with per-module coverage metrics, defect rates, charts, and quality assessment |
| `Screenshots/` | Evidence screenshots for all Fail and N/A test cases, organized by module |

---

## 👤 Author

**Hoàng Đỉnh** — Manual QA Tester

---

*This project was conducted independently by a single tester using manual testing only — no automation tools were used. All defects were identified through hands-on exploration of the live Moriitalia.com website.*
