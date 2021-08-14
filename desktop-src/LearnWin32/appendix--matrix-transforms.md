---
title: Appendice- Trasformazioni di matrici
description: In questo argomento viene fornita una panoramica matematica delle trasformazioni di matrice per la grafica 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d02976446824bba07829173bb326338a55732b39c640c93319630a209096b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389261"
---
# <a name="appendix-matrix-transforms"></a>Appendice: Trasformazioni di matrice

In questo argomento viene fornita una panoramica matematica delle trasformazioni di matrice per la grafica 2D. Tuttavia, non è necessario conoscere i calcoli matematici delle matrici per usare le trasformazioni in Direct2D. Leggere questo argomento se si è interessati ai calcoli matematici. In caso contrario, è possibile ignorare questo argomento.

-   [Introduzione alle matrici](#introduction-to-matrices)
    -   [Operazioni matrice](#matrix-operations)
-   [Trasformazioni affine](#affine-transforms)
    -   [Translation Transform](#translation-transform)
    -   [Trasformazione ridimensionamento](#scaling-transform)
    -   [Rotazione intorno all'origine](#rotation-around-the-origin)
    -   [Rotazione intorno a un punto arbitrario](#rotation-around-an-arbitrary-point)
    -   [Trasformazione a inclinazione](#skew-transform)
-   [Rappresentazione di trasformazioni in Direct2D](#representing-transforms-in-direct2d)
-   [Avanti](#next)

## <a name="introduction-to-matrices"></a>Introduzione alle matrici

Una matrice è una matrice rettangolare di numeri reali. *L'ordine* della matrice è il numero di righe e colonne. Ad esempio, se la matrice ha 3 righe e 2 colonne, l'ordine è 3 × 2. Le matrici vengono in genere visualizzate con gli elementi della matrice racchiusi tra parentesi quadre:

![Matrice 3 x 2.](images/matrix01.png)

Notazione: una matrice è designata da una lettera maiuscola. Gli elementi sono designati da lettere minuscole. Gli indice indicano il numero di riga e di colonna di un elemento. Ad esempio,*un elemento ij* è l'elemento in corrispondenza dell'esima riga e della colonna j della matrice A.

Il diagramma seguente mostra una × matrice j, con i singoli elementi in ogni cella della matrice.

![matrice con righe i e colonne j.](images/matrix15.png)

### <a name="matrix-operations"></a>Operazioni matrice

In questa sezione vengono descritte le operazioni di base definite nelle matrici.

*Aggiunta di*. La somma A + B di due matrici viene ottenuta aggiungendo gli elementi corrispondenti di A e B:

<dl> A + B = \[ a *ij* \]  +  \[ b *ij* \]  =  \[ a *ij* + b *ij*\]
</dl>

*Moltiplicazione scalare*. Questa operazione moltiplica una matrice per un numero reale. Dato un numero reale *k*, il prodotto scalare kA viene ottenuto moltiplicando ogni elemento di A per *k*.

<dl> kA = k \[ a *ij* \]  =  \[ k × a *ij*\]
</dl>

*Moltiplicazione di matrici*. Date due matrici A e B con ordine (m × n) e (n × p), il prodotto C = A × B è una matrice con ordine (m × p), definita come segue:

![Mostra una formula per la moltiplicazione di matrici.](images/matrix02.png)

o, in modo equivalente:

<dl> c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</dl>

In altri modi, per calcolare ogni elemento c *ij*, eseguire le operazioni seguenti:

1.  Prendere la i'esima riga di A e la colonna j'esima di B.
2.  Moltiplicare ogni coppia di elementi nella riga e nella colonna: la prima voce di riga per la prima voce di colonna, la seconda voce di riga per la seconda voce di colonna e così via.
3.  Sommare il risultato.

Di seguito è riportato un esempio di moltiplicazione di una matrice (2 × 2) per una matrice (2 × 3).

![moltiplicazione di matrici.](images/matrix03.png)

La moltiplicazione di matrici non è commutativa. Ciò significa che A × B ≠ B × A. Inoltre, dalla definizione che segue non tutte le coppie di matrici possono essere moltiplicate. Il numero di colonne nella matrice a sinistra deve essere uguale al numero di righe nella matrice di destra. In caso contrario, ×'operatore non è definito.

*Identificare la matrice*. Una matrice di identità, definita I, è una matrice quadrata definita come segue:

<dl> I *ij* = 1 se *i*  =  *j* o 0 in caso contrario.  
</dl>

In altre parole, una matrice di identità contiene 1 per ogni elemento in cui il numero di riga è uguale al numero di colonna e zero per tutti gli altri elementi. Ecco, ad esempio, la matrice di identità 3 × 3.

![Matrice di identità.](images/matrix04.png)

Le equalità seguenti sono presenti per qualsiasi matrice M.

<dl> M x I = M  
I x M = M  
</dl>

## <a name="affine-transforms"></a>Trasformazioni affine

Una *trasformazione affine è un'operazione* matematica che esegue il mapping di uno spazio delle coordinate a un altro. In altre parole, esegue il mapping di un set di punti a un altro set di punti. Le trasformazioni affine hanno alcune funzionalità che le rendono utili nella grafica computer.

-   Le trasformazioni affine mantengono *la riservatezza*. Se tre o più punti rientrano in una linea, formano comunque una linea dopo la trasformazione. Le linee rette rimangono rette.
-   La composizione di due trasformazioni affine è una trasformazione affine.

Le trasformazioni affine per lo spazio 2D hanno il formato seguente.

![Mostra una trasformazione affine per lo spazio 2D.](images/matrix05.png)

Se si applica la definizione di moltiplicazione di matrici specificata in precedenza, è possibile mostrare che il prodotto di due trasformazioni affine è un'altra trasformazione affine. Per trasformare un punto 2D usando una trasformazione affine, il punto viene rappresentato come matrice 1 × 3.

<dl> P = \| x y 1 \|  
</dl>

I primi due elementi contengono le coordinate x e y del punto. Il valore 1 viene inserito nel terzo elemento per fare in modo che i calcoli matematici funzionino correttamente. Per applicare la trasformazione, moltiplicare le due matrici come indicato di seguito.

<dl> P' = P × M  
</dl>

Si espande come segue.

![trasformazione affine.](images/matrix06.png)

dove

<dl> x' = ax + cy + e  
y' = bx + dy + f  
</dl>

Per ottenere il punto trasformato, prendere i primi due elementi della matrice P'.

<dl> p = (x', y') = (ax + cy + e, bx + dy + f)  
</dl>

> [!Note]  
> Una matrice 1 × *n* è denominata *vettore di riga*. Direct2D e Direct3D usano entrambi vettori di riga per rappresentare i punti nello spazio 2D o 3D. È possibile ottenere un risultato equivalente usando un vettore di colonna (*n* × 1) ed esponendo la matrice di trasformazione. La maggior parte dei testi grafici usa la forma vettoriale della colonna. Questo argomento presenta la forma del vettore di riga per la coerenza con Direct2D e Direct3D.

 

Le sezioni successive derivano le trasformazioni di base.

### <a name="translation-transform"></a>Translation Transform

La matrice di trasformazione della traslazione ha il formato seguente.

![trasformazione della traduzione.](images/matrix07.png)

L'inserimento di un *punto P* in questa equazione produce:

<dl> P' = (*x*  +  *dx*, *y*  +  *dy*)
</dl>

che corrisponde al punto (x, y) convertito da *dx* nell'asse X e *da dy* nell'asse Y.

![diagramma che mostra la traslazione di due punti.](images/graphics22.png)

### <a name="scaling-transform"></a>Trasformazione ridimensionamento

La matrice di trasformazione del ridimensionamento ha il formato seguente.

![trasformazione di ridimensionamento.](images/matrix09.png)

L'inserimento di un *punto P* in questa equazione produce:

<dl> P' = (*x ∙* *dx*, *y ∙* *dy*)
</dl>

che corrisponde al punto (x,y) ridimensionato in base *a dx* e *dy*.

![diagramma che mostra il ridimensionamento di due punti.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Rotazione intorno all'origine

La matrice per ruotare un punto intorno all'origine ha il formato seguente.

![Mostra una formula per una trasformazione di rotazione.](images/matrix11.png)

Il punto trasformato è:

<dl> P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)
</dl>

Prova. Per mostrare che P' rappresenta una rotazione, si consideri il diagramma seguente.

![diagramma che mostra la rotazione intorno all'origine.](images/graphics24.png)

Si consideri quanto segue:

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)
</dt> <dd>

Punto originale da trasformare.

</dd> <dt>

Φ
</dt> <dd>

Angolo formato dalla linea (0,0) a P.

</dd> <dt>

Θ
</dt> <dd>

Angolo in base al quale ruotare (x,y) sull'origine.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')
</dt> <dd>

Punto trasformato.

</dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Lunghezza della riga (da 0,0) a P. Anche il raggio del cerchio di rotazione.

</dd> </dl>

> [!Note]  
> Questo diagramma usa il sistema di coordinate standard usato nella geometria, in cui l'asse y positivo punta verso l'alto. Direct2D usa il sistema Windows coordinate, in cui l'asse y positivo punta verso il basso.

 

L'angolo tra l'asse x e la linea (0,0) a P' è Θ + Θ. Le identità seguenti contengono:

<dl> x = R cosO  
y = R sinO  
x' = R cos(Θ + Θ)  
y' = R sin(Θ+ Θ)  
</dl>

Risolvere ora x' e y' in termini di Θ. Con le formule di addizione trigonometrica:

<dl> x' = R(cosOcosΘ – sinAsinΘ) = RcosYcosΘ – RsinAsin  
y' = R(sin YcosΘ + cosOsinΘ) = Rsin YcosΘ + RcosOSin  
</dl>

Sostituendo, si ottiene:

<dl> x' = xcosΘ – ysinΘ  
y' = xsinΘ + ycos'  
</dl>

che corrisponde al punto trasformato P' illustrato in precedenza.

### <a name="rotation-around-an-arbitrary-point"></a>Rotazione intorno a un punto arbitrario

Per ruotare intorno a un punto (x,y) diverso dall'origine, viene usata la matrice seguente.

![trasformazione di rotazione.](images/matrix13.png)

È possibile derivare questa matrice prendendo il punto (x,y) come origine.

![diagramma che mostra la rotazione intorno a un punto.](images/graphics25.png)

(x1, y1) è il punto che risulta dalla rotazione del punto (x0, y0) intorno al punto (x,y). È possibile derivare x1 come indicato di seguito.

<dl> x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x  
x1 = x0cosΘ – y0sinΘ + \[ (1 - cos') + ysinΘ \]  
</dl>

A questo punto, inserire nuovamente questa equazione nella matrice di trasformazione usando la formula x1 = ax0 + cy0 + e della precedente. Usare la stessa procedura per derivare y1.

### <a name="skew-transform"></a>Trasformazione a inclinazione

La trasformazione skew è definita da quattro parametri:

-   Θ: quantità da inclinare lungo l'asse x, misurata come angolo rispetto all'asse y.
-   ZIONI: quantità da incresciare lungo l'asse y, misurata come angolo rispetto all'asse x.
-   (*px*, *py*): coordinate x e y del punto su cui viene eseguita l'ancoraggio.

La trasformazione skew usa la matrice seguente.

![Trasformazione di a inclinazione.](images/matrix14.png)

Il punto trasformato è:

<dl> P' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanA) - *py* tanA
</dl>

o in modo equivalente:

<dl> P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* - *px*)tanA)
</dl>

Per vedere il funzionamento di questa trasformazione, prendere in considerazione ogni componente singolarmente. Il parametro Θ sposta ogni punto nella direzione x di una quantità uguale a tanΘ. Il diagramma seguente mostra la relazione tra Θ e l'a inclinazione dell'asse x.

![Diagramma che mostra l'aasing lungo l'asse x.](images/graphics26.png)

Ecco la stessa aassazione applicata a un rettangolo:

![Diagramma che mostra l'aassazione lungo l'asse x quando viene applicata a un rettangolo.](images/graphics27.png)

Il parametro IA ha lo stesso effetto, ma lungo l'asse y:

![Diagramma che mostra l'aasing lungo l'asse y.](images/graphics28.png)

Il diagramma successivo mostra l'a inclinazione dell'asse y applicata a un rettangolo.

![Diagramma che mostra l'a inclinazione lungo l'asse y quando viene applicato a un rettangolo.](images/graphics29.png)

Infine, i *parametri px* e *py* spostano il punto centrale per l'ancoraggio lungo gli assi x e y.

## <a name="representing-transforms-in-direct2d"></a>Rappresentazione di trasformazioni in Direct2D

Tutte le trasformazioni Direct2D sono trasformazioni affine. Direct2D non supporta trasformazioni non affine. Le trasformazioni sono rappresentate dalla [**struttura D2D1 \_ MATRIX \_ 3X2 \_ F.**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) Questa struttura definisce una matrice 3 × 2. Poiché la terza colonna di una trasformazione affine è sempre la stessa ( 0, 0, 1 ) e poiché Direct2D non supporta trasformazioni non affine, non è necessario specificare l'intera matrice \[ \] 3 × 3. Internamente, Direct2D usa 3 × 3 matrici per calcolare le trasformazioni.

I membri di [**D2D1 \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) sono denominati in base alla relativa posizione di indice: **\_ il membro 11** è element (1,1), **\_ il membro 12** è element (1,2) e così via. Anche se è possibile inizializzare direttamente i membri della struttura, è consigliabile usare la [**classe D2D1::Matrix3x2F.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) Questa classe eredita **D2D1 \_ MATRIX \_ 3X2 \_ F** e fornisce metodi helper per la creazione di una delle trasformazioni affine di base. La classe definisce anche [**l'operatore \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) per la composizione di due o più trasformazioni, come descritto in [Applicazione di trasformazioni in Direct2D.](applying-transforms-in-direct2d.md)

## <a name="next"></a>Prossima

[Modulo 4. Input utente](module-4--user-input.md)

 

 