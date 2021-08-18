---
description: Informazioni su Filter Graph Manager
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Informazioni su Filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ce7c9c9af137853efba501cace7680b533c13994a559102fd08dc48efa2076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074865"
---
# <a name="about-the-filter-graph-manager"></a>Informazioni su Filter Graph Manager

[Filter Graph Manager è](filter-graph-manager.md) un oggetto COM che controlla i filtri in un grafico filtri. Esegue molte funzioni, tra cui le seguenti:

-   Coordinamento delle modifiche dello stato tra i filtri.
-   Definizione di un clock di riferimento.
-   Comunicazione degli eventi all'applicazione.
-   Fornire metodi per le applicazioni per compilare il grafico dei filtri.

Ognuna di queste funzioni è descritta brevemente qui. I dettagli sono disponibili altrove nella documentazione.

**Lo stato cambia**. Le modifiche di stato all'interno dei filtri devono verificarsi in un ordine specifico. Pertanto, l'applicazione non esegue comandi di modifica dello stato direttamente ai filtri. Assegna invece un singolo comando a Filter Graph Manager, che distribuisce il comando a ognuno dei filtri. La ricerca funziona in modo simile: l'applicazione assegna un comando seek a Filter Graph Manager, che lo distribuisce ai filtri.

**Orologio di riferimento**. Tutti i filtri nel grafico usano lo stesso clock, denominato *clock di riferimento.* L'orologio di riferimento garantisce che tutti i flussi siano sincronizzati. L'ora in cui deve essere eseguito il rendering di un fotogramma video o di un campione audio è denominata *ora di presentazione.* L'ora di presentazione viene misurata in relazione all'orologio di riferimento. Filter Graph Manager sceglie un orologio di riferimento, in genere l'orologio sulla scheda audio o l'orologio di sistema.

**Graph eventi .** Filter Graph Manager usa una coda di eventi per informare l'applicazione degli eventi che si verificano nel grafico dei filtri. Questo meccanismo è simile a un ciclo Windows di messaggi.

**Graph metodi di compilazione predefiniti**. Gestione filtri Graph fornisce metodi per l'applicazione per aggiungere filtri al grafo, connettere filtri ad altri filtri e disconnettere i filtri.

Una funzione non gestita da Filter Graph Manager è lo spostamento dei dati da un filtro a quello successivo. Questa operazione viene eseguita dai filtri stessi, tramite le connessioni pin. L'elaborazione avviene sempre in un thread separato.

> [!Note]  
> I filtri sono sempre a thread libero, risiedono nello stesso processo di Filter Graph Manager e vengono caricati dai server in-process. Di conseguenza, non viene effettuato il marshalling delle chiamate ai metodi tra i filtri o tra i filtri e gestione Graph filtri.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dati Flow nel filtro Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Impostazione dell Graph clock](setting-the-graph-clock.md)
</dt> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



