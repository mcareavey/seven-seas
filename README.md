# Seven Seas Spa

A responsive multi-page website for **Seven Seas Spa**, a fictional wellness spa, built as a practice project for a Full Stack course.

The spa, its staff, services, testimonials and contact details are all made up. This is not a real business.

## Built with

- HTML5 and CSS3
- [Bootstrap 5.3](https://getbootstrap.com/) (via CDN) for the grid, navbar, cards, carousel and forms
- [Font Awesome](https://fontawesome.com/) for icons
- [Google Fonts](https://fonts.google.com/): **Handlee** for headings, **Quicksand** for sub-headings and buttons
- A single custom stylesheet: `assets/css/styles.css`

There is no build step and no backend. A few lines of plain JavaScript keep the footer year up to date and personalise the thank-you page.

## Pages

| Page      | File             | What's on it |
| --------- | ---------------- | ------------ |
| Home      | `index.html`     | Full-height hero, service cards, wellness tips and a testimonials carousel |
| About     | `about.html`     | Who we are, our mission and team profiles |
| Services  | `services.html`  | Each service in detail, including the yoga class timetable |
| Contact   | `contact.html`   | Contact form (name, email, subject, message) |
| Thank You | `thankyou.html`  | Shown after the contact form is submitted |

Every page shares the same navbar, footer and hero styling. The inner pages use a shorter hero (`.hero-short`) so their content is visible straight away.

### Contact form

The form uses the browser's built-in validation (`required` fields and an email check). Once it's valid, the Send button's `formaction` takes the visitor to `thankyou.html`.

As there is no server, messages aren't actually sent anywhere. The form submits with GET, so the entered details appear in the thank-you page's URL. To make it work for real, point `formaction` at a form-handling service or backend and switch to `formmethod="post"`.

## Design

| Colour    | Use |
| --------- | --- |
| `#3B2F2F` | Main text, headings and buttons |
| `#6F4E37` | Footer background and accents |
| `#FFEBD4` | Hero text, icons and highlights |
| `#FFF6EC` | Cream background bands |

- The layout is responsive from small phones (320px) up to large desktops.
- Photos are prepared in fixed shapes (3:2 for services, square for team and testimonial photos) so they show in full at every screen size without heads being cropped.

## Project structure

```
seven-seas/
├── index.html
├── about.html
├── services.html
├── contact.html
├── thankyou.html
├── README.md
└── assets/
    ├── css/
    │   └── styles.css
    └── images/
        ├── seven-seas-logo.png
        ├── hero-image-1600x900.jpg          # hero background (all pages)
        ├── *-card.jpg                       # service photos (Home and Services)
        ├── testimonial-*-avatar.jpg         # testimonial avatars (Home)
        ├── john_doe.png, jane_smith.png,
        │   emily_johnson.png                # team photos (About)
        └── seven-seas-originals/            # full-size source photos, not used by the site
```

The images used on the site are web-sized copies cropped from the full-size originals in `seven-seas-originals/`. Keep the originals if you need to re-crop an image later.

## Viewing the site

Open `index.html` in a browser, or use the VS Code **Live Server** extension.
