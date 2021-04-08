---
description: Sempre più, le applicazioni impiegano effetti speciali comunemente utilizzati nei film e nei video, come dissolvenze, scorrimenti e dissolvenza.
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: Dissolvenze, dissolvenze e scorrimenti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ad837ea846ca43d61102ce426d415270d2f27f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746858"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a>Dissolvenze, dissolvenze e scorrimenti (Direct3D 9)

Sempre più, le applicazioni impiegano effetti speciali comunemente utilizzati nei film e nei video, come dissolvenze, scorrimenti e dissolvenza.

In una dissolvenza, un'immagine viene sostituita gradualmente da un'altra in una sequenza uniforme di frame. Sebbene Direct3D fornisca metodi di utilizzo della combinazione di più trame per ottenere lo stesso effetto, le applicazioni che utilizzano il buffer dello stencil per le soluzioni possono utilizzare le funzionalità di combinazione di trame per altri effetti mentre eseguono una dissolvenza.

Quando l'applicazione esegue una dissolvenza, deve eseguire il rendering di due immagini diverse. Usa il buffer dello stencil per controllare quali pixel di ogni immagine vengono disegnati nell'area di destinazione del rendering. È possibile definire una serie di maschere dello stencil e copiarle nel buffer dello stencil nei frame successivi. In alternativa, è possibile definire una maschera di stencil di base per il primo frame e modificarla in modo incrementale.

All'inizio della dissolvenza, l'applicazione imposta la funzione stencil e la maschera dello stencil in modo che la maggior parte dei pixel dall'immagine iniziale superi il test di stencil. La maggior parte dei pixel dell'immagine finale deve avere esito negativo per il test di stencil. Nei frame successivi la maschera dello stencil viene aggiornata in modo che il test venga superato da un minor numero di pixel nell'immagine iniziale. Con l'avanzamento dello stato dei frame, il test non viene superato dal numero inferiore e inferiore dei pixel nell'immagine finale. In questo modo, l'applicazione può eseguire una dissolvenza usando qualsiasi modello di dissolvenza arbitraria.

Dissolvenza o dissolvenza è un caso speciale di risoluzione. Quando si dissolve in, il buffer dello stencil viene usato per dissolversi da un'immagine nera o bianca a un rendering di una scena 3D. Il dissolvenza è il contrario, l'applicazione inizia con un rendering di una scena 3D e viene risolta in nero o bianco. La dissolvenza può essere eseguita utilizzando qualsiasi modello arbitrario che si desidera utilizzare.

Le applicazioni Direct3D utilizzano una tecnica simile per i SWIP. Ad esempio, quando un'applicazione esegue un scorrimento da sinistra a destra, l'immagine finale appare gradualmente sulla parte superiore dell'immagine iniziale da sinistra verso destra. Come in una dissolvenza, è necessario definire una serie di maschere di stencil caricate nel buffer dello stencil nei frame successivi oppure modificare successivamente la maschera iniziale dello stencil. Le maschere degli stencil vengono usate per disabilitare la scrittura dei pixel dall'immagine iniziale e per abilitare la scrittura dei pixel dall'immagine finale.

Un scorrimento è leggermente più complesso rispetto a una dissolvenza in quanto l'applicazione deve leggere i pixel dall'immagine finale nell'ordine inverso del dito. Ovvero, se il dito viene spostato da sinistra a destra, l'applicazione deve leggere i pixel dall'immagine finale da destra a sinistra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche del buffer dello stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



