# Sem5_JiPP_Micro

## Projekt
Projekt to gra zręcznościowa stworzona na mikrokontrolerze micro:bit, w której uczestnicy walczą o jak najwyższe wyniki i miejsce w globalnym rankingu. Gra polega na tym, że dioda zapala się losowo po lewej stronie ekranu, po prawej lub na środku. Gracz musi natychmiast wcisnąć odpowiedni przycisk. Po zakończeniu rundy gracz wprowadza swój nick.

## Komunikacja sprzętowa
Ponieważ micro:bit nie posiada wbudowanego Wi-Fi, komunikacja sprzętowa opiera się na połączeniu kablem USB z komputerem. Urządzenie przesyła uzyskany wynik oraz nick gracza przez port szeregowy. Informacje te odczytuje bezpośrednio strona otwarta w przeglądarce, wykorzystując do tego API Web Serial, co całkowicie eliminuje potrzebę instalowania jakiegokolwiek dodatkowego oprogramowania na komputerze. Następnie przeglądarka samodzielnie przesyła zebrane dane do API.

## Technologie i infrastruktura
Od strony programistycznej kod samej gry powstaje w środowisku MakeCode. Aplikacja webowa, łącząca stronę z rankingiem oraz interfejs API, zrealizowana jest w frameworku Next.js. Do przechowywania danych graczy i wyników wykorzystana zostanie baza Microsoft SQL Server.

## Prezentacja wyników
Zapisane w bazie osiągnięcia tworzą ranking widoczny na stronie internetowej. Wyniki prezentowane są nie tylko w chmurze – po zakończonej grze micro:bit samodzielnie przewija zestawienie TOP 3 graczy na swojej matrycy diodowej.
