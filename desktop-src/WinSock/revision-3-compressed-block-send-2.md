---
description: In questa versione dell'applicazione viene utilizzato un blocco di invio dei dati compresso. Questa modifica comporta un miglioramento significativo delle prestazioni.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revisione 3: invio blocco compresso'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310443"
---
# <a name="revision-three-compressed-block-send"></a>Revisione 3: invio blocco compresso

In questa versione dell'applicazione viene utilizzato un blocco di invio dei dati compresso. Questa modifica comporta un miglioramento significativo delle prestazioni.


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a>Modifiche in questa versione

Questa versione riflette le modifiche seguenti:

-   Gli aggiornamenti delle celle non vengono più serializzati.
-   Poiché viene utilizzato un blocco Send, l'applicazione non è più in chat.
-   Viene utilizzata la compressione dei dati, causando un'applicazione meno FAT.

Si è verificato un problema con questa versione dell'applicazione. il rischio di deadlock esiste poiché viene utilizzata un'invio di grandi dimensioni con nessuna ricezione. Il server invia un byte per ogni 3 byte ricevuti. Questo potrebbe causare un deadlock se la dimensione del buffer di ricezione è inferiore a 1000 byte per questa applicazione di esempio.

## <a name="key-performance-metrics"></a>Metriche delle prestazioni chiave

Le metriche delle prestazioni seguenti sono espresse in tempo di round trip (RTT), Goodput e sovraccarico del protocollo. Per una spiegazione di questi termini, vedere l'argomento [terminologia di rete](network-terminology-2.md) .

Questa versione riflette le metriche delle prestazioni seguenti:

-   Tempo cella-. 002 \* RTT
-   Goodput-2 kilobyte/RTT
-   Overhead del protocollo: 14%

Del 14% di overhead, il 6% è dalle intestazioni Ethernet e l'altro l'8% viene dall'avvio della connessione e da teardown.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologia di rete](network-terminology-2.md)
</dt> <dt>

[Versione di base: applicazione con prestazioni molto scarsa](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisione 1: pulizia dell'ovvia](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisione 2: riprogettazione per un minor numero di connessioni](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Miglioramenti futuri](future-improvements-2.md)
</dt> </dl>

 

 



