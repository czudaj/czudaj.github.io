# czudaj.github.io

Strona konta w GitHub Pages: lista aplikacji i strony główne aplikacji.
Domena `czudaj.github.io` jest weryfikowana w Google Search Console na potrzeby
ekranu zgody OAuth (projekty Google Cloud aplikacji).

| Adres | Plik |
|---|---|
| https://czudaj.github.io/ | `index.html` – lista aplikacji |
| https://czudaj.github.io/modlitewnik/ | `modlitewnik/index.html` – strona główna Modlitewnika |
| https://czudaj.github.io/modlitewnik/warunki/ | `modlitewnik/warunki/index.html` – warunki korzystania |
| https://czudaj.github.io/Modlitewnik-Privacy-Policy/ | osobne repozytorium `Modlitewnik-Privacy-Policy` |

Kolejną aplikację dodaj jako nowy katalog (np. `nazwa-aplikacji/`) i wpis w `index.html`.
Raz zweryfikowana domena wystarcza dla wszystkich aplikacji.

## Publikacja

1. Na GitHubie utwórz **publiczne** repozytorium o nazwie dokładnie `czudaj.github.io`
   (puste, bez README, żeby nie było konfliktu z lokalnym commitem).
2. W tym katalogu (repozytorium Git na gałęzi `main` jest już zainicjowane):

   ```powershell
   git add .
   git commit -m "Strona konta i strona główna Modlitewnika"
   git remote add origin https://github.com/czudaj/czudaj.github.io.git
   git push -u origin main
   ```

3. Repozytorium → Settings → Pages: źródło „Deploy from a branch”, gałąź `main`, katalog `/ (root)`.
   Po minucie strona działa pod https://czudaj.github.io/.

## Weryfikacja domeny w Google Search Console

Zaloguj się kontem, które jest **Właścicielem lub Edytorem** projektu Google Cloud `modlitewnik`.

1. https://search.google.com/search-console → Dodaj usługę → **Prefiks URL** → `https://czudaj.github.io/`
   (opcja „Domena” wymaga DNS, którego na github.io nie da się ustawić).
2. Wybierz metodę **Plik HTML**, pobierz plik `googleXXXXXXXX.html`, skopiuj go do katalogu głównego
   tego repozytorium, zrób commit i push. Gdy plik będzie dostępny pod
   `https://czudaj.github.io/googleXXXXXXXX.html`, kliknij „Zweryfikuj”.
   Nie usuwaj tego pliku po weryfikacji.

## Ekran zgody OAuth (Google Auth Platform → Branding)

https://console.cloud.google.com/auth/branding?project=modlitewnik

- Nazwa aplikacji: `Modlitewnik`
- Adres e-mail pomocy: konto Google lub grupa Google (widoczny dla użytkowników)
- Strona główna: `https://czudaj.github.io/modlitewnik/`
- Polityka prywatności: `https://czudaj.github.io/Modlitewnik-Privacy-Policy/`
- Warunki korzystania: `https://czudaj.github.io/modlitewnik/warunki/`
- Autoryzowane domeny: `czudaj.github.io`
- Dane kontaktowe dewelopera: Twój adres e-mail

Następnie „Verify Branding”, a po pozytywnym wyniku „Publish branding” (w ciągu 7 dni).
Zmiana nazwy, logo, adresów lub domen po weryfikacji wymaga ponownej weryfikacji.
