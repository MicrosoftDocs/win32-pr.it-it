---
description: In questa versione dell'applicazione viene usato un blocco compresso di invio dei dati. Questa modifica comporta un miglioramento significativo delle prestazioni.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revisione tre: Compressed Block Send'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bba84010a09755c5b978665cbd8aa1b29068ec42294ab7b1e499c631fc6b472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121281"
---
# <a name="revision-three-compressed-block-send"></a>Revisione tre: Compressed Block Send

In questa versione dell'applicazione viene usato un blocco compresso di invio dei dati. Questa modifica comporta un miglioramento significativo delle prestazioni.


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



## <a name="changes-in-this-version"></a>Modifiche apportate a questa versione

Questa versione riflette le modifiche seguenti:

-   Gli aggiornamenti delle celle non vengono più serializzati.
-   Poiché viene usata un'invio a blocchi, l'applicazione non è più in chat.
-   Viene usata la compressione dei dati, con un'applicazione meno fat.

Esiste ancora un problema con questa versione dell'applicazione. il rischio di deadlock esiste perché viene usato un invio di grandi dimensioni senza ricevere. Il server invia un byte ogni 3 byte ricevuti. Ciò potrebbe causare un deadlock se le dimensioni del buffer di ricezione sono inferiori a 1000 byte per questa applicazione di esempio.

## <a name="key-performance-metrics"></a>Metriche delle prestazioni chiave

Le metriche delle prestazioni seguenti sono espresse in Tempo di round trip (RTT), Goodput e Sovraccarico del protocollo. Per una [spiegazione di questi termini,](network-terminology-2.md) vedere l'argomento Terminologia della rete.

Questa versione riflette le metriche delle prestazioni seguenti:

-   Ora cella - 0,002 \* RTT
-   Goodput : 2 kilobyte/RTT
-   Sovraccarico del protocollo: 14%

Del sovraccarico del 14%, il 6% deriva dalle intestazioni Ethernet e l'altro 8% deriva dall'avvio e dalla rimozione della connessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologia della rete](network-terminology-2.md)
</dt> <dt>

[Versione di base: un'applicazione con prestazioni molto scarse](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisione 1: Pulizia dell'ovvio](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisione 2: Riprogettazione per un minor numero di connessione](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Miglioramenti futuri](future-improvements-2.md)
</dt> </dl>

 

 



