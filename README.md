# Portfolio SEO na GitHub Pages

To jest prosta, statyczna strona portfolio: jeden plik HTML, jeden plik CSS i folder na pliki PDF.

## Struktura plików

```text
portfolio-seo-github/
├── index.html
├── style.css
├── .nojekyll
└── assets/
    └── pdf/
        ├── projekt-strony-internetowej.pdf
        ├── audyt-seo.pdf
        └── plan-contentowy.pdf
```

## Gdzie wrzucać PDF-y?

Wszystkie pliki PDF wrzucaj do folderu:

```text
assets/pdf/
```

Przykład: jeśli plik nazywa się `audyt-sklepu.pdf`, jego ścieżka w HTML będzie taka:

```html
href="assets/pdf/audyt-sklepu.pdf"
```

## Jak dodać nowy kafelek z PDF-em?

W pliku `index.html` znajdź sekcję:

```html
<section class="section work" id="prace">
```

W środku znajduje się lista kafelków w:

```html
<div class="cards">
```

Skopiuj jeden cały blok:

```html
<article class="card">
  <div class="card-top">
    <span class="tag">SEO</span>
    <span class="file-type">PDF</span>
  </div>
  <h3>Tytuł pracy</h3>
  <p>Opis pracy.</p>
  <a class="download-link" href="assets/pdf/nazwa-pliku.pdf" download>
    Pobierz PDF
    <span aria-hidden="true">↓</span>
  </a>
</article>
```

Następnie zmień:
- tekst w `<span class="tag">`,
- tytuł w `<h3>`,
- opis w `<p>`,
- nazwę pliku w `href`.

## Jak opublikować na GitHub Pages?

1. Utwórz nowe repozytorium na GitHubie, np. `portfolio`.
2. Wrzuć do niego pliki z tego folderu.
3. Wejdź w `Settings` repozytorium.
4. Przejdź do `Pages`.
5. W sekcji `Build and deployment` ustaw `Source` na `Deploy from a branch`.
6. Wybierz branch, najczęściej `main`, oraz folder `/root`.
7. Zapisz ustawienia.
8. Po chwili strona będzie dostępna pod adresem podobnym do:

```text
https://twoj-login.github.io/portfolio/
```

Jeżeli nazwiesz repozytorium dokładnie `twoj-login.github.io`, strona może działać jako strona główna użytkownika:

```text
https://twoj-login.github.io/
```

## Co warto podmienić przed publikacją?

- `Twoje Imię i Nazwisko`
- `twoj.email@example.com`
- link do LinkedIna
- opisy projektów
- nazwy plików PDF
- meta description w `<head>`
