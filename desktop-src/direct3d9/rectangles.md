---
description: Durante la programmazione di Direct3D e finestre, gli oggetti sullo schermo vengono definiti in termini di rettangoli di delimitazione.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rettangoli (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123435"
---
# <a name="rectangles-direct3d-9"></a>Rettangoli (Direct3D 9)

Durante la programmazione di Direct3D e finestre, gli oggetti sullo schermo vengono definiti in termini di rettangoli di delimitazione. I lati di un rettangolo di delimitazione sono sempre paralleli ai lati dello schermo, quindi il rettangolo può essere descritto da due punti, dall'angolo superiore sinistro e dall'angolo inferiore destro. La maggior parte delle applicazioni usa la struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per includere informazioni su un rettangolo di delimitazione da usare quando blitting sullo schermo o eseguendo il rilevamento dei riscontri.

In C++, la struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) presenta la definizione seguente.


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



Nell'esempio precedente i membri Left e Top sono le coordinate x e y dell'angolo superiore sinistro di un rettangolo di delimitazione. Analogamente, i membri destro e inferiore costituiscono le coordinate dell'angolo inferiore destro. Nella figura seguente viene illustrato come è possibile visualizzare questi valori.

![illustrazione del rettangolo delimitato dai valori sinistro, superiore, destro e inferiore](images/rect.png)

La colonna di pixel sul bordo destro e la riga di pixel sul bordo inferiore non sono inclusi in RECT. Ad esempio, il blocco di un oggetto RECT con i membri {10, 10, 138, 138} restituisce un oggetto 128 pixel in larghezza e altezza.

Per l'efficienza, la coerenza e la semplicità d'uso, tutte le funzioni di presentazione Direct3D funzionano con i rettangoli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
