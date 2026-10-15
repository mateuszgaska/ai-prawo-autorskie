# Sztuczna inteligencja a prawa autorskie

Prezentacja akademicka Mateusza Gąski. Politechnika Częstochowska, Finanse i rachunkowość w biznesie, I semestr 2026/2027.

29 slajdów, plan wystąpienia około 30 minut. Aktualna treść, notatki i bibliografia są częścią strony.

## Korzystanie

1. Otwórz `index.html` z hostingu GitHub Pages na komputerze.
2. Wybierz „Połącz telefon”.
3. Zeskanuj kod QR telefonem albo skopiuj pełny link do pilota. Sam numer sesji nie wystarcza do sterowania.
4. Pozostaw prezentację otwartą na komputerze. Telefon pokazuje notatki i steruje slajdami.

Najpewniejsze połączenie: oba urządzenia w tej samej sieci Wi-Fi albo komputer podłączony do hotspotu telefonu. Urządzenia potrzebują internetu podczas zestawiania połączenia. Nie zamykaj i nie usypiaj komputera podczas wystąpienia.

Pełny ekran: przycisk lub F; wyjście: Esc. Klawiatura: strzałki, PageUp/PageDown, Home/End. Pilot obsługuje wybór slajdu, wygaszanie ekranu, podpowiedzi, pełny tekst i stoper.

## Połączenie

Komputer przechowuje bieżący slajd w otwartej karcie. Pilot używa komunikatów zdarzeniowych przez dwa niezależne publiczne przekaźniki MQTT: EMQX i Eclipse Mosquitto. Każda sesja ma losowy klucz 256-bitowy, a komunikaty są szyfrowane i uwierzytelniane AES-256-GCM. Przekaźniki otrzymują zaszyfrowane dane i skrót identyfikatora. Klucz jest przekazywany wyłącznie we fragmencie linku (po #), którego GitHub Pages nie otrzymuje. Krótki numer sesji jest wyłącznie oznaczeniem.

Komendy wymagają potwierdzenia komputera. Dostarczenie tej samej komendy przez dwa przekaźniki nie przesuwa slajdu dwukrotnie. Po utracie sieci połączenie jest ponawiane. Strona nie korzysta z Vercel Blob ani odpytywania bazy danych i nie żąda kamery ani mikrofonu.

Publiczne przekaźniki są usługami społecznościowymi/testowymi, bez gwarancji dostępności. Nie przesyłaj przez tę stronę danych poufnych. Przed wystąpieniem sprawdź pilot na własnym telefonie i komputerze w sieci, z której będziesz korzystać. Zapasowe sterowanie klawiaturą działa również podczas przerwy w połączeniu pilota.

Link i kod QR udostępniają sterowanie otwartą prezentacją; udostępniaj je tylko prowadzącemu. Nie umieszczaj linku z kluczem w publicznym repozytorium.

## Pliki

`index.html` i `pilot.html` są samodzielnymi plikami z wbudowanymi obrazami i stylami. Można je opublikować na GitHub Pages lub innym hostingu statycznym. Nie zawierają prywatnych kluczy ani danych logowania.

Komplet edytowalnych źródeł: [Prezentacja_AI_GitHub.zip](./Prezentacja_AI_GitHub.zip). W paczce źródła interfejsu są w `source/src/`, a treść prezentacji w `source/src/content.json`.

Budowanie po rozpakowaniu paczki: przejdź do `source/`, uruchom `npm ci`, następnie `npm run build`. Nowe pliki do opublikowania znajdziesz w `source/dist/`.

## Źródła i grafiki

Pełna bibliografia jest na końcu prezentacji i przy poszczególnych slajdach. Reprodukcje dzieł służą analizie w prezentacji edukacyjnej. Nie stanowią materiałów z ogólną licencją na dalsze wykorzystanie.

## Aktualizacja 15.10.2026

Przebudowano porównanie plakatu przed i po, wyjaśnienie TDM, historię sprawy GEMA przeciwko Suno i quiz z odpowiedziami FAŁSZ / PRAWDA / FAŁSZ. Notatki i tekst wystąpienia odpowiadają aktualnym slajdom. Pozostaje 29 slajdów i plan na 30 minut.

Ilustrację futurystycznego miasta do slajdu 9 wygenerowano narzędziem imagegen. Ten sam obraz pokazano osobno i jako element hipotetycznego projektu plakatu. To demonstracja, a nie rozstrzygnięcie o ochronie widocznego projektu. Prompt i opis pliku znajdują się w paczce w GRAFIKA_AI.txt.
