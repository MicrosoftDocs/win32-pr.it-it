---
description: Durante la programmazione Direct3D e Window, gli oggetti sullo schermo vengono definiti in termini di rettangoli di delimitazione.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rettangoli (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02dda6e8a4f10128ab11ffeb8b390e79be7cc0f698ed1625ca3f2c5df995d67e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119368876"
---
# <a name="rectangles-direct3d-9"></a>Rettangoli (Direct3D 9)

Durante la programmazione Direct3D e Window, gli oggetti sullo schermo vengono definiti in termini di rettangoli di delimitazione. I lati di un rettangolo di delimitazione sono sempre paralleli ai lati dello schermo, quindi il rettangolo può essere descritto da due punti, l'angolo superiore sinistro e l'angolo inferiore destro. La maggior parte delle applicazioni [**usa la struttura RECT**](/previous-versions//dd162897(v=vs.85)) per portare informazioni su un rettangolo di delimitazione da usare durante il b blitting sullo schermo o l'esecuzione del rilevamento di hit.

In C++ la [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) ha la definizione seguente.


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



Nell'esempio precedente i membri sinistro e superiore sono le coordinate x e y dell'angolo superiore sinistro di un rettangolo di delimitazione. Analogamente, i membri destro e inferiore costituiscono le coordinate dell'angolo inferiore destro. La figura seguente mostra come è possibile visualizzare questi valori.

![illustrazione del rettangolo delimitato dai valori sinistro, superiore, destro e inferiore](images/rect.png)

La colonna di pixel sul bordo destro e la riga di pixel sul bordo inferiore non sono incluse nel rect. Ad esempio, il blocco di un rect con membri {10, 10, 138, 138} comporta un oggetto di 128 pixel in larghezza e altezza.

Per garantire efficienza, coerenza e facilità d'uso, tutte le funzioni di presentazione Direct3D funzionano con i rettangoli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
