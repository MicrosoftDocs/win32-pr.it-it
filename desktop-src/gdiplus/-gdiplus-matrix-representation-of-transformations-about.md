---
description: Un m&\# 215; n matrice è un set di numeri disposti in m righe e n colonne. Nella figura seguente sono illustrate diverse matrici.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Rappresentazione tramite matrici delle trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751335"
---
# <a name="matrix-representation-of-transformations"></a>Rappresentazione tramite matrici delle trasformazioni

Una matrice *m × n* è un set di numeri disposti in *m* righe e *n* colonne. Nella figura seguente sono illustrate diverse matrici.

![illustrazione che mostra sei matrici di dimensioni variabili](images/aboutgdip05-art04.png)

È possibile aggiungere due matrici con le stesse dimensioni aggiungendo singoli elementi. Nella figura seguente sono illustrati due esempi di aggiunta di matrici.

![illustrazione che Mostra come eseguire l'aggiunta di matrici](images/aboutgdip05-art05.png)

Una matrice *m × n* può essere moltiplicata per una matrice *n × p* e il risultato è una matrice *m × p* . Il numero di colonne nella prima matrice deve corrispondere al numero di righe della seconda matrice. Ad esempio, una matrice di 4 × 2 può essere moltiplicata per una matrice 2 × 3 per produrre una matrice 4 × 3.

I punti del piano e delle righe e delle colonne di una matrice possono essere considerati vettori. Ad esempio, (2, 5) è un vettore con due componenti e (3, 7, 1) è un vettore con tre componenti. Il prodotto punto di due vettori viene definito come segue:

(a, b) • (c, d) = AC + BD

(a, b, c) • (d, e, f) = ad + be + CF

Ad esempio, il prodotto punto di (2, 3) e (5, 4) è (2) (5) + (3) (4) = 22. Il prodotto punto di (2, 5, 1) e (4, 3, 1) è (2) (4) + (5) (3) + (1) (1) = 24. Si noti che il prodotto punto di due vettori è un numero, non un altro vettore. Si noti anche che è possibile calcolare il prodotto punto solo se i due vettori hanno lo stesso numero di componenti.

Lasciare a (i, j) la voce della matrice a nella riga i **th** e **della colonna j** . Ad esempio A (3, 2) è la voce nella matrice a nella riga 3 **Rd** e la colonna 2 **ND** . Si supponga che A, B e C siano matrici e AB = C. Le voci di C vengono calcolate come segue:

C (i, j) = (riga i di A) • (colonna j di B)

Nella figura seguente vengono illustrati alcuni esempi di moltiplicazione di matrici.

![illustrazione che illustra come eseguire la moltiplicazione di matrici](images/aboutgdip05-art06.png)

Se si pensa a un punto nel piano come una matrice da 1 × 2, è possibile trasformare tale punto moltiplicando il punto per una matrice 2 × 2. Nella figura seguente sono illustrate diverse trasformazioni applicate al punto (2, 1).

![illustrazione che Mostra come usare la moltiplicazione di matrici per ridimensionare, ruotare o riflettere un punto in un piano](images/aboutgdip05-art07.png)

Tutte le trasformazioni mostrate nella figura precedente sono trasformazioni lineari. Alcune altre trasformazioni, ad esempio la traduzione, non sono lineari e non possono essere espresse come moltiplicazione da una matrice 2 × 2. Si supponga di voler iniziare con il punto (2, 1), ruotarlo 90 gradi, tradurlo 3 unità nella direzione x e tradurlo 4 unità nella direzione y. È possibile eseguire questa operazione eseguendo una moltiplicazione di matrici seguita da un'aggiunta della matrice.

![illustrazione che Mostra come la moltiplicazione e l'addizione della matrice possono ruotare un punto e tradurlo due volte](images/aboutgdip05-art08.png)

Una trasformazione lineare (moltiplicazione per una matrice 2 × 2) seguita da una traduzione (aggiunta di una matrice 1 × 2) viene definita trasformazione affine. Un'alternativa all'archiviazione di una trasformazione affine in una coppia di matrici (una per la parte lineare e una per la traduzione) consiste nell'archiviare l'intera trasformazione in una matrice di 3 × 3. Per eseguire questa operazione, un punto nel piano deve essere archiviato in una matrice da 1 × 3 con una terza coordinata fittizia. La tecnica usuale consiste nel rendere tutte le 3 Coordinate uguali a 1. Il punto (2, 1), ad esempio, è rappresentato dalla matrice \[ 2 1 1 \] . Nella figura seguente viene illustrata una trasformazione affine (ruota 90 gradi; trasla 3 unità nella direzione x, 4 unità nella direzione y) espresse come moltiplicazione da una singola matrice 3 × 3.

![illustrazione che Mostra come la moltiplicazione di matrici può eseguire una trasformazione affine](images/aboutgdip05-art09.png)

Nell'esempio precedente, il punto (2, 1) viene mappato al punto (2, 6). Si noti che la terza colonna della matrice 3 × 3 contiene i numeri 0, 0, 1. Questo sarà sempre il caso della matrice 3 × 3 di una trasformazione affine. I numeri importanti sono i sei numeri nelle colonne 1 e 2. La parte superiore sinistra 2 × 2 della matrice rappresenta la parte lineare della trasformazione e le prime due voci della terza riga rappresentano la traduzione.

![illustrazione che mostra che le prime due colonne sono più significative per una matrice 3x3 di una trasformazione affine](images/aboutgdip05-art10.png)

In Windows GDI+ è possibile archiviare una trasformazione affine in un oggetto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Poiché la terza colonna di una matrice che rappresenta una trasformazione affine è sempre (0, 0, 1), si specificano solo i sei numeri nelle prime due colonne quando si costruisce un oggetto **Matrix** . L'istruzione `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` costruisce la matrice mostrata nella figura precedente.

## <a name="composite-transformations"></a>Trasformazioni composite

Una trasformazione composita è una sequenza di trasformazioni, una seguita dall'altra. Prendere in considerazione le matrici e le trasformazioni nell'elenco seguente:

-   Matrice A ruota 90 gradi
-   Matrice B scala per fattore 2 nella direzione x
-   Matrice C trasla 3 unità nella direzione y

Se si inizia con il punto (2, 1), rappresentato dalla matrice \[ 2 1 1 \] , e si moltiplica per a, quindi B, quindi C, il punto (2, 1) subirà le tre trasformazioni nell'ordine indicato.

\[2 1 1 \] ABC = \[ -2 5 1\]

Anziché archiviare le tre parti della trasformazione composita in tre matrici separate, è possibile moltiplicare a, B e C per ottenere una singola matrice da 3 × 3 che archivia l'intera trasformazione composita. Si supponga ABC = D. Un punto moltiplicato per D restituisce lo stesso risultato di un punto moltiplicato per A, quindi B, quindi C.

\[2 1 1 \] D = \[ -2 5 1\]

Nella figura seguente sono illustrate le matrici A, B, C e D.

![illustrazione che illustra come eseguire più trasformazioni moltiplicando le matrici costitutive](images/aboutgdip05-art12.png)

Il fatto che la matrice di una trasformazione composita possa essere formata moltiplicando le singole matrici di trasformazione significa che qualsiasi sequenza di trasformazioni affini può essere archiviata in un singolo oggetto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .

> [!Note]  
> L'ordine di una trasformazione composita è importante. In generale, ruotare, quindi ridimensionare, quindi tradurre non corrisponde a scala, quindi ruotare e quindi traslare. Analogamente, l'ordine di moltiplicazione della matrice è importante. In generale, ABC non corrisponde a BAC.

 

La classe [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) offre diversi metodi per la compilazione di una trasformazione composita: [**Matrix:: Multiply**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix:: Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix:: RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix:: scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix:: Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)e [**Matrix:: translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate). Nell'esempio seguente viene creata la matrice di una trasformazione composita che ruota per prima 30 gradi, quindi viene ridimensionata in base a un fattore 2 nella direzione y, quindi vengono convertite 5 unità nella direzione x.


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



Nella figura seguente viene illustrata la matrice.

![illustrazione che mostra una matrice con valori espressi come funzioni trigonometriche e una matrice con valori approssimativi di tali funzioni](images/aboutgdip05-art13.png)

 

 



