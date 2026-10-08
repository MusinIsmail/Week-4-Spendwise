# SpendWise Dashboard Shell

A clean, responsive financial dashboard layout built using modern CSS layout techniques (CSS Grid & Flexbox), CSS Custom Properties, accessible micro-interactions, and dark mode support.

---

## 🚀 Overview & What Was Built

The **SpendWise Dashboard Shell** serves as the foundation for a personal budget tracking capstone project. It implements a modern layout composed of:

1. **Sidebar Navigation**: App branding, primary section links, and user account avatar.
2. **Header Bar**: Dashboard title, search bar, and notification trigger.
3. **Overview Pills**: High-level spend versus remaining budget figures.
4. **Category Cards Grid**: Six static financial category cards representing **Food & Dining**, **Transportation**, **Housing & Rent**, **Entertainment**, **Savings & Growth**, and **Utilities & Bills**.

---

## 🎨 Core Technical Implementation

### 1. Theme Variables (`:root`)
Color scheme defined using standardized CSS custom properties on `:root`:
* `--brand`: Primary application color (`#2563eb`)
* `--accent`: Positive status accent (`#22c55e`)
* `--surface`: Surface background color (`#ffffff`)
* `--background`: Page background (`#f5f7fb`)
* `--text`: Primary text color (`#1f2937`)

### 2. Page Layout (CSS Grid & Flexbox)
* **Overall Page Grid**: `.dashboard` sets `display: grid; grid-template-columns: 250px 1fr;`.
* **Internal Component Alignment**: Flexbox (`display: flex`) aligns elements inside `.header`, `.sidebar`, and `.card`.
* **No absolute positioning** is used for page structure.

### 3. Card Micro-Interactions
Card elements (`.card`) use smooth transitions lasting 250ms or less:
```css
.card {
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.card:hover,
.card:focus {
  transform: translateY(-4px);
  box-shadow: var(--shadow-hover);
}