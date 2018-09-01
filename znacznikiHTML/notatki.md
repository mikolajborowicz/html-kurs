HIPERŁĄCZA

<a href="http://pasja-informatyki.pl">Pasja informatyki</a>
Atrybut href to skrót od ang. hypertext reference – określamy tutaj adres dokumentu HTML, do którego hiperłącze ma prowadzić. Reference oznacza z ang. odniesienie – i rzeczywiście czasami tak określamy linki – mówimy, że to odnośniki do innych dokumentów. Co ważne – atrybut href nie jest wcale wymagany. Mogą istnieć znaczniki <a>, bez podania adresu linka – np. w menu głównym strony (w górnej belce witryny).

Dochodzimy tutaj do wniosku, iż tak naprawdę hiperłączem możemy nazwać jedynie element <a>, który posiada określony wartością atrybut href – sam element <a> odnośnika jeszcze nie ustanawia. Hiperłącze może także posiadać atrybut target (ang. cel), który określa gdzie docelowo w przeglądarce ma trafić podlinkowany dokument:

<a href="http://pasja-informatyki.pl" target="_blank">Pasja informatyki</a>
Możliwe wartości atrybutu target:

target="_self" – otwórz stronę w tej samej karcie/ramce, w której znajduje się link (ponieważ jest to zachowanie domyślne, można ten atrybut pominąć);
target="_blank" – otwórz witrynę w nowej, nieużywanej karcie przeglądarki (uwaga: nie należy nadużywać tego mechanizmu! Kieruj się empatią wobec internauty i otwieraj nowe karty tylko tam, gdzie rzeczywiście wydaje się to pożądane – w przeciwnym wypadku gość odwiedzający naszą stronę zirytuje się i natychmiast ją opuści);
target="_parent", target="_top" – otworzy adres hiperłącza w odpowiedniej ramce – jest to związane z tzw. framesetem (ang. zestaw ramek). Wartość _parent otworzy witrynę w ramce o jeden poziom wyższej we framesetowej hierarchii, a _top w nadrzędnej ramce). Jednak budowanie witryny na ramkach to relikt przeszłości – są one fatalne zwłaszcza w kontekście SEO, jak również niewygodne dla samego internauty. W praktyce więc raczej nie zdarzy Ci się używać tych wartości atrybutu target
abele (ang. table) nadają się fantastycznie do czytelnego, dwuwymiarowego przedstawiania danych. Cały obszar tabeli ograniczony jest – rzecz jasna – znacznikami <table></table>. Pojedynczy wiersz tabeli tworzymy tagami <tr></tr> (ang. table row), zaś wewnątrz wierszy definiować będziemy komórki tabeli <td></td> (ang. table drawer). Jako przykład, przyjrzyjmy się tabeli zawierającej 3 wiersze, a w każdym z nich po 3 komórki:

 <style> td { border: 1px solid black; } </style>
 <!-- ustawienie czarnego obramowania komórek tabeli w CSS -->

 <table>
    <tr>
       <td>1</td> <td>2</td> <td>3</td>
    </tr>
    <tr>
       <td>4</td> <td>5</td> <td>6</td>
    </tr>
    <tr>
       <td>7</td> <td>8</td> <td>9</td>
    </tr>
 </table> 
Rezultat w przeglądarce:

1	2	3
4	5	6
7	8	9
Kolejna ważna umiejętność w kontekście budowania tabel to scalanie komórek. Scalanie to łączenie dwóch lub więcej komórek w jedną. Czasami trzeba wykonać takie złączenie w tabeli, chociażby dla przejrzystości pokazywania danych. Służą do tego dwa atrybuty: rowspan, jeśli scalaniu ulegają wiersze oraz colspan, jeżeli scalaniu ulegają kolumny. Zobaczmy to jednak na konkretnych przykładach!

Scalanie z użyciem atrybutu colspan:

 <style> td { border: 1px solid black; } </style>
 <!-- ustawienie czarnego obramowania komórek tabeli w CSS -->

 <table>
    <tr>
       <td colspan="2">1</td> <td>3</td>
    </tr>
    <tr>
       <td>4</td> <td>5</td> <td>6</td>
    </tr>
    <tr>
       <td>7</td> <td>8</td> <td>9</td>
    </tr>
 </table> 
Rezultat w przeglądarce:

1	3
4	5	6
7	8	9
Scalanie z użyciem atrybutu rowspan:

 <style> td { border: 1px solid black; } </style>
 <!-- ustawienie czarnego obramowania komórek tabeli w CSS -->

 <table>
    <tr>
       <td>1</td> <td>2</td> <td>3</td>
    </tr>
    <tr>
       <td rowspan="2">4</td> <td>5</td> <td>6</td>
    </tr>
    <tr>
       <td>7</td> <td>8</td>
    </tr>
 </table> 
Rezultat w przeglądarce:

1	2	3
4	5	6
    7   8

    
