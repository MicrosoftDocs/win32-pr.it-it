---
description: In questa versione del programma di esempio sono state apportate alcune modifiche ovvie che incideranno inizialmente sul miglioramento delle prestazioni.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: "Revisione 1: Pulizia dell'ovvio"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5da015620727764d686a0c76649e23137de123099b978d323b94184d4df4bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111612"
---
# <a name="revision-one-cleaning-up-the-obvious"></a>Revisione 1: Pulizia dell'ovvio

In questa versione del programma di esempio sono state apportate alcune modifiche ovvie che incideranno inizialmente sul miglioramento delle prestazioni. Questa versione del codice è ben diversa dall'ottimizzazione delle prestazioni, ma è un buon passaggio incrementale che consente di esaminare gli effetti di approcci incrementalmente migliori.

> [!WARNING]
> Questo esempio dell'applicazione offre prestazioni intenzionalmente scarse, per illustrare i possibili miglioramenti delle prestazioni con le modifiche al codice. Non usare questo esempio di codice nell'applicazione. è solo a scopo illustrativo.

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a>Modifiche apportate a questa versione

Questa versione riflette le modifiche seguenti:

-   Rimozione di SNDBUF=0. I ritardi di 200 millisecondi dovuti a invii senza buffer e riconoscimenti ritardati vengono rimossi.
-   Rimozione del comportamento Send-Send-Receive. Questa modifica elimina i ritardi di 200 millisecondi dovuti a Nagle e alle interazioni ACK ritardate.
-   Rimozione del presupposto little-endian. I byte sono ora in ordine.

## <a name="remaining-problems"></a>Problemi rimanenti

In questa versione rimangono i problemi seguenti:

-   L'applicazione è ancora in grado di connettersi in modo pesante. Poiché vengono rimossi più di 600 millisecondi di ritardo, l'applicazione raggiunge ora la velocità sostenuta di 12 connessione al secondo. Molte connessioni simultanee ora diventano un problema.
-   L'applicazione è ancora fat; le celle non modificate vengono comunque propagate al server.
-   L'applicazione presenta ancora uno streaming non disponibile. Gli invii a 3 byte sono ancora di piccole dimensioni.
-   L'applicazione invia ora 2 byte/RTT, che equivale a 4 KB/s su Ethernet connessa direttamente. Questo non è troppo veloce, ma TIME-WAIT causerà probabilmente prima problemi.
-   Il sovraccarico scende al 99,3%, che non è ancora una percentuale di sovraccarico valida.

## <a name="key-performance-metrics"></a>Metriche delle prestazioni chiave

Le metriche delle prestazioni chiave seguenti sono espresse in tempo di round trip (RTT), goodput e sovraccarico del protocollo. Per una [spiegazione di questi termini,](network-terminology-2.md) vedere l'argomento Terminologia della rete.

Questa versione riflette le metriche delle prestazioni seguenti:

-   Cell Time—2×RTT
-   Goodput: 2 byte/RTT
-   Sovraccarico del protocollo: 99,3%

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologia della rete](network-terminology-2.md)
</dt> <dt>

[Versione di base: un'applicazione con prestazioni molto scarse](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisione 2: Riprogettazione per un minor numero di connessione](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisione 3: Invio a blocchi compresso](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Miglioramenti futuri](future-improvements-2.md)
</dt> </dl>

 

 



