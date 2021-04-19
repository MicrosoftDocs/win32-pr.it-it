---
description: La classe CDynamicOutputPin implementa un pin di output che supporta la riconnessione dinamica e le modifiche del formato.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: Classe CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c6dab41c122456076299df22bf90d886c905cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329858"
---
# <a name="cdynamicoutputpin-class"></a>Classe CDynamicOutputPin

La `CDynamicOutputPin` classe implementa un pin di output che supporta la riconnessione dinamica e le modifiche del formato.

Questa classe deriva dalla classe [**CBaseOutputPin**](cbaseoutputpin.md) e implementa l'interfaccia [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) . Supporta diverse operazioni importanti per la compilazione dinamica dei grafici:

-   Riconnessione dinamica: il pin può essere disconnesso e riconnesso mentre il filtro è ancora attivo (in pausa o in esecuzione).
-   Modifica del formato dinamico: il pin può negoziare un nuovo tipo di supporto mentre il filtro è ancora attivo, senza riconnettersi.
-   Controllo di flusso: il filtro proprietario (o un'applicazione) può bloccare il flusso di dati dal pin senza arrestare il filtro.

Per altre informazioni, vedere [creazione di grafici dinamici](dynamic-graph-building.md).

Il pin ha tre stati possibili: bloccato, sbloccato e in sospeso. Nello stato in *sospeso* , il PIN è in attesa del completamento di un'operazione in un altro thread, prima che il pin cambi nello stato bloccato. Quando il PIN è bloccato, il filtro non è in grado di recapitare i dati tramite il PIN o di modificare la connessione del PIN.

Per coordinare tra più thread, il filtro proprietario deve seguire determinate regole. Per ulteriori informazioni sui thread nel grafico dei filtri, vedere [thread e sezioni critiche](threads-and-critical-sections.md). Prima di tutto, il thread di streaming deve sempre chiamare il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) prima di chiamare uno dei metodi seguenti:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Successivamente, deve chiamare il metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) .

In secondo luogo, il thread dell'applicazione non deve chiamare alcun metodo nell'elenco precedente. Terzo, il thread di streaming non deve chiamare i metodi della classe che bloccano o sbloccano il PIN. Questi metodi sono: [**CDynamicOutputPin:: Block**](cdynamicoutputpin-block.md), [**CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md), [**CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)e [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md).

Queste regole assicurano che il thread dell'applicazione non possa bloccare il pin mentre il thread di streaming lo usa e viceversa. Dopo che il thread di streaming ha chiamato **StartUsingOutputPin**, il PIN non verrà bloccato fino a quando il thread di streaming non chiamerà **StopUsingOutputPin**. Viceversa, se il PIN è bloccato, **StartUsingOutputPin** attende fino a quando il PIN non viene sbloccato.

Per evitare di dimenticare di chiamare **StopUsingOutputPin**, è possibile usare la classe [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md) . Chiama **StopUsingOutputPin** automaticamente quando esce dall'ambito.

Quando il filtro proprietario si unisce o leaveds il grafico del filtro (nel metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) ), deve chiamare il metodo [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) del PIN.



| Variabili membro protette                                                                      | Descrizione                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**\_BlockStateLock m**](cdynamicoutputpin-m-blockstatelock.md)                                 | Sezione critica che protegge lo stato di blocco.                                                                            |
| [**\_hUnblockOutputPinEvent m**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Evento segnalato quando il PIN non è bloccato.                                                                           |
| [**\_hNotifyCallerPinBlockedEvent m**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Evento segnalato quando il pin si blocca correttamente oppure l'utente annulla un blocco in sospeso.                                 |
| [**\_BlockState m**](cdynamicoutputpin-m-blockstate.md)                                         | Stato di blocco.                                                                                                               |
| [**\_dwBlockCallerThreadID m**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | Identificatore del thread che ha chiamato per ultimo il metodo [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) su questo pin. |
| [**\_dwNumOutstandingOutputPinUsers m**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Numero di thread di streaming che usano questo pin.                                                                                   |
| [**\_hStopEvent m**](cdynamicoutputpin-m-hstopevent.md)                                         | Evento segnalato quando il filtro viene arrestato o il pin Scarica i dati.                                                         |
| [**\_pGraphConfig m**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Puntatore all'interfaccia [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) per l'esecuzione di riconnessioni dinamiche.                           |
| [**\_bPinUsesReadOnlyAllocator m**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Flag che specifica se i campioni dall'allocatore del pin sono di sola lettura.                                                   |
| Metodi protetti                                                                               | Descrizione                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Blocca il PIN. non restituisce alcun risultato finché il PIN non viene bloccato.                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Blocca il PIN. potrebbe restituire prima del blocco del PIN.                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Sblocca il PIN.                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | Blocca il PIN.                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | Attende che l'evento specificato venga segnalato.                                                                                  |
| Metodi pubblici                                                                                  | Descrizione                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Metodo del costruttore.                                                                                                           |
| [**~ CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Metodo del distruttore.                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Specifica il puntatore [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e l'evento Stop.                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | Richiede al pin di input connesso di iniziare un'operazione di svuotamento.                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | Richiede al pin di input connesso di terminare un'operazione di svuotamento.                                                                    |
| [**Inattivo**](cdynamicoutputpin-inactive.md)                                                  | Notifica al pin che il filtro è stato arrestato.                                                                                 |
| [**Attivo**](cdynamicoutputpin-active.md)                                                      | Notifica al pin che il filtro è ora attivo.                                                                               |
| [**CompleteConnect**](cdynamicoutputpin-completeconnect.md)                                    | Completa una connessione a un pin di input. Virtuale.                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | Ottiene l'accesso al pin per un'operazione di flusso. Virtuale.                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Rilascia l'accesso al pin dopo un'operazione di flusso. Virtuale.                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Determina se un thread sta eseguendo un'operazione di flusso sul pin. Virtuale.                                        |
| [**ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)                              | Modifica dinamicamente il tipo di supporto per la connessione e recapita nuove informazioni sul segmento.                                  |
| [**ChangeMediaType**](cdynamicoutputpin-changemediatype.md)                                    | Modifica dinamicamente il tipo di supporto per la connessione.                                                                        |
| [**DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | Esegue una riconnessione dinamica con un nuovo tipo di supporto.                                                                        |
| Metodi IPin                                                                                    | Descrizione                                                                                                                   |
| [**Disconnetti**](cdynamicoutputpin-disconnect.md)                                              | Interrompe la connessione al pin corrente.                                                                                            |
| Metodi IPinFlowControl                                                                         | Descrizione                                                                                                                   |
| [**Bloccato**](cdynamicoutputpin-block.md)                                                        | Blocca o Sblocca il flusso di dati dal pin.                                                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




