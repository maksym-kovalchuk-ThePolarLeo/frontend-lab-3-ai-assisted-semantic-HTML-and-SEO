# Frontend Lab 2: CSS Basics

A practice and research project focusing on core CSS mechanics (Box Model, Cascade, Specificity, Inheritance, CSS Variables, and Code Reusability) along with a responsive, component-based Pricing Plans layout.

## Project Structure & Features

### 1. Main Pricing Page (`index.html`)

- **Responsive Pricing Table**: Modern pricing cards layout (Basic, Pro, Enterprise) built with CSS Flexbox fluid grid.
- **Component Styling & BEM Architecture**: Structured class naming (`.mockup__card`, `.mockup__badge`, `.mockup__cta`, etc.).
- **CSS Variables & Design Tokens**: Centralized color palette, spacing scale, and typography configured in `css/root.css`.
- **Micro-interactions & States**: Hover transitions on call-to-action buttons, badge overlays, and pseudo-elements (`::before` checkmarks).

### 2. CSS Research & Concept Demos (`researches/`)

- **4.1 Box Model** (`researches/html/4-1-box-model.html`): Visual comparison of `box-sizing: content-box` vs `box-sizing: border-box`.
- **4.2 Cascade** (`researches/html/4-2-cascade.html`): Demonstrates stylesheet link ordering, internal `<style>` precedence, and rule order in CSS.
- **4.3 Specificity** (`researches/html/4-3-specificity.html`): Comparison of CSS selector weights (element type vs class chaining vs ID selector).
- **4.4 Inheritance** (`researches/html/4-4-inheritance.html`): Exploration of inherited vs non-inherited properties and explicit usage of the `inherit` keyword.
- **4.5 CSS Variables** (`researches/html/4-5-variables.html`): Global variable scope (`:root`) vs component-level local scope overrides (`.dark-card`).
- **4.6 Reusability & Refactoring** (`researches/html/4-6-reuse.html`): Modular component architecture with reusable base classes and modifier classes (`.btn`, `.btn-primary`, `.btn-outline`).

## Running locally

1. Clone or download this repository.
2. Open `index.html` directly in your browser, **or** serve it locally, e.g.:
   ```bash
   npx serve .
   ```
3. (Optional) Install dev dependencies to use lint/format tooling:
   ```bash
   npm install
   npm run lint
   npm run format
   ```

## Links & Deployment

- Repository: https://github.com/maksym-kovalchuk-ThePolarLeo/frontend-lab-2-css-basics
- GitHub Pages: https://maksym-kovalchuk-thepolarleo.github.io/frontend-lab-2-css-basics/
- Vercel: https://frontend-lab-2-css-basics.vercel.app/
