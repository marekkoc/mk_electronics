
## 2.2 Sygnały w technice cyfrowej [s. 21]

W technice cyfrowe przekazywanie informacji dokonywane jest za pomocą odpowiedniej kombinacji sygnałów, tzw. kodu o ==dwóch== różniących się co do wartości ==poziomach napięcia== ==pojawiających się na jednym lub kilku przewodach ==(wyjściach).

Kryteria dotyczące sygnałów:
1. poziomy napięć muszą leżeć w zakresie napięcia zasilającego układ scalony
2. obydwie wartości powinny być od siebie możliwe odległe, aby były łatwe do rozróżnienia, a wpływ sygnałów zakłócających łatwy do eliminowania. 

W większości rodzin układów scalonych jeden z poziomów napięcia przyjmuje wartość bliską zera, a drugi wartość bliską napięcia zasilania. [s. 22].

Logika dodatnia w sygnałach TTL: stan niski to 0V, a stan wysoki to +5V. Układy TTL są zasilane napięciem +5V. 



| Stan logiczny | Wersja 1 | Wersja 4 |
| ------------- | -------- | -------- |
| Tak           | 0        | H        |
| Nie           | 1        | L        |
 
## 2.3 [[tranzystor-jako-wlacznik]]
[s. 23]


#TTL-punkt-pracy-tranzystora #Tranzystor-jako-wlacznik

Układy cyfrowe, obojętnie jakiego rodzaju, mają na wejściu i na wyjściu włącznik. Punkt pracy tych tranzystorów nie jest ustalany na stałe jak to ma miejsce w układach analogowych. Punkt pracy zmienia się w zależności od wysterowania i może przyjmować na charakterystyce jedno z dwóch skrajnych położeń:

1. położenie w **stanie nasycenia** - przez tranzystor przepływa maksymalny prąd wynikający z rezystancji rezystora kolektorowego
2. stan **blokowania** w którym prąd kolektora jest równy 0. Może płynąć niewielki prąd blokowania, który powoduje spadek napięcia na $R_c$ , zatem napięcia na kolektorze jest mniejsze niż napięcie zasilania np. $U_c=4.9V$
3.  
   
Jest to tzw. #Praca-dwustanowa-tranzystora


!![[tranystor-jako-wlacznik-schemat.JPEG]]

Przy większych prądach bazy wzrasta czas przełączania tranzystora.

!![[tranystor-jako-wlacznik-charakterystyki.JPEG.JPEG]]


## 2.4 Inverter

#Tranzystor-jako-inwerter

Tranzystor spełnia funkcję tzw.  inwertera, zatem sygnał na jego wyjściu jest zawsze odwrotny do sygnału na wejściu. Napięcie wejściowe jest sygnałem sterującym bazy, a napięcie wyjściowe jest wyprowadzane z kolektora.

![[tranystor-jako-inwerter.JPEG.JPEG]]


| $U_{we}$ | $U_{wy}$ |
| -------- | -------- |
| H        | L        |
| L        | H        |

## 2.5 Dozwolone poziomy napięć [s. 26]

W produkowanych układach cyfrowych napięcia od 2.0V na wejściu i 2.4 V na wyjściu rozpoznawane są jako stan wysoki.

Poziomy dozwolone L i H są oddzielone trzecim poziomem zabronionym. Jest to spowodowane **1) rozrzutem parametrów** poszczególnych egzemplarzy układów scalonych (każdy egzemplarz ma indywidualną granicę rozróżniającą poziomy L i H) oraz **2)** możliwość nałożenia się **sygnału zakłócającego** na sygnał sterujący co spowoduje niekontrolowane przełączenie stanów układu.

| ![[2.5-obszary-dozwolone.JPEG]]                                                                                               | ![[2.5-czas-przelaczania.JPEG]]                                                                                                                                                                                                |
| ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Umowna definicja obszarów dozwolonych H i L w układach cyfrowych. Obszary te są oddzielone dodatkowym obszarem - zabronionym. | Czas przełączania układów powinien być krótki, jednak nigdy nie jest on do pominięcia. Im większy jest zakres potencjałów zabronionych tym większa jest pewność wyróżnienia właściwego sygnału spośród sygnałów zakłócających. |
Na powyższych rysunkach zakres napięć sygnałów L (+1 V) i H (+4 V) został ustalony dowolnie. Wartości te są zbliżone do wartości przedstawionych poniżej (rozdział 3.1)

| ![[3.1-poziomy-napiec-wejsciowych-i-wyjsciowych.JPEG]]                                                                                                                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tak przedstawiają się poziomy napięć wejściowych i  wyjściowych w układach TTL. Widzimy nierównomierność w interpretacji wartości napięć na wejściu i na wyjściu układów cyfrowych. Granica (rozrzut) wartości sygnałów wejściowych jest większy niż ma to miejsce w przypadku wartości sygnałów wyjściowych. |


## 2.6 Czasy przełączania w sygnałach cyfrowych [s. 28]
