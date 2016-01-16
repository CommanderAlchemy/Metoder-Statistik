![image](https://pbs.twimg.com/profile_images/624172340/mah-logo-twitter_normal.png "Malmö Högskola") Malmö Högskola


Artur Olech <br>
M10P2603 <br>
[Kurssida: Metoder & Statistik](http://edu.mah.se/DA237A "Metoder för mätning av användbarhet i informationssystem")
# Metoder & Statistik
### Lecture 9
> Tidigare
> n/a

# Konfidens intervall vid jämförelsestudie

| Två undersökningar | storlek | medelvärde | standardavikelse |
| -- | -- | -- | -- |
| 1  | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/n_1.png?raw=true) | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/x_1.png?raw=true) | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/s_1.png?raw=true)
| 2  | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/n_2.png?raw=true) | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/x_2.png?raw=true) | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/s_2.png?raw=true)

Intervall för differens

<!-- \bar x2 - \bar x1 + Zalpha * sqrt(S1^2/n1 + S2^2/n2) -->
![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/intervall_diff.png?raw=true)

Zalpha = {  
  1.64 90%  
  1.96 95%  
  2.57 99%  
}

### Slutsatsen

1. Om detta intervall inehåller noll  
  Medelvärden från dessa två undersökningar är lika

2. Om noll ligger utanför detta intervall  
  Det finns skillnad i medelvärdet

***Exempel***: Är TS studeter duktigare än LS studenter?

|    | Personer | medelpoäng | standardavikelse |
| -- | -- | -- | -- |
| **LS** | 150 | 48 | 5.7 |
| | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/n_1.png?raw=true) | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/x_1.png?raw=true) | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/s_1.png?raw=true) |
| | | | |
| **TS** | 90 | 51 | 7 |
| | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/n_2.png?raw=true) | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/x_2.png?raw=true) | ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/s_2.png?raw=true) |

**Lösning 95%** -> Zalpha = 1.96

***insättningen ger***  
<!-- 51 - 48 +/- 1.96 * sqrt(5*7^2/150 + 7^2/90) -->
![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/example_1_solve95%25.png?raw=true)

**Intervall** [1.29, 4.71]

> Tolkningen av resultat:
> Med 95% säkerhet variarer differensen av medelpoäng för LS och TS studenter  
> mellan 1.29 poäng samt 4.71 poäng.  
> ** Eftersom resultatet är _positivt_ samt _intervallet_ inte har med 0
> håller det med andra slutsatsen
> samt TS studenter är duktigare**

# Hypotesprövning
_Är en metod för att avgöra om ett påstående är `sant` || `falskt`_

* **Nollhypotes ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_0.png?raw=true)**  
* **Mothypotes ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_1.png?raw=true)**  


|Slutsatsregel Förkasta ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_0.png?raw=true) eller ej!| | |
|--|--|--|
| Förkasta ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_0.png?raw=true) | <---> | Acceptera ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_1.png?raw=true)
| Förkasta ej ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_0.png?raw=true) | <---> | Acceptera ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_0.png?raw=true)

***Exempel***: Mjölk 2L Skånemejerier  
> Stickprov vill bekräfta att förpackningen innehåller 2L

![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_0.png?raw=true): En 2L flaska innehåller 2L mjölk.  
µ = 2  

![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_1.png?raw=true): En 2L flaska innehåller <2 L mjölk.  
µ <2

***Exempel***: Bensinförbrukning för Volvo v70  
> Mål 0.55L/mil

H0: Bensinförbrukning är högre än 0.55L/mil  
µ > 0.55  

H1: Bensinförbrukning är max 0.55L/mil
µ < 0.55

> Exemplen ovan kallas för **ensidig** hypotesprövning!

# Teststatistik
S = standardavikelse från undersökning.  
n = storlek av undersökning.  
µ = Från ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/H_0.png?raw=true)  
<!-- Medelärdet Z = (\bar x - µ0) / (S/sqrt(\bar n)) -->
Medelärdet: ![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/teststatistik_medelv%C3%A4rde.png?raw=true)

***Exempel***: Mjölk 30 flaskor  
![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/bar_x.png?raw=true) = 1.95  
S = 0.1

**Teststatistik:**  
<!-- Z = (1.95 - 2) / ( 0.1 / sqrt(30) ) -->
![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/teststatistik_example_1_Z.png?raw=true)

**Andel**  
<!-- Z = \bar P - H0 / sqrt(H0(1-H0) / n) -->
![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/teststatistik_example_1_andel.png?raw=true)

***Exempel***: Stöd För M,  H0 = 28%  
Undersökning \bar P = 23.2% = 0.232  
1500 Personer

**Teststatistik**  
<!-- Z = 0,232 - 0,28 / sqrt(0.28*(1-0,28) / 1500) -->
![image](https://github.com/CommanderAlchemy/Metoder-Statistik/blob/master/Lectures/Lecture7_images/teststatistik_example2_Z.png?raw=true)

# P - värdet
Mjölk H1: µ <2 (vänster svans)  

Sannorlikheten = P(z < Z)  
= P(z < -2.7)  
= P(z > 2.7)  
= 1 - P(z < 2.7)  
= 1 - 0,9965 = 0,0035  
P = 0.0035

Pvärdet = 2*P(z > Z) (Om det är tvåsidigt)



Konfidens: 90%, osv...  
alpha värdet: 1-0,9 = 0.1 osv...  
alpha = Sannolikheten att dra felaktig slutsats.

### Slutsatsen

1. Om p-värdet är mindre än alpha  
  H0 förkastas

2. Om p-värdet är >= alpha  
  H0 förkastas ej.

> Med konfidensgraden 99.9% så är 0,0035 är större och slutsatsen H0 stämmer.  
> Med konfidensgraden 99% så är 0,0035 mindre och H1 stämmer.
