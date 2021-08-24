---
description: Molte applicazioni CAD offrono funzionalità che ruotano gli oggetti disegnati nell'area client.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa6552411e2e018d04ff55cbeeb430d185fe62d61dc59d421d08dbe6e0d7174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602701"
---
# <a name="rotation"></a>Rotazione

Molte applicazioni CAD offrono funzionalità che ruotano gli oggetti disegnati nell'area client. Le applicazioni che includono funzionalità di rotazione usano [**la funzione SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare lo spazio globale appropriato sulla trasformazione dello spazio della pagina. Questa funzione riceve un puntatore a una [**struttura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) contenente i valori appropriati. I membri eM11, eM12, eM21 ed eM22 di XFORM specificano rispettivamente il coseno, il seno, il seno negativo e il coseno dell'angolo di rotazione.

Quando *si verifica* la rotazione, i punti che costituiscono un oggetto vengono ruotati rispetto all'origine dello spazio delle coordinate. La figura seguente mostra un rettangolo di 20 per 20 unità ruotato di 30 gradi quando viene copiato dallo spazio delle coordinate del mondo allo spazio delle coordinate di pagina.

![illustrazione che mostra due spazi delle coordinate; ognuno ha un rectange in una posizione diversa e con una rotazione diversa](images/cstrn-11.png)

Nella figura precedente ogni punto del rettangolo è stato ruotato di 30 gradi rispetto all'origine dello spazio delle coordinate.

L'algoritmo seguente calcola la nuova coordinata x (x ') per un punto (x,y ) ruotato in base all'angolo A rispetto all'origine dello spazio delle coordinate.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

L'algoritmo seguente calcola la coordinata y (y ') per un punto (x,y ) ruotato in base all'angolo A rispetto all'origine.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

Le due trasformazioni di rotazione possono essere combinate in una matrice 2 per 2 come indicato di seguito.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

La matrice 2 per 2 che ha generato la rotazione contiene i valori seguenti.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Derivazione dell'algoritmo di rotazione

Gli algoritmi di rotazione si basano sul teorema di addizione della trigonometria che indica che la funzione trigonometrica di una somma di due angoli (A1 e A2) può essere espressa in termini di funzioni trigonometriche dei due angoli.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

La figura seguente mostra un punto p ruotato in senso antiorario in una nuova posizione p'. Mostra inoltre due triangoli formati da una linea disegnata dall'origine dello spazio delle coordinate a ogni punto e da una linea disegnata da ogni punto attraverso l'asse x.

![diagramma che mostra l'origine, p e p' e due triangoli](images/cstrn-12.png)

Usando la trigonometria, è possibile ottenere la coordinata x del punto p moltiplicando la lunghezza dell'ipotenusa h per il coseno di A1.

``` syntax
x = h * cos A1 
```

La coordinata y del punto p può essere ottenuta moltiplicando la lunghezza dell'ipotenusa h per il seno di A1.

``` syntax
y = h * sin A1 
```

Analogamente, la coordinata x del punto p' può essere ottenuta moltiplicando la lunghezza dell'ipotenusa h per il coseno di (A1 +A2).

``` syntax
x' = h * cos (A1 + A2) 
```

Infine, è possibile ottenere la coordinata y del punto p' moltiplicando la lunghezza dell'ipotenusa h per il seno di (A1 +A2).

``` syntax
y' = h * sin (A1 + A2) 
```

Usando il theorema di addizione, gli algoritmi precedenti diventano i seguenti:

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Gli algoritmi di rotazione per un determinato punto ruotato in base all'angolo A2 possono essere ottenuti sostituendo x per ogni occorrenza di (h cos A1) e sostituendo y per ogni occorrenza di \* (h \* sin A1).

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



