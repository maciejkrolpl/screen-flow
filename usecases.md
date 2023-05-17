# USE CASES

## 🟢 ŁATWY

Dzwoni klient do call-center firmy **Kły Mamuta**. Agent otwiera HomePage i wprowadza dane klienta, korzystając z formularza przygotowanego w screen flow. Niezbędne dane to: 

- imię
- e-mail
- numer telefonu komórkowego

Przed zapisaniem dane są ponownie wyświetlane w celu weryfikacji poprawności.

## 🟠 MNIEJ ŁATWY

Firma **Zielony Pluszak** w wyniku szeroko zakrojonej akcji marketingowej nawiązała współpracę z kilkorgiem potencjalnych klientów. Dane leadów często są podawane przez telefon, co jest źródłem błędów, więc pracownicy muszą mieć możliwość szybkiej edycji danych. Na stronie głównej znajduje się tabela wyświetlająca imiona, nazwiska, e-maile i numery telefonów. Zaznaczenie wybranego rekordu i kliknięcie w przycisk powoduje otwarcie kolejnego ekranu z możliwością edycji. Po zapisaniu zmian powinna wyświetlić się zaktualizowana tabela.

## 🔴 DOŚĆ WYMAGAJĄCY

Rūta jest asystentką w fabryce **Vilniaus traktorių**. W związku z wprowadzeniem nowej serii części zamiennych, fabryka zbiera szczegółowy feedback od swoich kooperantów. Zadaniem Rūty jest umawianie spotkań kooperantów. Rūta tworzy w systemie `Event`, pomaga jej w tym formularz umieszczony na Lightning Home Page'u umożliwiający wprowadzenie niezbędnych danych:
- Kooperant (`Contact` -> `WhoId`) 
- Część której dotyczy spotkanie (`Product2` -> `WhatId`)
- Typ spotkania (`Type`) w zależności, skąd jest firma-kooperant (parent-Account kooperanta) 
  - jeśli z USA, spotkanie musi odbyć się online (`Call`), 
  - w przeciwnym razie jest to spotkanie stacjonarne (`Meeting`)
- W tym drugim wypadku Rūta musi mieć możliwość wpisania miejsca spotkania (`Location`).
- Daty i godziny rozpoczęcia i zakończenia spotkania
  
Event musi mieć także wypełnione pole `Subject`.