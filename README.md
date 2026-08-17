# react, next.js, typescript

### repo setup notes
---
This package will install:
Node.js v24.18.0 to /usr/local/bin/node
npm v11.16.0 to /usr/local/bin/npm

### layout.tsx & page.tsx notes
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


### typescript notes
---
- `export default function`
- `export const metadata: Metadata = {}`
- `export` is like `public` so the code isn't confined to a file
- `default` lets there be one default component exported from a file
- `function` - each component is a function rather than a class. functions take in props and output/return JSX
- `const` is an object that is exported and can be opened by other files
- `Readonly<{children: React.ReactNode; }>)`
- `Readonly` is a built-in TypeScript utility type
- `React.ReactNode:` is the type assigned to `children`
- `ReactNode` can mean JSX elements, React components, plaintext, fragments, arrays of elements, null, or undefined
- `Readonly` means the state cannot be mutated, it must be passed back to the state machine