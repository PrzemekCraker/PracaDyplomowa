# Praca Dyplomowa

## Aplikacja do zarzadzania wartościami odżywczymi

## <p>1. Krótki opis pracy + 4. Technologie &#9989;</p>

__Main aplikacji:__
Aplikacja umożliwia skanowanie produktu za pomocą kodu QR/Barcode i dodanie wartości odżywczych tegoż produktu do swojego dziennego spożycia makroelementów (wartości odżywczych) – jeśli produktu nie było dotychczas w bazie, użytkownik może własnoręcznie go dodać i uzupełnić jego dane wartości odżywczych. Użytkownik ma możliwość dodania dziennych limitów na spożycie konkretnych wartości odżywczych oraz dostaje codzienne/tygodniowe podsumowania.

__Technologie:__
- React Native + MySQL / MongoDB

__Główne założenia na aplikację:__
- Prostota
- Funkcjonalność
- Przejrzystość
## <p>2. Schemat bazy danych &#9989;</p>

<img src="2. DPU Main.jpg" alt="DPU Main">

## <p>3. Diagram przypadków użycia &#9989;</p>

<img src="1. SchematBazyDanych.png" alt="Schemat Bazy Danych">

## <p>4. Opisy funkcjonalności &#9989;</p>

### 1. Skanuj QR/barcode
<table>
  <tbody>
    <tr>
      <td>Nazwa</td>
      <td>Skanuj QR/barcode</td>
    </tr>
    <tr>
      <td>Aktor</td>
      <td>Użytkownik</td>
    </tr>
    <tr>
      <td>Główny przepływ zdarzeń</td>
      <td>
          1. Użytkownik przechodzi na ekran skanowania<br/>
          2. Użytkownik skanuje za pomocą aparatu kod<br/>
          3. System wyświetla nazwę produktu<br/>
      </td>
    </tr>
    <tr>
      <td>Alternatywne przepływy zdarzeń</td>
      <td>
          2a. System zwraca informację o źle zeskanowanym kodzie
      </td>
    </tr>
    <tr>
      <td>Specjalne wymagania</td>
      <td>1. Użytkownik jest zalogowany<br/>
          2. Użytkownik zezwala aplikacji na używanie aparatu 
        </td>
    </tr>
  </tbody>
</table>

### 2. Podaj gramaturę produktu
<table>
  <tbody>
    <tr>
      <td>Nazwa</td>
      <td>Podaj gramaturę produktu</td>
    </tr>
    <tr>
      <td>Aktor</td>
      <td>Użytkownik</td>
    </tr>
    <tr>
      <td>Główny przepływ zdarzeń</td>
      <td>
          1. Użytkownik wpisuje gramaturę produktu<br/>
          2. System zwraca informację o dodaniu produktu<br/>
      </td>
    </tr>
    <tr>
      <td>Alternatywne przepływy zdarzeń</td>
      <td>
          1a. System zwraca informację o błędnym wypełnieniu danych
      </td>
    </tr>
    <tr>
      <td>Specjalne wymagania</td>
      <td>Użytkownik jest zalogowany<br/>
        </td>
    </tr>
  </tbody>
</table>

### 3. Zapisz do bazy
<table>
  <tbody>
    <tr>
      <td>Nazwa</td>
      <td>Zapisz do bazy</td>
    </tr>
    <tr>
      <td>Aktor</td>
      <td>Administrator, użytkownik</td>
    </tr>
    <tr>
      <td>Główny przepływ zdarzeń</td>
      <td>
          System zapisuje zmiany użytkownika/administratora w bazie<br/>
      </td>
    </tr>
    <tr>
      <td>Alternatywne przepływy zdarzeń</td>
      <td>
          Brak
      </td>
    </tr>
    <tr>
      <td>Specjalne wymagania</td>
      <td>Administrator/użytkownik jest zalogowany
        </td>
    </tr>
  </tbody>
</table>

### 4. Dodaj produkt do bazy
<table>
  <tbody>
    <tr>
      <td>Nazwa</td>
      <td>Dodaj produkt do bazy</td>
    </tr>
    <tr>
      <td>Aktor</td>
      <td>Administrator, użytkownik</td>
    </tr>
    <tr>
      <td>Główny przepływ zdarzeń</td>
      <td>
          Administrator/użytkownik wybrał opcję dodania nowego produktu po zeskanowaniu<br/>
      </td>
    </tr>
    <tr>
      <td>Alternatywne przepływy zdarzeń</td>
      <td>
          Brak
      </td>
    </tr>
    <tr>
      <td>Specjalne wymagania</td>
      <td>1. Administrator/użytkownik jest zalogowany<br/>
          2. Poprawnie zeskanowany produkt 
        </td>
    </tr>
  </tbody>
</table>

### 5. Uzupełnij dane wartości odżywczych nowego produktu
<table>
  <tbody>
    <tr>
      <td>Nazwa</td>
      <td>Uzupełnij dane wartości odżywczych nowego produktu</td>
    </tr>
    <tr>
      <td>Aktor</td>
      <td>Administrator, użytkownik</td>
    </tr>
    <tr>
      <td>Główny przepływ zdarzeń</td>
      <td>
          Użytkownik wypełnia dane o nowym produkcie (wartości odżywcze na 100 gram)
      </td>
    </tr>
    <tr>
      <td>Alternatywne przepływy zdarzeń</td>
      <td>
          Brak
      </td>
    </tr>
    <tr>
      <td>Specjalne wymagania</td>
      <td>Administrator/użytkownik jest zalogowany
        </td>
    </tr>
  </tbody>
</table>

### 6. Zatwierdź produkt
<table>
  <tbody>
    <tr>
      <td>Nazwa</td>
      <td>Zatwierdź produkt</td>
    </tr>
    <tr>
      <td>Aktor</td>
      <td>Administrator, użytkownik 2</td>
    </tr>
    <tr>
      <td>Główny przepływ zdarzeń</td>
      <td>
          1. Administrator/użytkownik 2 zatwierdza produkt
      </td>
    </tr>
    <tr>
      <td>Alternatywne przepływy zdarzeń</td>
      <td>
          1b. Administrator/użytkownik 2 odrzuca wypełnione dane
      </td>
    </tr>
    <tr>
      <td>Specjalne wymagania</td>
      <td>Brak
        </td>
    </tr>
  </tbody>
</table>

### 7. Generuj tygodniowe podsumowanie
<table>
  <tbody>
    <tr>
      <td>Nazwa</td>
      <td>Generuj tygodniowe podsumowanie</td>
    </tr>
    <tr>
      <td>Aktor</td>
      <td>Użytkownik</td>
    </tr>
    <tr>
      <td>Główny przepływ zdarzeń</td>
      <td>
          Użytkownik generuje tygodniowe podsumowanie spożycia
      </td>
    </tr>
    <tr>
      <td>Alternatywne przepływy zdarzeń</td>
      <td>
          Brak
      </td>
    </tr>
    <tr>
      <td>Specjalne wymagania</td>
      <td>Brak – w przypadku braku 7 dni, system generuje podsumowanie z zebranych dotychczas danych
        </td>
    </tr>
  </tbody>
</table>

### 8. Ustaw dzienny limit
<table>
  <tbody>
    <tr>
      <td>Nazwa</td>
      <td>Ustaw dzienny limit</td>
    </tr>
    <tr>
      <td>Aktor</td>
      <td>Użytkownik</td>
    </tr>
    <tr>
      <td>Główny przepływ zdarzeń</td>
      <td>
          Użytkownik ustawia dzienny limit spożycia wartości odżywczych
      </td>
    </tr>
    <tr>
      <td>Alternatywne przepływy zdarzeń</td>
      <td>
          Brak
      </td>
    </tr>
    <tr>
      <td>Specjalne wymagania</td>
      <td>Brak
        </td>
    </tr>
  </tbody>
</table>

## <p>5. Zgłoszenie tematu &#9989;</p>
<a href="https://github.com/PrzemekCraker/PracaDyplomowa/blob/master/5.%20Zg%C5%82oszenie%20tematu.doc">Zgłoszenie tematu pracy dyplomowej w formacie .docx</a>

### Inne dodatkowe rzeczy, które mogą pojawić się w aplikacji:
- dodawanie ceny produktu (średnia cena jaka jest spotykana w sklepach – np. jeśli zostanie dodana weryfikacja dodania nowego produktu to po 10 potwierdzeniach – opcja dla użytkowników weryfikujących – podanie ceny, jeśli spotkali inna w innym sklepie - cena zostanie uśredniona lub pokazana w widełkach)
- użytkownik wybiera gramaturę produktu, którą dodaje do dziennego spożycia (stała w aplikacji to Wartość odżywcza/100g, ale aplikacja będzie sama wyliczać z podanej gramatury przez użytkownika)
- użytkownik dodaje „wolne” wartości odżywcze (bez potrzeby określania jaki to był produkt lub wybierania go z bazy) – po prostu dodaje makro do swojego dziennego spożycia
- weryfikacja dodanych produktów do bazy danych – jeśli zostaje dodany nowy produkt (czyli uzupełniona przez użytkownika tabela wartości odżywczych) – dopiero po zatwierdzeniu administratora lub potwierdzeniu 10 innych użytkowników – produkt zostanie dodany do bazy, jako zweryfikowany <- jeśli baza będzie na serwerze, jeśli lokalnie niepotrzebna funkcja
- po dniu/tygodniu/miesiącu użytkownik może zobaczyć raport z podsumowania ile średnio jadł dzienne wart.odż., liczbę kalorii, wydanych pieniędzy (w przypadku dodania też ceny dla produktów) oraz łącznie liczba na dzień/tydzień/miesiąc
- aplikacja mogłaby zostać umieszczona na Google Play – występowałyby reklamy (śr.30sec) i aplikacja oparta byłaby na ilość skanów – po obejrzeniu reklamy na konto użytkownika wpływałoby 15 skanów kodów.
- (hard) skanowanie nie tylko kodów QR/barcode, ale też tabeli wartości odżywczych – nie byłoby potrzeby spisywania ręcznie – zawsze można byłoby jednak po zeskanowaniu poprawić zeskanowane wartości.