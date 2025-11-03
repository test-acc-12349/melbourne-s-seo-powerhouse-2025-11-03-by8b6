# Melbourne SEO Powerhouse - Landing Page Maintenance Guide

Welcome! This comprehensive guide will help you maintain and customize your SEO agency landing page. Whether you're updating text, fixing links, or adding new content, you'll find detailed step-by-step instructions below.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text and Content](#updating-text-and-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing Broken Links](#fixing-broken-links)
6. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
7. [Common Customization Tasks](#common-customization-tasks)
8. [Troubleshooting](#troubleshooting)

---

## Getting Started

### What You'll Need

- A text editor (we recommend **VS Code**, **Notepad++**, or even simple **Notepad**)
- Basic understanding of HTML tags (covered below)
- The `index.html` file open in your editor
- Optional: A web browser to preview changes

### How to Open and Edit the File

1. **Right-click** on your `index.html` file
2. Select **"Open With"** and choose your text editor
3. The file will open showing all the HTML code
4. Make your changes following the instructions in this guide
5. **Save the file** (Ctrl+S on Windows, Cmd+S on Mac)
6. **Refresh your web browser** to see the changes

---

## Understanding the Page Structure

Your landing page is organized into clear sections. Here's what each section does:

| Section | Purpose | Location in Code |
|---------|---------|------------------|
| **Header/Navigation** | Menu bar at top of page | Lines 51-77 |
| **Mobile Menu** | Mobile navigation (hidden on desktop) | Lines 79-91 |
| **Hero Section** | Large banner with main headline | Lines 93-145 |
| **Features Section** | Three feature cards (Keyword Research, On-Page, Technical SEO) | Lines 147-220 |
| **Benefits Section** | Three benefit cards with results | Lines 222-310 |
| **About Section** | Company background and mission | Lines 312-350 |
| **Testimonials Section** | Client reviews and ratings | Lines 352-430 |
| **CTA Section** | Call-to-action banner with background image | Lines 432-460 |
| **FAQ Section** | Frequently asked questions (expandable) | Lines 462-565 |
| **Footer** | Bottom navigation and contact info | Lines 567-635 |

---

## Updating Text and Content

### 1. Updating the Header/Logo Text

**Current Text:** "SEO Powerhouse"

**Location:** Line 54-56

**How to Change:**

1. Find this section:
```html
<div class="flex items-center space-x-2">
    <i class="fas fa-rocket text-blue-600 text-2xl"></i>
    <span class="text-2xl font-bold text-gray-900">SEO Powerhouse</span>
</div>
```

2. Replace `SEO Powerhouse` with your company name:
```html
<span class="text-2xl font-bold text-gray-900">Your Company Name Here</span>
```

3. Save the file and refresh your browser

**Pro Tip:** The logo appears in two places:
- Header navigation (Line 56)
- Footer (Line 596)

Update both for consistency!

---

### 2. Updating Navigation Menu Links

**Current Links:** Features, Benefits, About, Testimonials, FAQ

**Location:** Lines 60-67 (desktop menu) and Lines 81-88 (mobile menu)

**How to Change Menu Text:**

1. **Desktop Menu** - Find this section:
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 smooth-transition font-medium">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 smooth-transition font-medium">Benefits</a>
```

2. Replace the text between the `>` and `</a>`:
```html
<!-- Change FROM this: -->
<a href="#features" class="text-gray-700 hover:text-blue-600 smooth-transition font-medium">Features</a>

<!-- Change TO this: -->
<a href="#features" class="text-gray-700 hover:text-blue-600 smooth-transition font-medium">Our Services</a>
```

3. **Mobile Menu** - Update the same text in Lines 81-88 (inside the `.mobile-menu` div)

**Important:** Don't change the `href="#features"` part - only change the visible text!

---

### 3. Updating the Hero Section (Main Banner)

**Current Headline:** "Melbourne's SEO Powerhouse"

**Location:** Lines 106-108

**How to Change:**

1. Find the main headline:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 tracking-tight">
    Melbourne's SEO Powerhouse
</h1>
```

2. Replace with your headline:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 tracking-tight">
    Your New Headline Here
</h1>
```

**Updating Hero Subheading:**

Find this section (Lines 109-113):
```html
<p class="text-lg md:text-xl text-blue-100 mb-4 leading-relaxed">
    Dominate Google. Skyrocket your traffic and conversions with
</p>
<p class="text-base md:text-lg text-blue-100 mb-8 leading-relaxed">
    Our proven SEO strategies...
</p>
```

Replace the text inside the `<p>` tags with your content:
```html
<p class="text-lg md:text-xl text-blue-100 mb-4 leading-relaxed">
    Your subheading text here
</p>
```

**Updating Hero Statistics:**

Find this section (Lines 130-136):
```html
<div class="text-center">
    <div class="text-3xl font-bold">300%</div>
    <div class="text-sm text-blue-100">Avg Traffic Growth</div>
</div>
```

Change the numbers and labels:
```html
<div class="text-center">
    <div class="text-3xl font-bold">250%</div>
    <div class="text-sm text-blue-100">Your Stat Here</div>
</div>
```

---

### 4. Updating Feature Cards

**Location:** Lines 147-220 (Three feature cards)

Each feature card has this structure:

```html
<div class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl smooth-transition transform hover:scale-105">
    <!-- Icon -->
    <div class="bg-blue-100 w-16 h-16 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-search text-blue-600 text-2xl"></i>
    </div>
    
    <!-- Title -->
    <h3 class="text-xl font-bold text-gray-900 mb-4">Keyword Research Mastery</h3>
    
    <!-- Description -->
    <p class="text-gray-600 leading-relaxed mb-4">
        Our expert team conducts comprehensive keyword research...
    </p>
    
    <!-- Bullet Points -->
    <ul class="space-y-2 text-gray-700">
        <li class="flex items-start space-x-3">
            <i class="fas fa-check text-blue-600 mt-1 flex-shrink-0"></i>
            <span>Competitor analysis and gap identification</span>
        </li>
    </ul>
</div>
```

**To Update a Feature Card:**

1. **Change the Title:**
```html
<!-- Find: -->
<h3 class="text-xl font-bold text-gray-900 mb-4">Keyword Research Mastery</h3>

<!-- Replace with: -->
<h3 class="text-xl font-bold text-gray-900 mb-4">Your New Title</h3>
```

2. **Change the Description:**
```html
<!-- Find: -->
<p class="text-gray-600 leading-relaxed mb-4">
    Our expert team conducts comprehensive keyword research...
</p>

<!-- Replace with: -->
<p class="text-gray-600 leading-relaxed mb-4">
    Your new description text here...
</p>
```

3. **Update Bullet Points:**
```html
<!-- Find: -->
<li class="flex items-start space-x-3">
    <i class="fas fa-check text-blue-600 mt-1 flex-shrink-0"></i>
    <span>Competitor analysis and gap identification</span>
</li>

<!-- Replace with: -->
<li class="flex items-start space-x-3">
    <i class="fas fa-check text-blue-600 mt-1 flex-shrink-0"></i>
    <span>Your new bullet point text</span>
</li>
```

---

### 5. Updating Testimonials

**Location:** Lines 352-430

Each testimonial has this structure:

```html
<div class="testimonial-card bg-white border border-gray-200 p-8 rounded-lg shadow-md hover:shadow-xl smooth-transition">
    <!-- Name and Title -->
    <div class="flex items-center mb-4">
        <div class="flex-1">
            <h3 class="text-lg font-bold text-gray-900">Sarah Mitchell</h3>
            <p class="text-sm text-gray-600">Owner, Mitchell's Dental Clinic</p>
        </div>
    </div>
    
    <!-- Stars (don't change) -->
    <div class="flex items-center mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <!-- 5 star icons -->
    </div>
    
    <!-- Testimonial Text -->
    <p class="text-gray-700 leading-relaxed">
        "The team at Melbourne's SEO Powerhouse..."
    </p>
</div>
```

**To Update a Testimonial:**

1. **Change the Name:**
```html
<!-- Find: -->
<h3 class="text-lg font-bold text-gray-900">Sarah Mitchell</h3>

<!-- Replace with: -->
<h3 class="text-lg font-bold text-gray-900">New Client Name</h3>
```

2. **Change the Job Title:**
```html
<!-- Find: -->
<p class="text-sm text-gray-600">Owner, Mitchell's Dental Clinic</p>

<!-- Replace with: -->
<p class="text-sm text-gray-600">Your Client's Title</p>
```

3. **Change the Testimonial Text:**
```html
<!-- Find: -->
<p class="text-gray-700 leading-relaxed">
    "The team at Melbourne's SEO Powerhouse completely transformed..."
</p>

<!-- Replace with: -->
<p class="text-gray-700 leading-relaxed">
    "Your client's testimonial text here..."
</p>
```

---

### 6. Updating FAQ Answers

**Location:** Lines 462-565

Each FAQ item has this structure:

```html
<div class="faq-item bg-white border border-gray-200 rounded-lg overflow-hidden hover:shadow-md smooth-transition">
    <!-- Question (visible) -->
    <button class="faq-question w-full px-6 py-4 flex items-center justify-between hover:bg-gray-50 smooth-transition cursor-pointer">
        <span class="font-bold text-lg text-gray-900 text-left">How long does it take to see SEO results?</span>
        <i class="faq-icon fas fa-chevron-down text-gray-600 flex-shrink-0 smooth-transition"></i>
    </button>
    
    <!-- Answer (hidden until clicked) -->
    <div class="faq-answer hidden px-6 pb-4 text-gray-700 leading-relaxed border-t border-gray-200 pt-4">
        <p>
            Most clients see initial improvements within 4-8 weeks...
        </p>
    </div>
</div>
```

**To Update an FAQ:**

1. **Change the Question:**
```html
<!-- Find: -->
<span class="font-bold text-lg text-gray-900 text-left">How long does it take to see SEO results?</span>

<!-- Replace with: -->
<span class="font-bold text-lg text-gray-900 text-left">Your new question here?</span>
```

2. **Change the Answer:**
```html
<!-- Find: -->
<div class="faq-answer hidden px-6 pb-4 text-gray-700 leading-relaxed border-t border-gray-200 pt-4">
    <p>
        Most clients see initial improvements within 4-8 weeks...
    </p>
</div>

<!-- Replace with: -->
<div class="faq-answer hidden px-6 pb-4 text-gray-700 leading-relaxed border-t border-gray-200 pt-4">
    <p>
        Your new answer text here...
    </p>
</div>
```

---

### 7. Updating Footer Text

**Location:** Lines 567-635

**Company Description in Footer:**

Find this section (Lines 598-601):
```html
<p class="text-gray-400 text-sm leading-relaxed mb-4">
    Melbourne's leading SEO agency helping businesses dominate Google and drive sustainable growth.
</p>
```

Replace with your description:
```html
<p class="text-gray-400 text-sm leading-relaxed mb-4">
    Your company description here.
</p>
```

**Footer Contact Information:**

Find this section (Lines 627-641):
```html
<div class="flex items-start space-x-4">
    <i class="fas fa-map-marker-alt text-blue-500 mt-1 flex-shrink-0"></i>
    <div>
        <h4 class="text-white font-semibold mb-1">Address</h4>
        <p class="text-gray-400 text-sm">Melbourne, Victoria, Australia</p>
    </div>
</div>
```

Update the address:
```html
<p class="text-gray-400 text-sm">Your Street, Your City, Your State, Country</p>
```

Update the email (Lines 638-644):
```html
<p class="text-gray-400 text-sm"><a href="mailto:test@test.com" class="hover:text-blue-500 smooth-transition">test@test.com</a></p>
```

Replace `test@test.com` with your actual email address (in both places):
```html
<p class="text-gray-400 text-sm"><a href="mailto:your-email@yourcompany.com" class="hover:text-blue-500 smooth-transition">your-email@yourcompany.com</a></p>
```

---

## Modifying Tailwind CSS Classes

### What Are Tailwind Classes?

Tailwind CSS is a system of pre-made style classes. Instead of writing custom CSS, you add class names to HTML elements. For example:

```html
<!-- This creates a blue button with padding -->
<a href="#" class="bg-blue-600 text-white px-6 py-2 rounded-lg">Click Me</a>
```

The classes mean:
- `bg-blue-600` = Blue background
- `text-white` = White text
- `px-6` = Horizontal padding
- `py-2` = Vertical padding
- `rounded-lg` = Rounded corners

### Common Tailwind Classes in Your Landing Page

#### Colors

```
bg-blue-600      = Blue background
bg-white         = White background
bg-gray-50       = Light gray background
text-gray-900    = Dark gray text
text-white       = White text
text-blue-100    = Light blue text
```

**To Change a Color:**

Find the class and replace it:
```html
<!-- Change FROM: -->
<button class="bg-blue-600 text-white px-8 py-3 rounded-lg">Button</button>

<!-- Change TO (using purple): -->
<button class="bg-purple-600 text-white px-8 py-3 rounded-lg">Button</button>
```

**Available Colors:** red, orange, yellow, green, blue, purple, pink, gray

#### Spacing (Padding & Margins)

```
p-8              = Padding all sides
px-6             = Horizontal padding (left & right)
py-3             = Vertical padding (top & bottom)
mb-6             = Margin bottom
mt-4             = Margin top
space-x-2        = Horizontal spacing between items
space-y-4        = Vertical spacing between items
```

#### Text Sizes

```
text-sm          = Small text
text-base        = Normal text
text-lg          = Large text
text-xl          = Extra large
text-2xl         = 2x large
text-3xl         = 3x large
text-4xl         = 4x large
text-5xl         = 5x large
text-6xl         = 6x large
```

**To Make Text Larger:**

```html
<!-- Change FROM: -->
<h2 class="text-3xl font-bold">Heading</h2>

<!-- Change TO: -->
<h2 class="text-5xl font-bold">Heading</h2>
```

#### Responsive Design

Your page automatically adjusts for mobile, tablet, and desktop. Classes like `md:` and `lg:` control this:

```
md:              = Medium screens (tablets)
lg:              = Large screens (desktops)
```

Example:
```html
<!-- This text is 2xl on mobile, 4xl on tablets, 6xl on desktop -->
<h1 class="text-2xl md:text-4xl lg:text-6xl">Responsive Heading</h1>
```

**To Change Responsive Sizes:**

```html
<!-- Change FROM: -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">Heading</h1>

<!-- Change TO: -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">Heading</h1>
```

#### Shadows and Hover Effects

```
shadow-md        = Medium shadow
shadow-xl        = Extra large shadow
hover:shadow-xl  = Shadow appears on hover
hover:scale-105  = Scales up 5% on hover
smooth-transition = Smooth animation
```

### Common Customization Examples

#### Example 1: Change Button Color from Blue to Green

**Find:**
```html
<a href="https://test.com" class="bg-blue-600 text-white px-8 py-3 rounded-lg font-bold hover:bg-blue-700 smooth-transition">
    Start Your Free Audit
</a>
```

**Replace with:**
```html
<a href="https://test.com" class="bg-green-600 text-white px-8 py-3 rounded-lg font-bold hover:bg-green-700 smooth-transition">
    Start Your Free Audit
</a>
```

#### Example 2: Make Feature Cards Larger

**Find:**
```html
<div class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl smooth-transition transform hover:scale-105">
```

**Replace with (adds more padding):**
```html
<div class="feature-card bg-white p-12 rounded-lg shadow-md hover:shadow-xl smooth-transition transform hover:scale-105">
```

#### Example 3: Change Hero Section Background Color

**Find (Line 93):**
```html
<section class="hero-gradient text-white py-24 md:py-32 lg:py-40">
```

The `hero-gradient` is defined in the `<style>` section. To change it, find this (Line 33):
```css
.hero-gradient {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

Change the hex colors:
```css
.hero-gradient {
    background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
}
```

(This creates a blue gradient instead of purple)

---

## Fixing Broken Links

### Understanding Links

A link in HTML looks like this:
```html
<a href="URL_GOES_HERE">Click Text</a>
```

- `href` = The destination (where the link goes)
- Click Text = What users see and click

### Finding All Links in Your Page

Here are all the links that need to be updated:

#### Navigation Links (Should stay as-is)

These are **internal links** (they point to sections on the same page):

```html
<a href="#features">Features</a>      <!-- Points to Features section -->
<a href="#benefits">Benefits</a>      <!-- Points to Benefits section -->
<a href="#about">About</a>            <!-- Points to About section -->
<a href="#testimonials">Testimonials</a> <!-- Points to Testimonials section -->
<a href="#faq">FAQ</a>                <!-- Points to FAQ section -->
```

**These are correct and should NOT be changed.**

#### External Links (Need to be Updated)

These are **external links** that currently point to placeholder URLs:

**Location 1: "Get Started" Button in Header (Line 68)**
```html
<a href="https://test.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 smooth-transition font-semibold">Get Started</a>
```

**Location 2: "Get Started" Button in Mobile Menu (Line 89)**
```html
<a href="https://test.com" class="block bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 smooth-transition font-semibold text-center">Get Started</a>
```

**Location 3: Hero Section - "Start Your Free Audit" (Line 116)**
```html
<a href="https://test.com" class="bg-white text-blue-600 px-8 py-3 rounded-lg font-bold hover:bg-blue-50 smooth-transition transform hover:scale-105 text-center">
    Start Your Free Audit
</a>
```

**Location 4: CTA Section - "Get Your Free SEO Audit" (Line 446)**
```html
<a href="https://test.com" class="bg-blue-600 text-white px-8 py-4 rounded-lg font-bold hover:bg-blue-700 smooth-transition transform hover:scale-105 text-lg">
    Get Your Free SEO Audit
</a>
```

**Location 5: CTA Section - "Contact Us Today" (Line 449)**
```html
<a href="mailto:test@test.com" class="border-2 border-white text-white px-8 py-4 rounded-lg font-bold hover:bg-white hover:text-blue-600 smooth-transition transform hover:scale-105 text-lg">
    Contact Us Today
</a>
```

**Location 6: Footer - Blog Link (Line 617)**
```html
<a href="blog.html" class="text-gray-400 hover:text-blue-500 smooth-transition">Blog</a>
```

**Location 7: Footer - Contact Link (Line 621)**
```html
<a href="https://test.com" class="text-gray-400 hover:text-blue-500 smooth-transition">Contact</a>
```

**Location 8: Footer - Email Link (Line 643)**
```html
<p class="text-gray-400 text-sm"><a href="mailto:test@test.com" class="hover:text-blue-500 smooth-transition">test@test.com</a></p>
```

### How to Fix Broken Links

#### Step 1: Update "Get Started" Buttons

These buttons should link to your booking page, contact page, or lead capture form.

**Find all instances of:**
```html
href="https://test.com"
```

**Replace with your actual URL:**
```html
href="https://yourwebsite.com/get-started"
```

Or if you have a contact form:
```html
href="https://yourwebsite.com/contact"
```

**Complete Updated Example:**
```html
<!-- Change FROM: -->
<a href="https://test.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 smooth-transition font-semibold">Get Started</a>

<!-- Change TO: -->
<a href="https://yourwebsite.com/get-started" class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 smooth-transition font-semibold">Get Started</a>
```

#### Step 2: Update Email Links

**Find:**
```html
<a href="mailto:test@test.com">Contact Us Today</a>
```

**Replace with your email:**
```html
<a href="mailto:your-email@yourcompany.com">Contact Us Today</a>
```

**And update the displayed email address too:**
```html
<!-- Change FROM: -->
<p class="text-gray-400 text-sm"><a href="mailto:test@test.com" class="hover:text-blue-500 smooth-transition">test@test.com</a></p>

<!-- Change TO: -->
<p class="text-gray-400 text-sm"><a href="mailto:your-email@yourcompany.com" class="hover:text-blue-500 smooth-transition">your-email@yourcompany.com</a></p>
```

#### Step 3: Update Blog Link

**Find (Line 617):**
```html
<a href="blog.html" class="text-gray-400 hover:text-blue-500 smooth-transition">Blog</a>
```

**If you have a blog page, update to:**
```html
<a href="https://yourwebsite.com/blog" class="text-gray-400 hover:text-blue-500 smooth-transition">Blog</a>
```

**Or if you don't have a blog yet, remove this link entirely:**
Delete the entire `<li>` containing the blog link.

### Quick Reference: All Links to Update

| Link Text | Current URL | Should Point To |
|-----------|-------------|-----------------|
| Get Started (Header) | https://test.com | Your booking/contact page |
| Get Started (Mobile) | https://test.com | Your booking/contact page |
| Start Your Free Audit | https://test.com | Your booking/contact page |
| Get Your Free SEO Audit | https://test.com | Your booking/contact page |
| Contact Us Today | mailto:test@test.com | Your email address |
| Blog | blog.html | Your blog page URL |
| Contact (Footer) | https://test.com | Your contact page |
| Email (Footer) | mailto:test@test.com | Your email address |

---

## Linking Privacy and Terms Pages

### Understanding What You Need to Do

Your landing page currently has links to "Privacy Policy" and "Terms of Service" pages, but those pages don't exist yet. You need to:

1. Create the privacy and terms HTML files
2. Update the links to point to them correctly

### Step 1: Create Privacy Policy Page

1. **Create a new file** called `privacy.html` in the same folder as your `index.html`

2. **Copy this basic template** into the new file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Melbourne's SEO Powerhouse">
    <title>Privacy Policy | Melbourne's SEO Powerhouse</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-rocket text-blue-600 text-2xl"></i>
                <span class="text-2xl font-bold text-gray-900">SEO Powerhouse</span>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 lg:py-32">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Introduction</h2>
                <p>
                    Melbourne's SEO Powerhouse ("we", "us", "our", or "Company") operates this website. 
                    This page informs you of our policies regarding the collection, use, and disclosure 
                    of personal data when you use our Service and the choices you have associated with that data.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Information Collection and Use</h2>
                <p>
                    We collect several different types of information for various purposes to provide 
                    and improve our Service to you.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Use of Data</h2>
                <p>
                    Melbourne's SEO Powerhouse uses the collected data for various purposes:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>To provide and maintain our Service</li>
                    <li>To notify you about changes to our Service</li>
                    <li>To allow you to participate in interactive features of our Service</li>
                    <li>To provide customer support</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Security of Data</h2>
                <p>
                    The security of your data is important to us but remember that no method of 
                    transmission over the Internet or method of electronic storage is 100% secure.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Contact Us</h2>
                <p>
                    If you have any questions about this Privacy Policy, please contact us at 
                    <a href="mailto:test@test.com" class="text-blue-600 hover:text-blue-700">test@test.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p>&copy; 2025 Melbourne's SEO Powerhouse. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

3. **Save the file** as `privacy.html`

### Step 2: Create Terms of Service Page

1. **Create a new file** called `terms.html` in the same folder as your `index.html`

2. **Copy this basic template** into the new file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Melbourne's SEO Powerhouse">
    <title>Terms of Service | Melbourne's SEO Powerhouse</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-rocket text-blue-600 text-2xl"></i>
                <span class="text-2xl font-bold text-gray-900">SEO Powerhouse</span>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 lg:py-32">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website, you accept and agree to be bound by the terms 
                    and provision of this agreement. If you do not agree to abide by the above, 
                    please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) 
                    on Melbourne's SEO Powerhouse's website for personal, non-commercial transitory viewing only.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Disclaimer</h2>
                <p>
                    The materials on Melbourne's SEO Powerhouse's website are provided on an 'as is' basis. 
                    Melbourne's SEO Powerhouse makes no warranties, expressed or implied, and hereby disclaims 
                    and negates all other warranties including, without limitation, implied warranties or conditions 
                    of merchantability, fitness for a particular purpose, or non-infringement of intellectual property 
                    or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Limitations</h2>
                <p>
                    In no event shall Melbourne's SEO Powerhouse or its suppliers be liable for any damages 
                    (including, without limitation, damages for loss of data or profit, or due to business interruption) 
                    arising out of the use or inability to use the materials on Melbourne's SEO Powerhouse's website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Melbourne's SEO Powerhouse's website could include technical, 
                    typographical, or photographic errors. Melbourne's SEO Powerhouse does not warrant that any 
                    of the materials on its website are accurate, complete, or current.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Contact Us</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at 
                    <a href="mailto:test@test.com" class="text-blue-600 hover:text-blue-700">test@test.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p>&copy; 2025 Melbourne's SEO Powerhouse. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

3. **Save the file** as `terms.html`

### Step 3: Verify Links in index.html

Your `index.html` already has the correct links to these pages. Let's verify they're correct:

**In the Footer (Lines 619-620):**
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-500 smooth-transition">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-500 smooth-transition">Terms of Service</a></li>
```

**In the Footer Bottom (Lines 654-655):**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-500 smooth-transition">Privacy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-500 smooth-transition">Terms</a>
```

✅ **These links are already correct!** They point to `privacy.html` and `terms.html`, which are the files you just created.

### Step 4: Verify File Structure

After creating the files, your folder should look like this:

```
your-website-folder/
├── index.html          (your main landing page)
├── privacy.html        (privacy policy page)
├── terms.html          (terms of service page)
└── blog.html           (optional blog page)
```

### Step 5: Test the Links

1. **Open `index.html`** in your web browser
2. **Scroll to the footer**
3. **Click on "Privacy Policy"** - it should open `privacy.html`
4. **Click on "Terms of Service"** - it should open `terms.html`
5. **Click "Back to Home"** link on those pages - it should return to `index.html`

### Troubleshooting: Links Not Working?

**Problem:** Links show 404 error or don't work

**Solution:**
- Make sure `privacy.html` and `terms.html` are in the **exact same folder** as `index.html`
- Check that filenames match exactly (lowercase, correct spelling)
- Make sure you saved the files with `.html` extension

**Problem:** Links work but styling looks different

**Solution:**
- This is normal. The templates provided are basic.
- To make them match your landing page style, copy the header and footer from `index.html` into the policy pages

---

## Common Customization Tasks

### Task 1: Change Hero Section Background Color

The hero section currently has a purple gradient. To change it:

**Find this in the `<style>` section (Line 33):**
```css
.hero-gradient {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

**Replace with one of these options:**

**Blue Gradient:**
```css
.hero-gradient {
    background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
}
```

**Green Gradient:**
```css
.hero-gradient {
    background: linear-gradient(135deg, #10b981 0%, #059669 100%);
}
```

**Red Gradient:**
```css
.hero-gradient {
    background: linear-gradient(135deg, #ef4444 0%, #dc2626 100%);
}
```

### Task 2: Add a New Testimonial

**Find the testimonials section (Lines 352-430) and add a new card:**

```html
<!-- Add this after the last testimonial -->
<div class="testimonial-card bg-white border border-gray-200 p-8 rounded-lg shadow-md hover:shadow-xl smooth-transition">
    <div class="flex items-center mb-4">
        <div class="flex-1">
            <h3 class="text-lg font-bold text-gray-900">Your Client Name</h3>
            <p class="text-sm text-gray-600">Client's Job Title, Company Name</p>
        </div>
    </div>
    <div class="flex items-center mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 leading-relaxed">
        "Your client's testimonial text here..."
    </p>
</div>
```

### Task 3: Change Button Colors

**All buttons in your page use the blue color scheme (`bg-blue-600`). To change them:**

1. **Find all buttons** - Search for `bg-blue-600` in your code
2. **Replace with your color:**
   - `bg-green-600` for green
   - `bg-purple-600` for purple
   - `bg-red-600` for red
   - `bg-indigo-600` for indigo

**Example:**
```html
<!-- Change FROM: -->
<a href="https://test.com" class="bg-blue-600 text-white px-8 py-3 rounded-lg font-bold hover:bg-blue-700">
    Button Text
</a>

<!-- Change TO: -->
<a href="https://test.com" class="bg-green-600 text-white px-8 py-3 rounded-lg font-bold hover:bg-green-700">
    Button Text
</a>
```

**Important:** When you change `bg-blue-600` to another color, also change the hover state:
- `hover:bg-blue-700` becomes `hover:bg-green-700`

### Task 4: Change Feature Card Icons

Each feature card has an icon. To change them:

**Find the icon in the feature card (Line 158):**
```html
<i class="fas fa-search text-blue-600 text-2xl"></i>
```

**Replace `fa-search` with another icon:**
- `fa-chart-line` = Line chart
- `fa-cogs` = Gears/settings
- `fa-shield-alt` = Shield
- `fa-rocket` = Rocket
- `fa-star` = Star
- `fa-check-circle` = Check mark

**Example:**
```html
<!-- Change FROM: -->
<i class="fas fa-search text-blue-600 text-2xl"></i>

<!-- Change TO: -->
<i class="fas fa-rocket text-blue-600 text-2xl"></i>
```

### Task 5: Add More Feature Cards

Currently you have 3 feature cards. To add a 4th:

**Find the features grid (Line 155):**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

**Change to accommodate 4 columns on desktop:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
```

**Then add a new feature card after the 3rd one:**
```html
<!-- Feature 4: Your New Feature -->
<div class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl smooth-transition transform hover:scale-105">
    <div class="bg-red-100 w-16 h-16 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-star text-red-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Your Feature Title</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Your feature description goes here.
    </p>
    <ul class="space-y-2 text-gray-700">
        <li class="flex items-start space-x-3">
            <i class="fas fa-check text-red-600 mt-1 flex-shrink-0"></i>
            <span>Your bullet point</span>
        </li>
        <li class="flex items-start space-x-3">
            <i class="fas fa-check text-red-600 mt-1 flex-shrink-0"></i>
            <span>Your bullet point</span>
        </li>
    </ul>
</div>
```

---

## Troubleshooting

### Issue 1: Text Changes Not Showing Up

**Problem:** You changed text in the HTML but it's not showing on the website.

**Solution:**
1. Make sure you **saved the file** (Ctrl+S or Cmd+S)
2. **Hard refresh** your browser (Ctrl+Shift+R or Cmd+Shift+R)
3. Close and reopen the browser
4. Check that you edited the correct file

---

### Issue 2: Styling Looks Broken

**Problem:** Colors are wrong, spacing is off, or layout looks strange.

**Solution:**
1. Make sure you didn't accidentally delete any HTML tags
2. Check that you have matching opening and closing tags:
   ```html
   <div>...</div>      ✅ Correct
   <div>...</span>     ❌ Wrong - opening <div> but closing </span>
   ```
3. Verify Tailwind classes are spelled correctly
4. Make sure you're not mixing up class names

---

### Issue 3: Links Don't Work

**Problem:** Clicking links does nothing or shows 404 error.

**Solution:**
1. Check that the URL is correct:
   ```html
   href="https://yourwebsite.com"    ✅ Correct (full URL)
   href="yourwebsite.com"             ❌ Wrong (missing https://)
   href="privacy.html"                ✅ Correct (local file)
   href="privacy"                     ❌ Wrong (missing .html)
   ```

2. For local files, make sure they're in the same folder as `index.html`
3. Check for typos in the filename

---

### Issue 4: Mobile Menu Doesn't Work

**Problem:** The hamburger menu on mobile doesn't open/close.

**Solution:**
1. Make sure you didn't delete or modify the JavaScript code at the bottom
2. Check that the mobile menu button and menu have the correct classes:
   ```html
   <button class="md:hidden mobile-menu-button">  ✅ Correct
   <div class="mobile-menu hidden md:hidden">      ✅ Correct
   ```
3. Refresh the page

---

### Issue 5: FAQ Accordion Doesn't Work

**Problem:** Clicking FAQ questions doesn't expand answers.

**Solution:**
1. Make sure the JavaScript at the bottom is intact
2. Check that each FAQ item has the correct structure:
   ```html
   <div class="faq-item">
       <button class="faq-question">...</button>
       <div class="faq-answer hidden">...</div>
   </div>
   ```
3. Verify the `hidden` class is on the answer div
4. Refresh the page

---

### Issue 6: Hero Section Image Not Showing

**Problem:** The hero section looks empty or has no background image.

**Solution:**
1. The hero section uses a gradient, not an image - this is normal
2. If you want to add a background image, find the hero section (Line 93):
   ```html
   <section class="hero-gradient text-white py-24 md:py-32 lg:py-40">
   ```
   
   And modify it:
   ```html
   <section class="hero-gradient text-white py-24 md:py-32 lg:py-40" style="background-image: url('YOUR_IMAGE_URL'); background-size: cover; background-position: center;">
   ```

---

### Issue 7: Colors Look Different on Mobile

**Problem:** Colors or styling looks different on phone vs desktop.

**Solution:**
1. This is usually intentional - responsive design adapts to screen size
2. Check if you accidentally changed responsive classes (like `md:` or `lg:`)
3. Test on actual devices, not just browser zoom

---

### Issue 8: Page Loading Slowly

**Problem:** The website takes a long time to load.

**Solution:**
1. Check if you added large image files - optimize them
2. Remove unnecessary images or content
3. Make sure external resources (CDN links) are working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>  ✅ Should load from internet
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">  ✅ Should load from internet
   ```

---

## Final Checklist

Before publishing your landing page, verify:

- [ ] All text has been updated to your company information
- [ ] All links have been updated (no more `https://test.com`)
- [ ] Email addresses are correct
- [ ] Contact information in footer is accurate
- [ ] Phone number is added (if applicable)
- [ ] Logo/branding matches your company
- [ ] Colors match your brand (if you want to change them)
- [ ] All testimonials are updated or removed
- [ ] FAQ questions and answers are relevant
- [ ] Privacy and Terms pages are created and linked
- [ ] Social media links are updated (or removed)
- [ ] Blog link works (or is removed)
- [ ] All buttons link to correct pages
- [ ] Page looks good on mobile
- [ ] Page loads quickly
- [ ] No broken links (test each one)
- [ ] Spelling and grammar are correct

---

## Quick Reference Guide

### Common File Locations

| Element | Line Number |
|---------|-------------|
| Header Logo | 54-56 |
| Navigation Links | 60-67 |
| Hero Title | 106-108 |
| Hero Subtitle | 109-113 |
| Feature Cards | 147-220 |
| Benefit Cards | 222-310 |
| About Section | 312-350 |
| Testimonials | 352-430 |
| FAQ Section | 462-565 |
| Footer | 567-635 |

### Common Tailwind Classes

| Class | Does | Example |
|-------|------|---------|
| `bg-blue-600` | Blue background | `class="bg-blue-600"` |
| `text-white` | White text | `class="text-white"` |
| `px-8` | Horizontal padding | `class="px-8"` |
| `py-3` | Vertical padding | `class="py-3"` |
| `text-3xl` | Large text | `class="text-3xl"` |
| `md:text-5xl` | Larger text on tablets | `class="md:text-5xl"` |
| `lg:text-6xl` | Largest text on desktop | `class="lg:text-6xl"` |
| `rounded-lg` | Rounded corners | `class="rounded-lg"` |
| `shadow-md` | Medium shadow | `class="shadow-md"` |
| `hover:bg-blue-700` | Darker on hover | `class="hover:bg-blue-700"` |

### Common Icon Names

| Icon | Class | Use |
|------|-------|-----|
| Search | `fa-search` | Keyword research |
| Chart | `fa-chart-line` | Analytics |
| Gear | `fa-cogs` | Settings/Technical |
| Star | `fa-star` | Rating |
| Rocket | `fa-rocket` | Launch |
| Trophy | `fa-trophy` | Achievement |
| Check | `fa-check` | Confirmation |
| Phone | `fa-phone` | Contact |
| Email | `fa-envelope` | Email |

---

## Need More Help?

### Resources

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **Font Awesome Icons:** https://fontawesome.com/icons
- **HTML Basics:** https://www.w3schools.com/html/
- **CSS Basics:** https://www.w3schools.com/css/

### Common Mistakes to Avoid

1. ❌ Deleting opening or closing tags
2. ❌ Forgetting to save the file
3. ❌ Not hard-refreshing the browser
4. ❌ Changing link text instead of the `href`
5. ❌ Mixing up class names (e.g., `md:` vs `lg:`)
6. ❌ Forgetting the `https://` in external links
7. ❌ Using spaces in filenames (use hyphens: `my-file.html`)

---

## Summary

You now have a fully customizable landing page! Remember:

✅ **Update text** in HTML tags (between `>` and `</`)
✅ **Change links** in the `href` attribute
✅ **Modify colors** by changing Tailwind class names
✅ **Keep the structure** - don't delete tags
✅ **Always save** and refresh your browser
✅ **Test everything** before publishing

Good luck with your landing page! If you get stuck, refer back to the specific sections in this guide.