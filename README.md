Swag Labs (SauceDemo) — Non-Functional, Performance & Console QA Audit

Project Overview
A structured non-functional quality assurance audit of the Swag Labs e-commerce application (`saucedemo.com`), evaluating UI layout stability, cross-page data integrity, client-side latency against SLA thresholds, and unhandled JavaScript runtime exceptions across specialized test personas.

Tools & Methodology
* Browser DevTools (`F12`): Network tab (`No throttling` baseline vs. degraded latency, `DOMContentLoaded` vs. `Load`), Performance flame-chart profiler (Main-thread `Scripting` Long Tasks), and Console exception stack-trace capture.
* Test Documentation: Microsoft Excel (`SwagLabs_NonFunctional_Visual_QA.xlsx`) with severity/priority triage, variance calculations, and reproducible steps.

Key Findings Summary
1.UI & Data Integrity (`visual_user`): Identified 6 defects, including a Critical cross-page pricing discrepancy (`$81.37` catalog price reverting to `$29.99` in detail/cart views) and layout alignment regressions.
2.Performance & SLA Benchmarking (`performance_glitch_user`): Established a `447 ms` baseline using `standard_user`. Identified a `5.30 s` login page load (breaching the `< 2.0 s` SLA by `+4.85 s`) and recorded a `5,013 ms` first-party JavaScript `Scripting` Long Task blocking route transitions.
3.Frontend Exception Handling (`error_user`): Captured unhandled `Uncaught Error` and `Uncaught TypeError` stack traces (`onChange` failure blocking checkout Last Name input; `onClick` `wa.cesetRart is not a function` breaking order completion).

Repository Contents
* `SwagLabs_NonFunctional_Visual_QA.xlsx` — Complete multi-tab test suite (`00_Summary`, `01_Visual_UI_Audit`, `02_Performance_SLA`, `03_Console_Exceptions`).
* `Project2_Evidence/` — DevTools Network, Performance flame-chart, and Console stack-trace screenshots.

* `SwagLabs_NonFunctional_Visual_QA.xlsx` — Complete multi-tab test suite (`00_Summary`, `01_Visual_UI_Audit`, `02_Performance_SLA`, `03_Console_Exceptions`).
* `Project2_Evidence/` — DevTools Network, Performance flame-chart, and Console stack-trace screenshots.
