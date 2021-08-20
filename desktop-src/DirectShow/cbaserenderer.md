---
description: La classe CBaseRenderer è una classe di base per l'implementazione di filtri del renderer.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: Classe CBaseRenderer (Renbase.h)
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
ms.openlocfilehash: 81e529493bfd892607748423bb1bab9016eb232aaeb3ed22287fa2c1c1917687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954806"
---
# <a name="cbaserenderer-class"></a>Classe CBaseRenderer

![Gerarchia di classi cbaserenderer](images/rbase02.png)

La `CBaseRenderer` classe è una classe di base per l'implementazione di filtri del renderer. Supporta un pin di input, implementato dalla [**classe CRendererInputPin.**](crendererinputpin.md) Per usare questa classe, dichiarare una classe derivata che eredita `CBaseRenderer` . Come minimo, la classe derivata deve implementare i metodi seguenti, dichiarati come virtuali puri nella classe di base:

-   [**CBaseRenderer::CheckMediaType:**](cbaserenderer-checkmediatype.md)accetta o rifiuta i tipi di supporti proposti. Il filtro chiama questo metodo durante il processo di connessione del pin.
-   [**CBaseRenderer::D oRenderSample:**](cbaserenderer-dorendersample.md)esegue il rendering di un esempio. Il filtro chiama questo metodo per ogni esempio ricevuto durante l'esecuzione.

La classe base gestisce le modifiche di stato e i problemi di sincronizzazione. Pianifica anche gli esempi per il rendering, anche se non implementa alcuna misura di controllo di qualità. La classe base dichiara anche diversi metodi "gestore". Si tratta di metodi che il filtro chiama in punti specifici del processo di streaming. Non eseguono alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override. Nella tabella seguente sono elencati sotto l'intestazione Metodi pubblici: Gestori.

Il [**gestore CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) merita una menzione speciale. Il filtro chiama questo metodo se riceve un campione mentre il filtro è sospeso. Ciò può verificarsi se il grafico passa da arrestato a sospeso o se il grafo viene cercato durante la sospensione. I renderer video usano in genere l'esempio per visualizzare un fotogramma fermo. Quando il filtro passa dalla sospensione all'esecuzione, invia lo stesso esempio al metodo [**CBaseRenderer::D oRenderSample,**](cbaserenderer-dorendersample.md) come primo esempio nel flusso.

La `CBaseRenderer` classe espone le interfacce **IMediaSeeking** e **IMediaPosition** tramite l'oggetto [**CRendererPosPassThru.**](crendererpospassthru.md) Passa tutte le richieste di ricerca al filtro successivo a monte.

## <a name="scheduling"></a>Pianificazione

Quando il filtro upstream chiama il metodo [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del pin di input per recapitare un esempio, il pin passa questa chiamata al metodo [**CBaseRenderer::Receive del**](cbaserenderer-receive.md) filtro. Il filtro elimina l'esempio, lo esegue immediatamente o lo pianifica per il rendering.

Se l'esempio non ha timestamp o se non è disponibile alcun orologio di riferimento, il filtro esegue immediatamente il rendering dell'esempio. In caso contrario, il filtro chiama il metodo [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) per determinare cosa fare. Per impostazione predefinita, l'esempio viene pianificato in base ai relativi timestamp. La classe derivata può eseguire l'override **di ShouldDrawSampleNow per** supportare il controllo qualità.

Per pianificare un esempio, il filtro chiama il [**metodo IReferenceClock::AdviseTime,**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) che crea una richiesta di consulenza. Il [**metodo Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) si blocca quindi fino all'ora pianificata o fino a quando lo stato del filtro non cambia. Il blocco impedisce al filtro upstream di fornire più campioni fino a quando non viene eseguito il rendering dell'esempio corrente.

Quando il filtro upstream chiama il metodo [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) per segnalare la fine del flusso, il filtro invia un evento [**EC \_ COMPLETE**](ec-complete.md) al gestore del grafico del filtro. Il filtro attende il tempo di arresto dell'esempio corrente prima di inviare l'evento.



| Variabili membro protette                                                   | Descrizione                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bAbort**](cbaserenderer-m-babort.md)                                  | Flag che indica se arrestare il rendering e rifiutare altri esempi.                                                               |
| [**m \_ bEOS**](cbaserenderer-m-beos.md)                                      | Flag che indica se è stata raggiunta la fine del flusso.                                                                                  |
| [**m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md)                    | Flag che indica se il filtro ha pubblicato l'evento EC \_ COMPLETE.                                                               |
| [**m \_ bInReceive**](cbaserenderer-m-binreceive.md)                          | Flag che indica se il filtro sta elaborando una **chiamata Receive.**                                                                |
| [**m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)                  | Flag che abilita o disabilita il ridisegno degli eventi.                                                                                           |
| [**m \_ bStreaming**](cbaserenderer-m-bstreaming.md)                          | Flag che indica se il filtro è un flusso di dati.                                                                               |
| [**m \_ dwAdvise**](cbaserenderer-m-dwadvise.md)                              | Identificatore dell'evento timer che pianifica il rendering.                                                                                 |
| [**m \_ EndOfStreamTimer**](cbaserenderer-m-endofstreamtimer.md)              | Identificatore dell'evento timer, per la pianificazione delle notifiche EC \_ COMPLETE.                                                                      |
| [**m \_ evComplete**](cbaserenderer-m-evcomplete.md)                          | Evento segnalato al termine di una transizione di stato.                                                                             |
| [**m \_ InterfaceLock**](cbaserenderer-m-interfacelock.md)                    | Blocco dello stato del filtro.                                                                                                                      |
| [**m \_ ObjectCreationLock**](cbaserenderer-m-objectcreationlock.md)          | Blocco per proteggere la creazione di oggetti all'interno del filtro.                                                                              |
| [**m \_ pInputPin**](cbaserenderer-m-pinputpin.md)                            | Puntatore al pin di input del filtro.                                                                                                      |
| [**m \_ pMediaSample**](cbaserenderer-m-pmediasample.md)                      | Puntatore all'esempio multimediale corrente.                                                                                                    |
| [**m \_ pPosition**](cbaserenderer-m-pposition.md)                            | Oggetto helper per passare i comandi seek a monte.                                                                                           |
| [**m \_ pQSink**](cbaserenderer-m-pqsink.md)                                  | Puntatore all'oggetto che riceve messaggi di controllo qualità.                                                                           |
| [**m \_ RendererLock**](cbaserenderer-m-rendererlock.md)                      | Blocco di streaming.                                                                                                                         |
| [**m \_ RenderEvent**](cbaserenderer-m-renderevent.md)                        | Evento usato per pianificare il rendering.                                                                                                       |
| [**m \_ SignalTime**](cbaserenderer-m-signaltime.md)                          | Ora di arresto nell'esempio corrente.                                                                                                        |
| [**m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)                      | Evento utilizzato per rilasciare il thread di streaming.                                                                                             |
| Metodi pubblici                                                               | Descrizione                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | Annulla l'evento timer che pianifica il rendering. Virtuale.                                                                              |
| [**CBaseRenderer**](cbaserenderer-cbaserenderer.md)                         | Metodo del costruttore.                                                                                                                     |
| [**~CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | Metodo del distruttore.                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | Recupera i puntatori a interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro. Virtuale. |
| [**GetPin**](cbaserenderer-getpin.md)                                       | Recupera un segnaposto. Virtuale.                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | Recupera il numero di pin. Virtuale.                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | Recupera i timestamp da un esempio. Virtuale.                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | Invia un [**evento EC \_ DISPLAY \_ CHANGED**](ec-display-changed.md) al gestore del grafico dei filtri.                                          |
| [**PrepareReceive**](cbaserenderer-preparereceive.md)                       | Si prepara per il rendering di un esempio. Virtuale.                                                                                                   |
| [**Ricevere**](cbaserenderer-receive.md)                                     | Riceve l'esempio multimediale successivo nel flusso. Virtuale.                                                                                  |
| [**rendere**](cbaserenderer-render.md)                                       | Esegue il rendering di un esempio. Virtuale.                                                                                                              |
| [**ScheduleSample**](cbaserenderer-schedulesample.md)                       | Pianifica un esempio per il rendering. Virtuale.                                                                                              |
| [**SendNotifyWindow**](cbaserenderer-sendnotifywindow.md)                   | Notifica il filtro upstream dell'handle della finestra video.                                                                                |
| [**SendRepaint**](cbaserenderer-sendrepaint.md)                             | Invia un evento repaint al gestore del grafico dei filtri.                                                                                      |
| [**SetMediaType**](cbaserenderer-setmediatype.md)                           | Chiamato quando viene impostato il tipo di supporto del pin. Virtuale.                                                                                       |
| [**SignalTimerFired**](cbaserenderer-signaltimerfired.md)                   | Cancella l'identificatore del timer usato per pianificare il rendering.                                                                                 |
| [**SourceThreadCanWait**](cbaserenderer-sourcethreadcanwait.md)             | Contiene o rilascia il thread di streaming. Virtuale.                                                                                        |
| [**WaitForReceiveToComplete**](cbaserenderer-waitforreceivetocomplete.md)   | Attende il completamento [**del metodo CBaseRenderer::Receive.**](cbaserenderer-receive.md)                                               |
| [**WaitForRenderTime**](cbaserenderer-waitforrendertime.md)                 | Attende l'ora di presentazione dell'esempio corrente. Virtuale.                                                                              |
| Metodi pubblici: metodi delle funzioni di accesso                                             | Descrizione                                                                                                                             |
| [**ClearPendingSample**](cbaserenderer-clearpendingsample.md)               | Rilascia l'esempio corrente. Virtuale.                                                                                                   |
| [**GetCurrentSample**](cbaserenderer-getcurrentsample.md)                   | Recupera l'esempio corrente. Virtuale.                                                                                                  |
| [**GetRealState**](cbaserenderer-getrealstate.md)                           | Recupera lo stato del filtro.                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | Recupera l'evento che pianifica il rendering.                                                                                           |
| [**HaveCurrentSample**](cbaserenderer-havecurrentsample.md)                 | Determina se il filtro include un campione. Virtuale.                                                                                    |
| [**IsEndOfStream**](cbaserenderer-isendofstream.md)                         | Esegue una query per determinare se è stata ricevuta la notifica di fine flusso.                                                                            |
| [**IsEndOfStreamDelivered**](cbaserenderer-isendofstreamdelivered.md)       | Esegue una query per determinare se l'evento EC COMPLETE è \_ stato recapitato al gestore del grafico dei filtri.                                                  |
| [**IsStreaming**](cbaserenderer-isstreaming.md)                             | Esegue una query per determinare se il filtro è un flusso di dati.                                                                                           |
| [**SetAbortSignal**](cbaserenderer-setabortsignal.md)                       | Imposta un flag che indica se arrestare il rendering e rifiutare altri esempi.                                                       |
| [**SetRepaintStatus**](cbaserenderer-setrepaintstatus.md)                   | Abilita o disabilita gli eventi di ridisegno.                                                                                                     |
| Metodi pubblici: metodi State-Change pubblici                                         | Descrizione                                                                                                                             |
| [**Attivo**](cbaserenderer-active.md)                                       | Chiamato quando lo stato viene sospeso o in esecuzione. Virtuale.                                                                        |
| [**BeginFlush**](cbaserenderer-beginflush.md)                               | Avvia un'operazione di scaricamento. Virtuale.                                                                                                      |
| [**BreakConnect**](cbaserenderer-breakconnect.md)                           | Rilascia il pin di input da una connessione. Virtuale.                                                                                      |
| [**CheckReady**](cbaserenderer-checkready.md)                               | Esegue una query sul completamento di una transizione di stato.                                                                                         |
| [**CompleteConnect**](cbaserenderer-completeconnect.md)                     | Completa la connessione del pin di input a un altro pin. Virtuale.                                                                           |
| [**CompleteStateChange**](cbaserenderer-completestatechange.md)             | Determina se una transizione allo stato sospeso è stata completata. Virtuale.                                                               |
| [**EndFlush**](cbaserenderer-endflush.md)                                   | Termina un'operazione di scaricamento. Virtuale.                                                                                                        |
| [**Inattivo**](cbaserenderer-inactive.md)                                   | Chiamato quando lo stato viene arrestato. Virtuale.                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | Segnala che una transizione di stato non è ancora completata.                                                                                    |
| [**Ready**](cbaserenderer-ready.md)                                         | Segnala che una transizione di stato è stata completata.                                                                                            |
| [**StartStreaming**](cbaserenderer-startstreaming.md)                       | Avvia lo streaming quando il filtro passa a uno stato di esecuzione. Virtuale.                                                               |
| [**StopStreaming**](cbaserenderer-stopstreaming.md)                         | Interrompe lo streaming quando il filtro esce dallo stato di esecuzione. Virtuale.                                                             |
| Metodi pubblici: metodi di fine flusso                                        | Descrizione                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | Notifica al filtro che il pin di input ha ricevuto una notifica di fine flusso. Virtuale.                                                 |
| [**NotifyEndOfStream**](cbaserenderer-notifyendofstream.md)                 | Invia un [**evento EC \_ COMPLETE**](ec-complete.md) al gestore del grafico dei filtri.                                                         |
| [**ResetEndOfStream**](cbaserenderer-resetendofstream.md)                   | Reimposta i flag di fine flusso.                                                                                                         |
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | Annulla il timer che pianifica le notifiche EC \_ COMPLETE. Virtuale.                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | Se è stata raggiunta la fine del flusso, pianifica un evento EC \_ COMPLETE per il gestore del grafico filtri. Virtuale.                                    |
| [**Timercallback**](cbaserenderer-timercallback.md)                         | Metodo di callback per l'evento timer di fine flusso.                                                                                      |
| Metodi pubblici: gestori                                                     | Descrizione                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | Chiamato quando il filtro riceve un campione durante la sospensione. Virtuale.                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | Chiamato dopo il rendering di un esempio. Virtuale.                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | Chiamato quando il rendering sta per iniziare. Virtuale.                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | Chiamato quando il filtro inizia lo streaming. Virtuale.                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | Chiamato quando il filtro interrompe lo streaming. Virtuale.                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | Chiamato quando il filtro viene eseguito in attesa dell'ora di presentazione di un esempio. Virtuale.                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | Chiamato quando il filtro inizia ad attendere l'ora di presentazione di un esempio. Virtuale.                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | Chiamato prima che il filtro esere il rendering di un esempio. Virtuale.                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | Determina la modalità di pianificazione del rendering di un esempio. Virtuale.                                                                            |
| Metodi virtuali puri                                                         | Descrizione                                                                                                                             |
| [**CheckMediaType**](cbaserenderer-checkmediatype.md)                       | Determina se il filtro accetta un tipo di supporto specifico.                                                                                 |
| [**DoRenderSample**](cbaserenderer-dorendersample.md)                       | Esegue il rendering di un esempio.                                                                                                                       |
| Metodi IMediaFilter                                                         | Descrizione                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | Recupera lo stato del filtro (in esecuzione, arrestato o sospeso).                                                                             |
| [**Sospendi**](cbaserenderer-pause.md)                                         | Sospende il filtro.                                                                                                                      |
| [**Esegui**](cbaserenderer-run.md)                                             | Esegue il filtro.                                                                                                                        |
| [**Fermare**](cbaserenderer-stop.md)                                           | Arresta il filtro.                                                                                                                       |
| Metodi IBaseFilter                                                          | Descrizione                                                                                                                             |
| [**FindPin**](cbaserenderer-findpin.md)                                     | Recupera il pin con l'identificatore specificato.                                                                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




