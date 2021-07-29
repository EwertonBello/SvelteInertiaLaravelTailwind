# Svelte + Inertia + Laravel + Tailwind

Simple implementation of Svelte + Inertia + Laravel + Tailwind

## Steps - Svelte + Inertia

01 - https://inertiajs.com/server-side-setup  

02 - https://inertiajs.com/client-side-setup  

03 - `npm install laravel-mix-svelte --save-dev`  
reference: https://github.com/wewowweb/laravel-mix-svelte  

04 - Configure `laravel-mix-svelte` in `webpack.mix.js`  
```js
// add laravel-mix-svelte
require('laravel-mix-svelte');

// and call svelte()
mix.js('resources/js/app.js', 'public/js')
    .svelte();
```  

05 - `npm install svelte svelte-loader --save-dev`  
reference: https://github.com/sveltejs/svelte-loader  

06 - Create dir `Pages` in `./resources/js/`

07 - `npm i && npm run dev`  

## Steps - Tailwind  

01 - `npm install -D tailwindcss@latest postcss@latest autoprefixer@latest`  

02 - `npx tailwindcss init`  

03 - Configure tailwind with `purge` in `tailwind.config.js`, add paths:  
```js
   purge: [
     './resources/**/*.blade.php',
     './resources/**/*.js',
     './resources/**/*.svelte',
   ]
```

04 - Configure Laravel Mix in `webpack.mix.js`  
```js
// add tailwindcss in postCss
mix.js("resources/js/app.js", "public/js")
    .postCss("resources/css/app.css", "public/css", [
        require("tailwindcss"),
    ]);
```

05 - Include directives in `./resources/css/app.css`  
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
