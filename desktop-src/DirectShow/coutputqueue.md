---
description: La classe COutputQueue implementa una coda per fornire esempi di contenuti multimediali.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: Classe COutputQueue (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd6167402abd36db8f436f6e27b18213642f010b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328941"
---
# <a name="coutputqueue-class"></a>Classe COutputQueue

![coutputqueue](images/oput01.png)

La `COutputQueue` classe implementa una coda per fornire esempi di contenuti multimediali.

Questa classe consente a un pin di output di recapitare esempi in modo asincrono. Gli esempi vengono inseriti in una coda e un thread di lavoro li recapita al pin di input. La coda può inoltre conservare messaggi di controllo che indicano un nuovo segmento, una notifica di fine flusso o un'operazione di scaricamento.

Per usare questa classe, creare un oggetto **COutputQueue** per ogni pin di output sul filtro. Nel metodo del costruttore specificare il pin di input connesso al pin di output. Utilizzando questa classe, il pin di output non chiama i metodi direttamente sul pin di input. Al contrario, chiama i metodi corrispondenti in `COutputQueue` , come illustrato nella tabella seguente.



| Metodo PIN                                                            | Metodo COutputQueue                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**BeginFlush**](coutputqueue-beginflush.md)           |
| [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**EndFlush**](coutputqueue-endflush.md)               |
| [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**EOS**](coutputqueue-eos.md)                         |
| [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**NewSegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Ricevere**](coutputqueue-receive.md)                 |
| [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

Facoltativamente, è possibile configurare l' `COutputQueue` oggetto per recapitare in modo sincrono gli esempi, senza un thread di lavoro. L'oggetto può anche decidere in fase di esecuzione se usare un thread di lavoro, in base alle caratteristiche del PIN di input. Per ulteriori informazioni, vedere [**COutputQueue:: COutputQueue**](coutputqueue-coutputqueue.md).



| Variabili membro protette                                   | Descrizione                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**\_pPin m**](coutputqueue-m-ppin.md)                       | Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input.                                               |
| [**\_pInputPin m**](coutputqueue-m-pinputpin.md)             | Puntatore all'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del PIN di input.                               |
| [**\_bBatchExact m**](coutputqueue-m-bbatchexact.md)         | Flag che specifica se l'oggetto recapita esempi in batch esatti.                                |
| [**\_lBatchSize m**](coutputqueue-m-lbatchsize.md)           | Dimensioni batch.                                                                                              |
| [**\_elenco m**](coutputqueue-m-list.md)                       | Coda di esempio multimediale.                                                                                      |
| [**\_hSem m**](coutputqueue-m-hsem.md)                       | Handle per un semaforo, utilizzato dal thread per attendere gli esempi.                                           |
| [**\_evFlushComplete m**](coutputqueue-m-evflushcomplete.md) | Evento che segnala al termine di un'operazione di svuotamento.                                                  |
| [**\_hThread m**](coutputqueue-m-hthread.md)                 | Handle per il thread di lavoro.                                                                             |
| [**\_ppSamples m**](coutputqueue-m-ppsamples.md)             | Matrice di campioni di dimensioni [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).               |
| [**\_nBatched m**](coutputqueue-m-nbatched.md)               | Numero di campioni attualmente in batch e in attesa di elaborazione.                                             |
| [**\_lWaiting m**](coutputqueue-m-lwaiting.md)               | Flag che ha un valore diverso da zero quando il thread è in attesa di un campione.                                   |
| [**\_bFlushing m**](coutputqueue-m-bflushing.md)             | Flag che specifica se l'oggetto sta eseguendo un'operazione di svuotamento.                                  |
| [**\_bTerminate m**](coutputqueue-m-bterminate.md)           | Flag che specifica se il thread deve terminare.                                                 |
| [**\_bSendAnyway m**](coutputqueue-m-bsendanyway.md)         | Flag per l'override dell'elaborazione batch.                                                                       |
| [**m \_ HR**](coutputqueue-m-hr.md)                           | Valore **HRESULT** che indica se l'oggetto accetterà esempi.                                 |
| [**\_hEventPop m**](coutputqueue-m-heventpop.md)             | Evento che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda.                              |
| Metodi protetti                                            | Descrizione                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | Chiama il metodo [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) quando viene creato il thread. |
| [**ThreadProc**](coutputqueue-threadproc.md)                | Recupera gli esempi dalla coda e li recapita al pin di input.                                     |
| [**IsQueued**](coutputqueue-isqueued.md)                    | Determina se l'oggetto utilizza un thread di lavoro per recapitare esempi.                               |
| [**QueueSample**](coutputqueue-queuesample.md)              | Accoda un esempio di supporto o un messaggio di controllo.                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | Determina se i dati in coda sono un messaggio di controllo.                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | Libera tutti gli esempi in sospeso.                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | Notifica al thread che la coda contiene dati.                                                        |
| Metodi pubblici                                               | Descrizione                                                                                              |
| [**COutputQueue**](coutputqueue-coutputqueue.md)            | Metodo del costruttore.                                                                                      |
| [**~ COutputQueue**](coutputqueue--coutputqueue.md)          | Metodo del distruttore.                                                                                       |
| [**BeginFlush**](coutputqueue-beginflush.md)                | Avvia un'operazione di svuotamento.                                                                                |
| [**EndFlush**](coutputqueue-endflush.md)                    | Termina un'operazione di svuotamento.                                                                                  |
| [**EOS**](coutputqueue-eos.md)                              | Recapita una chiamata di fine flusso al pin di input.                                                         |
| [**SendAnyway**](coutputqueue-sendanyway.md)                | Recapita tutti gli esempi in sospeso.                                                                            |
| [**NewSegment**](coutputqueue-newsegment.md)                | Recapita un nuovo segmento al pin di input.                                                                 |
| [**Ricevere**](coutputqueue-receive.md)                      | Recapita un campione multimediale al pin di input.                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | Recapita un batch di esempi di supporti al pin di input.                                                      |
| [**Reset**](coutputqueue-reset.md)                          | Reimposta l'oggetto in modo che possa ricevere più dati.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Determina se l'oggetto è in attesa di dati.                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | Specifica un evento che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda.                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




