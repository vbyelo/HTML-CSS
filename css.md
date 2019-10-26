# CSS

Kaskadowe arkusze stylów (ang. Cascading Style Sheets) to język służący do opisu formy prezentacji stron WWW. CSS został opracowany przez organizację W3C w 1996 r. jako potomek języka DSSSL przeznaczony do używania w
połączeniu z SGML-em. Arkusz stylów CSS to lista dyrektyw (tzw. reguł) ustalających w jaki sposób ma zostać wyświetlana przez przeglądarkę internetową zawartość wybranego elementu HTML lub XML. Można w ten sposób opisać wszystkie pojęcia odpowiedzialne za prezentację elementów dokumentów internetowych, wykorzystanie arkuszy stylów daje znacznie większe możliwości pozycjonowania elementów na stronie, niż oferuje sam HTML. CSS został stworzony w celu odseparowania struktury dokumentu od formy jego prezentacji. Separacja ta zwiększa zakres dostępności witryny, zmniejsza zawiłość dokumentu, ułatwia wprowadzanie zmian w strukturze dokumentu. CSS ułatwia także zmiany w renderowaniu strony w zależności od obsługiwanego medium.

Kaskadowe arkusze stylów - CSS

(ang. Cascading Style Sheets) jest językiem służący do opisu sposobu
renderowania stron WWW. Język ten został opracowany przez
organizację W3C w 1996 roku. Kaskadowe arkusze stylów to lista
dyrektyw (reguł) ustalających w jaki sposób ma zostać renderowana
przez przeglądarkę internetową zawartość wybranych elementów
HTML.

Arkusz stylów składa się z definicji stylu, czyli reguł, reguła składa się z
selektora określającego formatowany element lub grupę oraz jednej
lub więcej rozdzielonych dwukropkiem oraz zakończonych
średnikiem par właściwość-wartość. Pary te muszą być otoczone
nawiasami klamrowymi.

```css
selektor { właściwość: wartość; inna-właściwość: inna
wartość;}
```

Przykład:

```css
p { font-family: sans-serif; }
```

Dokument można powiązać z arkuszem określając relację tego pierwszego z
osobnym dokumentem CSS za pomocą elementu link:

```css
<link rel="stylesheet" href="arkusz.css">
```

lub

Reguły CSS można też umieszczać wewnątrz nagłówka dokumentu :

```css
<style type="text/css">p

{ color: red; }

</style>
```

lub

Można również dodawać deklaracje bezpośrednio do danego elementu
dokumentu za pomocą atrybutu style:

```css
<p style="color: red;"></p>
```

Ta ostatnia metoda nie jest jednak zalecana, ponieważ utrudnia zachowanie
spójności w wyglądzie.

Własności dla czcionki :

Imienne wartości absolutne:

xx-small - najmniejsza

x-small - mniejsza

small - mała

medium - średnia

large - duża

x-large - większa

xx-large - największa


```css
<p style="font-size: x-large;">rozmiar x-large</p>
```

Wartości względne:

smaller - mniejsza od bieżącej

larger - większa od bieżącej

```css
<p style="font-size: larger;">rozmiar larger</p>
```

lub wielkość określić w pikselach :

```css
<p style="font-size: 15px;">rozmiar 15px</p>
```

Własności dla czcionki :

Oprócz podania rodzaju czcionki wprost, możliwe jest także wpisanie
rodziny ogólnej:

serif - czcionka szeryfowa (końcówki znaków posiadają "ozdobniki"),
np.: 'Times New Roman', Georgia, Garamond, Bodoni

sans-serif - czcionka bezszeryfowa (końcówki znaków są proste), np.:
Arial, Verdana, 'Trebuchet MS', Helvetica, Univers, Futura

monospace - czcionka o stałej szerokości znaków - monotypiczna
(wygląda, jak pisana na maszynie), np.: Courier, 'Courier New'

cursive - czcionka mająca pewne cechy pochyłej (wygląda, jak pisana
ręcznie)

fantasy - czcionka fantazyjna (dekoracyjna)

```css
 <p style="font-family: sans-serif;">To jest rodzina ogólna
sans-serif</p>
```

```css
<p style="font-family: 'Times New Roman';">To jest czcionka 'Times
New Roman'</p>
```

Własności dla czcionki :

Natomiast jako "styl" należy wpisać:

normal - czcionka normalna (podstawowa)

italic - czcionka pochylona (jeżeli niedostępna, automatycznie
wybierany jest styl oblique)

oblique - również czcionka pochylona (podobna jak poprzednio)

```css
<p style="font-style: italic;">styl italic</p>
```

Wartości absolutne dla wagi:

normal - czcionka normalna (podstawowa)

bold - czcionka pogrubiona

100, 200, 300, 400 (odpowiednik "normal"), 500, 600, 700 (odpowiednik
"bold"), 800, 900 wskazuje wagę czcionki przynajmniej tak samo
wytłuszczonej jak dla poprzedniej wartości w sekwencji;

```css
<p style="font-weight: 700;">waga 700 (bold)</p>
```

Własności dla czcionki :

Wartości względne dla wagi:

lighter - czcionka mniej wytłuszczona od odziedziczonej lub przypisanej
do znacznika (np. typowo znaczniki <b>...</b> oraz
<strong>...</strong> mają przypisaną domyślną wagę "bold")

bolder - czcionka bardziej wytłuszczona

```css <span style="font-weight: bolder;">waga bolder w stosunku do
wartości "800"</span>
```

Natomiast jako "wariant" należy wpisać:

normal - czcionka normalna (podstawowa)

small-caps - kapitaliki

```css
<p style="font-size: larger; font-variant: small-caps;">Wariant
small-caps</p>
```

### Atrybuty mieszane:

Polecenie to pozwala w wygodny sposób zdefiniować wszystkie atrybuty dotyczące czcionek, nie musimy
wypisywać kolejno wszystkich cech, a jedynie ich konkretne wartości. Wszystkie wartości należy
wpisywać w określonej kolejności (przy czym można niektóre pominąć), a także oddzielić je od siebie
spacjami. Dodatkowo przed line-height należy obowiązkowo postawić ukośnik (ponieważ atrybuty
font-size oraz line-height mogą mieć takie same wartości, a więc musimy je jakoś odróżnić).

```css
p { font-weight: bold; font: 12pt Arial }

p { font: 12pt Arial; font-weight: bold }

p { font: bold 12pt Arial }

<p style="font: italic small-caps bold 12pt /1cm 'Times New Roman',Verdana,'MS Sans Serif'">
tekst mieszany </p>
```

### Czcionki systemowe:

Jako "wartości atrybutów" własności font można podać:

caption - czcionka używana do podpisanych przycisków

icon - czcionka etykiet ikon

menu - menu

message-box - okna dialogowe

small-caption - etykiety małych kontrolek

status-bar - pasek statusu okna

```css
<p style="x-system-font: icon;">czcionka icon</p>
```

Rozciągnięcie:

należy wpisać:

ultra-condensed - najbardziej ścieśniona

extra-condensed

condensed - ścieśniona

semi-condensed

normal - czcionka normalna (podstawowa)

semi-expanded

expanded - rozciągnięta

extra-expanded

ultra-expanded - najbardziej rozciągnięta


```css
<p style="font-stretch: extra-expanded;">rozciągnięcie extra duże</p>
```

KOLOR - należy wpisać definicję koloru;


```css
<p style="color: rgb(102, 170, 255);">kolor niebieski jasny</p>

<p style="color: red;">kolor czerwony</p>

<p style="color: #66AAFF;” >kolor niebieski jasny</p>
```

Proporcje:

wg. wzoru: w' = w * (p / p')

gdzie:

w - wysokość czcionki określona w poleceniu

p - proporcje określone w poleceniu

w' - obliczona wysokość

p' - proporcje dostępnej czcionki

```css
<p style="font-family: 'Times New Roman'; font-size-adjust: 0.68;">czcionkaTimes
New Roman o proporcji 0.68</p>

<p style="font-family: 'Times New Roman';">czcionka Times New Roman o
proporcjach domyślnych 0.46</p>

<p style="font-family: ‘Arial'; font-size-adjust: 0.12;">czcionka Arial o proporcji
0.12</p>
```

Dekoracja:

none - bez zmian

underline - podkreślenie

line-through - przekreślenie

overline - nadkreślenie

blink - migotanie tekstu (tylko w Netscape/Mozilla/Firefox i Opera 7)


```css
<p style="text-decoration: underline overline line-through blink;">
```

## Tekst podkreślony,
przekreślony, nadkreślony i migający</p>

Transformacja:

none - bez zmian

capitalize - zamiana pierwszych liter wszystkich wyrazów na wielkie

uppercase - zamiana wszystkich liter na wielkie

lowercase - zamiana wszystkich liter na małe


```css
<p style="text-transform: capitalize;">to jest tekst z transformacją typu capitalize
</p>
```

### Wyrównanie:

left - wyrównanie tekstu do lewego marginesu (domyślnie)

right - wyrównanie do prawego marginesu

center - do środka (wyśrodkowanie)

justify - do obu marginesów jednocześnie (justowanie)


```css
<p style="text-align: right;">wyrównanie tekstu do prawej</p>
```

Wcięcie – należy podać konkretną długość wcięcia:


```css
<p style="text-indent: 1cm;">to jest tekst, w którego pierwszej linijce
wcięcie wynosi 1cm</p>
```

----
## Cień:

poziom - przesunięcie cienia w prawo (ujemne wartości przesuwają w lewo)

pion - przesunięcie cienia w dół (ujemne wartości przesuwają w górę)

rozmycie - promień efektu rozmycia (opcjonalnie)

kolor - kolor bazowy efektu (opcjonalnie - jeśli go nie podamy, przyjmie kolor taki, jak sam
element)


```css
<p style="text-shadow: 0.2em 0.2em; font-weight: bold;
font-size: larger;">tekst z cieniem</p>

<p style="text-shadow: 3px 3px 5px red; font-weight: bold;
font-size: larger;">tekst z cieniem</p>

<p style="text-shadow: 3px 3px red, -3px 3px 2px yellow, 3px
-3px; font-weight: bold; font-size: larger;">tekst z
cieniem</p>
```

## TŁO

### Kolor:

jako "kolor" należy podać definicję koloru, wpisanie "transparent" ustali tło
przezroczyste.


```css
<p style="background-color: yellow;">Tło koloru żółtego </p>

<p style="background-color: rgb(208, 138, 255);">Tło koloru liliowego</p>

<p style="background-color: #FF0000;”>Tło koloru czerwonego</p>
```

### Tło obrazkowe:

```css
<p style="color: white; background-image: url(../pliki/obrazek.jpg);">To jest
akapit z tłem obrazkowym.</p>
```

Powtrzanie małego obrazka:

repeat - powtarzanie tła w obu kierunkach (domyślnie)

repeat-x - powtarzanie tła tylko w kierunku poziomym

repeat-y - powtarzanie tła tylko w kierunku pionowym

no-repeat - brak powtarzania tła (zostanie wyświetlone jako pojedynczy obrazek)

```css
<p style="color: white; background-image: url(../pliki/obrazek.jpg); background-repeat:
repeat;”> akapit z powtarzanym obrazkiem</p>
```

### Pozycja tła obrazka:

Jedną wartość:

center - obrazek na środku (w centrum)

left - obrazek po lewej

right - po prawej

top - na górze

bottom - na dole

jednostka długości - odległość od lewej krawędzi

Dwie wartości (oddzielone spacją):

left top - lewy-górny róg

left bottom - lewy-dolny róg

right top - prawy-górny róg

right bottom - prawy-dolny róg

dwie jednostki długości, z których pierwsza oznacza odległość od lewej
krawędzi, a druga od górnej;


```css
<div style="background-image: url(../pliki/punkt.gif); background-repeat:
no-repeat; background-position: right bottom;"> pozycja dla jednego obrazka
</div>

<div style="background-image: url(../pliki/punkt.gif); background-repeat:
repeat-x; background-position: center center;"> pozycja dla grupy obrazków
</div>
```

Zaczepienie obrazka:

scroll - przewijanie tła (domyślnie)

fixed - tło nieruchome, przewija się tylko zawartość strony


```css
body { background-image: url(obrazek.jpg); background-attachment: fixed }
```

Mieszanie atrybutów tła:

```css
<p style="color: red; background: url(obrazek.jpg) no-repeat left"> To jest akapit z
obrazkiem w tle, obrazek ma podaną w nawiasie ścieżkę dostępu, jest ustawiony
do lewej stronie. </p>

p { background-color: red; background: url(tlo.gif) }

p { background: url(tlo.gif); background-color: red }
```

tworzymy arkusz stylów css:
```css
*.obrazek { background: url(obrazek.jpg) no-repeat left top; padding-left: 110px }
```

linkujemy go na stronie i dopisujemy na stronie html:

```css
<p class="obrazek">Po lewej stronie tego tekstu znajduje się obrazek, dużo
tekstu…</p>
```
