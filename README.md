# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build
A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)
Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 | 16-01-2026</p>
```

✅ This proof must be visible in your browser screenshot submission.

## Dynamic Deployment Date in Footer

### Requirement
The website footer displays the date in `DD Mon YYYY` format, along with the group and week information.

### Implementation
Option A — JavaScript is used to generate the date dynamically. The HTML contains a `<span>` element with the ID `deployDate`, and JavaScript inserts the formatted date into that element.

### Code Snippet

```html
Date: <span id="deployDate"></span>

<script>
  const today = new Date();

  const options = {
    day: "2-digit",
    month: "short",
    year: "numeric"
  };

  document.getElementById("deployDate").textContent =
    today.toLocaleDateString("en-GB", options);
</script>
```

### Expected Output
`Date: 24 Oct 2026`

The date updates automatically based on the visitor's browser date whenever the page loads. This implementation does not record the actual deployment timestamp.
