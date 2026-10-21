Filmdle
Podział projektu na 5 etapów zorientowanych na prezentację postępów (od warstwy wizualnej i szkieletu, przez kolejne minigry, aż po moduł sieciowy i wdrożenie):
Etap 1: Main-page i szkielet aplikacji (Hub / Nawigacja)
Cel prezentacji: Prowadzący widzi działający szkielet webowy, spójny interfejs dashboardu, routing oraz przygotowane kontenery na poszczególne tryby gry.
1. Architektura i projekt bazowy
 * Frontend: Struktura SPA (lub Razor Pages/Blazor/czysty JS) ze zdefiniowanym motywem graficznym (typ stradev valley).
 * Zarządzanie tożsamością bez kont:
   * Skrypt startowy weryfikujący sessionStorage pod kątem obecności playerId. W przypadku braku – generowanie i zapisanie crypto.randomUUID().
2. Widok główny (Mainscreen)
 * Karty minigierek: Trzy kafelki reprezentujące gry (Filmdle, Zpixelowany Aktor, Kto to powiedział?) z dynamicznymi statusami:
   * Badge trybu Daily: Dostępne / Ukończone dzisiaj (np. 2/3 próby) / Zablokowane.
 * Przełącznik dni: Kontrolka pozwalająca wybrać grę „Dzisiejszą” lub „Wczorajszą” (z blokadą dat przyszłych i starszych niż 48h).
 * Placeholder sekcji duelowej: Sekcja „Pojedynek 1v1” z przyciskami Stwórz pokój i polem Dołącz z kodem (na tym etapie jeszcze z zaślepkami wizualnymi).
 * Lokalny stan: Inicjalizacja struktury w localStorage przechowującej dzisiejsze wyniki, aby po odświeżeniu strony kafelki od razu pokazywały poprawny status.
