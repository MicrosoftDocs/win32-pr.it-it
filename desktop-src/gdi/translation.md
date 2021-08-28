---
description: Alcune applicazioni traslano (o spostano) gli oggetti disegnati nell'area client.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Traduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115af82d1e5b80fa4c50d081e6d042d2f2c9c8950f3b4b8f6ed09108df4c52bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613341"
---
# <a name="translation"></a>Traduzione

Alcune applicazioni traslano (o spostano) gli oggetti disegnati nell'area client. chiamando la [**funzione SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare lo spazio globale appropriato sulla trasformazione dello spazio di pagina. La funzione SetWorldTransform riceve un puntatore a una [**struttura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) contenente i valori appropriati. I membri eDx ed eDy di XFORM specificano rispettivamente i componenti di traslazione orizzontale e verticale.

Quando *si verifica* la traslazione, ogni punto di un oggetto viene spostato verticalmente, orizzontalmente o entrambi di una quantità specificata. La figura seguente mostra un rettangolo di 20 x 20 unità convertito a destra di 10 unità quando viene copiato dallo spazio delle coordinate del mondo allo spazio delle coordinate della pagina.

![figura che mostra un rettangolo in una posizione nello spazio mondiale e in una posizione diversa nello spazio della pagina](images/cstrn-09.png)

Nella figura precedente la coordinata x di ogni punto nel rettangolo è maggiore di 10 unità rispetto alla coordinata x originale.

La conversione orizzontale può essere rappresentata dall'algoritmo seguente.

``` syntax
x' = x + Dx 
```

Dove x' è la nuova coordinata x, x è la coordinata x originale e Dx è la distanza orizzontale spostata.

La conversione verticale può essere rappresentata dall'algoritmo seguente.

``` syntax
y' = y + Dy 
```

Dove y' è la nuova coordinata y, y è la coordinata y originale e Dy è la distanza verticale spostata.

Le trasformazioni di traslazione orizzontale e verticale possono essere combinate in una singola operazione usando una matrice 3 per 3.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

Le regole di moltiplicazione della matrice specificano che il numero di righe in una matrice deve essere uguale al numero di colonne nell'altra. Il numero intero 1 nella matrice x y 1 è un segnaposto aggiunto \| per soddisfare questo \| requisito.

La matrice 3 per 3 che ha prodotto la trasformazione della traduzione illustrata contiene i valori seguenti.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



