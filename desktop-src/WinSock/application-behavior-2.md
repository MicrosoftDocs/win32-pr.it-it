---
description: Un altro aspetto dello sviluppo di applicazioni da considerare è la differenza nel comportamento tra le operazioni locali o tra computer e il comportamento quando le operazioni avvengono tra due computer in rete.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportamento dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526214"
---
# <a name="application-behavior"></a>Comportamento dell'applicazione

Un altro aspetto dello sviluppo di applicazioni da considerare è la differenza nel comportamento tra le operazioni locali o tra computer e il comportamento quando le operazioni avvengono tra due computer in rete. Esistono comportamenti dell'applicazione che possono funzionare correttamente in un computer locale, ma quando vengono eseguiti in una rete, provoca un calo significativo delle prestazioni e l'utilizzo delle risorse. Quando si sviluppano applicazioni Windows Sockets, è consigliabile evitare i comportamenti seguenti dell'applicazione.

## <a name="behaviors-to-avoid"></a>Comportamenti da evitare

-   Applicazioni loquaci.

    Alcune applicazioni eseguono molte transazioni di piccole dimensioni. In combinazione con il sovraccarico di rete associato a ogni transazione di questo tipo, l'effetto viene moltiplicato. Nelle reti, le transazioni di piccole dimensioni possono utilizzare tutte le risorse e il tempo di transazioni di grandi dimensioni. Un approccio migliore consiste nel combinare molte piccole transazioni in un'unica transazione di grandi dimensioni.

-   Transazioni serializzate.

    La serializzazione delle transazioni non necessaria può comportare una riduzione delle prestazioni e influire sulla scalabilità. Ad esempio, 1000 transazioni serializzate accettano almeno 1000 \* RTT per il completamento. Un approccio migliore consiste nell'eseguire transazioni non correlate in parallelo. Quando le applicazioni serializzate vengono combinate con le applicazioni chattate, la velocità di risposta può essere gravemente ostacolata.

    > [!Note]  
    > La deserializzazione corretta di un'applicazione può essere difficile. Se il passaggio da serializzato a parallelo risulta troppo complesso, provare a combinare più transazioni in un minor numero di transazioni di grandi dimensioni.

     

-   Transazioni FAT.

    Le applicazioni che inviano byte superflui sulla rete sono considerate applicazioni FAT. Le applicazioni che inviano byte superflui sulla rete aumentano il sovraccarico della rete e le prestazioni sono ostacolate. Questa situazione deriva spesso da strutture di dati inefficienti o da flussi di dati inefficienti. Per risolvere questo problema, ottimizzare le strutture dei dati o prendere in considerazione l'utilizzo della compressione.

Le sezioni seguenti affrontano gli aspetti dello sviluppo di applicazioni da considerare.

-   [Problemi specifici di TCP/IP](tcp-ip-specific-issues-2.md)
-   [Riconoscimento di applicazioni lente](recognizing-slow-applications-2.md)
-   [Calcolo del sovraccarico con netstat](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni Windows Sockets a prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



