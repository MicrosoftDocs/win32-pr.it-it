---
description: La classe CDynamicOutputPin implementa un pin di output che supporta riconnessioni dinamiche e modifiche di formato.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: Classe CDynamicOutputPin (Amfilter.h)
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
ms.openlocfilehash: 6e0b8903f83c372aa85bd1c41fb12ce9065798d79dc4dbd940df926a395f8bc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871801"
---
# <a name="cdynamicoutputpin-class"></a>Classe CDynamicOutputPin

La `CDynamicOutputPin` classe implementa un pin di output che supporta riconnessioni dinamiche e modifiche di formato.

Questa classe deriva dalla [**classe CBaseOutputPin**](cbaseoutputpin.md) e implementa [**l'interfaccia IPinFlowControl.**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) Supporta diverse operazioni importanti per la creazione dinamica di grafi:

-   Riconnessione dinamica: il pin può disconnettersi e riconnettersi mentre il filtro è ancora attivo (in pausa o in esecuzione).
-   Modifica del formato dinamico: il pin può negoziare un nuovo tipo di supporto mentre il filtro è ancora attivo, senza riconnettersi.
-   Flow controllo: il filtro proprietario (o un'applicazione) può bloccare il flusso di dati dal pin senza arrestare il filtro.

Per altre informazioni, vedere [Dynamic Graph Building](dynamic-graph-building.md).

Il pin ha tre stati possibili: bloccato, sbloccato e in sospeso. Nello stato *in* sospeso, il pin è in attesa del completamento di un'operazione in un altro thread, prima che il pin passa allo stato bloccato. Mentre il pin è bloccato, il filtro non può recapitare i dati tramite il pin o modificare la connessione del pin.

Per coordinarsi tra più thread, il filtro proprietario deve seguire determinate regole. Per altre informazioni sui thread nel grafico dei filtri, vedere [Thread e sezioni critiche.](threads-and-critical-sections.md) Prima di tutto, il thread di streaming deve chiamare sempre il metodo [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) prima di chiamare uno dei metodi seguenti:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Successivamente, deve chiamare il [**metodo CDynamicOutputPin::StopUsingOutputPin.**](cdynamicoutputpin-stopusingoutputpin.md)

In secondo piano, il thread dell'applicazione non deve chiamare nessuno dei metodi nell'elenco precedente. In terzo piano, il thread di streaming non deve chiamare i metodi della classe che bloccano o sbloccano il pin. Questi metodi sono: [**CDynamicOutputPin::Block**](cdynamicoutputpin-block.md), [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md), [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)e [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md).

Queste regole assicurano che il thread dell'applicazione non possa bloccare il pin mentre il thread di streaming lo usa e viceversa. Dopo che il thread di streaming ha chiamato **StartUsingOutputPin,** il pin non si bloccherà fino a quando il thread di streaming non chiama **StopUsingOutputPin**. Al contrario, se il pin è bloccato, **StartUsingOutputPin** attende fino a quando il pin non viene sbloccato.

Per evitare di dimenticare di chiamare **StopUsingOutputPin,** è possibile usare la [**classe CAutoUsingOutputPin.**](cautousingoutputpin-cautousingoutputpin.md) Chiama **StopUsingOutputPin** automaticamente quando esce dall'ambito.

Quando il filtro proprietario unisce o lascia il grafo del filtro (nel relativo metodo [**IBaseFilter::JoinFilterGraph),**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) deve chiamare il metodo [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) del pin.



| Variabili membro protette                                                                      | Descrizione                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md)                                 | Sezione critica che protegge lo stato di blocco.                                                                            |
| [**m \_ hUnblockOutputPinEvent**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Evento segnalato quando il pin non è bloccato.                                                                           |
| [**m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Evento segnalato quando il pin si blocca correttamente o l'utente annulla un blocco in sospeso.                                 |
| [**m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)                                         | Stato di blocco.                                                                                                               |
| [**m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | Identificatore dell'ultimo thread che ha chiamato il [**metodo IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) su questo pin. |
| [**m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Numero di thread di streaming che usano questo pin.                                                                                   |
| [**m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)                                         | Evento segnalato quando il filtro si arresta o il pin scarica i dati.                                                         |
| [**m \_ pGraphConfig**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Puntatore [**all'interfaccia IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) per l'esecuzione di riconnessioni dinamiche.                           |
| [**m \_ bPinUsesReadOnlyAllocator**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Flag che specifica se i campioni dell'allocatore del pin sono di sola lettura.                                                   |
| Metodi protetti                                                                               | Descrizione                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Blocca il segnaposto. non restituisce finché il pin non viene bloccato.                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Blocca il segnaposto. potrebbe restituire prima che il pin venga bloccato.                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Sblocca il segnaposto.                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | Blocca il segnaposto.                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | Attende fino a quando non viene segnalato l'evento specificato.                                                                                  |
| Metodi pubblici                                                                                  | Descrizione                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Metodo del costruttore.                                                                                                           |
| [**~CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Metodo del distruttore.                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Specifica il [**puntatore IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e l'evento di arresto.                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | Richiede al pin di input connesso di avviare un'operazione di scaricamento.                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | Richiede al pin di input connesso di terminare un'operazione di scaricamento.                                                                    |
| [**Inattivo**](cdynamicoutputpin-inactive.md)                                                  | Notifica al pin che il filtro è stato arrestato.                                                                                 |
| [**Attivo**](cdynamicoutputpin-active.md)                                                      | Notifica al pin che il filtro è ora attivo.                                                                               |
| [**CompleteConnect**](cdynamicoutputpin-completeconnect.md)                                    | Completa una connessione a un pin di input. Virtuale.                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | Ottiene l'accesso al pin per un'operazione di streaming. Virtuale.                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Rilascia l'accesso al pin dopo un'operazione di streaming. Virtuale.                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Determina se un thread sta eseguendo un'operazione di streaming sul pin. Virtuale.                                        |
| [**ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)                              | Modifica dinamicamente il tipo di supporto per la connessione e recapita le informazioni sul nuovo segmento.                                  |
| [**ChangeMediaType**](cdynamicoutputpin-changemediatype.md)                                    | Modifica dinamicamente il tipo di supporto per la connessione.                                                                        |
| [**DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | Esegue una riconnessione dinamica con un nuovo tipo di supporto.                                                                        |
| Metodi IPin                                                                                    | Descrizione                                                                                                                   |
| [**Disconnetti**](cdynamicoutputpin-disconnect.md)                                              | Interrompe la connessione pin corrente.                                                                                            |
| Metodi IPinFlowControl                                                                         | Descrizione                                                                                                                   |
| [**Blocca**](cdynamicoutputpin-block.md)                                                        | Blocca o sblocca il flusso di dati dal segnaposto.                                                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




