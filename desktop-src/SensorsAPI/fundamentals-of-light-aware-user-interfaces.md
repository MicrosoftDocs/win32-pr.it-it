---
description: Nozioni fondamentali Light-Aware utente
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Nozioni fondamentali Light-Aware utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8955180dfc57219d3b640c6463f2ee2025f22500d3d29b688bc4b0c154895f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890207"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a>Nozioni fondamentali Light-Aware utente

Il  termine interfaccia utente con luce si riferisce a un programma che usa i dati dei sensori di luce per ottimizzarne il contenuto, i controlli e altri elementi grafici per un'esperienza utente ottimale in molte condizioni di illuminazione, che vanno dalla luce alla luce diretta. Probabilmente le ottimizzazioni più importanti sono la leggibilità, la leggibilità e le interazioni in modo diretto, perché le schermate in genere non hanno prestazioni ottimali in queste condizioni. In questa sezione vengono trattate tre proprietà dell'interfaccia utente: scala, contrasto e colore. Queste proprietà possono essere modificate per ottimizzare l'esperienza utente visiva.

## <a name="scale-and-brightness"></a>Scala e luminosità

In generale, gli oggetti più grandi sono più facili da visualizzare. Quando il computer si trova in condizioni di illuminazione negative (ad esempio in modo diretto) la dimensione del contenuto può contribuire a migliorare la leggibilità e l'interattività del contenuto.

Le fotografie seguenti confrontano un portatile in modo diretto con la luminosità e i livelli di zoom tipici dello schermo a un portatile nelle stesse condizioni di illuminazione con l'interfaccia utente con luce. La prima fotografia mostra la visualizzazione impostata su una luminosità del 40% con livelli di zoom normali. La seconda fotografia mostra la luminosità dello schermo impostata su 100% con livelli di zoom maggiori.

![Schermo portatile con luminosità del 40% con livelli di zoom normali](images/laptop-40.png)![schermo portatile con luminosità del 100% con livelli di zoom maggiori](images/laptop-100.png)

### <a name="varying-font-size"></a>Dimensioni del carattere variabili

Se si aumentano le dimensioni del tipo di carattere usato per visualizzare il testo, il testo è più leggibile in condizioni di illuminazione negative. Lo stile del carattere, il viso del carattere e altre caratteristiche possono anche essere diversi per ottimizzare la leggibilità e la leggibilità. Ad esempio, i tipi di carattere sans serif sono in genere più facili da leggere rispetto ai tipi di carattere serif.

![Confronto tra il tipo di carattere sans serif e il tipo di carattere serif](images/fonts.png)

### <a name="zooming-content"></a>Zoom del contenuto

Se il programma implementa lo zoom, può essere usato per ridimensionare il contenuto. Lo zoom avanti migliora la leggibilità mentre lo zoom indietro consente al programma di visualizzare più contenuto.

### <a name="altering-vector-graphic-rendering-properties"></a>Modifica delle proprietà di rendering grafico vettoriale

Se il programma esegue il rendering di primitive grafiche vettoriali (ad esempio linee, cerchi e così via), le caratteristiche del rendering possono essere modificate per ottimizzare la leggibilità. Ad esempio, se il programma esegue il rendering dei rettangoli, la larghezza delle linee usate per il rendering dei rettangoli può essere ridimensionata (più ampia per ambienti esterni e più stretta per interni) per ottimizzare l'aspetto e la leggibilità del contenuto grafico vettoriale.

## <a name="contrast"></a>Si confronti

Quando gli schermi LCD vengono usati in condizioni di illuminazione luminosi, il contrasto complessivo dello schermo viene ridotto. Quando lo schermo è inondato di luce (dal sole, ad esempio), la percezione dell'utente di aree scuri sullo schermo è ridotta. In generale, ciò rende importante aumentare il contrasto del contenuto e dell'interfaccia utente quando la luce ambientale è luminosità. Può essere utile usare una combinazione colori monocromatica per ottimizzare il contrasto in queste condizioni di illuminazione. Un altro modo per aumentare il contrasto è sostituire il contenuto a contrasto basso (ad esempio, una modalità foto aerea in un programma di mapping) con elementi a contrasto elevato (ad esempio la modalità grafica vettoriale strada nera su bianco).

## <a name="color"></a>Color

I colori utilizzati da un programma per visualizzare il contenuto possono avere un effetto drastico sull'esperienza utente complessiva e sulla leggibilità del contenuto sottoposto a rendering. Modificando il contrasto dei colori in base alla luce ambientale, è possibile rendere il contenuto più leggibile in condizioni di illuminazione sfavorevoli, ad esempio luce esterna o luce interna scura.

Un modo per aumentare il contrasto dei colori è tramite la saturazione dei colori. Un altro modo è usare colori complementari anziché colori adiacenti per una migliore leggibilità. I colori complementari sono coppie di colori di tonalità opposta, ad esempio blu e giallo. L'esempio affiancato seguente illustra come l'uso di colori complementari può contribuire a migliorare il contrasto dei colori.

![esempio degli effetti del colore del testo sulla leggibilità.](images/color.png)

 

 



