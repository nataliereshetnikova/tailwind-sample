# Tutorial
[Sample project from creator](https://tailwindcss.com/course/setting-up-tailwind-and-postcss/)

# Setting up

- Start from
```
- npm install tailwindcss postcss-cli autoprefixer 
```
- create tailwind.config.js
```
- npx tailwind init
```
- create postcss.config.js with code inside:
``` js
module.exports = {
	plugins:[
        require('tailwindcss'),
        require('autoprefixer'),
    ]
}
``` 
- create css/tailwind.css with markers:
<br> /* tailwind will look up for your custom markers and replace tailwind generated code */
```

@tailwind base;
@tailwind components;
@tailwind utilities;
```
- add build command to package.json:
``` js
  "scripts": {
    "build":"postcss css/tailwind.css -o public/build/tailwind.css",
  },
```
- run build command
```
npm run build
```
- include in html as normal stylesherr within head
``` html
<link rel="stylesheet" href="build/tailwind.css">
```
- install live-server globally (works only globally)
```
npm i -g live-server
```
