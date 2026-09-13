# AI Usage Log

## Assignment
SWE 380 / CSC 580 Assignment 1: GitHub + AI Engineering Practice

## Student
Ibrahim Atatri

## AI Tool Used
Google Gemini

## Date
September 13, 2026

---

# Initial Planning Prompt

You are assisting me with a small public static portfolio website for
SWE 380 / CSC 580 Assignment 1.

Project purpose:
Create a professional online portfolio that presents my software engineering
skills, projects, education, and experience to internship recruiters and
other professional reviewers.

Existing system:
The project is based on the vCard Personal Portfolio template and uses
HTML, CSS, and JavaScript.

Allowed changes:
- Portfolio text/content
- Existing HTML
- Existing CSS
- Existing JavaScript when necessary
- Images/assets when necessary

Do not add:
- A backend
- A database
- A login system
- Analytics tracking
- External data collection

Acceptance criteria:
1. The landing page displays my name, Ibrahim Atatri, and identifies me
   as a Software Engineering student.
2. The portfolio contains at least two real projects with a title,
   description, and relevant technologies.
3. All navigation links move to the correct sections of the portfolio.
4. The website remains readable and usable on a narrow mobile viewport.
5. No placeholder names, email addresses, project descriptions, or images
   from the starter template remain on the published site.

Technical constraints:
- Preserve the overall existing layout unless a change is needed for
  usability or accessibility.
- Do not invent education, employment, awards, projects, links, or
  technical skills.
- Preserve the original license and attribution.
- Keep the site usable on mobile screens.
- Maintain readable contrast and keyboard navigation.
- Use meaningful link text and useful image alternative text.
- Do not expose private information, passwords, API keys, or tokens.
- Keep the project entirely front-end.

Before making any implementation changes, provide:

1. A file-by-file implementation plan.
2. Assumptions you are making.
3. Risks you identify.
4. A proposed testing checklist.
5. Questions that should be answered before implementation.

Do not modify or generate replacement files yet. I want to review the plan first.

---

# Initial AI Response

Here is the comprehensive plan for customizing your vCard Personal Portfolio
for SWE 380 / CSC 580 Assignment 1. As requested, no files will be modified
or generated until we address the questions below.

## 1. File-by-File Implementation Plan

### `index.html`

- Head:
  Update `<title>`, `<meta name="description">`, and favicon links to reflect
  your identity.

- Sidebar / Hero Section:
  Update the placeholder name to Ibrahim Atatri and the primary subtitle to
  Software Engineering student.

- About Section:
  Replace the placeholder bio with your actual summary. Update personal
  details such as location and email while ensuring no highly sensitive
  private information is exposed.

- Resume / Education Section:
  Insert your real university timeline, relevant coursework, and any actual
  employment or volunteer experience. Remove any template sections such as
  Testimonials or Services if you do not have real data for them.

- Portfolio Section:
  Swap placeholder items with at least two real projects. Each project will
  include the project title, a brief description, technologies used, and a
  repository or live-site link if applicable.

- Contact Section:
  Ensure the contact information or social links point to actual professional
  profiles such as GitHub and LinkedIn.

- Accessibility & Cleanup:
  Audit and update image `alt` attributes, ensure structural semantic tags are
  used, and remove any remaining Lorem Ipsum or template placeholder content.
  Preserve the original template license and attribution.

### `css/style.css` or equivalent stylesheet

- Adjust font sizes or padding if real text overflows the template's default
  containers.
- Verify readable color contrast.
- Make changes only if necessary for readability, mobile responsiveness, or
  accessibility.

### `js/script.js` or equivalent main script

- Verify that section-toggling and navigation continue working with the new
  content.
- Remove unnecessary JavaScript only if a related feature is removed and the
  change has been reviewed to ensure it does not affect other functionality.

### `assets/images/`

- Replace placeholder images when necessary.
- Add appropriate images for real projects if suitable images are available.
- Ensure useful alternative text is used for meaningful images.

---

## 2. Assumptions

- The vCard template uses a single `index.html` page with JavaScript-based
  navigation between sections.
- The source code is available locally and can be inspected before changes
  are made.
- Real content will be provided for the biography, skills, education,
  experience, and projects.
- The website will remain a static front-end project.
- The website will ultimately be published using GitHub Pages as required by
  the assignment.

---

## 3. Risks Identified by the AI

### Content gaps

If real information is not available for a template section, leaving template
content in place could violate the requirement to remove placeholder
information.

Mitigation:
Remove or replace sections only after confirming that real information is
available.

### Mobile responsiveness

Long descriptions or images could cause content to overflow on small screens.

Mitigation:
Test the site at narrow viewport widths and adjust CSS only when necessary.

### Accessibility

The existing template may contain poor keyboard focus behavior, image
alternative text, or low-contrast content.

Mitigation:
Manually test keyboard navigation, image alternative text, and readability.

---

## 4. Proposed Testing Checklist

- [ ] The landing page displays "Ibrahim Atatri".
- [ ] The landing page identifies me as a Software Engineering student.
- [ ] At least two real projects are displayed.
- [ ] Each project contains a title, description, and technologies used.
- [ ] All navigation links open the intended sections.
- [ ] The website remains usable at a narrow mobile viewport.
- [ ] There is no unintended horizontal scrolling on mobile.
- [ ] All template placeholder personal information has been removed.
- [ ] The website can be navigated using the keyboard.
- [ ] Meaningful images contain appropriate alternative text.
- [ ] Project and external links work correctly.
- [ ] No private information, passwords, API keys, or tokens are exposed.
- [ ] The browser console contains no unexplained errors.
- [ ] The final implementation satisfies all five acceptance criteria.

---

## 5. Questions Before Implementation

1. What exact biography should be used in the About section?
2. Which technical skills and education information should be included?
3. Which projects should be featured?
4. Which professional links should be included?
5. Which existing template sections should be removed if they are not
   relevant?
6. Which images should replace template placeholder images?

---

# Human Review of the AI Plan

## Accepted Plan Element

I accepted the recommendation to update the existing `index.html` rather than
rebuild the portfolio from scratch. The assignment requires preserving the
existing project structure while making controlled changes, so modifying the
existing content is more appropriate than replacing the entire template.

I also accepted the recommendation to review mobile responsiveness,
accessibility, image alternative text, navigation, and placeholder content.
These items directly support my acceptance criteria and the testing
requirements.

## Revised Plan Element

I revised the AI's original suggestion regarding deployment and contact-form
options.

The AI mentioned static hosting options such as GitHub Pages, Vercel, or
Netlify and suggested that a static form provider might be used. For this
assignment, I will use GitHub Pages because that is the required deployment
method.

I will also avoid adding an external form provider because the project
constraints prohibit unnecessary external data collection. The portfolio
will use professional links such as GitHub and LinkedIn and may use a public
email link if needed.

I also decided not to remove JavaScript simply because a visual section is
removed. I will first inspect how the template JavaScript references the HTML
elements so that removing code does not accidentally break navigation or
other functionality.

## Risk the AI Identified

The AI identified the risk that adding longer real project descriptions and
other personal content could break the mobile layout.

This is important because the site must remain usable on a narrow viewport.
I will test the site using the browser's responsive design tools and make CSS
changes only if problems are found.

The AI also identified accessibility and leftover placeholder content as
risks that require manual review.

## Risk the AI Missed

One risk the AI did not fully address is that removing or renaming sections in
the HTML could break JavaScript selectors used by the template's navigation.

Because this template uses JavaScript to switch between portfolio sections,
an HTML element might appear unnecessary while still being referenced by
`script.js`.

Before deleting sections or related JavaScript, I will inspect both the HTML
and JavaScript to verify that the change will not break navigation or produce
browser console errors.

Another deployment-specific risk is that a site can work locally but behave
differently after being published through GitHub Pages. Relative paths,
filename capitalization, image paths, and links must therefore be tested
again on the live GitHub Pages version.

---

# Human Decision Before Implementation

I reviewed the AI-generated plan before allowing any implementation changes.

The approved implementation approach is:

1. Preserve the existing vCard template structure.
2. Replace template identity and biography information with my real
   professional content.
3. Add real education, experience, skills, and project information.
4. Remove irrelevant placeholder content only after checking for JavaScript
   dependencies.
5. Preserve the original license and attribution.
6. Keep the project entirely front-end.
7. Avoid external tracking or unnecessary data collection.
8. Review each AI-generated change before committing it.
9. Make changes incrementally rather than rewriting the entire repository.
10. Test both the local version and the final GitHub Pages deployment.

The AI plan is approved with the revisions documented above.

---

# Implementation Log

Implementation has not started at the time of this planning review.

Future AI-assisted implementation requests and important responses will be
recorded below.

## Implementation Entry 1

Date:

Prompt:

AI Response Summary:

Files Changed:

Human Review:

Commit:

---

## Implementation Entry 2

Date:

Prompt:

AI Response Summary:

Files Changed:

Human Review:

Commit:

---

## Implementation Entry 3

Date:

Prompt:

AI Response Summary:

Files Changed:

Human Review:

Commit: