---
description: In questa versione del programma di esempio, sono state apportate alcune modifiche ovvie che porteranno a un miglioramento delle prestazioni.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Revisione uno: pulizia ovvia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310445"
---
# <a name="revision-one-cleaning-up-the-obvious"></a>Revisione uno: pulizia ovvia

In questa versione del programma di esempio, sono state apportate alcune modifiche ovvie che porteranno a un miglioramento delle prestazioni. Questa versione del codice è distante da quella ottimizzata per le prestazioni, ma è un passaggio incrementale che consente di esaminare gli effetti degli approcci migliori in modo incrementale.

> [!WARNING]
> Questo esempio di applicazione fornisce prestazioni intenzionalmente insoddisfacenti, per illustrare i miglioramenti delle prestazioni possibili con le modifiche al codice. Non usare questo esempio di codice nell'applicazione. è solo a scopo illustrativo.

 


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



## <a name="changes-in-this-version"></a>Modifiche in questa versione

Questa versione riflette le modifiche seguenti:

-   Rimosso SNDBUF = 0. I ritardi 200 millisecondi causati da invii non memorizzati nel buffer e riconoscimenti ritardati vengono rimossi.
-   Rimosso il comportamento di trasmissione-invio-ricezione. Questa modifica elimina i ritardi di 200 millisecondi a causa delle interazioni Nagle e ACK ritardate.
-   È stato rimosso il presupposto little-endian. I byte sono ora in ordine.

## <a name="remaining-problems"></a>Problemi rimanenti

In questa versione, rimangono i seguenti problemi:

-   L'applicazione è ancora in stato di connessione pesante. Poiché i ritardi di 600 millisecondi vengono rimossi, l'applicazione raggiunge ora la velocità sostenuta di 12 connessioni al secondo. Molte connessioni simultanee ora diventano un problema.
-   L'applicazione è ancora grassa; le celle non modificate vengono comunque propagate al server.
-   L'applicazione presenta ancora un flusso scarso; gli invii da 3 byte sono ancora di piccole dimensioni.
-   L'applicazione invia ora 2 byte/RTT, che è uguale a 4 KB/s sull'Ethernet direttamente connessa. Questa operazione non è troppo veloce, ma il tempo di attesa potrebbe causare problemi.
-   L'overhead è inferiore al 99,3%, che non è ancora una percentuale di overhead corretta.

## <a name="key-performance-metrics"></a>Metriche delle prestazioni chiave

Le metriche delle prestazioni chiave seguenti sono espresse in tempo di round trip (RTT), Goodput e sovraccarico del protocollo. Per una spiegazione di questi termini, vedere l'argomento [terminologia di rete](network-terminology-2.md) .

Questa versione riflette le metriche delle prestazioni seguenti:

-   Tempo cella: 2 × RTT
-   Goodput-2 byte/RTT
-   Overhead del protocollo: 99.3 percent

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologia di rete](network-terminology-2.md)
</dt> <dt>

[Versione di base: applicazione con prestazioni molto scarsa](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisione 2: riprogettazione per un minor numero di connessioni](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisione 3: invio blocco compresso](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Miglioramenti futuri](future-improvements-2.md)
</dt> </dl>

 

 



