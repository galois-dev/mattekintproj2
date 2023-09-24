
Obs: Opgaven er udarbejdet udelukkende af Benjamin (s234911@dtu.dk) da jeg missede første dag med gruppen og de havde skrevet den færdig forinden jeg kom i gang og jeg ville ikke stjæle deres arbejde så jeg lavede den selv. Jeg kan ikke se at de har uploadet en opgaven endnu så hvis du finder opgaven under min gruppe så har de muligvis fundet en anden måde at uploade på. Du kan forresten læse alt kildekoden på [github](https://github.com/galois-dev/mattekintproj2)


Lad os definere de væstenlige konstanter ved notationen brugt til grafer $G=(V,E)$ hvor $V$ er et knudepunkt og er en kant $E: V\times V \rightarrow \mathbb{F}$  hvor en kant er en funktion som forbinder to punkter og afbilder dem over i en værdi som for eksempel ligger i $\mathbb{R}$. $E$ er ikke kommutativ i vores tilfælde. Kommutative grafer er også kaldet netværk. 
1. Familien af $E$ i vores tilfælde for brændstofsomkostninger kan vi kalde $\mathscr{B}$ som for eksempel gives ved $\set{E_{M,Z}=700,E_{Z,V}=1800,E_{V,S}=2200,E_{S,M}=2800} \subset \mathscr{b} \in \mathscr{B}$. 
2. Hvorefter vi kan kalde familien af optankningsmønstre for $\mathscr{O}$ for eksempel givet ved $\set{V_M=2\times2000, V_Z = 2 \times 1000, V_V = 2 \times 1000, V_S=0}\subset\mathscr{o}\in\mathscr{O}$
3. Dertil har vi reserve stipulationerne givet ved $\mathscr{S}$ som for eksempel er $\set{V_M=1000,V_Z=1200,V_V=1800,V_S=2800}\subset\mathscr{s}\in\mathscr{S}$. De definerer hvor meget i tanken der skal være før man tager afsted fra en havn
4. Til sidst har vi priserne ved hver havn for eksempel givet ved $\set{V_M=600,P_Z=900,P_V=1100,P_S=1200}\subset\mathscr{p}\in\mathscr{P}$
Det er klart at se at $\mathscr{O},\mathscr{S},\mathscr{P}$ er defineret som $\mathscr{O},\mathscr{S},\mathscr{P}: (v)_{v\in V} \rightarrow (k)_{k\in\mathbb{R}}$   hvorimod $\mathscr{B}: (e)_{e\in E} \rightarrow (k)_{k\in\mathbb{R}}$. Hvad der menes med det her er bare at familierne er vilkårlige punktvise afbildninger fra en mængde af knuder eller kanter over i en mængde af tal. Familierne er en mængde af alle mulige kombinationer som opfylder denne betegnelse så det er vigtigt at vi formår at definere hvilket medlem af familierne vi snakker om når vi regner på dem. 
For eksempel kan vi bruge $\mathscr{b}_{p1}\in\mathscr{B}$ hvor $\mathscr{b}_{p1} =  \set{E_{M,Z}=700,E_{Z,V}=1800,E_{V,S}=2200,E_{S,M}=2800}$ som afbilder en mængde af kanter over i en mængde af tal. Her har vi valgt at bruge $\mathbb{R}$ men det udelukker ikke $\mathbb{N}$ og hvis preciseringen af disse ønskes senere med hensyn til deres legmer, så bruger vi $\mathscr{B}_{\mathbb{N}}$ for at betegne familien af alle afbildninger af kanter over i en tilsvarende mængde af naturlige tal.  

### Problem 1
Lad $\mathscr{b}_{p1}\in\mathscr{B}, \mathscr{o}_{p1}\in\mathscr{O}, \mathscr{s}_{p1}\in\mathscr{S}$ og $\mathscr{p}_{p1}\in\mathscr{P}$ være givet ved de afbildninger som tabellerne for opgave 1 beskriver. 
Her starter vi med at beregne brændstofs forbruget ved hjælp af de konstanter som vi definerede. 
Først ved vi at målet for den resterende mængde af brændstof for turen til problem 1 $\mu_B$ er givet ved 

$$
\mu_{B} = \sum_{V\in(\mathscr{o})_{\mathscr{o}\in{\mathscr{O}}}} V - \sum_{E\in(\mathscr{b})_{\mathscr{b}\in\mathscr{B}}} E 
$$
Hvilket for vores behov bliver $\mu_B^{p1}$ for problem 1

$$
\begin{equation}
	\begin{gathered}
\mu_B^{p1}=\sum_{V\in{\mathscr {o_{p1}}}}V - \sum_{E\in{\mathscr {b_{p1}}}}E 
\\\\
= (4000+2000+2000) \\-(700+1800+2200+2800) \\=500
	\end{gathered}
\end{equation}
$$

Så vi skulle meget gerne ankomme til Mombasa igen med en tank på $500$ mt brændstof. Allerede der kan vi se at ved Mombasa som er sidste punkt på ruten ankommer med under 1000 mt brændstof som er for lidt.

### Problem 2
###### a
Her foreslår fragtsselvskabet at ændre optankningsforholdene til dette sæt.  
 $\mathscr{o}_{p2}=\set{V_M=2\times2000, V_Z = 2 \times 1000, V_V = 2 \times 750, V_S=0}$
Det resulterer i at der bliver købt 500 mt mindre brændstof før sidste led og vi ankommer til Mombasa med ingen brændstof. Så vi har faktisk bare at $\mu_B^{p2}=\mu_B^{p1}-500=0$. Det opfylder ikke alle betingelser heller. 

###### b
Her bruger vi $\mathscr{p}_{p2}\in\mathscr{P}$ og $\mathscr{b}_{p2}\in\mathscr{B}$ er priserne og brændstofsforbruget som angivet til opgaven. Samt har vi at $(a_n \times b_m) \subset (\mathscr{p}_{p2} \times \mathscr{b}_{p2}) = (a_0,b_0), (a_1,b_1), \dots, (a_n,b_m)$ for $a_n\in\mathscr{p}_{p2}$ og $b_m\in\mathscr{b}_{p2}$ således at    

$$
	\mu_P=\sum_{(a,b)\in({\mathscr{p}\times\mathscr{b})}} ab
$$
og for vores problem h-ar vi at 
$$\begin{equation}
	\begin{gathered}
	 \mu_P^{p2} \\
	 \\ = \sum_{(a,b)\in({\mathscr{p}_{p2}\times\mathscr{b}_{p2})}} ab
	 \\
	 \\ = 4000*600 + 2000*900 + 1500*1100 
	 \\ = 2.4 \times 10^6 + 1.8 \times 10^6 + 1.65 \times 10^6
	 \\ =$\ 5.85 \times 10^6
	\end{gathered}
\end{equation}
$$

### Problem 3

$$
	l_{i,s} = \sum_{s\in S}\sum_{i\in P} is
$$

Dette kunne også beskrives som $\sum_{s\in S, i \in P} is$ men jeg tror alt efter definition at det er en ekvivalens.
### Problem 4
Udtrykket beskriver en begrænsning at der for alle ture i ruten skal mængden af brændstof i tanken være højere end eller lig med mængden af forbruget af brændstof til den tur som skibet skal bruge for at komme til næste havn.

### Problem 5
Udtrykket er en rekursiv betegnelse for udregningen af hvor meget brændstof der ligger i tanken baseret på tre variable. Først hvor meget brændstof der var i tanken ved sidste gang man var i havnen, samt hvor meget fyldte på der og til sidst hvor meget brændstof det krævede at komme til næste havn hvori man måler fra nu. 

Vi bemærker at denne rekursive betegnelse har et basistilfælde fra startpunktet $i=0$ som ligesom fibonacci har man altså et konstant udtryk for lave værdier af $i$, iflg problem 1 er denne værdi $2000$ for hver $s\in S$. 

I dette tilfælde er det konstante udtryk betegnet med en anden ligning hvor $i$ ikke indgår men vi tager blot udgangspunkt i det sidste led i ruten samt opkostningen ved at nå derfra og over i første led. Ulempen ved dette udtryk er et såkaldt "kold start" problem hvor vi først må vide værdien for $h_{3s}$ før vi ved værdien for $h_{0s}$ og derfor er beregningen af dette konstante led mere besværligt end i andre tilfælde af rekursive betegnelser såsom fibonacci. 

### Problem 6

$$
	h_{11} + h_{h12} \geq R_2 + F_1
$$

$$
	h_{21} + h_{h22} \geq R_3 + F_2
$$

### Problem 7
Det sammenlagte brændstofsforbrug fra havn til havn er lig med summen af brændstofsforbruget på hver tank fra havn til havn for alle havne i ruten.

### Problem 8
Hvis vi lader $l_{i,s}$ være brændstofsforbruget for et enkelt punkt i turen men $L$ være den $1\times 4$ vektor som bliver frembragt ved punktvis addition af elementerne langs $i$. Herfra kan vi lade prislisten af brændstof være $P$ så har vi at $PL^T$ bliver til en enkelt $1 \times 1$ vektor som vi kan betragte som en skalar og derved har vi
$$
	\min{PL^T}
$$

### Problem 9

```python
shipping_problem = pulp.LpProblem(name = "shipping_problem", sense = pulp.LpMinimize)
MY_DESTINATIONS = {
	0: "Mombasa",
	1: "Zanzibar",
	2: "Victoria",
	3: "Salalah",
	4: "Mombasa",
}
PRICES = [600, 900, 1100, 1200, 600]
FUEL_USAGE = [700, 1800, 2200, 2800]
MINIMUM_TANK_AMOUNT = [1000, 1200, 1800, 2800, 1000]
MAXIMUM_TANK_AMOUNT = [7000, 7000, 7000, 7000, 7000]
TANK_ONE = [0, 0, 0, 0, 0]
TANK_TWO = [0, 0, 0, 0, 0]

# Variables
s1 = pulp.LpVariable.dict(name = "s1", indices=MY_DESTINATIONS.keys(), lowBound = 0, cat = "Integer", upBound = 3500)
s2 = pulp.LpVariable.dict(name = "s2", indices=MY_DESTINATIONS.keys(), lowBound = 0, cat = "Integer", upBound = 3500)
h_xs = pulp.LpVariable.dict(name = "h_xs", indices=MY_DESTINATIONS.keys(), lowBound = 0, cat = "Integer", upBound = 7000)

# Objective function
shipping_problem += sum(PRICES[i] * (s1[i] + s2[i]) for i in range(len(PRICES))), "Objective Function"

# Constraints
# Eq 5 and 1
for i in range(len(FUEL_USAGE)):
	# Eq 2
	if i == 0:
		shipping_problem += h_xs[i] == s1[i] + s2[i], f"Eq2 for {MY_DESTINATIONS[i]}"
	else:
		shipping_problem += h_xs[i] == h_xs[i-1] + s1[i-1] + s2[i-1] - FUEL_USAGE[i-1], f"Eq 2 for {MY_DESTINATIONS[i]}"
	shipping_problem += s1[i] + s2[i] >= MINIMUM_TANK_AMOUNT[i], f"Minimum tank amount constraint for {MY_DESTINATIONS[i]}"
	shipping_problem += s1[i] + s2[i] <= MAXIMUM_TANK_AMOUNT[i], f"Maximum tank amount constraint for {MY_DESTINATIONS[i]}"
	# Eq 1
	shipping_problem += s1[i] + s2[i] <= h_xs, f"Eq 1 for {MY_DESTINATIONS[i]}"
	# Eq 4
	shipping_problem += h_xs[i] >= MINIMUM_TANK_AMOUNT[i] + FUEL_USAGE[i], f"Eq 4 for {MY_DESTINATIONS[i]}"

# Solve the problem
shipping_problem += s1[3] + s2[3] >= 1000 + FUEL_USAGE[3]
hipping_problem.solve()
```
Her er det python program jeg har skrevet til at løse opgaverne indtil nu. Se github i bibliografi for kildekode.

### Problem 10
| h | f | S1 | S2 |
| ---- | ----| ---- | ---- | 
| h[0] = 3650.0 | f[0] = 700 | l[1,0] = 150.0 | l[2,0] = 3500.0 | 
| h[1] = 6600.0 | f[1] = 1800 | l[1,1] = 1200.0 | l[2,1] = 0.0 | 
| h[2] = 6000.0 | f[2] = 2200 | l[1,2] = 1800.0 | l[2,2] = 0.0 |
| h[3] = 5600.0 | f[3] = 2800 | l[1,3] = 300.0 | l[2,3] = 3500.0 |

her har jeg sammenlagt værdierne for $S\in\set{0,1}$ 

### Problem 11
Ja den virker lovlig da $i_4 < f_4 +1000$ så skibet ankommer med 1000 i tanken.
### Problem 12
Domænet for $h_{i,s}$ er $h: \set{0,1,2,3} \times \set{1,2} \rightarrow \mathbb{N}$ således at $$\set{0,1,2,3} \times \set{1,2} = 
\begin{bmatrix}
	h_{0,0} \ h_{0,1} \\
	h_{1,0} \ h_{1,1} \\
	\vdots \\
	h_{3,0} \ h_{3,1}
\end{bmatrix}$$
Domænet for $l$ er måske interresant hvis man behøves at vide noget om hvor meget der er i hvert enkelte tank hvorimod $f$ er mere eller mindre ligegyldig da det bare bruges som en samlet betingelse for brændstofsforbrug som lige så godt kunne have været en betingelse hvis vi ville kontrollere brændstof brugt for hvert enkelte tank. 
### Problem 13
Jeg tror her at der menes billedemængde for $h$ som i allerhøjeste grad kan være 7000 iflg opgaven. Altså har vi $0\leq h \leq 7000$. Det satte jeg på fra starten da det er lig med kapaciteten for $S$. Det ændrer derfor ikke noget for mine beregninger.
### Problem 14
Jeg tilføjede 
```python
shipping_problem += s1[i] == s2[i], f"Problem 14 for {MY_DESTINATIONS[i]}"
```
til mine constraints.
### Problem 15
| h | f | S1 | S2 |
| ---- | ----| ---- | ---- | 
| h[0] = 3650.0 | f[0] = 700 | l[1,0] = 1825.0 | l[2,0] = 1825.0 | 
| h[1] = 6600.0 | f[1] = 1800 | l[1,1] = 600.0 | l[2,1] = 600.0 | 
| h[2] = 6000.0 | f[2] = 2200 | l[1,2] = 900.0 | l[2,2] = 900.0 | 
| h[3] = 5600.0 | f[3] = 2800 | l[1,3] = 1900.0 | l[2,3] = 1900.0 |
Overordnet ændrer det ikke noget ved løsningen men vi kan se at tankene er ens fyld op og ingen af dem kommer op og rammer loftet på $3500$ som før.
### Problem 16
På den tank hvor der er sparet altså $S2$ har vi sparet $1775$ 

### Problem 17
Jeg har forsøgt så godt jeg kan at skære ned på det. Ved for eksmpel at bruge den constraint som hedder $s[0] == s[1]$ har vi allerede set at vi kan gøre os fri fra en masse dobblet registering af brændstofsforbrug og reserve beregning. Især har vi at $h$ kan udregnes som en vektor fremfor en matrice, samme for $l$ og $f$ og $R$ som bliver væsentligt nemmere at beregne med denne constraint. Det har jeg mere eller mindre spottet allerede fra start så jeg laver ikke specifikke ændringer i koden men bemærker blot at dette kunne gøres hvis jeg havde fulgt opgaven mere nøjagtigt i starten.
### Problem 18
Vi tilføjer 
```python
SAILING_DAYS = [0, 2, 6, 6, 7]
```
Samt i vores constraint loop tilføjer vi
```python 
s1[i] *= (1-SAILING_DAYS[i]*0.01)
s2[i] *= (1-SAILING_DAYS[i]*0.01)
```
Desværre lader plup ikke os gøre dette på en linje ved brug af $x,y = 1,2$ syntax. 

Jeg ved ikke helt hvorfor vi skal estimere vægten når vi har adgang til værdien men koden ville ellers se således ud 

```python
shipping_problem += h_xs[i] >= MINIMUM_TANK_AMOUNT[i] + FUEL_USAGE[i] * 3/2, f"Eq 4 for {MY_DESTINATIONS[i]}"
```
Hvor vi bare ændrer Betingelse 3 til at have en ekstra $\frac{F_i}{2}$ med i beregningen. 
Vi bemærker at dette tilføjer lidt til omkostningen på turen både med og uden justeringen af $s1$ og $s2$ 
### Problem 19
Vi tilføjer blot 
```python
FIXED_COSTS = [2000000, 1000000, 4000000, 3000000]
```
Som en konstant og derefter opdateres obj funktionen såldes at 

```python
shipping_problem += sum(FIXED_COSTS[i] + (PRICES[i] * (s1[i] + s2[i])) for i in range(len(PRICES))), "Objective Function"
```

