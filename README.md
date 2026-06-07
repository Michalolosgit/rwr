# Podstawy Projekt WebXR

## Opis projektu

Projekt przedstawia aplikację VR/WebXR wykonaną w silniku Godot. Celem projektu było zaimplementowanie podstawowych mechanik poruszania się i interakcji w środowisku wirtualnej rzeczywistości, takich jak płynny ruch, obrót skokowy, teleportacja oraz obsługa modeli dłoni.

Projekt jest dostępny przez GitHub Pages i może być uruchamiany w przeglądarce z obsługą WebXR.

## Główne funkcje

* obsługa środowiska VR/WebXR,
* modele lewej i prawej dłoni,
* poprawna orientacja dłoni względem kontrolerów,
* płynny ruch gracza lewym joystickiem,
* ruch w kierunku patrzenia gracza,
* ograniczenie ruchu wyłącznie do płaszczyzny poziomej XZ,
* obrót skokowy prawym joystickiem,
* blokada ciągłego obrotu przy wychylonym joysticku,
* teleportacja z użyciem promienia RayCast,
* znacznik celu teleportacji na podłożu,
* poprawne uwzględnianie pozycji głowy gracza podczas teleportacji,
* scena testowa z obiektami referencyjnymi o różnych rozmiarach,
* publikacja gotowej aplikacji przez GitHub Pages.

## Technologie

W projekcie wykorzystano:

* Godot Engine,
* GDScript,
* WebXR,
* Git,
* GitHub,
* GitHub Pages.

## Struktura repozytorium

```text
/
├── docs/              # gotowy eksport aplikacji WebXR na GitHub Pages
├── project_files/     # pliki źródłowe projektu Godot
└── README.md          # dokumentacja projektu
```

Folder `/docs` zawiera wyeksportowaną wersję projektu przeznaczoną do publikacji przez GitHub Pages.

Folder `/project_files` zawiera pliki źródłowe projektu Godot, które można otworzyć i edytować w silniku Godot.

## Zaimplementowane mechaniki

### Modele rąk

W scenie znajdują się dwa modele dłoni: lewa i prawa. Ich skala została ustawiona realistycznie względem otoczenia. Modele są zorientowane tak, aby palce dłoni były skierowane zgodnie z lokalną osią `-Z` kontrolera, a punkt obrotu znajduje się w okolicy nadgarstka.

### Ruch płynny

Poruszanie gracza odbywa się za pomocą lewego joysticka. Kierunek ruchu zależy od kierunku patrzenia użytkownika, jednak ruch jest ograniczony do płaszczyzny poziomej `XZ`. Dzięki temu patrzenie w górę lub w dół nie powoduje zmiany wysokości gracza ani nie wywołuje efektu unoszenia się.

Ruch odbywa się ze stałą prędkością, bez dodatkowego przyspieszania.

### Obrót skokowy

Prawy joystick odpowiada za obrót skokowy typu Snap Turn. Kamera obraca się natychmiastowo o określony kąt, np. 45 stopni. Zaimplementowano również blokadę ciągłego obrotu, dzięki czemu kolejne obrócenie wymaga ponownego wychylenia joysticka lub odczekania krótkiego czasu.

### Teleportacja

Teleportacja została wykonana z wykorzystaniem promienia RayCast. Użytkownik celuje w podłoże, a w miejscu trafienia pojawia się widoczny znacznik. Mechanizm teleportacji uwzględnia aktualne przesunięcie głowy gracza względem środka przestrzeni, dzięki czemu po teleportacji głowa użytkownika znajduje się dokładnie w wybranym punkcie.

### Scena testowa

Scena zawiera podłoże z kolizją oraz kilka obiektów o różnych gabarytach, takich jak kostki lub kolumny. Obiekty pełnią funkcję punktów orientacyjnych i pomagają sprawdzić skalę sceny, prędkość ruchu oraz poprawność działania teleportacji.

## Uruchomienie projektu

Projekt można uruchomić przez GitHub Pages:

```text
https://michalolosgit.github.io/rwr/
```

## Cel projektu

Celem projektu było praktyczne poznanie podstaw tworzenia aplikacji VR w Godot oraz implementacja najważniejszych mechanik lokomocji używanych w środowiskach wirtualnej rzeczywistości. Projekt pokazuje umiejętność pracy z przestrzenią 3D, kontrolerami VR, ruchem gracza, teleportacją oraz eksportem aplikacji do wersji webowej.

## Czego się nauczyłem

Podczas realizacji projektu rozwinąłem umiejętności związane z:

* tworzeniem scen 3D w Godot,
* implementacją mechanik VR,
* obsługą kontrolerów i joysticków,
* pracą z RayCast,
* obsługą teleportacji w przestrzeni 3D,
* przygotowaniem projektu do działania w WebXR,
* publikacją aplikacji przez GitHub Pages,
* organizacją repozytorium projektowego.

## Autor

Michał Wierzbicki
Student kierunku Elektronika i Telekomunikacja
