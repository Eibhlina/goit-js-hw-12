# Zadanie — Wyszukiwanie obrazów



Wykorzystaj kod z pracy domowej do poprzedniego modułu, dodając nową funkcjonalność do kodu aplikacji będącej wyszukiwarką obrazów.



## Refaktoryzacja

Dodaj do projektu bibliotekę Axios, z której będziesz korzystać w celu obsługi żądań HTTP. Zrefaktoryzuj projekt, zastępując funkcje fetch.

Użyj składni async/await do obsługi żądań asynchronicznych. Przeprowadź refaktoryzację kodu.



## Paginacja

Interfejs API Pixabay obsługuje paginację i wykorzystuje parametry page i per_page. Upewnij się, że każdy wynik wyszukiwania obrazów obejmuje 40 obiektów (domyślnie 20).

Początkowa wartość parametru page powinna być równa 1.
Z każdym kolejnym żądaniem wartość ta powinna być zwiększana o 1.
W przypadku wyszukiwania przy użyciu nowego słowa kluczowego wartość page powinna zostać przywrócona do wartości początkowej, ponieważ zostanie wykonana paginacja dla nowego zbioru obrazów.


W dokumencie HTML pod galerią dodaj przycisk z tekstem Load more, który umożliwi pobranie i wyświetlenie kolejnej porcji obrazów, dodając je do załadowanych wcześniej elementów galerii. W tym celu przy wysyłaniu formularza należy zapisywać dane wprowadzone przez użytkownika w zmiennej globalnej.

Dopóki w galerii nie ma żadnych obrazów, przycisk powinien być ukryty.
Gdy w galerii będą wyświetlone obrazy, przycisk pojawi się w interfejsie pod galerią.
Przy ponownym przesłaniu formularza przycisk jest najpierw ukryty, a następnie pojawia się ponownie po otrzymaniu wyników żądania.
Przesuń wskaźnik ładowania pod przycisk pobierania kolejnych obrazów.


## Koniec zbioru

W odpowiedzi na żądanie back-end zwraca właściwość totalHits, tj. całkowitą liczbę obrazów spełniających kryterium wyszukiwania (w przypadku darmowego konta). Jeśli użytkownik dotarł do końca zbioru, przycisk Load more powinien zostać ukryty. Ponadto należy wyświetlić komunikat "We're sorry, but you've reached the end of search results.".


## Przewijanie strony

Zadbaj o płynne przewijanie strony po wysłaniu żądania i wyświetleniu każdej kolejnej porcji obrazów. W tym celu należy pobrać wysokość jednego elementu galerii w kodzie za pomocą funkcji getBoundingClientRect. Następnie użyj metody window.scrollBy, aby przewinąć stronę o dwie wysokości elementu galerii.
