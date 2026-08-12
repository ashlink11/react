# react

### repo setup notes
---
This package will install:
Node.js v24.18.0 to /usr/local/bin/node
npm v11.16.0 to /usr/local/bin/npm

### layout.tsx notes
---
tailwind css classes used on the `body` tag:
- `min-h-full` (`min-height: 100%;` or `min-height: 100vh;` depending on parent setup):
- `flex` (`display: flex;`), p.s. children can be `<header>`, `<main>`, and `<footer>`
- `flex-col` (`flex-direction: column;`)

classes used on the `html` tag:
- `h-full` which means `height: 100%;`

`{children}`:
- Anything placed in `layout.tsx` (like a `<Navbar/>`, `<footer>`, or global font setup) remains mounted and shared across pages, while `{children}` changes dynamically based on the current route
- `RootLayout` is a wrapper for the `Home` component
- `layout.tsx` is required
