# www.metacybernetyka.pl
www.metacybernetyka.pl


## Cel strony

Celem strony jest rpzyblizenie mozliwosci modelowania za pomocą modeli cybernetycznych


W trakcie analizy przedstawionych teorii w ceybernetyce poszukuję lepszego odwzorowania nie tylko samego procesu, ale też rzeczywistości, która tym procesom podlega.

Nasza rzeczywistość nie jest jednoznaczna, to kontekst nadaje znaczenie, a sama definicja modelu powstaje jako rezultat.
To jest zbyt mało by modelować przyszłosć i symulowac rezultaty.

Potrzebne jest odzworowanie rzecyzstości jako modelu zasobów i modelu użycia jako procesu.
Podobnie jak ma to miejsce w fizyce gdzie w stanie spoczynku ciało posiada energię potencjalną i podczas ruchu oddaje tę energię jako kinetyczną.

## Enegia potencjalna

![image](https://user-images.githubusercontent.com/5669657/225869785-cbfbf0bd-a4ec-4cf1-b81e-c04c9bb55b62.png)


## Enegia kinetyczna

![image](https://user-images.githubusercontent.com/5669657/225869913-efd31b51-606b-41a4-b0e5-6908f339b2ac.png)



## Digital Twin

Aby odwzorować rzeczywistość potrzebny jest uniwersalny model, który opisuje stan rzeczy w stanie spoczynku
oraz stan przepływu w stanie (re)akcji.

Energia, Informacja, Materia to checha każdego elementu sieci systemu, jednak są to parametry kontekstowe zależne od użycia i wartości będą różne dla tych samych ciał biorących udział w procesie, zależnie od procesu jaki zainicjujemy.

Zamykanie się na sam proces bez brania pod uwagę parametrów elementów biorących w tym udział nie daje możliwości symulacji całego spektrum możliwych scenariuszy.


Zamykanie rzeczywistości w prostych modelach z góry ogranicza też rekombinację tej rzeczywistości, pozostawiając ją obserwatorowi, podczas gdy autonomia systemów powinna brać pod uwagę to jak zmienia się rzeczywistość.

Życzeniem obserwatora mogło by być  wywieranie wpływu na system, w którym sam się znajduje, trudnośc tutaj polega na wywieraniu wpływu w układzie, w którym sam świadomie może poddać się działajacym siłom.

Korzyścią jest możliwość przygotowania się tak jak robi to kierowca samochodu kierując pojazxzdem i balansując ciałem w zalezności od sytuacji której podlega, skręcając i zatrzymując pojazd.



## najmniejszy możliwy element - organizm

https://wp-projektu.pl/teksty/teksty-autorskie/minimalny-organizm-zywy-jako-przyklad-zlozonosci-nieredukowalnej/


Elementem biorącym udział w każdym procesie jest cobit

charakteryzuje się parametrami:

Zasób, element


```
class Organizm {

metadane:
  energia
  masa
  informacja

}
```



### Relacje organizmów = cobit

Rola jaką ma w relacji


```
class Relacja { // Cobit

// siła wiązania:

  proporcja = Proporcja() // nadana waga
  rola = () // nadana rola
  
// elementy wiązania
  wejscie = new Organizm()
  wyjscie = new Organizm()

}
```


Operator – konstrukcja językowa jedno-, bądź wieloargumentowa zwracająca wartość.

Do podstawowych operatorów, będących elementem większości języków programowania, należą operatory arytmetyczne: dodawania (+), odejmowania (-), mnożenia (*), dzielenia (/); operatory porównania: większe niż (>), mniejsze niż (<), większe równe (>=), mniejsze równe (<=), równe (= lub ==), różne (<> lub !=), a także operatory operacji logicznych, operacji bitowych, przypisań itd. 



### Interakcja cobitu - stan aktywny

cykle  interakji w sieci cobitów

```
class Interakcja {

operator = Operator() 
relacje = CoBit[] // relacja organizmów


}
```





## Siec relacji - stan pasywny


relacja wielu organizmów lub/i wielu typów relacji

```
class siec {

relacje[] = 

}
```




## Sieć interakcji - stan aktywny 

proces - cykl relacji

intencja typów relacji
mapa typów relacji na sieci

typy Interakcja w sieci
Mapa sieci
sterowanie = siłowe nadawanie wag relacji
intencja = określenie 



```
class process {

intencja
energia
czas
siec = Relacje[]

}
```






## zaininicjowanie procesu


### Relacja

Relacja dwóch organizmów
Elementy powiązane pasywnie


```
class Relacja { 

 siec powiazan roli [
    { new Organizm(), new Rola Cel(), new Waga oporu() }
 ]
  
}
```


### Relacja dwóch Sieci organizmu i otoczenia
opis punktu w przestrzeni na podstawie relacji dwóch ośrodków

```
class Cobit { 

  organizm  = Relacja // aktywne oddziałwyanie // pasywna relacja organizmów - miara skutecznosci
  srodowisko = Relacja // bierne oddziaływanie // pasywna relacja organizmów otoczenia ośrodek oddziaływania - miara strat rozproszenia
  waga sieci = waga(cel,otoczenie) // np przedmiot leżący na ziemi ma wagę 1 - jest cłakowicie zależny od reakcji ziemi
  typ relacji styku dwóch środowisk, organizmów
  
}
```


### Akcja - ożywienie relacji 

Definijca Akcji - Działania

```
class Akcja {

  intencja = // opis -> Rola
  energia = // miara, jednostka -> szybkość reakcji
  czas =  // -> ogranicznie oddziaływania

```


### Interakcja - Akcja w relacjach organizmów - Proces

oddziaływanie Akcji na Relacje - Interakcja pomiędzy elementami

```
class Interakcja { // aktywne działanie na relację

  akcja = new Akcja()  // siła i czas oddziaływania
  punkt = new Cobit()
  
}
```



## Świadomość

łańcuch kolejnych zdarzeń: Interakcji procesów
// histria zdarzen map interakcji, wag relacji

```
class Swiadomosc {
  model świadomości = {czas=0.9, Interakcja= 0.2 } //proporcje sensytywnosciu na czas, miejsce, interakcje
  
  historia = [
    {datownik, Interakcja},
    ...
  ]  

}
```

