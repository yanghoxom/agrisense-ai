# AgriSense Company Branding Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rename Qidian VP to AgriSense and visibly identify AgriSense as a product of lembem across the public website.

**Architecture:** Keep the existing static HTML structure and Tailwind CDN styling. Apply direct copy changes to the five existing pages, then add two standalone informational pages using the same navigation and footer patterns. No framework, dependency, or backend change.

**Tech Stack:** Static HTML, Tailwind CSS CDN, existing JavaScript

---

## File map

- Modify `index.html`: home branding, company statement, contact details, metadata, footer links.
- Modify `product.html`: product branding, contact details, metadata, footer links.
- Modify `technology.html`: technology branding, contact details, metadata, footer links.
- Modify `market.html`: market branding, contact details, metadata, footer links.
- Modify `team.html`: founder/company branding, contact details, metadata, footer links.
- Create `company.html`: public lembem ownership and contact information.
- Create `privacy.html`: contact-form privacy disclosure.

### Task 1: Rename existing pages

**Files:**
- Modify: `index.html`
- Modify: `product.html`
- Modify: `technology.html`
- Modify: `market.html`
- Modify: `team.html`

- [ ] **Step 1: Apply exact global replacements**

Across all five files:

```text
Qidian VP                     => AgriSense
founder@qidian-vp.com         => phungha@lembem.com
```

Remove this obsolete sentence wherever present:

```text
QIDIAN — Quantified Intelligent Diagnostic & Insight for Agriculture Network. VP — Vietnam Platform.
```

- [ ] **Step 2: Make company relationship visible**

Use this navigation brand on every page:

```html
<span class="text-2xl font-bold text-[#006e2c] dark:text-[#34a853] font-['Lexend'] tracking-tight">AgriSense <span class="text-sm font-medium text-gray-500">by lembem</span></span>
```

Add this sentence to the home hero description:

```html
AgriSense is a product of <strong class="text-on-surface">lembem</strong>.
```

Use this footer ownership copy on every page:

```html
<p class="font-['Lexend'] text-sm text-gray-500 dark:text-gray-400 max-w-xs leading-relaxed">© 2026 lembem.<br/>AgriSense is a product of lembem.</p>
```

- [ ] **Step 3: Update metadata**

Set page titles to:

```text
index.html       AgriSense by lembem - AI Agronomist for Farmers
product.html     Product | AgriSense by lembem
technology.html  Technology | AgriSense by lembem
market.html      Market Analysis | AgriSense by lembem
team.html        Team | AgriSense by lembem
```

Ensure each page has a description containing:

```text
AgriSense is an agricultural AI product by lembem.
```

- [ ] **Step 4: Add footer links**

Add these links to every footer:

```html
<a class="text-gray-500 hover:text-[#006e2c] transition-all duration-300 hover:underline" href="company.html">Company</a>
<a class="text-gray-500 hover:text-[#006e2c] transition-all duration-300 hover:underline" href="privacy.html">Privacy</a>
```

### Task 2: Add company page

**Files:**
- Create: `company.html`

- [ ] **Step 1: Create a functional company page**

Reuse the existing Tailwind CDN, fonts, colors, navigation, and footer from `team.html`. Use this page-specific content:

```html
<title>Company | AgriSense by lembem</title>
<meta name="description" content="AgriSense is an agricultural AI product developed and operated by lembem in Ho Chi Minh City, Vietnam."/>

<main class="max-w-4xl mx-auto px-8 py-24">
  <p class="text-sm font-bold uppercase tracking-widest text-primary mb-4">Company</p>
  <h1 class="text-5xl md:text-7xl font-bold tracking-tight mb-8">AgriSense is a product of lembem.</h1>
  <p class="text-xl text-on-surface-variant leading-relaxed mb-12">lembem develops and operates AgriSense, an early-stage agricultural AI product focused on practical tools for farmers in Southeast Asia.</p>
  <div class="bg-surface-container-lowest rounded-3xl p-8 border border-outline-variant/20">
    <h2 class="text-2xl font-bold mb-6">Company details</h2>
    <dl class="space-y-4 text-on-surface-variant">
      <div><dt class="font-bold text-on-surface">Company</dt><dd>lembem</dd></div>
      <div><dt class="font-bold text-on-surface">Product</dt><dd>AgriSense</dd></div>
      <div><dt class="font-bold text-on-surface">Location</dt><dd>Ho Chi Minh City, Vietnam</dd></div>
      <div><dt class="font-bold text-on-surface">Contact</dt><dd><a class="text-primary font-semibold hover:underline" href="mailto:phungha@lembem.com">phungha@lembem.com</a></dd></div>
    </dl>
  </div>
</main>
```

### Task 3: Add privacy page

**Files:**
- Create: `privacy.html`

- [ ] **Step 1: Create a concise privacy notice**

Reuse the same page shell as `company.html`. Use this page-specific content:

```html
<title>Privacy | AgriSense by lembem</title>
<meta name="description" content="Privacy notice for the AgriSense website, a product of lembem."/>

<main class="max-w-4xl mx-auto px-8 py-24">
  <p class="text-sm font-bold uppercase tracking-widest text-primary mb-4">Privacy</p>
  <h1 class="text-5xl md:text-7xl font-bold tracking-tight mb-8">Privacy Notice</h1>
  <p class="text-on-surface-variant mb-10">Last updated: August 17, 2026</p>
  <div class="space-y-10 text-on-surface-variant leading-relaxed">
    <section><h2 class="text-2xl font-bold text-on-surface mb-3">Information we collect</h2><p>When you submit the contact form, lembem receives the name and email address you provide, submission time, and referral source.</p></section>
    <section><h2 class="text-2xl font-bold text-on-surface mb-3">How we use it</h2><p>We use this information only to respond to your request, share requested AgriSense materials, and manage potential collaboration or early-access interest.</p></section>
    <section><h2 class="text-2xl font-bold text-on-surface mb-3">Storage and sharing</h2><p>Form submissions are stored in a private Google Sheet. We do not sell personal information. We share it only with service providers needed to operate the website or when required by law.</p></section>
    <section><h2 class="text-2xl font-bold text-on-surface mb-3">Your choices</h2><p>You may request access, correction, or deletion of your submission by emailing <a class="text-primary font-semibold hover:underline" href="mailto:phungha@lembem.com">phungha@lembem.com</a>.</p></section>
    <section><h2 class="text-2xl font-bold text-on-surface mb-3">Contact</h2><p>lembem, Ho Chi Minh City, Vietnam. Email: <a class="text-primary font-semibold hover:underline" href="mailto:phungha@lembem.com">phungha@lembem.com</a>.</p></section>
  </div>
</main>
```

### Task 4: Validate public identity and links

**Files:**
- Verify: all seven HTML files

- [ ] **Step 1: Check obsolete branding is gone**

Run:

```powershell
rg -n "Qidian VP|QIDIAN|qidian-vp\.com" -g "*.html"
```

Expected: no matches.

- [ ] **Step 2: Check required identity appears everywhere**

Run:

```powershell
rg -l "lembem" -g "*.html"
rg -l "phungha@lembem\.com" -g "*.html"
```

Expected: all seven HTML files appear in both results.

- [ ] **Step 3: Check local links**

Run a PowerShell script that extracts local `.html` links from all pages and fails when a target does not exist:

```powershell
$missing = @()
Get-ChildItem *.html | ForEach-Object {
  $source = $_
  [regex]::Matches((Get-Content $source.FullName -Raw), 'href="([^"#?]+\.html)(?:#[^"]*)?"') | ForEach-Object {
    $target = Join-Path $source.DirectoryName $_.Groups[1].Value
    if (-not (Test-Path $target)) { $missing += "$($source.Name): $($_.Groups[1].Value)" }
  }
}
if ($missing) { $missing; exit 1 }
"All local HTML links resolve."
```

Expected: `All local HTML links resolve.`

- [ ] **Step 4: Review final diff**

Run:

```powershell
git --no-pager diff --check
git --no-pager diff --stat
```

Expected: no whitespace errors; only planned HTML and documentation files changed.

No commit is included because repository changes require explicit user consent.
