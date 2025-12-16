# Accessibility Conformance Report  
## WCAG 2.1 Level AA  

---

## Product Information

- **Name of Product:** Ximera
- **Product Type:** Web-based interactive educational content platform
- **Product Description:**  
  Ximera is an open-source platform for creating and delivering interactive STEM educational content using LaTeX-authored source files rendered as web pages with embedded interactivity.
- **Primary Use Case:** Postsecondary and secondary education
- **Hosting Model:** Self-hosted or institutionally hosted web application
- **Contact Information:** https://ximera.org
- **Report Date:** 12/2025

---

## Evaluation Methods Used

This report is based on:

- Manual expert review by developers and educators familiar with Ximera’s internal architecture and content pipeline.
- Review of rendered HTML output produced by Ximera’s LaTeX-to-HTML toolchain.
- Targeted testing with screen readers (NVDA, VoiceOver) and keyboard-only navigation.
- Reference to known accessibility constraints inherent to mathematical notation, interactive problem widgets, and third-party embedded tools.

This report reflects the **current state of the platform** and acknowledges ongoing accessibility improvements.

---

## Applicable Standards / Guidelines

This report covers the degree of conformance with:

| Standard | Included |
|--------|----------|
| WCAG 2.1 Level A | Yes |
| WCAG 2.1 Level AA | Yes |
| WCAG 2.1 Level AAA | Not Evaluated |

---

## Conformance Terminology

The terms used in this report are defined as follows:

- **Supports:** The functionality meets the success criterion without known defects.
- **Partially Supports:** Some functionality does not meet the criterion.
- **Does Not Support:** The majority of functionality does not meet the criterion.
- **Not Applicable:** The criterion does not apply to the product.

---

## WCAG 2.1 Conformance: Level A and AA

> **Note:** Conformance claims apply to Ximera-generated pages and workflows as authored. Accessibility outcomes may vary depending on content authoring choices and embedded third-party tools.

---

### **Table 1: WCAG 2.1 Level A Success Criteria**

| Criteria | Conformance | Remarks |
|--------|------------|--------|
| **1.1.1 Non-text Content** | Partially Supports | Mathematical notation and diagrams are primarily rendered as MathML or SVG with assistive text support. Some authored images may lack sufficient alternative text depending on author practices. |
| **1.2.1–1.2.3 Audio/Video (Prerecorded)** | Not Applicable | Ximera does not natively require audio or video for interaction. |
| **1.3.1 Info and Relationships** | Partially Supports | Semantic structure is generally preserved via HTML and MathML. Some complex mathematical layouts may not fully expose relationships programmatically. |
| **1.3.2 Meaningful Sequence** | Supports | Content order follows logical reading and navigation sequences. |
| **1.3.3 Sensory Characteristics** | Supports | Instructions do not rely solely on sensory characteristics such as color or location. |
| **1.4.1 Use of Color** | Partially Supports | Color is sometimes used to convey correctness or emphasis, but is generally accompanied by text or symbols. |
| **2.1.1 Keyboard** | Partially Supports | Core navigation is keyboard accessible. Some interactive math widgets and embedded tools may have limited keyboard support. |
| **2.1.2 No Keyboard Trap** | Supports | Users can navigate into and out of interactive components using standard keyboard controls. |
| **2.1.4 Character Key Shortcuts (2.1)** | Supports | No unmodifiable single-character shortcuts are used. |
| **2.2.1 Timing Adjustable** | Supports | No time limits are imposed on completing tasks. |
| **2.2.2 Pause, Stop, Hide** | Supports | No automatically moving or updating content that requires pausing. |
| **2.3.1 Three Flashes or Below Threshold** | Supports | No flashing content exceeding thresholds is used. |
| **2.4.1 Bypass Blocks** | Partially Supports | Headings and landmarks are generally present, but skip links are not consistently implemented across all themes. |
| **2.4.2 Page Titled** | Supports | Pages have descriptive titles reflecting content context. |
| **2.4.3 Focus Order** | Supports | Focus order follows DOM order and reading sequence. |
| **2.4.4 Link Purpose (In Context)** | Supports | Links are generally descriptive within context. |
| **2.5.1 Pointer Gestures (2.1)** | Not Applicable | No multi-point or path-based gestures are required. |
| **2.5.2 Pointer Cancellation** | Supports | Actions are triggered on release, not on initial contact. |
| **2.5.3 Label in Name** | Partially Supports | Most controls expose accessible names; some math-specific controls may need improved labeling. |
| **2.5.4 Motion Actuation** | Not Applicable | No motion-based input is used. |
| **3.1.1 Language of Page** | Supports | Default language is programmatically identified. |
| **3.2.1 On Focus** | Supports | Focus does not trigger unexpected context changes. |
| **3.2.2 On Input** | Supports | Input does not automatically cause context changes without user initiation. |
| **3.3.1 Error Identification** | Supports | Input errors are identified and described textually. |
| **3.3.2 Labels or Instructions** | Partially Supports | Most form fields include labels; some author-created inputs may require improved instructions. |
| **4.1.1 Parsing** | Supports | HTML output conforms to modern parsing requirements. |
| **4.1.2 Name, Role, Value** | Partially Supports | Standard controls expose name/role/value; some custom math widgets are still under improvement. |

---

### **Table 2: WCAG 2.1 Level AA Success Criteria**

| Criteria | Conformance | Remarks |
|--------|------------|--------|
| **1.3.4 Orientation (2.1)** | Supports | Content reflows in both portrait and landscape orientations. |
| **1.3.5 Identify Input Purpose (2.1)** | Partially Supports | Common input purposes are identified; specialized mathematical inputs may not map cleanly to autocomplete semantics. |
| **1.4.3 Contrast (Minimum)** | Partially Supports | Default themes generally meet contrast requirements; custom themes or author styling may introduce issues. |
| **1.4.4 Resize Text** | Supports | Text can be resized up to 200% without loss of content or functionality. |
| **1.4.5 Images of Text** | Supports | Text is rendered as text rather than images. |
| **1.4.10 Reflow (2.1)** | Partially Supports | Content generally reflows at 400% zoom; complex mathematical layouts may require horizontal scrolling. |
| **1.4.11 Non-text Contrast (2.1)** | Partially Supports | Focus indicators and graphical controls generally meet contrast requirements, with some exceptions in embedded tools. |
| **1.4.12 Text Spacing (2.1)** | Partially Supports | Increased spacing may cause minor layout issues in dense mathematical expressions. |
| **1.4.13 Content on Hover or Focus (2.1)** | Supports | Tooltips and hover content are generally dismissible or non-essential. |
| **2.4.5 Multiple Ways** | Supports | Content can be accessed through navigation, search, or direct linking. |
| **2.4.6 Headings and Labels** | Partially Supports | Headings are generally descriptive; quality depends on authoring practices. |
| **2.4.7 Focus Visible** | Supports | Keyboard focus is visually indicated. |
| **3.1.2 Language of Parts** | Partially Supports | Mathematical symbols and notation are language-neutral; mixed-language text may not always be explicitly marked. |
| **3.2.3 Consistent Navigation** | Supports | Navigation elements are consistent across pages. |
| **3.2.4 Consistent Identification** | Supports | Controls with the same function are identified consistently. |
| **3.3.3 Error Suggestion** | Supports | Where applicable, suggestions for correcting errors are provided. |
| **3.3.4 Error Prevention (Legal, Financial, Data)** | **Supports** | Ximera provides confirmation, revision, and unlimited retry mechanisms for problem submissions. No irreversible legal or financial transactions occur. |
| **4.1.3 Status Messages (2.1)** | Partially Supports | Some dynamic feedback is available to assistive technologies; improvements are ongoing for real-time math feedback. |

---

## Legal Disclaimer

This document is provided for informational purposes only and does not constitute a warranty of accessibility compliance. Accessibility outcomes may vary depending on content authoring practices, third-party integrations, and user configurations. The Ximera Project continues to improve accessibility as part of its ongoing development roadmap.

---

_End of Accessibility Conformance Report_
