---
layout: single
title: Content
type: page
parent_id: '0'
published: true
password: ''
#sidebar:
#  nav: "menu"
---
Ximera strives to be compliant with the Web Content Accessibility Guidelines (WCAG) 2.1 AA standard, as required by the United States Department of Education. These are the technical standards that will be required of public colleges and universities in April 2026, according to the Department of Justice's interpretation of Title II of the Americans with Disabilities Act. We are currently partnering with [Tailor Swift Bots LLC](https://tailorswiftbot.com/) to ensure that our content meets these standards.

Of course, meeting a technical standard does not imply that content will still be accessible to every user with a disability. It is important that instructors include an [accessibility statement](https://www.w3.org/WAI/planning/statements/) for their students. Depending on the institution's organization, the contact person may be the disability resources office, an instructional designer, or even another faculty member. If you wish to verify that your course meets WCAG 2.1 AA, you may email [Jeffrey Kuan](mailto:kuan.44@osu.edu), who can use a variety of screen readers and automatic accessibility checkers. **Do NOT claim that your course is WCAG 2.1 AA compliant without a manual human verification.**



## Current features

**MathJax** is supported in Ximera.  
Webpages created with Ximera will have the mathematical content displayed in MathJax, which can be read with EquatIO. In principle, the webpage can be edited so that screen readers like NVDA, JAWS, VoiceOver and Narrator can read it directly. We would recommend checking if your institution licenses EquatIO for your students. 

**Lists** can be compliant in Ximera.  
Using `itemize`, `enumerate`, and `description` environments in LaTeX will correctly create unordered, ordered, and description lists (respectively) in HTML. We do not offer custom list labeling, although labels can be modified in the CSS file (this will be done later). The references list will be displayed as a description list, which is the [recommendation of the DAISY consortium](http://kb.daisy.org/publishing/docs/html/bibliographies.html).

**Desmos and Geogebra** have accessibility features.  
Ximera is able to embed both [Desmos](https://www.desmos.com/accessibility) and [Geogebra](https://help.geogebra.org/hc/en-us/articles/20048444963869-Accessibility) and support their accessibility features.

## Upcoming features

**MathML 4.0** will be supported.  
As of the current date (June 25, 2025), we are still waiting for the final release of MathML 4.0, which is planned for August 2025. One notable feature will be the “intent” environment, which allows the author to insert their intended text-to-speech for math symbols. For example,  
```
a(b+c) = ab + ac
```  
can be read as "a times the quantity b plus c equals a b plus a c" rather than "a left paren b plus c right paren equals ab plus ac." Historically, this would be called “alternative text”; for a variety of reasons, that terminology is somewhat outdated. We will add a LaTeX command or environment, probably called `intent`, that will insert the author's intended text-to-speech in the webpage. 

**Tables**  
will need to have headers and scopes from the LaTeX code. This will soon be implemented with the LaTeX package `tabularray`.

**Headers** are required for environments.  
The `problem`, `exercise`, and `question` environments will need to have appropriate headers; same with theorem, proposition, etc.

**Answer** will need to be supported.  
In the future, screen readers will be able to inform readers if their answers are correct or incorrect.

**Navigation** will be improved.  
We will work with experts at Ohio State University who have worked on the navigability of webpages.

