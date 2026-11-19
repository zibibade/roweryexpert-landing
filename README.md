# zbind.pl — strona projektu RoweryExpert

Statyczna strona projektu (landing) opublikowana pod <https://zbind.pl/roweryexpert/>.

Projekt, który opisuje: **[RoweryExpert — panel serwisowy](https://github.com/zibibade/roweryexpert)** —
panel dla serwisu rowerowego w PHP 8 + MySQL, open source (MIT).

## Zawartość

| Plik | Rola |
|---|---|
| `index.html` | gotowa strona (samodzielny plik: CSS inline, bez fontów zewnętrznych, bez frameworków) |
| `img/screen-*.png` | zrzuty panelu (1440×900 i 390×844) — dane przykładowe, wygenerowane z atrap w `mockups/` |
| `mockups/*.html` | atrapy ekranów panelu, z których powstały zrzuty (statyczny HTML + `panel.css`) |
| `mockups/panel.css` | arkusz panelu użyty w atrapach (kopia robocza, nie jest częścią produktu) |

## Wdrożenie

Strona jest jednym plikiem HTML i leży w katalogu `/roweryexpert/` na `zbind.pl`.
Aktualizacja = podmiana `index.html` i `img/` na serwerze.

Zrzuty odtwarzamy z atrap przez Chromium w trybie headless:

```bash
chromium --headless --no-sandbox --hide-scrollbars --window-size=1440,900 \
  --virtual-time-budget=4000 --screenshot=img/screen-lista.png mockups/lista.html
```

Rozmiary: lista/karta/kalendarz `1440×900`, mobile `390×844`.

## Zasady treści

- Zero wzmianek o klientach, danych klientów i adresach produkcyjnych.
- Zero emoji, zero marketingu bez pokrycia — opisujemy to, co panel naprawdę robi.
- Nazwy własne w kodzie („RoweryExpert”) są stałe; strona mówi o projekcie, nie o konkretnym serwisie.

## Licencja

Kod strony: MIT. Zrzuty przedstawiają interfejs RoweryExpert (MIT).
