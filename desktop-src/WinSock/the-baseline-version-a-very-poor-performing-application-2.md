---
description: Versione di base di un'applicazione con prestazioni molto scarse in Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'Versione di base: applicazione con prestazioni molto scarsa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313230"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a>Versione di base: applicazione con prestazioni molto scarsa

Di seguito è riportato l'esempio di codice iniziale, che consente di eseguire il calcolo degli aggiornamenti:

> [!Note]  
> Per semplicità, negli esempi seguenti non è disponibile alcuna gestione degli errori. Qualsiasi applicazione di produzione controlla sempre i valori restituiti.

 

> [!WARNING]
> I primi esempi dell'applicazione forniscono prestazioni intenzionalmente insoddisfacenti, per illustrare i miglioramenti delle prestazioni possibili con le modifiche al codice. Non usare questi esempi di codice nell'applicazione. sono solo a scopo illustrativo.

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



In questo stato, l'applicazione presenta le peggiori prestazioni di rete possibili. I problemi relativi a questa versione dell'applicazione di esempio includono:

-   L'applicazione è in chat. Ogni transazione è troppo piccola: le celle non devono essere aggiornate una alla volta.
-   Le transazioni vengono serializzate rigorosamente, anche se le celle potrebbero essere aggiornate contemporaneamente.
-   Il buffer di invio è impostato su zero e l'applicazione comporta un ritardo di 200 millisecondi per ogni invio, tre volte per cella.
-   L'applicazione è molto connessa, connettendosi una volta per ogni cella. Le applicazioni sono limitate al numero di connessioni al secondo per una determinata destinazione a causa dello stato di attesa del tempo, ma questo non è un problema, poiché ogni transazione impiega più di 600 millisecondi.
-   L'applicazione è FAT; molte transazioni non hanno alcun effetto sullo stato del server, perché molte celle non cambiano da Update a Update.
-   L'applicazione presenta un flusso scarso; i piccoli invii utilizzano una quantità elevata di CPU e RAM.
-   L'applicazione presuppone una rappresentazione little-endian per le relative invii. Si tratta di un presupposto naturale per la piattaforma Windows corrente, ma può essere pericoloso per il codice di lunga durata.

## <a name="key-performance-metrics"></a>Metriche delle prestazioni chiave

Le metriche delle prestazioni seguenti sono espresse in tempo di round trip (RTT), Goodput e sovraccarico del protocollo. Per una spiegazione di questi termini, vedere l'argomento [terminologia di rete](network-terminology-2.md) .

-   Tempo della cella, tempo di rete per un aggiornamento a cella singola, richiede 4 \* RTT + 600 millisecondi per Nagle e interazioni con ACK ritardati.
-   Goodput è inferiore a 6 byte.
-   Il sovraccarico del protocollo è pari al 99,6%.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologia di rete](network-terminology-2.md)
</dt> <dt>

[Revisione 1: pulizia dell'ovvia](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisione 2: riprogettazione per un minor numero di connessioni](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisione 3: invio blocco compresso](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Miglioramenti futuri](future-improvements-2.md)
</dt> </dl>

 

 



