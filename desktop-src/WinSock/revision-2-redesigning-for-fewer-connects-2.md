---
description: In questa revisione, l'applicazione di esempio viene riprogettata per eliminare le connessioni non necessarie.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Revisione due: riprogettazione per un minor numero di connessioni'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131027"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a>Revisione due: riprogettazione per un minor numero di connessioni

In questa revisione, l'applicazione di esempio viene riprogettata per eliminare le connessioni non necessarie.

> [!WARNING]
> Questo esempio di applicazione fornisce anche prestazioni insoddisfacenti, per illustrare i miglioramenti delle prestazioni possibili con le modifiche al codice. Non usare questo esempio di codice nell'applicazione. è solo a scopo illustrativo.

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a>Problemi rimanenti

Le modifiche apportate alla revisione due hanno riprogettato l'applicazione per effettuare una sola connessione per ogni aggiornamento. L'applicazione include ancora i seguenti problemi di prestazioni:

-   L'applicazione è ancora serializzata e loquace.
-   L'applicazione ha ancora una progettazione Fat; sono presenti molti invii che non richiedono alcuna operazione in questa progettazione.
-   Gli invii sono ancora di 3 byte, che è un flusso insufficiente.

## <a name="key-performance-metrics"></a>Metriche delle prestazioni chiave

Le metriche delle prestazioni seguenti sono espresse in tempo di round trip (RTT), Goodput e sovraccarico del protocollo. Per una spiegazione di questi termini, vedere l'argomento [terminologia di rete](network-terminology-2.md) .

Questa versione riflette le metriche delle prestazioni seguenti:

-   Tempo cella: 1 \* RTT
-   Goodput-4 byte/RTT
-   Overhead del protocollo-96,8%

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

[Revisione 3: invio blocco compresso](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Miglioramenti futuri](future-improvements-2.md)
</dt> </dl>

 

 



