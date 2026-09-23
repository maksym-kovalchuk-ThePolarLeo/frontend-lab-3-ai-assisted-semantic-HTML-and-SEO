# Lab 3: AI-assisted semantic HTML & SEO

A front-end development and audit project focused on upgrading the semantic structure, web accessibility (WCAG 2.1), and on-page search engine optimization (SEO) of a responsive pricing plans web application and CSS research modules.

## Project Goal

The primary goal of this laboratory work is to transition an existing CSS/HTML layout into a standards-compliant, accessible, and SEO-optimized web application. Guided by MDN Web Docs, W3C Web Content Accessibility Guidelines (WCAG), and Google Search Central best practices, the project eliminates accessibility barriers and improves search engine crawlability and snippet presentation while strictly maintaining the visual design and CSS architecture.

## Key Audit Findings & Refactoring Changes

Following an AI-assisted audit based on the `frontend-review` framework, the following improvements were applied:

### 1. Blocker Fixes

- **Interactive CTA Elements (`.mockup__cta`)**:
  - _Problem_: Plan call-to-action triggers were implemented using non-interactive `<span class="mockup__cta">` elements. These lacked keyboard focusability (WCAG 2.1.1 Keyboard), could not be activated via `Enter`/`Space`, and were invisible to search engine web crawlers.
  - _Resolution_: Replaced `<span>` elements with semantic anchor links (`<a href="..." class="mockup__cta">`) styled to preserve the exact visual appearance while enabling full keyboard navigation and crawler indexability.
- **Canonical Tag Optimization**:
  - _Problem_: The `<head>` contained an invalid placeholder `<link rel="canonical" href="#" />`, which misleads search engines and fragments search equity.
  - _Resolution_: Updated to a valid absolute canonical URL pointing to the live GitHub Pages deployment.

### 2. Warning Fixes

- **Metadata Quality & Language Alignment**:
  - _Problem_: The page declared `lang="uk"`, but contained an English meta description and a technical assignment title (`ЛР-2: AI-assisted верстка`).
  - _Resolution_: Updated `<title>` to a human- and keyword-relevant title (`Тарифи та плани підписки | Хмарні AI-сервіси`), created an informative Ukrainian `<meta name="description">` (150+ chars), and added Open Graph social metadata (`og:title`, `og:description`, `og:url`, `og:type`).
- **Contextual Link Purpose (WCAG 2.4.4)**:
  - _Problem_: Isolated button labels ("Select", "Get Started", "Contact") provided insufficient context for screen reader users browsing links out of context.
  - _Resolution_: Added clear `aria-label` attributes (e.g., `aria-label="Обрати тарифний план Basic"`), establishing unambiguous purpose in assistive technology rotor/link menus.
- **Semantic Navigation Structure**:
  - _Problem_: The `<nav>` element contained bare links without an overarching list structure or distinguishing landmark label.
  - _Resolution_: Added `aria-label="Лабораторні дослідження"` to differentiate the landmark and wrapped navigation items in a semantic `<ul>`/`<li>` structure with CSS `display: contents` to preserve the flexbox layout.
- **Document Landmark Hierarchy**:
  - _Problem_: Pricing cards were contained in a generic `<div class="mockup__plans">`, missing an opportunity to define a key document landmark.
  - _Resolution_: Converted the container to `<section class="mockup__plans" aria-labelledby="pricing-heading">` and assigned `id="pricing-heading"` to the main `<h1>`.

## Project Structure

- `index.html`: Semantic, accessible, and SEO-optimized pricing page.
- `css/`: Modular stylesheets (`root.css`, `nav.css`, `styles.css`).
- `researches/`: Dedicated research pages exploring core CSS concepts:
  - `4-1-box-model.html`: Box sizing comparison (`content-box` vs `border-box`).
  - `4-2-cascade.html`: Cascade ordering and stylesheet precedence.
  - `4-3-specificity.html`: Selector specificity calculation.
  - `4-4-inheritance.html`: CSS property inheritance mechanics.
  - `4-5-variables.html`: Custom properties and scope.
  - `4-6-reuse.html`: Component reusability and modifier patterns.

## Running Locally & Verification

1. Open `index.html` directly in any modern browser, or run a local static server:
   ```bash
   npx serve .
   ```
2. Run code style and lint checks:
   ```bash
   npm run lint
   npm run format:check
   ```

## Links & Deployment

- **Repository**: [https://github.com/maksym-kovalchuk-ThePolarLeo/frontend-lab-3-ai-assisted-semantic-HTML-and-SEO](https://github.com/maksym-kovalchuk-ThePolarLeo/frontend-lab-3-ai-assisted-semantic-HTML-and-SEO)
- **GitHub Pages**: [https://maksym-kovalchuk-thepolarleo.github.io/frontend-lab-3-ai-assisted-semantic-HTML-and-SEO/](https://maksym-kovalchuk-thepolarleo.github.io/frontend-lab-3-ai-assisted-semantic-HTML-and-SEO/)
