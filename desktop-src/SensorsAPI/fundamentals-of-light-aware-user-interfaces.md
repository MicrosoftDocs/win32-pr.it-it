---
description: Nozioni fondamentali sulle interfacce utente Light-Aware
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Nozioni fondamentali sulle interfacce utente Light-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce71ab67e11684d14b188fef7ae73500edb7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758753"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a>Nozioni fondamentali sulle interfacce utente Light-Aware

Il termine *interfaccia utente chiara* fa riferimento a un programma che usa i dati del sensore chiaro per ottimizzare il contenuto, i controlli e altri elementi grafici per un'esperienza utente ottimale in molte condizioni di illuminazione, a partire dalle tenebre alla luce solare diretta. Forse le ottimizzazioni più importanti sono la leggibilità, la leggibilità e le interazioni nel sole diretto, perché le schermate in genere non offrono prestazioni ottimali in queste condizioni. Questa sezione è incentrata su tre proprietà dell'interfaccia utente: scala, contrasto e colore. Queste proprietà possono essere modificate per ottimizzare l'esperienza utente visiva.

## <a name="scale-and-brightness"></a>Scalabilità e luminosità

In generale, gli oggetti più grandi sono più semplici da vedere. Quando il computer si trova in condizioni di illuminazione indesiderate, ad esempio nella luce solare diretta, il contenuto può contribuire a migliorare la leggibilità e l'interoperabilità di tale contenuto.

Le fotografie seguenti confrontano un computer portatile in diretta Sunlight con la tipica luminosità dello schermo e i livelli di zoom per un computer portatile con le stesse condizioni di illuminazione con interfaccia utente con supporto chiaro. La prima foto mostra il set di luminosità del 40% con livelli di zoom normali. La seconda foto mostra il set di luminosità della luminosità del 100% con livelli di zoom maggiori.

![schermo portatile con luminosità al 40% con livelli di zoom normali](images/laptop-40.png)![schermo portatile con luminosità al 100% con livelli di zoom più elevati](images/laptop-100.png)

### <a name="varying-font-size"></a>Dimensioni del carattere variabili

Se si aumentano le dimensioni del tipo di carattere utilizzato per visualizzare il testo, il testo risulta più leggibile in condizioni di illuminazione indesiderate. È anche possibile variare lo stile del carattere, il tipo di carattere e altre caratteristiche per ottimizzare la leggibilità e la leggibilità. Ad esempio, i tipi di carattere Sans Serif sono in genere più facili da leggere rispetto ai tipi di carattere serif.

![tipo di carattere sans serif rispetto a Serif](images/fonts.png)

### <a name="zooming-content"></a>Zoom del contenuto

Se il programma implementa lo zoom, è possibile usarlo per ridimensionare il contenuto. Lo zoom avanti migliora la leggibilità mentre lo zoom indietro consente al programma di visualizzare più contenuti.

### <a name="altering-vector-graphic-rendering-properties"></a>Modifica delle proprietà del rendering grafico vettoriale

Se il programma esegue il rendering delle primitive grafiche vettoriali (ad esempio linee, cerchi e così via), è possibile modificare le caratteristiche del rendering per ottimizzare la leggibilità. Se, ad esempio, il programma esegue il rendering dei rettangoli, la larghezza delle linee utilizzate per il rendering dei rettangoli potrebbe essere ridimensionata (più ampia per le aree esterne e più strette per gli indoor) per ottimizzare l'aspetto e la leggibilità del contenuto grafico vettoriale.

## <a name="contrast"></a>Si confronti

Quando le schermate LCD vengono usate in condizioni di illuminazione luminose, il contrasto generale dello schermo viene ridotto. Quando lo schermo viene invaso da luce (ad esempio, dal sole), la percezione dell'utente delle aree scure sullo schermo viene ridotta. In generale, questo rende importante aumentare il contrasto del contenuto e dell'interfaccia utente quando la luce di ambiente è luminosa. Potrebbe essere utile usare una combinazione di colori monocromatico per ottimizzare il contrasto in queste condizioni di illuminazione. Un altro modo per aumentare il contrasto consiste nel sostituire il contenuto a contrasto ridotto (ad esempio, una modalità foto aerea in un programma di mapping) con elementi a contrasto elevato, ad esempio la modalità di grafica vettoriale in bianco e nero.

## <a name="color"></a>Colore

I colori usati da un programma per visualizzare il contenuto possono avere un impatto significativo sull'esperienza utente complessiva e la leggibilità del contenuto sottoposto a rendering. Modificando il contrasto dei colori in base alla luce di ambiente, è possibile rendere il contenuto più leggibile in condizioni di illuminazione indesiderate, ad esempio la luce esterna luminosa o la luce interna scura.

Un modo per aumentare il contrasto dei colori è la saturazione dei colori. Un altro modo consiste nell'usare colori complementari anziché colori adiacenti per migliorare la leggibilità. I colori complementari sono coppie di colori di tonalità opposta, ad esempio blu e giallo. Nell'esempio affiancato riportato di seguito viene illustrato come l'utilizzo di colori complementari possa migliorare il contrasto dei colori.

![esempio degli effetti del colore del testo sulla leggibilità.](images/color.png)

 

 



