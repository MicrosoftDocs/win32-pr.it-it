---
description: Un altro aspetto dello sviluppo di applicazioni da considerare è la differenza di comportamento tra le operazioni locali o intracomputer e il comportamento quando le operazioni vengono eseguite tra due computer in rete.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportamento dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb09441eda4f0d909652ac38a9ca0596a1b4bce456f58c0e1eae1a7af7dc53b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121461"
---
# <a name="application-behavior"></a>Comportamento dell'applicazione

Un altro aspetto dello sviluppo di applicazioni da considerare è la differenza di comportamento tra le operazioni locali o intracomputer e il comportamento quando le operazioni vengono eseguite tra due computer in rete. Esistono comportamenti dell'applicazione che possono funzionare in modo affidabile in un computer locale, ma quando vengono eseguiti in una rete, causano una riduzione significativa delle prestazioni e l'utilizzo delle risorse. Quando si sviluppano applicazioni Windows Sockets, è consigliabile evitare i comportamenti dell'applicazione seguenti.

## <a name="behaviors-to-avoid"></a>Comportamenti da evitare

-   Applicazioni chatty.

    Alcune applicazioni eseguono molte transazioni di piccole dimensioni. In combinazione con l'overhead di rete associato a ogni transazione, l'effetto viene moltiplicato. In rete, le transazioni di piccole dimensioni possono utilizzare tutte le risorse e il tempo necessario per le transazioni di grandi dimensioni. Un approccio migliore consiste nel combinare molte transazioni di piccole dimensioni in una singola transazione di grandi dimensioni.

-   Transazioni serializzate.

    La serializzazione non necessaria delle transazioni può comportare prestazioni scarse e influire sulla scalabilità. Ad esempio, per il completamento di 1000 transazioni serializzate sono necessari almeno 1000 \* RTT. Un approccio migliore consiste nell'eseguire transazioni non correlate in parallelo. Quando le applicazioni serializzate vengono combinate con applicazioni chatty, la velocità di risposta può essere gravemente ostacolata.

    > [!Note]  
    > La deserializzazione corretta di un'applicazione può essere difficile. Se il passaggio da serializzato a parallelo risulta troppo difficile, provare a combinare più transazioni in meno transazioni di grandi dimensioni.

     

-   Transazioni fat.

    Le applicazioni che inviano byte non necessari in rete sono considerate applicazioni fat. Le applicazioni che inviano byte non necessari nella rete aumentano il sovraccarico di rete e le prestazioni sono ostacolate. Questa situazione deriva spesso da strutture di dati inefficienti o da flussi di dati inefficienti. Per risolvere questo problema, ottimizzare le strutture dei dati o prendere in considerazione l'uso della compressione.

Le sezioni seguenti illustrano gli aspetti dello sviluppo di applicazioni da considerare.

-   [Problemi specifici di TCP/IP](tcp-ip-specific-issues-2.md)
-   [Riconoscimento di applicazioni lente](recognizing-slow-applications-2.md)
-   [Calcolo dell'overhead con Netstat](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni socket Windows ad alte prestazioni](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



