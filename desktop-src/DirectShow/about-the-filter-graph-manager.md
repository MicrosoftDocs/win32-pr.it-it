---
description: Informazioni su Filter Graph Manager
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Informazioni su Filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522241"
---
# <a name="about-the-filter-graph-manager"></a>Informazioni su Filter Graph Manager

[Filter Graph Manager](filter-graph-manager.md) è un oggetto com che controlla i filtri in un grafico a filtro. Esegue numerose funzioni, incluse le seguenti:

-   Coordinamento dei cambiamenti di stato tra i filtri.
-   Creazione di un orologio di riferimento.
-   Comunicazione degli eventi di nuovo all'applicazione.
-   Metodi che consentono alle applicazioni di compilare il grafico dei filtri.

Ognuna di queste funzioni è descritta brevemente qui. I dettagli sono disponibili altrove nella documentazione.

**Modifiche dello stato**. Le modifiche di stato all'interno dei filtri devono essere eseguite in un ordine specifico. Pertanto, l'applicazione non rilascia i comandi di modifica dello stato direttamente ai filtri. Al contrario, fornisce un unico comando al gestore del grafo del filtro, che distribuisce il comando a ognuno dei filtri. La ricerca funziona in modo analogo: l'applicazione fornisce un comando seek a Filter Graph Manager, che lo distribuisce ai filtri.

**Clock di riferimento**. Tutti i filtri nel grafico utilizzano lo stesso clock, denominato *clock di riferimento*. L'orologio di riferimento garantisce che tutti i flussi siano sincronizzati. L'ora in cui deve essere eseguito il rendering di un frame video o di un campione audio è denominata *ora presentazione*. Il tempo di presentazione viene misurato in relazione all'orologio di riferimento. Il gestore del grafico del filtro sceglie un orologio di riferimento, in genere l'orologio sulla scheda audio o il clock di sistema.

**Eventi Graph**. Filter Graph Manager usa una coda degli eventi per informare l'applicazione degli eventi che si verificano nel grafico dei filtri. Questo meccanismo è simile a un ciclo di messaggi di Windows.

**Metodi di creazione di grafici**. Filter Graph Manager fornisce metodi che consentono all'applicazione di aggiungere filtri al grafo, connettere filtri ad altri filtri e disconnettere i filtri.

Una funzione non gestita dal gestore del grafo del filtro è lo stato di trasferimento dei dati da un filtro a quello successivo. Questa operazione viene eseguita dai filtri, tramite le connessioni pin. L'elaborazione avviene sempre in un thread separato.

> [!Note]  
> I filtri sono sempre a thread libero, risiedono nello stesso processo di gestione del grafo dei filtri e vengono caricati dai server in-process. Pertanto, le chiamate al metodo non vengono sottoposte a marshalling tra i filtri o tra i filtri e il gestore del grafo del filtro.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Impostazione del clock del grafico](setting-the-graph-clock.md)
</dt> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



