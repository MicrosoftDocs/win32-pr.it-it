---
description: La classe CBaseRenderer è una classe di base per l'implementazione di filtri renderer.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: Classe CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e30bae52cf5a7eba642354d002173291cb7d38b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326572"
---
# <a name="cbaserenderer-class"></a>Classe CBaseRenderer

![gerarchia di classi cbaserenderer](images/rbase02.png)

La `CBaseRenderer` classe è una classe di base per l'implementazione di filtri renderer. Supporta un pin di input, implementato dalla classe [**CRendererInputPin**](crendererinputpin.md) . Per usare questa classe, dichiarare una classe derivata che eredita `CBaseRenderer` . Come minimo, la classe derivata deve implementare i metodi seguenti, che vengono dichiarati come virtuali puri nella classe di base:

-   [**CBaseRenderer:: CheckMediaType**](cbaserenderer-checkmediatype.md): accetta o rifiuta i tipi di supporto proposti. Questo metodo viene chiamato dal filtro durante il processo di connessione del PIN.
-   [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md): esegue il rendering di un campione. Il filtro chiama questo metodo per ogni campione ricevuto durante l'esecuzione.

La classe base gestisce le modifiche di stato e i problemi di sincronizzazione. Pianifica anche gli esempi per il rendering, anche se non implementa misure di controllo della qualità. La classe base dichiara anche diversi metodi "handler". Si tratta di metodi che il filtro chiama in punti specifici del processo di streaming. Non eseguono alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override. Nella tabella seguente vengono elencati sotto l'intestazione metodi pubblici: gestori.

Il gestore [**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) merita menzione speciale. Il filtro chiama questo metodo se riceve un campione mentre il filtro è sospeso. Ciò può verificarsi se il grafico passa da interrotto a sospeso o se il grafico viene cercato mentre è in pausa. I renderer video usano in genere l'esempio per visualizzare un frame ancora. Quando il filtro passa da sospeso a in esecuzione, invia lo stesso campione al metodo [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md) , come primo campione nel flusso.

La `CBaseRenderer` classe espone le interfacce **IMediaSeeking** e **IMediaPosition** tramite l'oggetto [**CRendererPosPassThru**](crendererpospassthru.md) . Passa tutte le richieste Seek al filtro successivo upstream.

## <a name="scheduling"></a>Pianificazione

Quando il filtro upstream chiama il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN di input per recapitare un campione, il pin passa questa chiamata al metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) del filtro. Il filtro rimuove l'esempio, ne esegue il rendering immediatamente o lo pianifica per il rendering.

Se l'esempio non dispone di timestamp o se non è disponibile alcun clock di riferimento, il filtro esegue immediatamente il rendering dell'esempio. In caso contrario, il filtro chiama il metodo [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) per determinare le operazioni da eseguire. Per impostazione predefinita, l'esempio è pianificato in base ai timestamp. La classe derivata può eseguire l'override di **ShouldDrawSampleNow** per supportare il controllo qualità.

Per pianificare un esempio, il filtro chiama il metodo [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) , che crea una richiesta di notifica. Il metodo [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) si blocca quindi fino all'ora pianificata o fino a quando il filtro non modifica lo stato. Il blocco impedisce al filtro upstream di consegnare più campioni fino a quando non viene eseguito il rendering dell'esempio corrente.

Quando il filtro upstream chiama il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) per segnalare la fine del flusso, il filtro Invia un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri. Il filtro attende l'ora di arresto dell'esempio corrente prima di inviare l'evento.



| Variabili membro protette                                                   | Descrizione                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_bAbort m**](cbaserenderer-m-babort.md)                                  | Flag che indica se arrestare il rendering e rifiutare ulteriori esempi.                                                               |
| [**n. \_ bEOS**](cbaserenderer-m-beos.md)                                      | Flag che indica se è stata raggiunta la fine del flusso.                                                                                  |
| [**\_bEOSDelivered m**](cbaserenderer-m-beosdelivered.md)                    | Flag che indica se il filtro ha inviato l' \_ evento di completamento EC.                                                               |
| [**\_bInReceive m**](cbaserenderer-m-binreceive.md)                          | Flag che indica se il filtro sta elaborando una chiamata di **ricezione** .                                                                |
| [**\_bRepaintStatus m**](cbaserenderer-m-brepaintstatus.md)                  | Flag che Abilita o Disabilita gli eventi di ridisegno.                                                                                           |
| [**\_bStreaming m**](cbaserenderer-m-bstreaming.md)                          | Flag che indica se il filtro esegue il flusso di dati.                                                                               |
| [**\_dwAdvise m**](cbaserenderer-m-dwadvise.md)                              | Identificatore dell'evento timer che pianifica il rendering.                                                                                 |
| [**\_EndOfStreamTimer m**](cbaserenderer-m-endofstreamtimer.md)              | Timer-identificatore evento, per la pianificazione delle \_ notifiche complete EC.                                                                      |
| [**\_evComplete m**](cbaserenderer-m-evcomplete.md)                          | Evento segnalato al completamento di una transizione di stato.                                                                             |
| [**\_InterfaceLock m**](cbaserenderer-m-interfacelock.md)                    | Blocco dello stato filtro.                                                                                                                      |
| [**\_ObjectCreationLock m**](cbaserenderer-m-objectcreationlock.md)          | Blocco per proteggere la creazione di oggetti all'interno del filtro.                                                                              |
| [**\_pInputPin m**](cbaserenderer-m-pinputpin.md)                            | Puntatore al pin di input del filtro.                                                                                                      |
| [**\_pMediaSample m**](cbaserenderer-m-pmediasample.md)                      | Puntatore all'esempio multimediale corrente.                                                                                                    |
| [**\_pPosition m**](cbaserenderer-m-pposition.md)                            | Oggetto helper per passare i comandi Seek upstream.                                                                                           |
| [**\_pQSink m**](cbaserenderer-m-pqsink.md)                                  | Puntatore all'oggetto che riceve i messaggi di controllo qualità.                                                                           |
| [**\_RendererLock m**](cbaserenderer-m-rendererlock.md)                      | Blocco di streaming.                                                                                                                         |
| [**\_RenderEvent m**](cbaserenderer-m-renderevent.md)                        | Evento utilizzato per pianificare il rendering.                                                                                                       |
| [**\_SignalTime m**](cbaserenderer-m-signaltime.md)                          | Ora di arresto dell'esempio corrente.                                                                                                        |
| [**\_ThreadSignal m**](cbaserenderer-m-threadsignal.md)                      | Evento usato per rilasciare il thread di streaming.                                                                                             |
| Metodi pubblici                                                               | Descrizione                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | Annulla l'evento del timer che pianifica il rendering. Virtuale.                                                                              |
| [**CBaseRenderer**](cbaserenderer-cbaserenderer.md)                         | Metodo del costruttore.                                                                                                                     |
| [**~ CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | Metodo del distruttore.                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | Recupera i puntatori dell'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro. Virtuale. |
| [**GetPin**](cbaserenderer-getpin.md)                                       | Recupera un PIN. Virtuale.                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | Recupera il numero di pin. Virtuale.                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | Recupera i timestamp da un campione. Virtuale.                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | Invia un evento di [**\_ \_ modifica della visualizzazione EC**](ec-display-changed.md) al gestore del grafico dei filtri.                                          |
| [**PrepareReceive**](cbaserenderer-preparereceive.md)                       | Prepara il rendering di un campione. Virtuale.                                                                                                   |
| [**Ricevere**](cbaserenderer-receive.md)                                     | Riceve il campione multimediale successivo nel flusso. Virtuale.                                                                                  |
| [**Rendering**](cbaserenderer-render.md)                                       | Esegue il rendering di un esempio. Virtuale.                                                                                                              |
| [**ScheduleSample**](cbaserenderer-schedulesample.md)                       | Pianifica un esempio per il rendering. Virtuale.                                                                                              |
| [**SendNotifyWindow**](cbaserenderer-sendnotifywindow.md)                   | Notifica al filtro upstream l'handle della finestra video.                                                                                |
| [**SendRepaint**](cbaserenderer-sendrepaint.md)                             | Invia un evento Repaint al gestore del grafico dei filtri.                                                                                      |
| [**SetMediaType**](cbaserenderer-setmediatype.md)                           | Chiamato quando viene impostato il tipo di supporto del PIN. Virtuale.                                                                                       |
| [**SignalTimerFired**](cbaserenderer-signaltimerfired.md)                   | Cancella l'identificatore del timer utilizzato per pianificare il rendering.                                                                                 |
| [**SourceThreadCanWait**](cbaserenderer-sourcethreadcanwait.md)             | Include o rilascia il thread di streaming. Virtuale.                                                                                        |
| [**WaitForReceiveToComplete**](cbaserenderer-waitforreceivetocomplete.md)   | Attende il completamento del metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) .                                               |
| [**WaitForRenderTime**](cbaserenderer-waitforrendertime.md)                 | Attende l'ora di presentazione dell'esempio corrente. Virtuale.                                                                              |
| Metodi pubblici: metodi della funzione di accesso                                             | Descrizione                                                                                                                             |
| [**ClearPendingSample**](cbaserenderer-clearpendingsample.md)               | Rilascia l'esempio corrente. Virtuale.                                                                                                   |
| [**GetCurrentSample**](cbaserenderer-getcurrentsample.md)                   | Recupera l'esempio corrente. Virtuale.                                                                                                  |
| [**GetRealState**](cbaserenderer-getrealstate.md)                           | Recupera lo stato del filtro.                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | Recupera l'evento che pianifica il rendering.                                                                                           |
| [**HaveCurrentSample**](cbaserenderer-havecurrentsample.md)                 | Determina se il filtro dispone di un campione. Virtuale.                                                                                    |
| [**IsEndOfStream**](cbaserenderer-isendofstream.md)                         | Esegue una query se è stata ricevuta la notifica di fine del flusso.                                                                            |
| [**IsEndOfStreamDelivered**](cbaserenderer-isendofstreamdelivered.md)       | Esegue una query che indica se l' \_ evento di completamento EC è stato recapitato al gestore del grafico dei filtri.                                                  |
| [**Flusso**](cbaserenderer-isstreaming.md)                             | Esegue una query sull'eventuale flusso di dati del filtro.                                                                                           |
| [**SetAbortSignal**](cbaserenderer-setabortsignal.md)                       | Imposta un flag che indica se arrestare il rendering e rifiutare ulteriori esempi.                                                       |
| [**SetRepaintStatus**](cbaserenderer-setrepaintstatus.md)                   | Abilita o Disabilita gli eventi di ridisegno.                                                                                                     |
| Metodi pubblici: metodi di State-Change                                         | Descrizione                                                                                                                             |
| [**Attivo**](cbaserenderer-active.md)                                       | Chiamato quando lo stato viene impostato su in pausa o in esecuzione. Virtuale.                                                                        |
| [**BeginFlush**](cbaserenderer-beginflush.md)                               | Avvia un'operazione di svuotamento. Virtuale.                                                                                                      |
| [**BreakConnect**](cbaserenderer-breakconnect.md)                           | Rilascia il pin di input da una connessione. Virtuale.                                                                                      |
| [**CheckReady**](cbaserenderer-checkready.md)                               | Esegue una query per determinare se una transizione di stato è stata completata.                                                                                         |
| [**CompleteConnect**](cbaserenderer-completeconnect.md)                     | Completa la connessione del PIN di input a un altro pin. Virtuale.                                                                           |
| [**CompleteStateChange**](cbaserenderer-completestatechange.md)             | Determina se una transizione allo stato di sospensione è stata completata. Virtuale.                                                               |
| [**EndFlush**](cbaserenderer-endflush.md)                                   | Termina un'operazione di svuotamento. Virtuale.                                                                                                        |
| [**Inattivo**](cbaserenderer-inactive.md)                                   | Chiamato quando lo stato viene impostato come arrestato. Virtuale.                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | Segnala che una transizione di stato non è ancora completa.                                                                                    |
| [**Ready**](cbaserenderer-ready.md)                                         | Segnala che una transizione di stato è stata completata.                                                                                            |
| [**StartStreaming**](cbaserenderer-startstreaming.md)                       | Avvia il flusso quando il filtro passa a uno stato di esecuzione. Virtuale.                                                               |
| [**StopStreaming**](cbaserenderer-stopstreaming.md)                         | Interrompe lo streaming quando il filtro si spegne dallo stato di esecuzione. Virtuale.                                                             |
| Metodi pubblici: metodi di fine del flusso                                        | Descrizione                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | Notifica al filtro che il pin di input ha ricevuto una notifica di fine del flusso. Virtuale.                                                 |
| [**NotifyEndOfStream**](cbaserenderer-notifyendofstream.md)                 | Invia un evento di [**\_ completamento EC**](ec-complete.md) al gestore del grafico dei filtri.                                                         |
| [**ResetEndOfStream**](cbaserenderer-resetendofstream.md)                   | Reimposta i flag di fine del flusso.                                                                                                         |
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | Annulla il timer che pianifica le \_ notifiche complete di EC. Virtuale.                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | Se è stata raggiunta la fine del flusso, pianifica un \_ evento di completamento EC per il gestore del grafico dei filtri. Virtuale.                                    |
| [**TimerCallback**](cbaserenderer-timercallback.md)                         | Metodo di callback per l'evento timer di fine del flusso.                                                                                      |
| Metodi pubblici: gestori                                                     | Descrizione                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | Chiamato quando il filtro riceve un campione mentre è sospeso. Virtuale.                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | Chiamato dopo il rendering di un campione. Virtuale.                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | Chiamato quando sta per iniziare il rendering. Virtuale.                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | Chiamato quando il filtro inizia il flusso. Virtuale.                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | Chiamato quando il filtro interrompe il flusso. Virtuale.                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | Chiamato quando il filtro viene eseguito in attesa dell'ora di presentazione di un campione. Virtuale.                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | Chiamato quando il filtro inizia ad attendere l'ora di presentazione di un campione. Virtuale.                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | Chiamato prima che il filtro esegua il rendering di un campione. Virtuale.                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | Determina il modo in cui un campione viene pianificato per il rendering. Virtuale.                                                                            |
| Metodi virtuali puri                                                         | Descrizione                                                                                                                             |
| [**CheckMediaType**](cbaserenderer-checkmediatype.md)                       | Determina se il filtro accetta un tipo di supporto specifico.                                                                                 |
| [**DoRenderSample**](cbaserenderer-dorendersample.md)                       | Esegue il rendering di un esempio.                                                                                                                       |
| Metodi IMediaFilter                                                         | Descrizione                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | Recupera lo stato del filtro (in esecuzione, arrestato o sospeso).                                                                             |
| [**Sospendere**](cbaserenderer-pause.md)                                         | Sospende il filtro.                                                                                                                      |
| [**Correre**](cbaserenderer-run.md)                                             | Esegue il filtro.                                                                                                                        |
| [**Interrompere**](cbaserenderer-stop.md)                                           | Arresta il filtro.                                                                                                                       |
| Metodi IBaseFilter                                                          | Descrizione                                                                                                                             |
| [**FindPin**](cbaserenderer-findpin.md)                                     | Recupera il pin con l'identificatore specificato.                                                                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




