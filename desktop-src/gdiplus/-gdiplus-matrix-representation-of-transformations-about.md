---
description: Una matrice m&\# 215;n è un set di numeri disposti in m righe e n colonne. La figura seguente mostra diverse matrici.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Rappresentazione tramite matrici delle trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122d59787038cd75a9806cac6cb0d225e8660eb13d7482d3ee1f47ff0732ca5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036659"
---
# <a name="matrix-representation-of-transformations"></a>Rappresentazione tramite matrici delle trasformazioni

Una *matrice m×n* è un set di numeri disposti in *m* righe e *n* colonne. La figura seguente mostra diverse matrici.

![illustrazione che mostra sei matrici di dimensioni variabili](images/aboutgdip05-art04.png)

È possibile aggiungere due matrici della stessa dimensione aggiungendo singoli elementi. Nella figura seguente vengono illustrati due esempi di addizione di matrici.

![illustrazione che illustra come eseguire l'aggiunta di matrici](images/aboutgdip05-art05.png)

Una *matrice m×n* può essere moltiplicata per una matrice *n×p* e il risultato è *una matrice m×p.* Il numero di colonne nella prima matrice deve corrispondere al numero di righe nella seconda matrice. Ad esempio, una matrice di 4 ×2 può essere moltiplicata per una matrice di 2 ×3 per produrre una matrice di 4 ×3.

I punti nel piano e le righe e le colonne di una matrice possono essere pensati come vettori. Ad esempio, (2, 5) è un vettore con due componenti e (3, 7, 1) è un vettore con tre componenti. Il prodotto del punto di due vettori è definito come segue:

(a, b) • (c, d) = ac + bd

(a, b, c) • (d, e, f) = ad + be + cf

Ad esempio, il prodotto punto di (2, 3) e (5, 4) è (2)(5) + (3)(4) = 22. Il prodotto punto di (2, 5, 1) e (4, 3, 1) è (2)(4) + (5)(3) + (1)(1) = 24. Si noti che il prodotto del punto di due vettori è un numero, non un altro vettore. Si noti anche che è possibile calcolare il prodotto del punto solo se i due vettori hanno lo stesso numero di componenti.

A(i, j) deve essere la voce nella matrice A nella riga i **e** nella colonna **j.** Ad esempio, A(3, 2) è la voce nella matrice A nella riga 3 **rd** e nella **seconda colonna.** Si supponga che A, B e C siano matrici e AB = C. Le voci di C vengono calcolate come segue:

C(i, j) = (riga i di A) • (colonna j di B)

La figura seguente mostra diversi esempi di moltiplicazione di matrici.

![Illustrazione che illustra come eseguire la moltiplicazione di matrici](images/aboutgdip05-art06.png)

Se si pensa a un punto nel piano come a una matrice 1 × 2, è possibile trasformare tale punto moltiplicando il punto per una matrice di 2 × 2. La figura seguente mostra diverse trasformazioni applicate al punto (2, 1).

![illustrazione che illustra come usare la moltiplicazione di matrici per ridimensionare, ruotare o riflettere un punto in un piano](images/aboutgdip05-art07.png)

Tutte le trasformazioni illustrate nella figura precedente sono trasformazioni lineari. Alcune altre trasformazioni, ad esempio la traslazione, non sono lineari e non possono essere espresse come moltiplicazione per una matrice di 2 × 2. Si supponga di voler iniziare con il punto (2, 1), ruotarlo di 90 gradi, traslarlo di 3 unità nella direzione x e traslarlo di 4 unità nella direzione y. A tale scopo, è possibile eseguire una moltiplicazione di matrici seguita da un'aggiunta di matrice.

![illustrazione che mostra come la moltiplicazione e l'addizione di matrici possono ruotare un punto e traslarlo due volte](images/aboutgdip05-art08.png)

Una trasformazione lineare (moltiplicazione per una matrice 2 × 2) seguita da una traslazione (aggiunta di una matrice 1 × 2) è detta trasformazione affine. Un'alternativa all'archiviazione di una trasformazione affine in una coppia di matrici (una per la parte lineare e una per la traslazione) consiste nell'archiviare l'intera trasformazione in una matrice di 3 × 3. Per eseguire questa operazione, un punto nel piano deve essere archiviato in una matrice di 1 × 3 con una terza coordinata fittizia. La tecnica consueta consiste nel rendere tutte le terze coordinate uguali a 1. Ad esempio, il punto (2, 1) è rappresentato dalla matrice \[ 2 1 1 \] . La figura seguente mostra una trasformazione affine (rotazione di 90 gradi, traslazione di 3 unità nella direzione x, 4 unità nella direzione y) espressa come moltiplicazione per una singola matrice di 3 × 3.

![Illustrazione che mostra come la moltiplicazione di matrici può eseguire una trasformazione affine](images/aboutgdip05-art09.png)

Nell'esempio precedente viene eseguito il mapping del punto (2, 1) al punto (2, 6). Si noti che la terza colonna della matrice 3 × 3 contiene i numeri 0, 0, 1. Questo sarà sempre il caso per la matrice 3 × 3 di una trasformazione affine. I numeri importanti sono i sei numeri nelle colonne 1 e 2. La parte superiore sinistra 2 × 2 della matrice rappresenta la parte lineare della trasformazione e le prime due voci nella terza riga rappresentano la traslazione.

![figura che mostra che le prime due colonne sono più significative per una matrice 3x3 di una trasformazione affine](images/aboutgdip05-art10.png)

In Windows GDI+ è possibile archiviare una trasformazione affine in un [**oggetto Matrix.**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Poiché la terza colonna di una matrice che rappresenta una trasformazione affine è sempre (0, 0, 1), quando si costruisce un oggetto **Matrix** si specificano solo i sei numeri nelle prime due colonne. `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);`L'istruzione costruisce la matrice illustrata nella figura precedente.

## <a name="composite-transformations"></a>Trasformazioni composite

Una trasformazione composita è una sequenza di trasformazioni, una seguita dall'altra. Si considerino le matrici e le trasformazioni nell'elenco seguente:

-   Matrice A Rotazione di 90° gradi
-   Matrice B Ridimensionare di un fattore di 2 nella direzione x
-   Matrice C Trasla 3 unità nella direzione y

Se si inizia con il punto (2, 1), rappresentato dalla matrice 2 1 1, e si moltiplica per A, quindi B, C, il punto \[ (2,1) verrà sottoposto alle tre trasformazioni nell'ordine \] elencato.

\[2 1 1 \] ABC = \[ -2 5 1\]

Anziché archiviare le tre parti della trasformazione composita in tre matrici separate, è possibile moltiplicare A, B e C insieme per ottenere una singola matrice di 3 × 3 che archivia l'intera trasformazione composita. Si supponga che ABC = D. Un punto moltiplicato per D restituisce quindi lo stesso risultato di un punto moltiplicato per A, quindi B e C.

\[2 1 1 \] D = \[ -2 5 1\]

La figura seguente mostra le matrici A, B, C e D.

![illustrazione che illustra come eseguire più trasformazioni moltiplicando le matrici costituenti](images/aboutgdip05-art12.png)

Il fatto che la matrice di una trasformazione composita possa essere formata moltiplicando le singole matrici di trasformazione significa che qualsiasi sequenza di trasformazioni affine può essere archiviata in un singolo [**oggetto Matrix.**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)

> [!Note]  
> L'ordine di una trasformazione composita è importante. In generale, ruotare, ridimensionare, quindi traslare non è uguale alla scala, quindi ruotare e quindi traslare. Analogamente, l'ordine di moltiplicazione della matrice è importante. In generale, ABC non corrisponde a BAC.

 

La classe [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) fornisce diversi metodi per la creazione di una trasformazione composita: [**Matrix::Multiply**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix::Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix::RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix::Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix::Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)e [**Matrix::Translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate). Nell'esempio seguente viene creata la matrice di una trasformazione composita che ruota prima di 30 gradi, quindi ridimensiona di un fattore di 2 nella direzione y e quindi trasla 5 unità nella direzione x.


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



La figura seguente illustra la matrice.

![figura che mostra una matrice con valori espressi come funzioni trigonometriche e una matrice con valori approssimativi di tali funzioni](images/aboutgdip05-art13.png)

 

 



