---
title: Trasformazioni di matrici di appendice
description: Questo argomento fornisce una panoramica matematica delle trasformazioni matrici per la grafica 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104567869"
---
# <a name="appendix-matrix-transforms"></a>Appendice: trasformazioni matrice

Questo argomento fornisce una panoramica matematica delle trasformazioni matrici per la grafica 2D. Tuttavia, non è necessario conoscerne la matematica per usare le trasformazioni in Direct2D. Leggere questo argomento se si è interessati alla matematica; in caso contrario, è possibile ignorare questo argomento.

-   [Introduzione alle matrici](#introduction-to-matrices)
    -   [Operazioni Matrix](#matrix-operations)
-   [Trasformazioni affini](#affine-transforms)
    -   [Trasformazione conversione](#translation-transform)
    -   [Ridimensionamento della trasformazione](#scaling-transform)
    -   [Rotazione intorno all'origine](#rotation-around-the-origin)
    -   [Rotazione intorno a un punto arbitrario](#rotation-around-an-arbitrary-point)
    -   [Trasformazione inclinazione](#skew-transform)
-   [Rappresentazione di trasformazioni in Direct2D](#representing-transforms-in-direct2d)
-   [Avanti](#next)

## <a name="introduction-to-matrices"></a>Introduzione alle matrici

Una matrice è una matrice rettangolare di numeri reali. L' *ordine* della matrice è il numero di righe e colonne. Se, ad esempio, la matrice include 3 righe e 2 colonne, l'ordine è 3 × 2. Le matrici vengono in genere visualizzate con gli elementi della matrice racchiusi tra parentesi quadre:

![matrice 3 x 2.](images/matrix01.png)

Notation: una matrice viene designata da una lettera maiuscola. Gli elementi sono designati da lettere minuscole. Gli indici indicano il numero di riga e colonna di un elemento. Ad esempio, un *IJ* è l'elemento nella riga volto della e la colonna j'th della matrice a.

Nel diagramma seguente viene illustrata una matrice i × j con i singoli elementi in ogni cella della matrice.

![matrice con le colonne i Rows e j.](images/matrix15.png)

### <a name="matrix-operations"></a>Operazioni Matrix

In questa sezione vengono descritte le operazioni di base definite nelle matrici.

*Aggiunta*. La somma A + B di due matrici viene ottenuta aggiungendo gli elementi corrispondenti di A e B:

<dl> A + b = \[ a *IJ* \]  +  \[ B *IJ* \]  =  \[ a *IJ* + b *IJ*\]
</dl>

*Moltiplicazione scalare*. Questa operazione Moltiplica una matrice per un numero reale. Dato un numero reale *k*, il prodotto scalare ka viene ottenuto moltiplicando ogni elemento di a per *k*.

<dl> kA = k \[ a *IJ* \]  =  \[ k × a *IJ*\]
</dl>

*Moltiplicazione di matrici*. Date due matrici A e B con Order (m × n) e (n × p), il prodotto C = A × B è una matrice con Order (m × p), definita come indicato di seguito:

![Mostra una formula per la moltiplicazione di matrici.](images/matrix02.png)

oppure, in modo equivalente:

<dl> c *IJ* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *in* + b *NJ*  
</dl>

Ovvero per calcolare ogni elemento c *IJ*, eseguire le operazioni seguenti:

1.  Prendere la riga volto della di un oggetto e la colonna j'th di B.
2.  Moltiplica ogni coppia di elementi nella riga e nella colonna: la prima voce di riga dalla prima voce di colonna, la seconda voce di riga per la seconda voce di colonna e così via.
3.  Sommare il risultato.

Di seguito è riportato un esempio di moltiplicazione di una matrice (2 × 2) per una matrice (2 × 3).

![moltiplicazione di matrici.](images/matrix03.png)

La moltiplicazione di matrici non è commutativa. Ovvero, A × B ≠ B × A. Inoltre, dalla definizione segue che non tutte le coppie di matrici possono essere moltiplicate. Il numero di colonne nella matrice di sinistra deve essere uguale al numero di righe della matrice a destra. In caso contrario, l'operatore × non è definito.

*Identificare la matrice*. Una matrice di identità, designata come, è una matrice quadrata definita nel modo seguente:

<dl> I *IJ* = 1 se *i*  =  *j* o 0 in caso contrario.  
</dl>

In altre parole, una matrice di identità contiene 1 per ogni elemento in cui il numero di riga è uguale al numero di colonna e zero per tutti gli altri elementi. Ecco ad esempio la matrice di identità 3 × 3.

![matrice di identità.](images/matrix04.png)

Le seguenti corrispondenze vengono mantenute per qualsiasi matrice M.

<dl> M x I = M  
I x M = M  
</dl>

## <a name="affine-transforms"></a>Trasformazioni affini

Una *trasformazione affine* è un'operazione matematica che esegue il mapping di uno spazio delle coordinate a un altro. In altre parole, esegue il mapping di un set di punti a un altro set di punti. Le trasformazioni affini includono alcune funzionalità che le rendono utili nella grafica del computer.

-   Le trasformazioni affini mantengono *collinearità*. Se tre o più punti rientrino in una riga, formano comunque una riga dopo la trasformazione. Le linee rette rimangono diritte.
-   La composizione di due trasformazioni affini è una trasformazione affine.

Le trasformazioni affini per lo spazio 2D hanno il formato seguente.

![Mostra una trasformazione affine per lo spazio 2D.](images/matrix05.png)

Se si applica la definizione della moltiplicazione di matrici fornita in precedenza, è possibile indicare che il prodotto di due trasformazioni affini è un'altra trasformazione affine. Per trasformare un punto 2D utilizzando una trasformazione affine, il punto viene rappresentato come una matrice 1 × 3.

<dl> P = \| x y 1 \|  
</dl>

I primi due elementi contengono le coordinate x e y del punto. 1 viene inserito nel terzo elemento per far funzionare correttamente la matematica. Per applicare la trasformazione, moltiplicare le due matrici come indicato di seguito.

<dl> P ' = P × M  
</dl>

In questo modo si espande il codice seguente.

![trasformazione affine.](images/matrix06.png)

dove

<dl> x ' = ax + CY + e  
y ' = BX + DY + f  
</dl>

Per ottenere il punto trasformato, prendere i primi due elementi della matrice P.

<dl> p = (x ', y ') = (AX + CY + e, BX + DY + f)  
</dl>

> [!Note]  
> Una matrice da 1 × *n* viene chiamata *vettore di riga*. Direct2D e Direct3D utilizzano entrambi vettori di riga per rappresentare punti nello spazio 2D o 3D. È possibile ottenere un risultato equivalente usando un vettore di colonna (*n* × 1) e trasponendo la matrice di trasformazione. La maggior parte dei testi grafici usa il formato vettoriale di colonna. In questo argomento viene presentato il formato vettoriale di riga per coerenza con Direct2D e Direct3D.

 

Le varie sezioni successive derivano le trasformazioni di base.

### <a name="translation-transform"></a>Trasformazione conversione

Il formato della matrice di trasformazione della traduzione è il seguente.

![trasformazione conversione.](images/matrix07.png)

L'inserimento di un punto *P* in questa equazione produce:

<dl> P ' = (*x*  +  *DX*, *y*  +  *dy*)
</dl>

che corrisponde al punto (x, y) tradotto da *dx* nell'asse x e *dy* nell'asse y.

![diagramma che mostra la conversione di due punti.](images/graphics22.png)

### <a name="scaling-transform"></a>Ridimensionamento della trasformazione

Il formato della matrice di trasformazione di ridimensionamento è il seguente.

![ridimensionamento della trasformazione.](images/matrix09.png)

L'inserimento di un punto *P* in questa equazione produce:

<dl> P ' = (*x* ∙ *DX*, *y* ∙ *dy*)
</dl>

che corrisponde al punto (x, y) ridimensionato da *dx* e *dy*.

![diagramma che mostra il ridimensionamento di due punti.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Rotazione intorno all'origine

La matrice per ruotare un punto intorno all'origine ha il formato seguente.

![Mostra una formula per una trasformazione di rotazione.](images/matrix11.png)

Il punto trasformato è:

<dl> P ' = (*x* CosΘ – ysinΘ, *x* sinθ + *y* cosΘ)
</dl>

Prova. Per mostrare che P ' rappresenta una rotazione, prendere in considerazione il diagramma seguente.

![diagramma che mostra la rotazione intorno all'origine.](images/graphics24.png)

Si consideri quanto segue:

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)
</dt> <dd>

Punto originale da trasformare.

</dd> <dt>

Φ
</dt> <dd>

Angolo formato dalla riga (0, 0) a P.

</dd> <dt>

Θ
</dt> <dd>

Angolo in base al quale ruotare (x, y) sull'origine.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')
</dt> <dd>

Punto trasformato.

</dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Lunghezza della riga (da 0, 0) a P. Anche il raggio del cerchio di rotazione.

</dd> </dl>

> [!Note]  
> Questo diagramma usa il sistema di coordinate standard usato in geometria, in cui l'asse y positivo punta verso l'alto. Direct2D utilizza il sistema di coordinate di Windows, in cui l'asse y positivo punta verso il basso.

 

L'angolo tra l'asse x e la riga (0, 0) a P ' è Φ + Θ. Le seguenti identità contengono:

<dl> x = cosΦ R  
y = R sinΦ  
x ' = R cos (Φ + Θ)  
y ' = peccato R (Φ + Θ)  
</dl>

A questo punto, risolvere per x "e y" in termini di Θ. Per le formule di addizione trigonometrica:

<dl> x ' = R (cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ-RsinΦsinΘ  
y ' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ  
</dl>

Sostituendo, si ottengono:

<dl> x ' = xcosΘ – ysinΘ  
y ' = xsinΘ + ycosΘ  
</dl>

che corrisponde al punto di trasformazione P ' illustrato in precedenza.

### <a name="rotation-around-an-arbitrary-point"></a>Rotazione intorno a un punto arbitrario

Per ruotare intorno a un punto (x, y) diverso dall'origine, viene utilizzata la matrice seguente.

![trasformazione di rotazione.](images/matrix13.png)

È possibile derivare questa matrice prendendo il punto (x, y) come origine.

![diagramma che mostra la rotazione intorno a un punto.](images/graphics25.png)

Let (x1, Y1) è il punto risultante dalla rotazione del punto (x0, y0) intorno al punto (x, y). È possibile derivare X1 come indicato di seguito.

<dl> X1 = (x0 – x) cosΘ – (y0-y) sinΘ + x  
X1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]  
</dl>

A questo punto, ricollegare questa equazione alla matrice di trasformazione, usando la formula X1 = aX0 + cy0 + e riportata in precedenza. Utilizzare la stessa procedura per derivare Y1.

### <a name="skew-transform"></a>Trasformazione inclinazione

La trasformazione asimmetria viene definita da quattro parametri:

-   Θ: la quantità di inclinazione lungo l'asse x, misurata come un angolo dall'asse y.
-   Φ: la quantità da inclinare lungo l'asse y, misurata come un angolo dall'asse x.
-   (*px*, *py*): coordinate x e y del punto in cui viene eseguita l'asimmetria.

La trasformazione inclinazione utilizza la matrice seguente.

![trasformazione asimmetria.](images/matrix14.png)

Il punto trasformato è:

<dl> P ' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΦ) – *py* tanΦ
</dl>

o equivalente:

<dl> P ' = (*x* + (*y* - *py*) tanΘ, *y* + (*x* - *px*) tanΦ)
</dl>

Per verificare il funzionamento di questa trasformazione, considerare ogni singolo componente. Il parametro Θ sposta ogni punto della direzione x di un importo uguale a tanΘ. Nel diagramma seguente viene illustrata la relazione tra Θ e l'inclinazione dell'asse x.

![Diagramma che mostra l'inclinazione lungo l'asse x.](images/graphics26.png)

Di seguito è illustrata la stessa asimmetria applicata a un rettangolo:

![Diagramma che mostra l'inclinazione lungo l'asse x quando viene applicato a un rettangolo.](images/graphics27.png)

Il parametro Φ ha lo stesso effetto, ma lungo l'asse y:

![Diagramma che mostra l'inclinazione lungo l'asse y.](images/graphics28.png)

Il diagramma seguente mostra l'inclinazione dell'asse y applicata a un rettangolo.

![Diagramma che mostra la distorsione lungo l'asse y quando viene applicato a un rettangolo.](images/graphics29.png)

Infine, i parametri *px* e *py* spostano il punto centrale per la distorsione lungo gli assi x e y.

## <a name="representing-transforms-in-direct2d"></a>Rappresentazione di trasformazioni in Direct2D

Tutte le trasformazioni Direct2D sono trasformazioni affini. Direct2D non supporta le trasformazioni non affini. Le trasformazioni sono rappresentate dalla struttura [**d2d1 \_ Matrix \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) . Questa struttura definisce una matrice di 3 × 2. Poiché la terza colonna di una trasformazione affine è sempre la stessa ( \[ 0, 0, 1 \] ) e perché Direct2D non supporta le trasformazioni non affini, non è necessario specificare l'intera matrice 3 × 3. Internamente, Direct2D USA 3 × 3 matrici per calcolare le trasformazioni.

I membri della [**matrice d2d1 \_ \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) sono denominati in base alla posizione di indice: il membro **\_ 11** è elemento (1,1), il **\_ 12** membro è elemento (1,2) e così via. Sebbene sia possibile inizializzare direttamente i membri della struttura, è consigliabile usare la classe [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Questa classe eredita **d2d1 \_ Matrix \_ 3x2 \_ F** e fornisce metodi helper per la creazione di una delle trasformazioni affini di base. La classe definisce anche [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) per la composizione di due o più trasformazioni, come descritto in [applicazione di trasformazioni in Direct2D](applying-transforms-in-direct2d.md).

## <a name="next"></a>Prossima

[Modulo 4. Input utente](module-4--user-input.md)

 

 