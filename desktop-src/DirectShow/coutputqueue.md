---
description: La classe COutputQueue implementa una coda per distribuire esempi multimediali.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: Classe COutputQueue (Outputq.h)
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
ms.openlocfilehash: 8911c7261af0bf2e140a551b0146b7764cd541368898e6d3905f5dee2eaa4c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813437"
---
# <a name="coutputqueue-class"></a>Classe COutputQueue

![coutputqueue](images/oput01.png)

La `COutputQueue` classe implementa una coda per distribuire campioni multimediali.

Questa classe consente a un pin di output di distribuire esempi in modo asincrono. Gli esempi vengono inseriti in una coda e un thread di lavoro li recapita al pin di input. La coda può anche contenere messaggi di controllo che indicano un nuovo segmento, una notifica di fine flusso o un'operazione di scaricamento.

Per usare questa classe, creare un **oggetto COutputQueue** per ogni pin di output nel filtro. Nel metodo del costruttore specificare il pin di input connesso a tale pin di output. Usando questa classe, il pin di output non chiama i metodi direttamente sul pin di input. Chiama invece i metodi corrispondenti in `COutputQueue` , come illustrato nella tabella seguente.



| Metodo Pin                                                            | Metodo COutputQueue                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**BeginFlush**](coutputqueue-beginflush.md)           |
| [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**EndFlush**](coutputqueue-endflush.md)               |
| [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**Eos**](coutputqueue-eos.md)                         |
| [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**NewSegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Ricevere**](coutputqueue-receive.md)                 |
| [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

Facoltativamente, è possibile configurare `COutputQueue` l'oggetto per distribuire gli esempi in modo sincrono, senza un thread di lavoro. L'oggetto può anche decidere in fase di esecuzione se usare un thread di lavoro, in base alle caratteristiche del pin di input. Per altre informazioni, vedere [**COutputQueue::COutputQueue.**](coutputqueue-coutputqueue.md)



| Variabili membro protette                                   | Descrizione                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**m \_ pPin**](coutputqueue-m-ppin.md)                       | Puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di input.                                               |
| [**m \_ pInputPin**](coutputqueue-m-pinputpin.md)             | Puntatore all'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del pin di input.                               |
| [**m \_ bBatchExact**](coutputqueue-m-bbatchexact.md)         | Flag che specifica se l'oggetto fornisce campioni in batch esatti.                                |
| [**m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)           | Dimensioni batch.                                                                                              |
| [**m \_ List**](coutputqueue-m-list.md)                       | Coda di esempio multimediale.                                                                                      |
| [**m \_ hSem**](coutputqueue-m-hsem.md)                       | Handle a un semaforo, usato dal thread per attendere i campioni.                                           |
| [**m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) | Evento che segnala il termine di un'operazione di scaricamento.                                                  |
| [**m \_ hThread**](coutputqueue-m-hthread.md)                 | Handle per il thread di lavoro.                                                                             |
| [**m \_ ppSamples**](coutputqueue-m-ppsamples.md)             | Matrice di esempi di dimensioni [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).               |
| [**m \_ nBatched**](coutputqueue-m-nbatched.md)               | Numero di campioni attualmente in batch e in attesa di elaborazione.                                             |
| [**m \_ lWaiting**](coutputqueue-m-lwaiting.md)               | Flag con un valore diverso da zero quando il thread è in attesa di un campione.                                   |
| [**m \_ bFlushing**](coutputqueue-m-bflushing.md)             | Flag che specifica se l'oggetto sta eseguendo un'operazione di scaricamento.                                  |
| [**m \_ bTerminate**](coutputqueue-m-bterminate.md)           | Flag che specifica se il thread deve terminare.                                                 |
| [**m \_ bSendAnyway**](coutputqueue-m-bsendanyway.md)         | Flag per eseguire l'override dell'elaborazione batch.                                                                       |
| [**m \_ hr**](coutputqueue-m-hr.md)                           | **Valore HRESULT** che indica se l'oggetto accetterà esempi.                                 |
| [**m \_ hEventPop**](coutputqueue-m-heventpop.md)             | Evento segnalato ogni volta che l'oggetto rimuove un campione dalla coda.                              |
| Metodi protetti                                            | Descrizione                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | Chiama il [**metodo COutputQueue::ThreadProc**](coutputqueue-threadproc.md) quando viene creato il thread. |
| [**Threadproc**](coutputqueue-threadproc.md)                | Recupera gli esempi dalla coda e li recapita al pin di input.                                     |
| [**IsQueued**](coutputqueue-isqueued.md)                    | Determina se l'oggetto usa un thread di lavoro per recapitare i campioni.                               |
| [**Esempio di coda**](coutputqueue-queuesample.md)              | Accoda un campione multimediale o un messaggio di controllo.                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | Determina se i dati in coda sono messaggi di controllo.                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | Libera tutti gli esempi in sospeso.                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | Notifica al thread che la coda contiene dati.                                                        |
| Metodi pubblici                                               | Descrizione                                                                                              |
| [**COutputQueue**](coutputqueue-coutputqueue.md)            | Metodo del costruttore.                                                                                      |
| [**~COutputQueue**](coutputqueue--coutputqueue.md)          | Metodo del distruttore.                                                                                       |
| [**BeginFlush**](coutputqueue-beginflush.md)                | Avvia un'operazione di scaricamento.                                                                                |
| [**EndFlush**](coutputqueue-endflush.md)                    | Termina un'operazione di scaricamento.                                                                                  |
| [**Eos**](coutputqueue-eos.md)                              | Recapita una chiamata di fine flusso al pin di input.                                                         |
| [**Invia comunque**](coutputqueue-sendanyway.md)                | Recapita eventuali campioni in sospeso.                                                                            |
| [**NewSegment**](coutputqueue-newsegment.md)                | Recapita un nuovo segmento al pin di input.                                                                 |
| [**Ricevere**](coutputqueue-receive.md)                      | Recapita un campione multimediale al pin di input.                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | Recapita un batch di campioni di supporti al pin di input.                                                      |
| [**Reset**](coutputqueue-reset.md)                          | Reimposta l'oggetto in modo che possa ricevere più dati.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Determina se l'oggetto è in attesa di dati.                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | Specifica un evento segnalato ogni volta che l'oggetto rimuove un campione dalla coda.                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




