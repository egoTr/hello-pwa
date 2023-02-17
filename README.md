> 💡 This is a sample `Next.JS/TypeScript` project with `PWA`.
     
# 🧁 Guideline
* [x] Create `Next.JS/TypeScript` project
```bash
# '.' means creating inside the current directory
npx --create-next-app@latest --ts .
```

* [x] Install `next-pwa`
```bash
npm i next-pwa
```

* [x] Update 📝`.gitignore` to ignore PWA entries

* [x] Add PWA icons with various sizes  
Place icons inside folder `public/icons`

* [x] Create 📝`public\manifest.json` file

* [x] Enable PWA by updating 📝`next.config.js` and 📝`pages/_app.tsx`   
📝`next.config.js`
```js
/** @type {import('next').NextConfig} */

const nextConfig = {
  reactStrictMode: true,
}

const withPWA = require('next-pwa')({
  dest: 'public',
})

module.exports = withPWA(nextConfig);
```