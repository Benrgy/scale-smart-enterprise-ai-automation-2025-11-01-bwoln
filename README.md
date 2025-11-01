# Scale Smart Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain, update, and customize the Scale Smart enterprise AI automation landing page. Whether you're updating text, fixing links, or adding new pages, this guide breaks down each task into simple, beginner-friendly steps.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Updating Links](#fixing-and-updating-links)
6. [Creating and Linking Policy Pages](#creating-and-linking-policy-pages)
7. [Common Customization Tasks](#common-customization-tasks)
8. [Troubleshooting](#troubleshooting)

---

## Getting Started

### What You'll Need

- A text editor (such as VS Code, Sublime Text, or even Notepad)
- The `index.html` file from this landing page
- Basic understanding of HTML tags (covered in this guide)
- A web browser to test your changes

### How to Open and Edit the File

1. **Locate your `index.html` file** on your computer
2. **Right-click** on the file
3. **Select "Open with"** and choose your text editor
4. **Make your changes** (following the instructions in this guide)
5. **Save the file** using `Ctrl+S` (Windows) or `Cmd+S` (Mac)
6. **View changes** by opening the HTML file in your web browser

### How to Test Your Changes

After making edits:
1. Save your file
2. Open or refresh your web browser
3. Press `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac) to do a **hard refresh** (this clears the browser cache and shows your latest changes)

---

## Understanding the Page Structure

The landing page is organized into clear sections. Here's what each section does:

### Main Sections of the Page

```
📄 index.html
│
├── <head> - Page metadata and styling (invisible to visitors)
│   ├── Title and description
│   ├── Tailwind CSS framework
│   ├── Font Awesome icons
│   └── Custom styles
│
└── <body> - Visible content
    ├── Header & Navigation (sticky at top)
    ├── Hero Section (main welcome area)
    ├── Features Section (#features)
    ├── Benefits Section (#benefits)
    ├── About Us Section (#about)
    ├── Testimonials Section (#testimonials)
    ├── FAQ Section (#faq)
    ├── Final CTA Section (call-to-action)
    ├── Footer
    └── JavaScript (interactive features)
```

### Why Sections Matter

Each section has an **ID** (like `id="features"`) that allows:
- Navigation links to jump directly to that section
- Smooth scrolling when you click menu items
- Easy organization of content

---

## Updating Text Content

This section shows you exactly where to find and update every piece of text on the landing page.

### 1. Updating the Page Title

The page title appears in your browser tab and in search results.

**Location:** Look for this line near the top of the file (in the `<head>` section):

```html
<title>Scale Smart: Enterprise AI Automation</title>
```

**How to Update:**
1. Find the line above
2. Change the text between `<title>` and `</title>`
3. **Example:** If you want a new title:
   ```html
   <title>Your Company Name: Your Service Description</title>
   ```

**What to Change:**
- Keep it under 60 characters for best search results
- Include your main keyword (like "Enterprise AI Automation")
- Make it descriptive and compelling

---

### 2. Updating the Page Description (Meta Description)

This appears in Google search results below your title.

**Location:** Find this line in the `<head>` section:

```html
<meta name="description" content="Scale Smart: Enterprise AI Automation - Designed for large organizations, our AI automation orchestrates complex operations and integrates seamlessly with existing systems.">
```

**How to Update:**
1. Locate the line above
2. Change the text inside `content="YOUR TEXT HERE"`
3. **Example:**
   ```html
   <meta name="description" content="Your Company: Your Service - Your unique value proposition here.">
   ```

**Tips:**
- Keep it between 150-160 characters
- Include your main keywords
- Make it compelling so people want to click

---

### 3. Updating the Company Name (Logo & Header)

The company name appears in multiple places. Here's how to update each one.

#### Header Logo and Name

**Location:** Find this section in the `<header>` (near the top):

```html
<div class="flex items-center gap-2">
    <div class="w-10 h-10 rounded-lg gradient-orange flex items-center justify-center text-white font-bold text-xl">
        <i class="fas fa-bolt"></i>
    </div>
    <span class="text-2xl font-bold text-gray-900">Scale Smart</span>
</div>
```

**How to Update the Company Name:**
1. Find `<span class="text-2xl font-bold text-gray-900">Scale Smart</span>`
2. Replace `Scale Smart` with your company name
3. **Example:**
   ```html
   <span class="text-2xl font-bold text-gray-900">Your Company Name</span>
   ```

**How to Change the Logo Icon:**
The `<i class="fas fa-bolt"></i>` displays a lightning bolt icon. To change it:
1. Visit [Font Awesome Icons](https://fontawesome.com/icons) (free version)
2. Search for an icon you like
3. Copy the icon name (e.g., `fa-rocket`, `fa-star`, `fa-shield`)
4. Replace `fa-bolt` with your chosen icon
5. **Example:**
   ```html
   <i class="fas fa-rocket"></i>
   ```

**Update Footer Logo Too:**
The footer has the same logo. Find this section near the bottom and update it the same way:

```html
<div class="flex items-center gap-2 mb-4">
    <div class="w-10 h-10 rounded-lg gradient-orange flex items-center justify-center text-white font-bold text-xl">
        <i class="fas fa-bolt"></i>
    </div>
    <span class="text-2xl font-bold text-white">Scale Smart</span>
</div>
```

---

### 4. Updating the Hero Section (Main Headline)

The hero section is the large welcome area at the top.

**Location:** Find this section:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 mb-6 leading-tight tracking-tight">
    Scale Smart: <span class="bg-gradient-to-r from-orange-500 to-orange-600 bg-clip-text text-transparent">Enterprise AI Automation</span>
</h1>
```

**How to Update:**
1. Change `Scale Smart:` to your company name
2. Change `Enterprise AI Automation` to your main service/product
3. The text in `<span>` tags appears in orange gradient color

**Example:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 mb-6 leading-tight tracking-tight">
    Your Company: <span class="bg-gradient-to-r from-orange-500 to-orange-600 bg-clip-text text-transparent">Your Main Service</span>
</h1>
```

---

### 5. Updating the Hero Section Description

**Location:** Find the paragraph below the hero headline:

```html
<p class="text-xl md:text-2xl text-gray-600 mb-8 leading-relaxed max-w-2xl">
    Designed for large organizations, our AI automation orchestrates complex operations and integrates seamlessly with existing systems. Transform your enterprise with intelligent automation that drives efficiency at scale.
</p>
```

**How to Update:**
1. Replace the text between `<p>` and `</p>` tags
2. Keep it 2-3 sentences
3. Focus on benefits and unique value

**Example:**
```html
<p class="text-xl md:text-2xl text-gray-600 mb-8 leading-relaxed max-w-2xl">
    Your compelling value proposition goes here. Explain what you do and why it matters to your customers.
</p>
```

---

### 6. Updating Feature Cards

The page has three feature cards. Here's how to update each one.

**Location:** Find the Features Section around line 200:

```html
<!-- Feature 1: Enterprise-Grade Security -->
<div class="card-hover p-8 rounded-2xl bg-gradient-to-br from-white to-gray-50 border border-gray-200">
    <div class="feature-icon mb-6">
        <i class="fas fa-shield-alt"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Enterprise-Grade Security</h3>
    <p class="text-gray-600 mb-6 leading-relaxed">
        Military-grade encryption, advanced threat detection, and comprehensive compliance frameworks...
    </p>
    <ul class="space-y-3 text-sm text-gray-600">
        <li class="flex items-center gap-2">
            <i class="fas fa-check-circle text-orange-500"></i>
            <span>End-to-end encryption</span>
        </li>
        <!-- More items... -->
    </ul>
</div>
```

**How to Update a Feature Card:**

**Step 1: Change the Icon**
- Find `<i class="fas fa-shield-alt"></i>`
- Replace `fa-shield-alt` with your chosen icon (e.g., `fa-lock`, `fa-key`, `fa-cog`)
- Visit [Font Awesome Icons](https://fontawesome.com/icons) to browse options

**Step 2: Change the Title**
- Find `<h3 class="text-2xl font-bold text-gray-900 mb-4">Enterprise-Grade Security</h3>`
- Replace `Enterprise-Grade Security` with your feature title

**Step 3: Change the Description**
- Find the `<p>` tag with the description
- Replace the text with your feature description

**Step 4: Update the Bullet Points**
- Find each `<li>` item
- Replace the text in `<span>` tags
- Add or remove `<li>` items as needed

**Example of a Complete Updated Feature:**
```html
<div class="card-hover p-8 rounded-2xl bg-gradient-to-br from-white to-gray-50 border border-gray-200">
    <div class="feature-icon mb-6">
        <i class="fas fa-rocket"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Lightning-Fast Deployment</h3>
    <p class="text-gray-600 mb-6 leading-relaxed">
        Get up and running in days, not months. Our streamlined deployment process ensures minimal disruption to your operations.
    </p>
    <ul class="space-y-3 text-sm text-gray-600">
        <li class="flex items-center gap-2">
            <i class="fas fa-check-circle text-orange-500"></i>
            <span>Quick implementation</span>
        </li>
        <li class="flex items-center gap-2">
            <i class="fas fa-check-circle text-orange-500"></i>
            <span>Minimal downtime</span>
        </li>
        <li class="flex items-center gap-2">
            <i class="fas fa-check-circle text-orange-500"></i>
            <span>Expert guidance</span>
        </li>
    </ul>
</div>
```

---

### 7. Updating Benefits Section

The benefits section has three large cards with icons and descriptions.

**Location:** Find the Benefits Section (around line 350):

```html
<!-- Benefit 1: Operational Excellence -->
<div class="card-hover group">
    <div class="p-8 rounded-2xl bg-white border border-gray-200 h-full">
        <div class="w-16 h-16 rounded-xl bg-gradient-to-br from-orange-100 to-orange-50 flex items-center justify-center text-orange-600 text-3xl mb-6 group-hover:scale-110 transition-transform duration-300">
            <i class="fas fa-chart-line"></i>
        </div>
        <h3 class="text-2xl font-bold text-gray-900 mb-4">Achieve Operational Excellence</h3>
        <p class="text-gray-600 leading-relaxed mb-6">
            Streamline workflows, eliminate bottlenecks...
        </p>
        <!-- Arrow list items... -->
    </div>
</div>
```

**How to Update Benefits:**

**Step 1: Change the Icon**
- Find `<i class="fas fa-chart-line"></i>`
- Replace `fa-chart-line` with your icon choice

**Step 2: Change the Title**
- Find and replace `Achieve Operational Excellence`

**Step 3: Change the Description**
- Find the `<p>` tag and update the text

**Step 4: Update the Arrow List Items**
- Find each `<p class="text-gray-600">` inside the list
- Update the text for each benefit point

---

### 8. Updating Testimonials

The testimonials section shows customer quotes. Here's how to update them.

**Location:** Find the Testimonials Section (around line 450):

```html
<!-- Testimonial 1 -->
<div class="card-hover p-8 rounded-2xl bg-white border border-gray-200 shadow-md">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6 text-lg">
        "Scale Smart has been a game-changer..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Sarah Chen</p>
        <p class="text-sm text-gray-600">VP of Operations, Global Finance Corp</p>
    </div>
</div>
```

**How to Update a Testimonial:**

**Step 1: Update the Quote**
- Find the `<p class="text-gray-700 leading-relaxed mb-6 text-lg">`
- Replace the quoted text with your customer's quote
- Keep the quotation marks

**Step 2: Update the Customer Name**
- Find `<p class="font-bold text-gray-900">Sarah Chen</p>`
- Replace with the actual customer's name

**Step 3: Update the Customer Title and Company**
- Find `<p class="text-sm text-gray-600">VP of Operations, Global Finance Corp</p>`
- Replace with the customer's actual job title and company

**Step 4: Change Star Rating (Optional)**
- If you want fewer stars, delete `<i class="fas fa-star star-rating"></i>` lines
- Each `<i>` tag is one star

**Example:**
```html
<div class="card-hover p-8 rounded-2xl bg-white border border-gray-200 shadow-md">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6 text-lg">
        "This company transformed our entire operation. The results were immediate and measurable. Highly recommended!"
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">John Smith</p>
        <p class="text-sm text-gray-600">CEO, Tech Innovations Inc</p>
    </div>
</div>
```

---

### 9. Updating FAQ Items

The FAQ section has expandable questions and answers.

**Location:** Find the FAQ Section (around line 550):

```html
<!-- FAQ Item 1 -->
<div class="faq-item border border-gray-200 rounded-xl overflow-hidden shadow-sm hover:shadow-md transition-shadow duration-300">
    <button class="faq-question w-full p-6 flex items-center justify-between bg-white hover:bg-gray-50 transition-colors duration-300 cursor-pointer focus:outline-none focus:ring-2 focus:ring-orange-500 focus:ring-inset" aria-expanded="false">
        <span class="text-lg font-semibold text-gray-900 text-left">How long does implementation typically take?</span>
        <i class="faq-icon fas fa-chevron-down text-orange-600 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden bg-gray-50 px-6 py-4 border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            Implementation timelines vary based on your organization's complexity...
        </p>
    </div>
</div>
```

**How to Update an FAQ Item:**

**Step 1: Change the Question**
- Find `<span class="text-lg font-semibold text-gray-900 text-left">How long does implementation typically take?</span>`
- Replace with your question

**Step 2: Change the Answer**
- Find `<p class="text-gray-700 leading-relaxed">` inside the `faq-answer` div
- Replace with your answer text

**Step 3: Add or Remove FAQ Items**
- To add a new FAQ, copy an entire `<div class="faq-item">` block
- Paste it before the closing `</div>` of the FAQ section
- Update the question and answer

**Example of New FAQ Item:**
```html
<!-- FAQ Item 6 -->
<div class="faq-item border border-gray-200 rounded-xl overflow-hidden shadow-sm hover:shadow-md transition-shadow duration-300">
    <button class="faq-question w-full p-6 flex items-center justify-between bg-white hover:bg-gray-50 transition-colors duration-300 cursor-pointer focus:outline-none focus:ring-2 focus:ring-orange-500 focus:ring-inset" aria-expanded="false">
        <span class="text-lg font-semibold text-gray-900 text-left">What is your pricing model?</span>
        <i class="faq-icon fas fa-chevron-down text-orange-600 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden bg-gray-50 px-6 py-4 border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            We offer flexible pricing plans tailored to your organization's needs...
        </p>
    </div>
</div>
```

---

### 10. Updating Footer Text

**Location:** Find the footer section (near the bottom):

```html
<p class="text-gray-400 text-sm mb-4 md:mb-0">
    &copy; 2025 Scale Smart. All rights reserved. | Powered by Claude AI
</p>
```

**How to Update:**
- Change `2025` to the current year
- Change `Scale Smart` to your company name
- Update the "Powered by" text as needed

**Example:**
```html
<p class="text-gray-400 text-sm mb-4 md:mb-0">
    &copy; 2025 Your Company Name. All rights reserved.
</p>
```

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility framework that controls styling. Don't worry—you don't need to write complex CSS code. Here's how to make common changes.

### Understanding Tailwind Classes

Tailwind uses short class names that control specific styles. Here's a breakdown:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900">
```

Breaking this down:
- `text-5xl` = Font size (very large)
- `md:text-6xl` = Font size on medium screens and up
- `lg:text-7xl` = Font size on large screens and up
- `font-bold` = Makes text bold
- `text-gray-900` = Text color (dark gray)

### Common Tailwind Classes Explained

| Class | What It Does | Examples |
|-------|--------------|----------|
| `text-*` | Font size | `text-sm`, `text-lg`, `text-2xl`, `text-5xl` |
| `text-*` | Text color | `text-gray-900`, `text-orange-600`, `text-white` |
| `bg-*` | Background color | `bg-white`, `bg-orange-50`, `bg-gray-900` |
| `p-*` | Padding (space inside) | `p-4`, `p-8`, `p-16` |
| `m-*` | Margin (space outside) | `m-4`, `m-8`, `mb-6` |
| `rounded-*` | Corner roundness | `rounded-lg`, `rounded-2xl`, `rounded-full` |
| `font-*` | Font weight | `font-normal`, `font-bold`, `font-semibold` |
| `w-*` | Width | `w-10`, `w-16`, `w-full` |
| `h-*` | Height | `h-10`, `h-16`, `h-full` |
| `flex` | Flexible layout | Used with `gap-*`, `items-center`, `justify-between` |
| `grid` | Grid layout | Used with `grid-cols-1`, `md:grid-cols-2` |
| `hidden` | Hides element | `hidden`, `md:hidden` (hidden on medium+ screens) |

### Responsive Design Prefixes

Tailwind uses prefixes to apply styles at different screen sizes:

```html
<div class="text-lg md:text-2xl lg:text-4xl">
```

- No prefix (`text-lg`) = Applied to all screen sizes
- `md:` = Applied on medium screens and up (tablets)
- `lg:` = Applied on large screens and up (desktops)
- `sm:` = Applied on small screens and up

### Common Customization Tasks with Tailwind

#### Changing Text Color

**Task:** Change the hero headline color from gray to orange

**Original:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900">
```

**Updated:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-orange-600">
```

**Available colors:**
- Gray shades: `text-gray-400`, `text-gray-600`, `text-gray-900`
- Orange shades: `text-orange-500`, `text-orange-600`
- White: `text-white`

---

#### Changing Background Color

**Task:** Change a section's background from white to light orange

**Original:**
```html
<section class="py-20 md:py-28 bg-white">
```

**Updated:**
```html
<section class="py-20 md:py-28 bg-orange-50">
```

**Available backgrounds:**
- `bg-white` (pure white)
- `bg-gray-50` (very light gray)
- `bg-orange-50` (very light orange)
- `bg-gray-900` (dark gray/black)

---

#### Changing Font Size

**Task:** Make feature card titles larger

**Original:**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">Feature Title</h3>
```

**Updated:**
```html
<h3 class="text-3xl font-bold text-gray-900 mb-4">Feature Title</h3>
```

**Size progression:**
- `text-sm` (small)
- `text-base` (normal)
- `text-lg` (large)
- `text-xl` (extra large)
- `text-2xl`, `text-3xl`, `text-4xl` (progressively larger)

---

#### Changing Padding/Spacing

**Task:** Add more space inside a card

**Original:**
```html
<div class="p-8 rounded-2xl">
```

**Updated:**
```html
<div class="p-12 rounded-2xl">
```

**Padding values:**
- `p-4` (small padding)
- `p-8` (medium padding)
- `p-12` (large padding)
- `p-16` (extra large padding)

---

#### Changing Border Radius (Corners)

**Task:** Make corners more rounded

**Original:**
```html
<div class="rounded-lg">
```

**Updated:**
```html
<div class="rounded-2xl">
```

**Roundness options:**
- `rounded-lg` (slightly rounded)
- `rounded-xl` (more rounded)
- `rounded-2xl` (very rounded)
- `rounded-full` (completely circular)

---

#### Adjusting Responsive Behavior

**Task:** Stack features in a single column on tablets instead of two columns

**Original:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

This means:
- 1 column on mobile (`grid-cols-1`)
- 2 columns on tablets and up (`md:grid-cols-2`)
- 3 columns on desktops and up (`lg:grid-cols-3`)

**Updated (for 1 column on tablets, 2 on desktop):**
```html
<div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
```

---

#### Changing Button Colors

**Task:** Change primary button color from orange to blue

**Location:** Find the button style in the `<style>` section:

```html
.btn-primary {
    @apply px-8 py-3 bg-gradient-to-r from-orange-500 to-orange-600 text-white font-semibold rounded-lg transition-all duration-300 hover:shadow-lg hover:scale-105 focus:outline-none focus:ring-2 focus:ring-orange-400 focus:ring-offset-2;
}
```

**Updated:**
```html
.btn-primary {
    @apply px-8 py-3 bg-gradient-to-r from-blue-500 to-blue-600 text-white font-semibold rounded-lg transition-all duration-300 hover:shadow-lg hover:scale-105 focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-offset-2;
}
```

**Changes made:**
- `from-orange-500 to-orange-600` → `from-blue-500 to-blue-600`
- `focus:ring-orange-400` → `focus:ring-blue-400`

---

### Testing Your CSS Changes

After modifying Tailwind classes:

1. **Save the file** (`Ctrl+S` or `Cmd+S`)
2. **Refresh your browser** (`Ctrl+F5` or `Cmd+Shift+R`)
3. **Check mobile view** by pressing `F12` to open developer tools
4. **Resize the browser** to test responsive design

---

## Fixing and Updating Links

Links are crucial for navigation. This section shows you how to find and update every link on the page.

### Understanding Links in HTML

A basic link looks like this:
```html
<a href="https://example.com">Click Here</a>
```

- `<a>` = Link tag
- `href="..."` = Where the link goes
- Text between tags = What visitors see

### All Links on This Page

Here's a complete list of every link that needs updating:

#### 1. Navigation Menu Links

**Location:** In the `<header>` section:

```html
<div class="hidden md:flex items-center gap-8">
    <a href="#features" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">Features</a>
    <a href="#benefits" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">Benefits</a>
    <a href="#about" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">About</a>
    <a href="#testimonials" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">Testimonials</a>
    <a href="#faq" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">FAQ</a>
    <a href="https://test.com" class="btn-primary">Get Started</a>
</div>
```

**What These Links Do:**
- `href="#features"` = Scrolls to Features section
- `href="#benefits"` = Scrolls to Benefits section
- `href="#about"` = Scrolls to About section
- `href="#testimonials"` = Scrolls to Testimonials section
- `href="#faq"` = Scrolls to FAQ section
- `href="https://test.com"` = **NEEDS TO BE UPDATED** - External link

**How to Update the "Get Started" Button:**

**Current:**
```html
<a href="https://test.com" class="btn-primary">Get Started</a>
```

**Updated (Example with your actual URL):**
```html
<a href="https://yourcompany.com/signup" class="btn-primary">Get Started</a>
```

Or if you want it to go to your email:
```html
<a href="mailto:youremail@company.com" class="btn-primary">Get Started</a>
```

---

#### 2. Mobile Menu Links

**Location:** Find the mobile menu section (same links as above, but for mobile):

```html
<div class="mobile-menu hidden md:hidden bg-white border-t border-gray-200 px-4 py-4 space-y-4">
    <a href="#features" class="block text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-orange-600">Features</a>
    <a href="#benefits" class="block text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-orange-600">Benefits</a>
    <a href="#about" class="block text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-orange-600">About</a>
    <a href="#testimonials" class="block text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-orange-600">Testimonials</a>
    <a href="#faq" class="block text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-orange-600">FAQ</a>
    <a href="https://test.com" class="block btn-primary text-center">Get Started</a>
</div>
```

**Update the "Get Started" button here too:**
```html
<a href="https://yourcompany.com/signup" class="block btn-primary text-center">Get Started</a>
```

---

#### 3. Hero Section CTA Buttons

**Location:** In the Hero Section:

```html
<div class="flex flex-col sm:flex-row gap-4">
    <a href="https://test.com" class="btn-primary text-center">
        <i class="fas fa-rocket mr-2"></i>Start Your Transformation
    </a>
    <button class="btn-secondary text-center">
        <i class="fas fa-play-circle mr-2"></i>Watch Demo
    </button>
</div>
```

**Update the Primary Button:**
```html
<a href="https://yourcompany.com/signup" class="btn-primary text-center">
    <i class="fas fa-rocket mr-2"></i>Start Your Transformation
</a>
```

**Note about the "Watch Demo" Button:**
- This is currently a `<button>` tag, not a link
- It would need JavaScript to work (showing a video modal)
- For now, you can either:
  - Leave it as is (it won't do anything)
  - Change it to a link: `<a href="https://youtube.com/your-video" ...>`
  - Or remove it entirely

---

#### 4. Benefits Section CTA Banner

**Location:** In the Benefits Section:

```html
<a href="https://test.com" class="inline-block px-10 py-4 bg-white text-orange-600 font-bold rounded-lg transition-all duration-300 hover:shadow-xl hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-orange-600">
    <i class="fas fa-arrow-right mr-2"></i>Schedule Your Demo Today
</a>
```

**Update:**
```html
<a href="https://yourcompany.com/demo" class="inline-block px-10 py-4 bg-white text-orange-600 font-bold rounded-lg transition-all duration-300 hover:shadow-xl hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-orange-600">
    <i class="fas fa-arrow-right mr-2"></i>Schedule Your Demo Today
</a>
```

---

#### 5. Final CTA Section

**Location:** Near the bottom of the page:

```html
<div class="flex flex-col sm:flex-row gap-4 justify-center">
    <a href="https://test.com" class="inline-block px-10 py-4 bg-white text-orange-600 font-bold rounded-lg transition-all duration-300 hover:shadow-xl hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-orange-600">
        <i class="fas fa-rocket mr-2"></i>Get Started Now
    </a>
    <a href="mailto:bengrauwde@hotmail.com" class="inline-block px-10 py-4 border-2 border-white text-white font-bold rounded-lg transition-all duration-300 hover:bg-white hover:text-orange-600 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-orange-600">
        <i class="fas fa-envelope mr-2"></i>Contact Us
    </a>
</div>
```

**Update the "Get Started Now" Button:**
```html
<a href="https://yourcompany.com/signup" class="inline-block px-10 py-4 bg-white text-orange-600 font-bold rounded-lg transition-all duration-300 hover:shadow-xl hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-orange-600">
    <i class="fas fa-rocket mr-2"></i>Get Started Now
</a>
```

**Update the "Contact Us" Email:**
```html
<a href="mailto:youremail@yourcompany.com" class="inline-block px-10 py-4 border-2 border-white text-white font-bold rounded-lg transition-all duration-300 hover:bg-white hover:text-orange-600 focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-orange-600">
    <i class="fas fa-envelope mr-2"></i>Contact Us
</a>
```

---

#### 6. Footer Navigation Links

**Location:** In the footer section:

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
    <!-- Column 1: Brand -->
    <div>
        <!-- Social media links -->
        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-gray-400 transition-all duration-300 hover:bg-orange-600 hover:text-white focus:outline-none focus:ring-2 focus:ring-orange-500" aria-label="Facebook">
            <i class="fab fa-facebook-f"></i>
        </a>
        <!-- More social links... -->
    </div>

    <!-- Column 2: Product -->
    <div>
        <h3 class="text-white font-bold text-lg mb-6">Product</h3>
        <ul class="space-y-3">
            <li><a href="#features" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Features</a></li>
            <li><a href="#benefits" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Benefits</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Pricing</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Security</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Integration</a></li>
        </ul>
    </div>

    <!-- Column 3: Company -->
    <div>
        <h3 class="text-white font-bold text-lg mb-6">Company</h3>
        <ul class="space-y-3">
            <li><a href="#about" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">About Us</a></li>
            <li><a href="blog.html" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Blog</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Careers</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Press</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Contact</a></li>
        </ul>
    </div>

    <!-- Column 4: Legal -->
    <div>
        <h3 class="text-white font-bold text-lg mb-6">Legal</h3>
        <ul class="space-y-3">
            <li><a href="privacy.html" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Privacy Policy</a></li>
            <li><a href="terms.html" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Terms of Service</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Cookie Policy</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">GDPR</a></li>
            <li><a href="#" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Compliance</a></li>
        </ul>
    </div>
</div>
```

**Update Footer Links:**

For **Social Media Links**, replace `href="#"` with actual URLs:
```html
<a href="https://facebook.com/yourcompany" class="...">
    <i class="fab fa-facebook-f"></i>
</a>
<a href="https://twitter.com/yourcompany" class="...">
    <i class="fab fa-twitter"></i>
</a>
<a href="https://linkedin.com/company/yourcompany" class="...">
    <i class="fab fa-linkedin-in"></i>
</a>
<a href="https://instagram.com/yourcompany" class="...">
    <i class="fab fa-instagram"></i>
</a>
```

For **Product Section**, update placeholder links:
```html
<li><a href="https://yourcompany.com/pricing" class="...">Pricing</a></li>
<li><a href="https://yourcompany.com/security" class="...">Security</a></li>
<li><a href="https://yourcompany.com/integration" class="...">Integration</a></li>
```

For **Company Section**, update placeholder links:
```html
<li><a href="https://yourcompany.com/careers" class="...">Careers</a></li>
<li><a href="https://yourcompany.com/press" class="...">Press</a></li>
<li><a href="https://yourcompany.com/contact" class="...">Contact</a></li>
```

For **Legal Section**, these will be updated in the next section (Creating and Linking Policy Pages).

---

#### 7. Contact Email Link

**Location:** In the footer:

```html
<p class="text-gray-400 text-sm">
    <a href="mailto:bengrauwde@hotmail.com" class="text-orange-500 transition-colors duration-300 hover:text-orange-400">bengrauwde@hotmail.com</a>
</p>
```

**Update with your email:**
```html
<p class="text-gray-400 text-sm">
    <a href="mailto:youremail@yourcompany.com" class="text-orange-500 transition-colors duration-300 hover:text-orange-400">youremail@yourcompany.com</a>
</p>
```

---

### Quick Reference: All Links to Update

| Location | Current | Update To |
|----------|---------|-----------|
| All "Get Started" buttons | `https://test.com` | Your signup/landing page |
| "Contact Us" email | `mailto:bengrauwde@hotmail.com` | Your company email |
| Social Media (Facebook) | `#` | Your Facebook URL |
| Social Media (Twitter) | `#` | Your Twitter URL |
| Social Media (LinkedIn) | `#` | Your LinkedIn URL |
| Social Media (Instagram) | `#` | Your Instagram URL |
| Footer Pricing | `#` | Your pricing page |
| Footer Security | `#` | Your security page |
| Footer Careers | `#` | Your careers page |
| Footer Press | `#` | Your press page |
| Footer Contact | `#` | Your contact page |
| Blog | `blog.html` | Your blog page |
| Privacy Policy | `privacy.html` | ✓ Created in next section |
| Terms of Service | `terms.html` | ✓ Created in next section |
| Cookie Policy | `#` | Your cookie policy page |
| GDPR | `#` | Your GDPR page |
| Compliance | `#` | Your compliance page |

---

## Creating and Linking Policy Pages

This section guides you through creating Privacy Policy and Terms of Service pages and linking them properly.

### Why You Need These Pages

- **Legal Requirement**: Most jurisdictions require privacy policies
- **Trust**: Shows customers you take their data seriously
- **SEO**: Helps search engines understand your site
- **Professionalism**: Expected by enterprise customers

### Step 1: Create the Privacy Policy Page

**Step 1a: Create a New File**

1. Open your text editor
2. Click **File → New File**
3. Save it as `privacy.html` in the same folder as your `index.html`

**Step 1b: Add Basic HTML Structure**

Paste this template into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Scale Smart">
    <meta name="robots" content="noindex, follow">
    <title>Privacy Policy - Scale Smart</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
        .gradient-orange {
            background: linear-gradient(135deg, #ff8c42 0%, #ff6b35 100%);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 rounded-lg gradient-orange flex items-center justify-center text-white font-bold text-xl">
                    <i class="fas fa-bolt"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold text-gray-900">Scale Smart</a>
            </div>
            <a href="index.html" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">
                <i class="fas fa-arrow-left mr-2"></i>Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2025</p>

            <div class="prose prose-lg max-w-none">
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    Scale Smart ("Company," "we," "us," or "our") operates the Scale Smart website and services. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our Service and the choices you have associated with that data.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information Collection and Use</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    We collect several different types of information for various purposes to provide and improve our Service to you.
                </p>
                <h3 class="text-xl font-semibold text-gray-900 mt-6 mb-3">Types of Data Collected:</h3>
                <ul class="list-disc list-inside text-gray-700 mb-6 space-y-2">
                    <li>Personal identification information (name, email address, phone number)</li>
                    <li>Technical data (IP address, browser type, pages visited)</li>
                    <li>Usage data (how you interact with our Service)</li>
                    <li>Marketing data (your preferences and interests)</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Data</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    Scale Smart uses the collected data for various purposes:
                </p>
                <ul class="list-disc list-inside text-gray-700 mb-6 space-y-2">
                    <li>To provide and maintain our Service</li>
                    <li>To notify you about changes to our Service</li>
                    <li>To allow you to participate in interactive features of our Service</li>
                    <li>To provide customer support</li>
                    <li>To gather analysis or valuable information so we can improve our Service</li>
                    <li>To monitor the usage of our Service</li>
                    <li>To detect, prevent and address technical issues</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Security of Data</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    The security of your data is important to us but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Contact Us</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    If you have any questions about this Privacy Policy, please contact us at:
                </p>
                <p class="text-gray-700 mb-6">
                    <strong>Email:</strong> <a href="mailto:youremail@yourcompany.com" class="text-orange-600 hover:text-orange-700">youremail@yourcompany.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 text-sm">
                &copy; 2025 Scale Smart. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

**What to Customize:**
- Replace `youremail@yourcompany.com` with your actual email
- Update the "Last updated" date
- Customize the privacy policy content to match your actual practices
- Change `Scale Smart` to your company name

---

### Step 2: Create the Terms of Service Page

**Step 2a: Create a New File**

1. Open your text editor
2. Click **File → New File**
3. Save it as `terms.html` in the same folder as your `index.html`

**Step 2b: Add Basic HTML Structure**

Paste this template into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Scale Smart">
    <meta name="robots" content="noindex, follow">
    <title>Terms of Service - Scale Smart</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
        .gradient-orange {
            background: linear-gradient(135deg, #ff8c42 0%, #ff6b35 100%);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 rounded-lg gradient-orange flex items-center justify-center text-white font-bold text-xl">
                    <i class="fas fa-bolt"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold text-gray-900">Scale Smart</a>
            </div>
            <a href="index.html" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">
                <i class="fas fa-arrow-left mr-2"></i>Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2025</p>

            <div class="prose prose-lg max-w-none">
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    By accessing and using the Scale Smart website and services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    Permission is granted to temporarily download one copy of the materials (information or software) on Scale Smart's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside text-gray-700 mb-6 space-y-2">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    The materials on Scale Smart's website are provided on an 'as is' basis. Scale Smart makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    In no event shall Scale Smart or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Scale Smart's website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    The materials appearing on Scale Smart's website could include technical, typographical, or photographic errors. Scale Smart does not warrant that any of the materials on its website are accurate, complete, or current. Scale Smart may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    Scale Smart has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Scale Smart of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    Scale Smart may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Contact Us</h2>
                <p class="text-gray-700 mb-6 leading-relaxed">
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p class="text-gray-700 mb-6">
                    <strong>Email:</strong> <a href="mailto:youremail@yourcompany.com" class="text-orange-600 hover:text-orange-700">youremail@yourcompany.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 text-sm">
                &copy; 2025 Scale Smart. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

**What to Customize:**
- Replace `youremail@yourcompany.com` with your actual email
- Update the "Last updated" date
- Customize the terms content to match your actual business terms
- Change `Scale Smart` to your company name

---

### Step 3: Verify Links in index.html

The links to these pages are already in your `index.html` file. Let's verify they're correct:

**Location 1: Footer Legal Section**

Find this in your `index.html`:

```html
<!-- Column 4: Legal -->
<div>
    <h3 class="text-white font-bold text-lg mb-6">Legal</h3>
    <ul class="space-y-3">
        <li><a href="privacy.html" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Terms of Service</a></li>
        <!-- Other links... -->
    </ul>
</div>
```

✅ **These links are already correct!** They point to:
- `privacy.html` - Your Privacy Policy page
- `terms.html` - Your Terms of Service page

---

### Step 4: Test Your Links

1. **Save all three files** in the same folder:
   - `index.html`
   - `privacy.html`
   - `terms.html`

2. **Open `index.html` in your browser**

3. **Scroll to the footer**

4. **Click "Privacy Policy"** - Should open `privacy.html`

5. **Click "Back to Home"** - Should return to `index.html`

6. **Repeat for "Terms of Service"**

**Troubleshooting if links don't work:**
- Make sure all three files are in the exact same folder
- Check that filenames match exactly (case-sensitive on some systems)
- Hard refresh your browser (`Ctrl+F5` or `Cmd+Shift+R`)
- Check for typos in the `href` attributes

---

### Step 5: Update Email Addresses in Policy Pages

Both policy pages have a contact email link. Update it to your actual email:

**In `privacy.html`, find:**
```html
<a href="mailto:youremail@yourcompany.com" class="text-orange-600 hover:text-orange-700">youremail@yourcompany.com</a>
```

**In `terms.html`, find:**
```html
<a href="mailto:youremail@yourcompany.com" class="text-orange-600 hover:text-orange-700">youremail@yourcompany.com</a>
```

**Replace both with your actual email:**
```html
<a href="mailto:your-actual-email@company.com" class="text-orange-600 hover:text-orange-700">your-actual-email@company.com</a>
```

---

### Step 6: Customize Policy Content

The templates I provided are generic. You should customize them to reflect your actual practices:

**For Privacy Policy:**
- Update data collection methods specific to your business
- Describe how you actually use customer data
- List any third-party services you use
- Explain cookie usage if applicable
- Add your data retention policies
- Include information about user rights (GDPR, CCPA, etc.)

**For Terms of Service:**
- Define your service limitations
- Explain user responsibilities
- Include warranty disclaimers
- Add liability limitations
- Explain your refund/cancellation policy
- Include intellectual property information

**Recommendation:** 
Consider having a lawyer review these documents to ensure they comply with applicable laws in your jurisdiction.

---

## Common Customization Tasks

### Task 1: Change the Main Brand Color from Orange to Blue

The entire site uses orange. Here's how to change it to blue throughout.

**Step 1: Update the CSS Gradient Classes**

Find the `<style>` section and update:

**Original:**
```html
.gradient-orange {
    background: linear-gradient(135deg, #ff8c42 0%, #ff6b35 100%);
}

.gradient-orange-light {
    background: linear-gradient(135deg, #ffe5cc 0%, #ffd9b3 100%);
}

.btn-primary {
    @apply px-8 py-3 bg-gradient-to-r from-orange-500 to-orange-600 text-white font-semibold rounded-lg transition-all duration-300 hover:shadow-lg hover:scale-105 focus:outline-none focus:ring-2 focus:ring-orange-400 focus:ring-offset-2;
}

.btn-secondary {
    @apply px-8 py-3 border-2 border-orange-500 text-orange-600 font-semibold rounded-lg transition-all duration-300 hover:bg-orange-50 hover:shadow-md focus:outline-none focus:ring-2 focus:ring-orange-400 focus:ring-offset-2;
}
```

**Updated to Blue:**
```html
.gradient-orange {
    background: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
}

.gradient-orange-light {
    background: linear-gradient(135deg, #dbeafe 0%, #bfdbfe 100%);
}

.btn-primary {
    @apply px-8 py-3 bg-gradient-to-r from-blue-500 to-blue-600 text-white font-semibold rounded-lg transition-all duration-300 hover:shadow-lg hover:scale-105 focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-offset-2;
}

.btn-secondary {
    @apply px-8 py-3 border-2 border-blue-500 text-blue-600 font-semibold rounded-lg transition-all duration-300 hover:bg-blue-50 hover:shadow-md focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-offset-2;
}
```

**Step 2: Replace Orange Classes Throughout HTML**

Search for each of these and replace:
- `text-orange-500` → `text-blue-500`
- `text-orange-600` → `text-blue-600`
- `from-orange-500` → `from-blue-500`
- `to-orange-600` → `to-blue-600`
- `from-orange-100` → `from-blue-100`
- `to-orange-50` → `to-blue-50`
- `text-orange-600` → `text-blue-600`
- `focus:ring-orange-500` → `focus:ring-blue-500`
- `hover:text-orange-600` → `hover:text-blue-600`
- `bg-orange-50` → `bg-blue-50`
- `hover:bg-orange-50` → `hover:bg-blue-50`
- `focus:ring-orange-400` → `focus:ring-blue-400`
- `focus:ring-offset-orange-600` → `focus:ring-offset-blue-600`

**Tip:** Use Find & Replace (Ctrl+H or Cmd+H) in your text editor to make this faster.

---

### Task 2: Add a New Section

**Step 1: Choose Where to Add It**

Sections are typically added after the Testimonials section and before the FAQ. Find this line:

```html
<!-- FAQ Section -->
<section id="faq" class="py-20 md:py-28 bg-white">
```

**Step 2: Add Your New Section Before This**

Insert this template before the FAQ section:

```html
<!-- New Section: Case Studies -->
<section id="case-studies" class="py-20 md:py-28 bg-gradient-to-br from-orange-50 via-white to-orange-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6 tracking-tight">
                Real Results from Real Clients
            </h2>
            <p class="text-xl text-gray-600 mb-12 max-w-3xl mx-auto">
                See how our solutions have transformed businesses across industries
            </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Case Study 1 -->
            <div class="card-hover p-8 rounded-2xl bg-white border border-gray-200">
                <div class="mb-6">
                    <h3 class="text-2xl font-bold text-gray-900 mb-2">Financial Services</h3>
                    <p class="text-sm text-orange-600 font-semibold">Case Study</p>
                </div>
                <p class="text-gray-600 mb-6 leading-relaxed">
                    Global bank reduced transaction processing time by 75% and saved $2M annually.
                </p>
                <div class="flex items-center justify-between pt-6 border-t border-gray-200">
                    <span class="text-sm text-gray-600">Read full case study</span>
                    <i class="fas fa-arrow-right text-orange-600"></i>
                </div>
            </div>

            <!-- Case Study 2 -->
            <div class="card-hover p-8 rounded-2xl bg-white border border-gray-200">
                <div class="mb-6">
                    <h3 class="text-2xl font-bold text-gray-900 mb-2">Healthcare</h3>
                    <p class="text-sm text-orange-600 font-semibold">Case Study</p>
                </div>
                <p class="text-gray-600 mb-6 leading-relaxed">
                    Hospital network improved patient data accuracy by 99% and reduced errors.
                </p>
                <div class="flex items-center justify-between pt-6 border-t border-gray-200">
                    <span class="text-sm text-gray-600">Read full case study</span>
                    <i class="fas fa-arrow-right text-orange-600"></i>
                </div>
            </div>

            <!-- Case Study 3 -->
            <div class="card-hover p-8 rounded-2xl bg-white border border-gray-200">
                <div class="mb-6">
                    <h3 class="text-2xl font-bold text-gray-900 mb-2">E-Commerce</h3>
                    <p class="text-sm text-orange-600 font-semibold">Case Study</p>
                </div>
                <p class="text-gray-600 mb-6 leading-relaxed">
                    Retail company increased order processing speed by 60% during peak season.
                </p>
                <div class="flex items-center justify-between pt-6 border-t border-gray-200">
                    <span class="text-sm text-gray-600">Read full case study</span>
                    <i class="fas fa-arrow-right text-orange-600"></i>
                </div>
            </div>
        </div>
    </div>
</section>
```

**Step 3: Add Navigation Link**

In the header navigation, add a link to your new section:

**Find this:**
```html
<a href="#faq" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">FAQ</a>
```

**Add before it:**
```html
<a href="#case-studies" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">Case Studies</a>
```

Do the same in the mobile menu.

---

### Task 3: Add a Blog Page

**Step 1: Create `blog.html`**

Create a new file called `blog.html` with this content:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Scale Smart Blog - AI Automation Insights and Tips">
    <title>Blog - Scale Smart</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
        .gradient-orange {
            background: linear-gradient(135deg, #ff8c42 0%, #ff6b35 100%);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 rounded-lg gradient-orange flex items-center justify-center text-white font-bold text-xl">
                    <i class="fas fa-bolt"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold text-gray-900">Scale Smart</a>
            </div>
            <a href="index.html" class="text-gray-700 font-medium transition-colors duration-300 hover:text-orange-600">
                <i class="fas fa-arrow-left mr-2"></i>Back to Home
            </a>
        </nav>
    </header>

    <!-- Blog Content -->
    <section class="py-20 md:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Scale Smart Blog</h1>
            <p class="text-xl text-gray-600 mb-12">Insights, tips, and best practices for enterprise AI automation</p>

            <div class="space-y-8">
                <!-- Blog Post 1 -->
                <article class="border-b border-gray-200 pb-8">
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">
                        <a href="#" class="hover:text-orange-600 transition-colors">Getting Started with Enterprise AI Automation</a>
                    </h2>
                    <p class="text-sm text-gray-600 mb-4">Published on January 15, 2025 by Admin</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Enterprise AI automation is transforming how organizations operate. In this guide, we'll walk you through the key steps to implement AI automation in your organization...
                    </p>
                    <a href="#" class="text-orange-600 font-semibold hover:text-orange-700">Read More →</a>
                </article>

                <!-- Blog Post 2 -->
                <article class="border-b border-gray-200 pb-8">
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">
                        <a href="#" class="hover:text-orange-600 transition-colors">5 Ways AI Automation Improves Compliance</a>
                    </h2>
                    <p class="text-sm text-gray-600 mb-4">Published on January 10, 2025 by Admin</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Compliance is critical for enterprises. Discover how AI automation can help you maintain compliance more effectively and reduce risk...
                    </p>
                    <a href="#" class="text-orange-600 font-semibold hover:text-orange-700">Read More →</a>
                </article>

                <!-- Blog Post 3 -->
                <article class="pb-8">
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">
                        <a href="#" class="hover:text-orange-600 transition-colors">Measuring ROI in Your AI Automation Implementation</a>
                    </h2>
                    <p class="text-sm text-gray-600 mb-4">Published on January 5, 2025 by Admin</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        How do you measure the success of your AI automation project? Learn the key metrics and KPIs to track...
                    </p>
                    <a href="#" class="text-orange-600 font-semibold hover:text-orange-700">Read More →</a>
                </article>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 text-sm">
                &copy; 2025 Scale Smart. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

**Step 2: Link to Blog from Footer**

The link is already in your `index.html`:

```html
<li><a href="blog.html" class="text-gray-400 transition-colors duration-300 hover:text-orange-500">Blog</a></li>
```

✅ This is already correct!

---

### Task 4: Change Hero Background Gradient

The hero section has a gradient background. To change it:

**Find this in the Hero Section:**
```html
<div class="absolute inset-0 bg-gradient-to-br from-orange-50 via-white to-orange-50 -z-10"></div>
```

**Change to:**
```html
<div class="absolute inset-0 bg-gradient-to-br from-blue-50 via-white to-blue-50 -z-10"></div>
```

Or for a different effect:
```html
<div class="absolute inset-0 bg-gradient-to-br from-gray-50 via-white to-gray-50 -z-10"></div>
```

---

### Task 5: Adjust Section Spacing

To make sections have more or less vertical space:

**Original:**
```html
<section class="py-20 md:py-28 bg-white">
```

**More space:**
```html
<section class="py-24 md:py-32 bg-white">
```

**Less space:**
```html
<section class="py-16 md:py-24 bg-white">
```

Spacing values:
- `py-12` (small)
- `py-16` (medium-small)
- `py-20` (medium)
- `py-24` (medium-large)
- `py-28` (large)
- `py-32` (extra large)

---

## Troubleshooting

### Problem: Changes Don't Appear When I Refresh

**Solution:**
1. Save your file (Ctrl+S or Cmd+S)
2. Do a **hard refresh**: Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)
3. Wait a few seconds for the page to load

**Why this happens:** Browsers cache (store) old versions of pages. A hard refresh forces your browser to download the latest version.

---

### Problem: Links Don't Work

**Checklist:**
1. ✓ Make sure all files are in the same folder
2. ✓ Check that filenames match exactly (e.g., `privacy.html` not `Privacy.html`)
3. ✓ For external links, make sure they start with `https://` (not `http://`)
4. ✓ For email links, use `mailto:email@example.com`
5. ✓ For section links, make sure the ID exists (e.g., `id="features"`)

**Test a link:**
- Right-click the link
- Select "Open Link in New Tab"
- See if it goes to the right place

---

### Problem: Text is Cut Off or Overlapping

**Likely cause:** Font size is too large or padding is too small

**Solutions:**
1. Reduce font size: `text-5xl` → `text-4xl`
2. Increase padding: `p-8` → `p-12`
3. Increase width: `max-w-3xl` → `max-w-4xl`

---

### Problem: Mobile View Looks Wrong

**Common issues:**
1. Text too large on mobile
2. Elements not stacking properly
3. Padding too large

**Solutions:**
1. Check responsive classes (e.g., `md:text-6xl` means "6xl on medium screens and up")
2. Test in browser developer tools (F12) and use device toolbar
3. Adjust mobile-specific classes (no prefix = mobile)

**Example:**
```html
<!-- Small on mobile, large on desktop -->
<h1 class="text-2xl md:text-4xl lg:text-6xl">
```

---

### Problem: Colors Look Different Than Expected

**Possible causes:**
1. Wrong color name (e.g., `text-gray-600` vs `text-gray-700`)
2. Browser not updated
3. CSS not loading

**Solutions:**
1. Check Tailwind color names: [Tailwind Color Reference](https://tailwindcss.com/docs/customizing-colors)
2. Hard refresh (Ctrl+F5 or Cmd+Shift+R)
3. Check that `<script src="https://cdn.tailwindcss.com"></script>` is in the `<head>`

---

### Problem: Button Text is Wrong or Links to Wrong Place

**Solution:**
1. Find the button code
2. Check the text between `>` and `</a>`
3. Check the `href=""` attribute
4. Update both if needed

**Example:**
```html
<!-- Find this -->
<a href="https://test.com" class="btn-primary">Get Started</a>

<!-- Update to -->
<a href="https://yourcompany.com/signup" class="btn-primary">Start Free Trial</a>
```

---

### Problem: Can't Find Where Something Is on the Page

**Solution:** Use Find & Replace (Ctrl+H or Cmd+H)

1. Open Find & Replace in your editor
2. Search for the text you want to find
3. The editor will highlight where it is in the code

**Example:**
- Search for "Enterprise-Grade Security" to find that feature card
- Search for "Sarah Chen" to find that testimonial
- Search for "test.com" to find all external links

---

### Problem: Accidentally Deleted Something and Can't Undo

**Solution:**
1. Try Ctrl+Z (Windows) or Cmd+Z (Mac) repeatedly to undo
2. If that doesn't work, close without saving and reopen
3. Keep backups of working versions

**Best practice:**
- Save a backup copy before making big changes
- Name it something like `index-backup.html`

---

## Best Practices for Maintenance

### 1. Keep Backups

Before making major changes:
1. Right-click your `index.html`
2. Select "Copy"
3. Right-click in the same folder
4. Select "Paste"
5. Rename to `index-backup.html` or `index-old.html`

This way, if something breaks, you have a working version to restore.

---

### 2. Make One Change at a Time

Don't change multiple things at once. Instead:
1. Change one thing
2. Save and test
3. If it works, move to the next change
4. If it breaks, you know what caused it

---

### 3. Test on Mobile

Always test your changes on mobile devices:
1. Open your page on your phone
2. Check that text is readable
3. Check that buttons are clickable
4. Check that images look good

Or use browser developer tools (F12) to simulate mobile.

---

### 4. Use Comments to Organize

Add comments to help you find things later:

```html
<!-- ===== HERO SECTION ===== -->
<section class="py-20">
    <!-- Hero headline -->
    <h1>...</h1>
    <!-- Hero CTA buttons -->
    <div class="flex">...</div>
</section>

<!-- ===== FEATURES SECTION ===== -->
<section id="features">
    <!-- Feature cards -->
</section>
```

---

### 5. Keep a Change Log

Keep a simple text file documenting changes:

```
CHANGE LOG - Scale Smart Landing Page

January 20, 2025:
- Updated company name to "Tech Innovations Inc"
- Changed hero headline color to blue
- Added new case studies section
- Updated all CTA links to point to /signup

January 15, 2025:
- Created privacy.html and terms.html
- Updated footer with proper legal links
- Added blog.html

January 10, 2025:
- Initial launch of landing page
```

---

## Summary of Key Files and Locations

| File | Purpose | Key Sections |
|------|---------|--------------|
| `index.html` | Main landing page | Header, Hero, Features, Benefits, About, Testimonials, FAQ, Footer |
| `privacy.html` | Privacy Policy | Legal compliance |
| `terms.html` | Terms of Service | Legal compliance |
| `blog.html` | Blog page | Content marketing |

---

## Quick Reference: All Customization Points

### Text Content
- Page title: `<title>` tag
- Meta description: `<meta name="description">`
- Company name: Multiple locations (search for "Scale Smart")
- Hero headline: `<h1>` in hero section
- Feature titles and descriptions: Feature cards
- Benefit titles and descriptions: Benefit cards
- Testimonials: Testimonial cards
- FAQ questions and answers: FAQ items

### Links
- Navigation menu: Desktop and mobile
- CTA buttons: Hero, benefits, final section
- Footer links: Product, company, legal, social
- Email links: Footer contact info

### Colors
- Primary color (orange): CSS gradients and Tailwind classes
- Button colors: `.btn-primary` and `.btn-secondary` in `<style>`
- Text colors: Tailwind `text-*` classes
- Background colors: Tailwind `bg-*` classes

### Spacing & Layout
- Section padding: `py-*` classes
- Element margins: `m-*` and `mb-*` classes
- Grid layouts: `grid-cols-*` and `md:grid-cols-*`
- Responsive design: `md:` and `lg:` prefixes

---

## Getting Help

### Resources
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [HTML Tutorial](https://www.w3schools.com/html/)
- [CSS Tutorial](https://www.w3schools.com/css/)

### Common Questions

**Q: How do I change the font?**
A: Update the `@import` line in the `<style>` section to import a different Google Font.

**Q: How do I add an image?**
A: Use `<img src="path/to/image.jpg" alt="Description">`. Place images in the same folder as your HTML files.

**Q: How do I make a section full-width?**
A: Change `max-w-7xl` to `max-w-full` in the container div.

**Q: How do I add more testimonials?**
A: Copy an entire testimonial card `<div>` block and paste it before the closing `</div>` of the testimonials grid. Update the content.

---

## Conclusion

You now have a comprehensive guide to maintaining and customizing your Scale Smart landing page. Remember:

✅ **Always save before testing**
✅ **Do hard refresh to see changes**
✅ **Make one change at a time**
✅ **Keep backups of working versions**
✅ **Test on mobile devices**

Good luck with your landing page! If you have questions, refer back to this guide or check the resources listed above.