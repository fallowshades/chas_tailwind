# Tailwindcss webbsida

Er uppgift är att återskapa toppen av hemsidan på [tailwindcss.com](http://tailwindcss.com). Detta inkluderar allt som är ovanför det svarta kod-fönstret. Sidan ska vara responsive och använda tailwind.

## Hur du klarar uppgiften

#### Skapa ett nytt projekt med vite

```
npm create vite@latest tailwindpage
```

Välj sedan Vanilla och sen Javascript.

1. Byt mapp till nya projektet
2. Installera beroenden från package.json
3. Kör projektet

```
cd tailwindpage
npm install
npm run dev
```

#### Installera tailwind

1. Installera beroenden som behövs för tailwind
2. Skapa tailwinds config fil

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Uppdatera config-filen

```
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Länka till style.css i index.html

```
<link rel="stylesheet" href="style.css" />
```

Lägg till tailwind directives i style.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Börja skriva tailwind klasser

Kör igång dev servern

```
npm run dev
```

I index.html

```
<h1 className="text-3xl font-bold underline">
  Hello world!
</h1>
```

## Sätt upp ett repo med Github

1. Skapa ett repo på github.
2. Ladda up dina filer till github:

```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin <Adressen till ditt repo>
git push -u origin main
```

## Hur du lämnar in

Klicka på uppgiften i canvas och ange länken till ditt repo.

---

### :boom: Success!

Efter denna uppgift vet du hur man skapar ett projekt med vite, intallerar tailwind och använder tailwind-klasser.
