# Modelli di Code

<hr>

## Definizioni Gerarchiche

<br>

- $\lambda$ rappresenta il tasso di arrivo nel sistema
- $T_s$ rappresenta il tempo di servizio
- $\mu = 1 / T_s$

<br>

## M/M/1

<br>

- $\rho$ rappresenta l'utilizzo dei serventi nel sistema.

<br>

$$\rho=\frac{\lambda}{\mu} <= 1$$

<br>

- L rappresenta la percentuale media di tempo in cui i serventi non lavorano.

<br>

$$L = 1-\rho$$

<br>

- La probabilità che ci sono un numero di utenti k nel sistema viene definita come:

<br>

$$\pi_0 = 1 - \rho$$

<br>

$$\pi_k = \rho^k \pi_0 = \rho^k(1-\rho) con k > 0$$

<br>

- Il numero di medio di utenti nel sistema N è definito come:

<br>

$$N = \rho / (1-\rho)$$

<br>

- Il numero medio di utenti in coda W è:

<br>

$$W = N − \rho = \rho^2 /(1 − \rho)$$

<br>

- Il tempo medio di risposta R è denotato da:

<br>

$$R = (1 / \mu) / (1 - \rho)$$

<br>

$$R = T_w + T_s$$

<br>

- Il tempo medio di attesa in coda $T_w$ si ottiene come:

<br>

$$T_W = (\rho / \mu ) / (1 - \rho)$$

<br>

- Possiamo calcolare la probabilità con cui si osservano almeno k utenti nel sisitema in condizioni di equilibrio.

<br>

$$\sum_{i>=k} \rho_i = \rho^k$$

<br>

## M/M/Infinito

<br>

- $\pi_k = \frac{\rho^k}{k!}e^{-\rho}$ con k <= 0
- $N = \rho$
- $R = T_s = 1 / \mu$

<br>

## M/M/m

<br>

$$\rho = \lambda / m\mu$$

<br>

$$\pi_k = \frac{(m \rho)^k}{k!} \pi_0 con 1 <= k <= m $$

<br>

$$\pi_k = \frac{m^m \rho^k}{m!} \pi_0 con k > m $$

<br>

$$\pi_0 = [\sum_{k=0}^{m-1} \frac{m \rho^k}{k!} + \frac{(m\rho)^m}{m!} \frac{1}{1  \rho}]$$

<br>

Il numero medio di serventi occupati $E[s]$ è dato da: $$m\rho = \frac{\lambda}{\mu}$$

<br>

$$N = m\rho + \pi_m \frac{\rho}{(1 - \rho)^2}$$

<br>

$$R = 1/\mu + \pi_m / (m \mu(1 − \rho)^2)$$

<br>

$$T_w = \pi_m / (m \mu (1 − \rho)^2)$$

<br>

La probabilità che un utente in arrivo trovi tutti i serventi occupati e quindi sperimenti coda è:

$$Prob{coda} = \sum_{k=m}^{\infty} \pi_k = \pi_0 \frac{(m \rho)^m}{m!} \frac{1}{1-\rho}$$

<br>

## M/M/1/K (memoria finita)

<br>

$$ \pi_k = \frac{1−\rho} {1 - \rho^{K+1}} \rho con 0 ≤ k ≤ K \pi_k = 0 con k > K $$

<br>

$$ \pi_0 = \mu / (\lambda + \mu) e \pi_1 = \lambda / (\lambda + \mu) con K = 1 $$

<br>

## M/M/1//M (popolazione finita)

<br>

$$ \pi_k = \pi_0 \rho^k \frac{M!}{}(M−k!) con 0 ≤ k < M $$

<br>

$$ \pi_k = 0 con k ≥ M $$

<br>

$$ \pi_0 = [ \sum*{k=0}^M \rho^k \frac{M!}{(M-k)!}]^-1$$

<br>

## M/G/1

<br>

Formula di Khintchine-Pollaczek $$N = \rho + \frac{\rho^2 (1 + C^2_B)}{2 (1 - \rho)}$$

<br>

$$C_B = \sigma \mu$$

<br>

$$\sigma = \sqrt{V a r}$$

<br>

$$N = \lambda R$$

<br>

$$W = \lambda T_W con W = N - \rho$$

<br>

## Distribuzioni e Densità

<br>

Stare bene a tenti a se la chiede in ore/minuti e dal $\lambda$ iniziale che da.

<br>

#### Esponenziale:

- Distribuzione: $1 - e^{-\lambda t}$

<br>

$$Se λ = 20/h allora: 1 - e^{−20 t}$$

<br>

- Densità: $\lambda * e^{- \lambda t}$

<br>

#### Poissoniana:

<br>

- Distribuzione e Densità: $\frac{(\lambda t)^n * e^{- \lambda t}}{n!}$

<br>

- Se $\lambda = \frac{1}{6} : \frac{(\frac{1}{6} t)^n * e^{-1/6 t}}{n!}$

<br>

Dopo 10 minuti quale è la probabilità che ci siano 5 utenti arrivati?

<br>

$P_5 = \frac{(10)^5 * e^{-10}}{5!}$

quindi $\lambda t$ è il tempo (minuti) e $n = 5$.

<br>

## Valori da calcolare

#### SOMMA n

<br>

Somma di tutti gli fi (osservazioni)

<br>

#### Per media x:

<br>

- Totale = $Valori (categorie) * f_i$

- Media effettiva x = $ SOMMA(Totale) / n$

<br>

#### Per varianza σ 2

<br>

- ris = $((Valori-Media)^2)*f_i$

- Varianza effettiva: $SOMMA(ris) / (n-1)$

<br>

#### Coeff. Var σ: RADQ(varianza)

<br>

$\frac{\sigma}{x}$ se viene vicino ad 1 posso provare un esponenziale, altrimenti Poissoniana. Se media e varianza sono uguali si utilizza la Poissoniana.

<br>

#### Poissoniana p(i):

<br>

$=(EXP(-Media) * Media^{valori}) / FATTORIALE(valori)$

Inserire Immagine

<br>

#### Esponenziale p(i):

<br>

1. $=(EXP(-Valori/Media)) / Media$

Inserire immagine

2. $=(1-EXP(-Valori/Media))$

Inserire immagine

<br>

Nel caso in cui ci fossero gli intervalli il ”Valori” va sostituito con intervallo più grande-più piccolo come in figura sopra.

<br>

#### Geometrica p(i):

<br>

Parametro Rho: $\rho$

<br>

$\frac{1}{media+1}$

<br>

$Distribuzione = \rho ∗ (1 - \rho)^{valori}$

Inserire foto

<br>

Se il parametro non viene dato direttamente dal testo bisogna calcolarlo come sopra

<br>

## Googness of Fit - Discreto: NO intevalli

<br>

Da utilizzare con più di 30 osservazioni.

<br>

Occorrono:

<br>

- Valori (categorie)

- $f_i$ : numero di osservazioni per ogni intervallo che deve essere > 5.

- f(i) = $f_i$ / n : frequenze osservate. (non serve in questo caso)

- p(i) la probabilità teorica.

- $F_i$ = n ∗ p(i): numero di intervalli unitari teorici con i arrivi.

- G = $\frac{(f_i - F_i)^2}{F_i}$

<br>

Calcolati tutti i valori per G, occorrerà sommarli e confrontare il valore ottenuto con la tabella $X^2$ con **Gradi di Libertà**:

<br>

$$Df = Num classi - 1 - Num parametri distribuzione:$$

- Geometrica: 0

- Poissoniana: 1 (media)

- Esponenziale: 1 (media)

- Normale: 2 (media e varianza)

<br>

## Googness of Fit - Continuo: SI intervalli

<br>

Da utilizzare con più di 30 osservazioni.

<br>

Occorrono:

<br>

- Valori (categorie)

- Intervalli in cui ricadono i valori $x_1 , x_2 con x_2 ≥ x_1$

- $f_i$: numero di osservazioni per ogni intervallo che deve essere > 5.

- $f(i)$ = $f_i$ / n Ovvero le frequenze osservate. (non serve in questo caso)

- $p(i)$ la probabilità teorica per ogni intervallo i calcolata come:

$$p(i) = p(x_2) - p(x_1)$$

che sarebbe **intervallo più grande - intervallo più piccolo.**

<br>

- $F_i$ = $n ∗ p(i)$ Il numero di intervalli unitari teorici con i arrivi.

- $G = \frac{(f_i - F_i)^2}{F_i}$

<br>

Calcolati tutti i valori per G, occorrerà sommarli e confrontare il valore ottenuto con la tabella $X^2$ con **Gradi di Libertà**:

<br>

$$Df = Num classi - 1 - Num parametri distribuzione:$$

<br>

- Geometrica: 0

- Poissoniana: 1 (media)

- Esponenziale: 1 (media)

- Normale: 2 (media e varianza)

<br>

## Kolmogorov Smirnov - Discreto

<br>

Da utilizzare con meno di 30 osservazioni.

<br>

Occorrono:

<br>

- Valori (categorie)

- $f_i$ : numero di osservazioni per ogni intervallo che deve essere $>$ 5.

- $f(i)$ = $f_i$ / n : frequenze osservate.

- p(i) la probabilità teorica.

- $d_i$ la cumulativa delle $f(i)$. Per il calcolo, la prima cella rimane uguale alla $f(i)$, le restanti si blocca e si tira giù la somma:

$$= SOMMA($F $5 : F5)$$

- $D_i$ la cumulativa delle $p(i)$. Per il calcolo, si fa la stessa identica cosa di cui sopra, ma si prende la colonna $p(i)$.

- D = $|d_i - D_i |$ cioè la differenza assoluta.

<br>

Seleziono il valore di D maggiore e lo confronto con la tabella dei Valori Critici Kolmogorov-Smirnov cercando la riga n-esima (somma del numero di osservazioni fatte $f_i$), se il valore è minore del numero nella colonna $D_{0,10}$ allora ok!

<br>

8. Il valore massimo è 0,0288, si ha in corrispondenza di 1 arrivo, quindi sempre prima colonna (quella tra 0 e 10) sulle slide.

9. Il valore da considerare è quello sulla riga del 20 (somma del numero di osservazioni fatte $f_i$), cioè 0,264. Notiamo che 0,00288 $<$ 0,264 quindi può
   essere ACCETTATO!

<br>

## Kolmogorov Smirnov - Continuo

<br>

Da utilizzare con meno di 30 osservazioni.

<br>

Occorrono:

<br>

- Valori (categorie)

- Intervalli in cui ricadono i valori $x_1$ , $x_2$ con $x2 ≥ x_1$ in modo tale da avere lo stesso numero di osservazioni (circa) per ogni intervallo.

- $f(i) = f_i / n$ Ovvero le frequenze osservate.

- p(i) la probabilità teorica per ogni intervallo i calcolata come: $p(i) = p(x_2) - p(x_1)$

- $d_i$ la cumulativa delle f (i). Per il calcolo, la prima cella rimane uguale alla $f(i)$, le restanti si blocca e si tira giù la somma:

$$= SOMMA($F $5 : F5)$$

- $D_i$ la cumulativa delle p(i). Per il calcolo, si fa la stessa identica cosa di cui sopra, ma si prende la colonna $p(i)$.

- $D = |d_i − D_i |$ cioè la differenza assoluta.

<br>

Seleziono il valore di D maggiore e lo confronto con la tabella dei Valori Critici Kolmogorov-Smirnov cercando la riga n-esima (somma del numero di
osservazioni fatte $f_i$), se il valore è minore del numero nella colonna $D_{0,10}$ allora ok!

<br>

## Chi Quadro

Inserire imaggine

<br>

## Komorov

<br>

Inserire Immagine
