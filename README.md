# OrthoNow Landing Page Assignment

## Overview

This project is a conversion-focused landing page built for the campaign:

> **"Get an expert orthopaedic opinion – Book your consultation at OrthoNow."**

The landing page targets **working professionals (28–50 years old) in Bengaluru** who are experiencing knee or back pain.

The project is built as a **single self-contained HTML file** using only **HTML, CSS, and Vanilla JavaScript**, with no external frameworks or libraries.

---

## Features

* Responsive mobile-first layout
* Clear headline and supporting subheadline
* Minimal lead generation form (Name + Phone)
* Trust indicators to improve credibility
* Primary Call-to-Action (CTA)
* Client-side form validation
* GTM-compatible `dataLayer.push()` on successful form submission
* Thank-you state displayed without page reload
* Lightweight implementation optimized for Core Web Vitals

---

## Tech Stack

* HTML5
* CSS3
* Vanilla JavaScript

No frameworks, build tools, or external dependencies are required.

---

## Project Structure

```
/
├── index.html
└── README.md
```

---

## Running the Project

Simply open the `index.html` file in any modern browser.

No server or installation is required.

---

## Form Submission

On successful submission:

1. User inputs are validated.
2. A Google Tag Manager compatible event is pushed to `window.dataLayer`.
3. The form is replaced with a thank-you message.
4. No page reload occurs.

Example event:

```javascript
window.dataLayer.push({
  event: "consultation_form_submitted",
  form_name: "orthonow_landing_page",
  user_name: "Rahul",
  phone_length: 10,
  city: "Bengaluru",
  page_location: window.location.href,
  timestamp: new Date().toISOString()
});
```

---

## Demonstrating GTM Event

To verify the implementation:

1. Open the page in Google Chrome.
2. Open Developer Tools (`F12`).
3. Select the **Console** tab.
4. Fill out the form.
5. Submit the form.

The console will display the event object and the updated `window.dataLayer`, confirming that the GTM event fires only on successful form submission.

---

## Conversion Strategy

The landing page is designed using common conversion optimization principles:

* Problem-focused headline
* Benefit-driven messaging
* Minimal two-field form to reduce friction
* Above-the-fold CTA
* Trust indicators positioned near the form
* Mobile-first responsive layout
* Privacy reassurance below the form

---

## Performance Considerations

To help achieve a high Lighthouse/PageSpeed Mobile score:

* Single HTML file
* No JavaScript frameworks
* No external CSS libraries
* No web fonts
* No render-blocking resources
* Lightweight CSS and JavaScript
* Semantic HTML

---

## Browser Compatibility

Tested for modern browsers including:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

---

## Author

Created as part of the OrthoNow Front-End Landing Page Assessment.
