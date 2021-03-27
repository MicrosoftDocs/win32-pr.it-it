---
description: Molte applicazioni CAD forniscono funzionalità che ruotano gli oggetti disegnati nell'area client.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980679"
---
# <a name="rotation"></a>Rotazione

Molte applicazioni CAD forniscono funzionalità che ruotano gli oggetti disegnati nell'area client. Le applicazioni che includono le funzionalità di rotazione usano la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare la trasformazione dello spazio globale nella pagina appropriata. Questa funzione [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati. I membri eM11, eM12, eM21 e eM22 di specificano rispettivamente il coseno, il seno, il seno negativo e il coseno dell'angolo di rotazione.

Quando si verifica la *rotazione* , i punti che costituiscono un oggetto vengono ruotati rispetto all'origine dello spazio delle coordinate. La figura seguente mostra un rettangolo di 20 unità ruotato di 30 gradi quando viene copiato dallo spazio delle coordinate internazionali allo spazio delle coordinate di pagina.

![illustrazione che mostra due spazi delle coordinate. ogni ha un rectange in una posizione diversa e con una rotazione diversa](images/cstrn-11.png)

Nell'illustrazione precedente ogni punto nel rettangolo è stato ruotato di 30 gradi rispetto all'origine dello spazio delle coordinate.

Nell'algoritmo seguente viene calcolata la nuova coordinata x (x) per un punto (x, y) ruotato dell'angolo A rispetto all'origine dello spazio delle coordinate.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

Nell'algoritmo seguente viene calcolata la coordinata y (y) per un punto (x, y) ruotato dall'angolo A rispetto all'origine.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

Le due trasformazioni di rotazione possono essere combinate in una matrice 2 per 2 come indicato di seguito.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

La matrice 2 per 2 che ha prodotto la rotazione contiene i valori seguenti.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Derivazione dell'algoritmo di rotazione

Gli algoritmi di rotazione sono basati sul teorema di addizione di trigonometria che informa che la funzione trigonometrica di una somma di due angoli (a1 e a2) può essere espressa in termini di funzioni trigonometriche dei due angoli.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

Nella figura seguente viene mostrato un punto p ruotato in senso antiorario a una nuova posizione p '. Inoltre, vengono visualizzati due triangoli formati da una linea disegnata dall'origine dello spazio delle coordinate a ogni punto e una linea disegnata da ogni punto attraverso l'asse x.

![diagramma che mostra l'origine, p e p ' e due triangoli](images/cstrn-12.png)

Con la trigonometria, è possibile ottenere la coordinata x del punto p moltiplicando la lunghezza dell'ipotenusa h per il coseno di a1.

``` syntax
x = h * cos A1 
```

La coordinata y del punto p può essere ottenuta moltiplicando la lunghezza dell'ipotenusa h per il seno di a1.

``` syntax
y = h * sin A1 
```

Analogamente, la coordinata x del punto p ' può essere ottenuta moltiplicando la lunghezza dell'ipotenusa h per il coseno di (a1 + a2).

``` syntax
x' = h * cos (A1 + A2) 
```

Infine, la coordinata y del punto p ' può essere ottenuta moltiplicando la lunghezza dell'ipotenusa h per il seno di (a1 + a2).

``` syntax
y' = h * sin (A1 + A2) 
```

Utilizzando il teorema di aggiunta, gli algoritmi precedenti diventano gli elementi seguenti:

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Gli algoritmi di rotazione per un determinato punto ruotato dell'angolo a2 possono essere ottenuti sostituendo x per ogni occorrenza di (h \* cos a1) e sostituendo y per ogni occorrenza di (h \* sin a1).

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



