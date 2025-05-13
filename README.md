# CeneoScraper

## Kod produktu, o którym będą pobierane opinie
84514582

## Algorytm pobierania opinii o pojedynczym produkcie z serwisu Ceneo.pl
- https://www.ceneo.pl/84514582#tab=reviews

1. wysłanie zapytania dostępu do strony z opiniami o produkcie
2. Jeśli operacja zakończy się sukcesem, wyodrębnienie z kodu strony fragmentów odpowiadających poszczególnym opiniom
3. Dla każdej z opinii wydobycie z kodu HTML poszczególnych składowych i zapisanie ich w postacji złożonych struktur danych
4. Jeżeli istnieje kolejna strona z opiniami, przejście na tę stronę i powtórzenie dla niej kroków 1-4
5. Zapisanie wszystkich opinii w bazie danych

##
<!-- |sładowa|zmienna|selektor|
|.......|.......|........|
|opinia|review|.user-post.user-post__card.js_product-review|
|identyfikator opinii|review_id|{review_class}[data-entry-id]|
|autora|author|.user-post__author-name|
|rekomendację|recommendation|.user-post__author-recomendation > em|
|liczbę gwiazdek|score|.user-post__score .user-post__score-count|
|czy opinia jest potwierdzona zakupem|approved|.review-pz|
|data wystawienia opinii|publish_date|.user-post__published time:nth-of-type(1)['datetime']|
|data zakupu produktu|purchase_date|.user-post__published time:nth-of-type(2)['datetime']|
|ile osób uznało opinię za przydatną|likes|.vote-yes > span|
|ile osób uznało opinię za nieprzydatną|dislikes|.vote-no > span|
|treść opinii|content|.user-post__text|
|listę wad|pros|.review-feature__item.review-feature__item--negative|
|listę zalet|cons|.review-feature__item.review-feature__item--positive| -->

