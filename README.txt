JABBA FOOD TRACKER — DARMOWE WDROŻENIE (Cloudflare Pages + Gemini API Free)

Co jest w paczce:
- index.html, manifest.webmanifest, sw.js — instalowalna aplikacja PWA
- functions/api/analyze.js — bezpieczny endpoint Cloudflare Pages Function
- analiza opisu i zdjęcia przez Gemini 2.5 Flash-Lite, z kluczem trzymanym wyłącznie jako sekret serwera

KOSZT:
- Cloudflare Pages ma plan Free.
- Gemini API ma Free Tier z limitami. Nie ma gwarancji nieograniczonej dostępności; po przekroczeniu limitu trzeba poczekać na reset. Nie dodawaj karty ani nie włączaj płatnego planu, jeśli chcesz zachować zerowy koszt.
- W darmowym planie Google może używać przesłanych danych do ulepszania produktów. Nie przesyłaj zdjęć ani opisów zawierających dane wrażliwe.
- Domenę *.pages.dev dostajesz bez kupowania własnej domeny.

WDROŻENIE:
1. Załóż konto Cloudflare i konto GitHub (oba mogą być bezpłatne).
2. Utwórz nowe repozytorium GitHub i wgraj zawartość tego folderu do katalogu głównego repozytorium.
3. W Cloudflare Dashboard wybierz Workers & Pages → Create → Pages → Connect to Git.
4. Wybierz repozytorium. Framework preset: None; Build command zostaw pusty; Build output directory ustaw na / (root).
5. Po wdrożeniu wejdź w Settings → Variables and Secrets i dodaj GEMINI_API_KEY jako Secret.
6. Wygeneruj klucz w Google AI Studio (https://aistudio.google.com/app/apikey), skopiuj go jako sekret GEMINI_API_KEY w Cloudflare. Nie wklejaj go do aplikacji ani do publicznego repozytorium.
7. Ponownie uruchom deployment (Retry deployment / nowy commit).
8. Otwórz adres *.pages.dev na Pixelu 8 w Chrome → menu → Zainstaluj aplikację.

Uwaga:
- Nie mogę zalogować się do Twoich kont ani wykonać publikacji bez Twojej autoryzacji. W tej paczce wszystko jest przygotowane do darmowego wdrożenia, ale klucz i publikację trzeba skonfigurować na Twoich kontach.
- Darmowe limity AI mogą się zmieniać i być ograniczone dziennie/minutowo. Jeśli limit się skończy, analiza zwróci komunikat, a nie naliczy opłat.
- Dane dziennika pozostają w pamięci przeglądarki na Twoim telefonie; nie synchronizują się między urządzeniami. Regularnie eksportuj kopię.
- Aplikacja jest PWA, nie natywnym plikiem APK.
