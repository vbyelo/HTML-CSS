# HTML

Kod HTML i CSS wyświetlany przez przeglądarkę w witrynie najprawdopodobniej pochodzi z serwera, na którym ona działą. Przeglądarka WWW interpretuje kod HTML i CSS tworząc na ich podstawie strony, które oglądamy.

Niektóre witryny przesyłają do przeglądarki także skrypty JavaScript.

## Jak działa WWW?

Serwer WWW, na którym działa witryna, może byż umieszczony w dowolnym miejscu świata. Aby określić jego położenie, przeglądarka najpierw łączy się z serwerem system nazw domen (DNS).

* Kiedy nawiązujemy połączenie z internetem, robimy to za pośrednictwem dostawcy usług internetowych (ang. Internet Service Provider - ISP) i wpisujemy w przeglądarce nazwę domeny.

* Komputer nawiązuje połączenie z DNS, który zwraca adres IP (12 cyfr oddzielonych od siebie kropkami) skojarzony z podaną nazwą domeny. 

* Unikalny numer zwrócony przez serwer DNS pozwala przeglądarce nawiązać połączenie z serwerem WWW.

## Strukturę stron opisuje kod HTML

```HTML
<html>
    <head>
        <meta http-equiv="content-type" content="text/html; charset=UTF-8">
    </head>
<body>
    <h1>To jest nagłówek pierwszego poziomu</h1>
    <p>Ten tekst może stanowić wprowadzenie do dalszej części strony. Jeśli strona jest długa to jej zawartość może zostać podzielona kilkoma nagłówkami niższego poziomu.</p>
    <h2>To jest nagłówek drugiego poziomu</h2>
    <p>Wiele długich artykułów zawiera nagłówki niższych poziomów, by ułatwić czytelnikom zrozumienie struktury tekstu. W dokumencie mogą się nawet pojawić nagłówki jeszcze niższych poziomów (trzeciego, a nawet czwartego).</p>
    <h2>Kolejny nagłówek drugiego poziomu</h2>
    <p>A to ostatni akapit.</p>
</body>
</html>
```

Kod HTML (niebieski kolor) składa się za znaków zapisanych pomiędzy nawiasami kątowymi - **elementy** HTML - otwierający i zamykający znaczniki. Wewnątrz znacznika zamykającego umieszczany jest dodatkowo znak ukośnika. 


__Kod__ strony znachodzi się pomiędzy  &lt;html&gt; i &lt;/html&gt;.

__Kod wyświetlone w głównym oknie__ przeglądarki znachodzi się pomiędzy &lt;body&gt; i &lt;/body&gt;.

__Akapity tekstu__ są zapisany pomiędzy znacznikami &lt;p&gt; i &lt;/p&gt;.

__Najważniejszy nagłówek strony__ jest pomiędzy &lt;h1&gt; i &lt;/h1&gt;.

__Nagłówek drugiego poziomu__ jest pomiędzy &lt;h2&gt; i &lt;/h2&gt;.
