# SpendWise Dashboard Shell

A responsive financial dashboard layout built using modern CSS layout techniques (CSS Grid & Flexbox), CSS Custom Properties, accessible micro-interactions, and dark mode support.

---

## 🚀 Overview & What Was Built

The **SpendWise Dashboard Shell** serves as the foundational user interface for a personal budget tracking application. It presents a clean, modern dashboard layout containing:

1. **Sidebar Navigation**: Branding, primary links, and user account status.
2. **Header Bar**: Contextual dashboard title, quick search input, and notifications trigger.
3. **Summary Section**: High-level spend versus remaining budget overview pills.
4. **Category Cards Grid**: Six static financial category cards representing **Food & Dining**, **Transportation**, **Housing & Rent**, **Entertainment**, **Savings & Growth**, and **Utilities & Bills**.

---

## 🎨 Architecture & CSS Techniques

### 1. Page Layout (CSS Grid)
The primary layout shell is constructed using **CSS Grid** (`grid-template-areas` & `grid-template-columns`), dividing the viewport into two main columns (Sidebar at `260px` and Main Content filling the remaining fraction `1fr`).

### 2. Internal Components (Flexbox)
**Flexbox** is used for layout inside components:
* **Header**: Aligns title details and user tools across the horizontal axis (`justify-content: space-between`).
* **Sidebar**: Uses column layout (`flex-direction: column`) to push the user profile pill to the bottom.
* **Category Cards**: Uses Flexbox to align icon headers, budget amount metrics, progress bars, and bottom status labels cleanly.
* **No Absolute Positioning** was used for structural page alignment.

### 3. Theme & CSS Custom Properties (`:root`)
All color values, background surfaces, borders, shadows, and radii are managed through CSS variables defined on `:root`:
* `--brand-color`, `--accent-color`
* `--surface-color`, `--bg-color`
* `--text-primary`, `--text-secondary`
* `--shadow-sm`, `--shadow-md`, `--shadow-hover`

### 4. Stretch Goal: Dark Theme
The theme includes automatic dark mode support using `@media (prefers-color-scheme: dark)`, re-declaring the CSS variables on `:root` to swap background surfaces and text contrast smoothly without duplicating component styles.

### 5. Card Micro-interactions
Each category card features a `200ms ease` transition applying:
* **Hover State**: `-4px` vertical transform (`transform: translateY(-4px)`) and active accent shadow (`box-shadow: var(--shadow-hover)`).
* **Keyboard Focus State**: Full keyboard accessibility (`tabindex="0"`) matching hover effects and adding a distinct focus outline (`:focus-visible`).

### 6. Responsive Breakdown (< 768px)
When viewed on screens below 768px (verified via browser DevTools Device Toolbar):
* The CSS Grid collapses into a single-column layout (`grid-template-columns: 1fr`).
* The cards grid renders as a single-column stack.
* Sidebar items collapse into an inline horizontal bar.

---

## 📁 Repository Structure