# Mountains Lover

Responsywna strona wizytówkowa o tematyce górskiej. Projekt pokazuje składanie interfejsu z komponentów Vue 3, stylowanie w Tailwind CSS oraz interakcje oparte na CSS (tryb ciemny, nakładki na galerii, karta 3D).

[![Vue.js](https://img.shields.io/badge/Vue.js-3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)](https://vuejs.org/)
[![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ESM-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Flowbite](https://img.shields.io/badge/Flowbite-2-1C64F2?style=flat-square&logo=flowbite&logoColor=white)](https://flowbite.com/)
[![Heroicons](https://img.shields.io/badge/Heroicons-2-0EA5E9?style=flat-square&logo=heroicons&logoColor=white)](https://heroicons.com/)
[![Firebase Hosting](https://img.shields.io/badge/Firebase-Hosting-FFCA28?style=flat-square&logo=firebase&logoColor=black)](https://firebase.google.com/docs/hosting)

**Demo:** [vue-app-b5141.web.app](https://vue-app-b5141.web.app/)

## Co widać na stronie

- Nagłówek z nawigacją desktopową i menu mobilnym.
- Galeria zdjęć górskich z nakładką pojawiającą się po najechaniu.
- Karta z pochyleniem za kursorem i obrotem 3D (hover oraz klawisz Enter).
- Przełącznik motywu jasny/ciemny: zapis w `localStorage` i start od preferencji systemu (`prefers-color-scheme`).
- Stopka z linkami i ikonami społecznościowymi.
- Układ dopasowany do telefonu i szerokich ekranów.

## Stos

| Warstwa | Technologia |
| --- | --- |
| Widok | Vue 3, Composition API (`<script setup>`) |
| Bundler | Vite 5 |
| Style | Tailwind CSS 3, PostCSS, Autoprefixer |
| Komponenty UI | Flowbite, Heroicons |
| Motyw | klasa `dark` na `<html>`, zmienne CSS |
| Hosting | Firebase Hosting (`dist`, rewrite na `index.html`) |

## Uruchomienie

Wymagany Node.js z npm.

```sh
npm install
npm run dev
```

Aplikacja startuje na adresie podanym przez Vite (domyślnie `http://localhost:5173`).

| Polecenie | Działanie |
| --- | --- |
| `npm run dev` | serwer deweloperski z hot reload |
| `npm run build` | build produkcyjny do katalogu `dist` |
| `npm run preview` | podgląd zbudowanej wersji |

Wdrożenie na Firebase Hosting korzysta z `firebase.json` (katalog publiczny: `dist`).

## Struktura

```text
src/
  main.js                 # montowanie aplikacji Vue
  App.vue                 # układ: nagłówek, dwie kolumny, stopka
  components/
    HeaderComponent.vue   # logo, nawigacja, menu mobilne
    DarkModeComponent.vue # przełącznik motywu
    Left.vue              # siatka zdjęć
    InfoComponent.vue     # nakładka na zdjęciu
    Right.vue             # kolumna z kartą
    CardComponent.vue     # karta 3D
    FooterComponent.vue
  css/                    # Tailwind oraz palety light/dark
```

## Zakres

To front-end bez backendu i bez routera. Linki w menu są wizualne. Część widoków (`Gallery.vue`, `LatestArticles.vue`) leży w repozytorium jako wcześniejsze szkice i nie jest podpięta w `App.vue`.
