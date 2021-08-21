---
description: Codici di notifica degli eventi
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Codici di notifica degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54792e433535ceefad416033d7758f4398b7777951173256c9be9b83913d61f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015789"
---
# <a name="event-notification-codes"></a>Codici di notifica degli eventi

In questa sezione vengono elencati DirectShow eventi non specifici del DVD. Per gli eventi specifici del DVD, vedere [DVD Event Notification Codes](dvd-notification-codes.md).

I filtri inviano eventi a Filter Graph Manager chiamando il [**metodo IMediaEventSink::Notify.**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) Gestione filtri Graph alcuni eventi e accoda altri eventi per l'applicazione. L'applicazione li recupera chiamando il [**metodo IMediaEvent::GetEvent.**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)

Nelle sezioni seguenti, ogni voce elenca il codice dell'evento, il significato dei parametri dell'evento e l'azione predefinita di Filter Graph Manager per l'evento, se presente. Per eseguire l'override dell'azione predefinita, chiamare [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling). I codici evento sono definiti nei file di intestazione Evcode.h e Audevcod.h. Se non è presente alcuna azione predefinita, Filter Graph Manager inoltra automaticamente l'evento all'applicazione (tramite la coda degli eventi).

**Eventi personalizzati**

I filtri possono definire eventi personalizzati con codici evento nell'intervallo EC \_ USER e versioni successive. Il gestore Graph filtri le inserirà direttamente nella coda degli eventi. Tuttavia, si applicano le avvertenze seguenti:

-   Filter Graph Manager non è in grado di liberare i parametri dell'evento usando il normale [**metodo IMediaEvent::FreeEventParams.**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) L'applicazione deve liberare memoria o conteggi dei riferimenti associati ai parametri dell'evento.
-   Il filtro deve inviare l'evento solo dall'interno di un'applicazione preparata per gestire l'evento. È possibile che l'applicazione possa impostare una proprietà personalizzata sul filtro per indicare che è sicuro inviare l'evento.



| Codice di notifica degli eventi                                                 | Descrizione                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ ACTIVATE**](ec-activate.md)                                     | È in corso l'attivazione o la disattivazione di una finestra video.                                                                         |
| [**EC \_ BANDWIDTHCHANGE**](ec-bandwidthchange.md)                       | Non supportata.                                                                                                            |
| [**EC \_ BUFFERING \_ DATA**](ec-buffering-data.md)                        | Il grafico sta buffering dei dati o ha interrotto la memorizzazione nel buffer dei dati.                                                               |
| [**EC \_ BUILT**](ec-built.md)                                           | Inviare tramite il controllo Video quando è stato creato un grafo. Non inoltrato alle applicazioni.                                     |
| [**EC \_ CLOCK \_ CHANGED**](ec-clock-changed.md)                          | L'orologio di riferimento è stato modificato.                                                                                          |
| [**EC \_ CLOCK \_ UNSET**](ec-clock-unset.md)                              | Il provider di clock è stato disconnesso.                                                                                      |
| [**EC \_ CODECAPI \_ EVENT**](ec-codecapi-event.md)                        | Inviato da un codificatore per segnalare un evento di codifica.                                                                           |
| [**EC \_ COMPLETE**](ec-complete.md)                                     | È stato eseguito il rendering di tutti i dati di un determinato flusso.                                                                      |
| [**MODIFICA \_ DI EC CONTENTPROPERTY \_**](ec-contentproperty-changed.md)      | Non supportata.                                                                                                            |
| [**EC \_ DEVICE \_ LOST**](ec-device-lost.md)                              | Un Plug and Play dispositivo è stato rimosso o è diventato nuovamente disponibile.                                                         |
| [**EC \_ DISPLAY \_ CHANGED**](ec-display-changed.md)                      | La modalità di visualizzazione è stata modificata.                                                                                             |
| [**EC \_ END \_ OF \_ SEGMENT**](ec-end-of-segment.md)                       | È stata raggiunta la fine di un segmento.                                                                                    |
| [**EC \_ EOS \_ A BREVE**](ec-eos-soon.md)                                    | Non supportata.                                                                                                            |
| [**ERRORE \_ EC \_ STILLPLAYING**](ec-error-stillplaying.md)                | Un comando asincrono per eseguire il grafo non è riuscito.                                                                      |
| [**EC \_ ERRORABORT**](ec-errorabort.md)                                 | Un'operazione è stata interrotta a causa di un errore.                                                                             |
| [**EC \_ ERRORABORTEX**](ec-errorabortex.md)                             | Un'operazione è stata interrotta a causa di un errore.                                                                             |
| [**EC \_ EXTDEVICE \_ MODE \_ CHANGE**](ec-extdevice-mode-change.md)         | Non supportata.                                                                                                            |
| [**EC \_ FILE \_ CLOSED**](ec-file-closed.md)                              | Il file di origine è stato chiuso a causa di un evento imprevisto.                                                                |
| [**EC \_ FULLSCREEN \_ LOST**](ec-fullscreen-lost.md)                      | Il renderer video sta per disattivare la modalità schermo intero.                                                                  |
| [**EC \_ GRAPH \_ MODIFICATO**](ec-graph-changed.md)                          | Il grafico dei filtri è stato modificato.                                                                                             |
| [**EC \_ LENGTH \_ CHANGED**](ec-length-changed.md)                        | La lunghezza di un'origine è stata modificata.                                                                                       |
| [**EC \_ LOADSTATUS**](ec-loadstatus.md)                                 | Notifica all'applicazione lo stato di avanzamento all'apertura di un file di rete.                                                         |
| [**EC \_ MARKER \_ HIT**](ec-marker-hit.md)                                | Non supportata.                                                                                                            |
| [**EC \_ NEED \_ RESTART**](ec-need-restart.md)                            | Un filtro richiede il riavvio del grafo.                                                                       |
| [**NUOVO PIN EC \_ \_**](ec-new-pin.md)                                      | Non supportata.                                                                                                            |
| [**FINESTRA \_ DI NOTIFICA \_ EC**](ec-notify-window.md)                          | Notifica un filtro della finestra del renderer video.                                                                         |
| [**EC \_ OLE \_ EVENT**](ec-ole-event.md)                                  | Un filtro passa una stringa di testo all'applicazione.                                                                     |
| [**EC \_ OPENING \_ FILE**](ec-opening-file.md)                            | Il grafico sta aprendo un file o ha terminato l'apertura di un file.                                                              |
| [**EC \_ PALETTE \_ CHANGED**](ec-palette-changed.md)                      | La tavolozza video è stata modificata.                                                                                            |
| [**EC \_ PAUSED**](ec-paused.md)                                         | Una richiesta di sospensione è stata completata.                                                                                            |
| [**EC \_ PLEASE \_ REOPEN**](ec-please-reopen.md)                          | Il file di origine è stato modificato.                                                                                              |
| [**EC \_ PREPROCESS \_ COMPLETE**](ec-preprocess-complete.md)              | Inviato dal filtro [WM ASF Writer](wm-asf-writer-filter.md) quando completa la pre-elaborazione per la codifica multipass. |
| [**LATENZA \_ DI \_ ELABORAZIONE EC**](ec-processing-latency.md)                | Indica il tempo necessario a un componente per elaborare ogni campione.                                           |
| [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md)                        | Il grafico sta rilasciando campioni per il controllo di qualità.                                                                       |
| [**EC \_ RENDER \_ FINISHED**](ec-render-finished.md)                      | Non supportata.                                                                                                            |
| [**EC \_ REPAINT**](ec-repaint.md)                                       | Un renderer video richiede un ridisegno.                                                                                      |
| [**EC \_ SAMPLE \_ LATENCY**](ec-sample-latency.md)                        | Specifica il ritardo nella pianificazione di un componente per l'elaborazione dei campioni.                                                  |
| [**EC \_ SAMPLE \_ NEEDED**](ec-sample-needed.md)                          | Richiede un nuovo esempio di input dal filtro Enhanced Video Renderer (EVR).                                                |
| [**EC \_ SCRUB \_ TIME**](ec-scrub-time.md)                                | Specifica il timestamp per il passaggio del frame più recente.                                                                  |
| [**SEGMENTO \_ EC \_ AVVIATO**](ec-segment-started.md)                      | È stato avviato un nuovo segmento.                                                                                                |
| [**ARRESTO \_ EC \_**](ec-shutting-down.md)                          | Il grafico dei filtri viene arrestato prima di essere eliminato.                                                              |
| [**EC \_ SNDDEV \_ IN \_ ERRORE**](ec-snddev-in-error.md)                     | Si è verificato un errore del dispositivo in un filtro di acquisizione audio.                                                                   |
| [**ERRORE \_ EC SNDDEV \_ \_ OUT**](ec-snddev-out-error.md)                   | Si è verificato un errore del dispositivo in un filtro del renderer audio.                                                                  |
| [**EC \_ STARVATION**](ec-starvation.md)                                 | Un filtro non riceve dati sufficienti.                                                                                    |
| [**MODIFICA \_ DELLO \_ STATO EC**](ec-state-change.md)                            | Lo stato del grafico dei filtri è stato modificato.                                                                                       |
| [**STATO \_ EC**](ec-status.md)                                         | Contiene due stringhe di stato arbitrarie.                                                                                    |
| [**EC \_ STEP \_ COMPLETE**](ec-step-complete.md)                          | Un filtro che esegue l'esecuzione di istruzioni dei fotogrammi ha eseguito il step del numero specificato di fotogrammi.                                            |
| [**CONTROLLO \_ DEL FLUSSO EC \_ \_ AVVIATO**](ec-stream-control-started.md)       | È stato eseguito un comando di avvio del controllo di flusso.                                                                          |
| [**CONTROLLO \_ DEL FLUSSO EC \_ \_ ARRESTATO**](ec-stream-control-stopped.md)       | È stato eseguito un comando di arresto del controllo di flusso.                                                                           |
| [**ERRORE DEL FLUSSO EC \_ \_ ANCORA IN \_ RIPRODUZIONE**](ec-stream-error-stillplaying.md) | Si è verificato un errore in un flusso. Il flusso è ancora in riproduzione.                                                           |
| [**ERRORE \_ DEL FLUSSO EC \_ \_ ARRESTATO**](ec-stream-error-stopped.md)           | Un flusso è stato arrestato a causa di un errore.                                                                                 |
| [**CODICE \_ TEMPORALE EC \_ DISPONIBILE**](ec-timecode-available.md)                | Non supportata.                                                                                                            |
| [**EC \_ UNBUILT**](ec-unbuilt.md)                                       | Inviare dal controllo video quando un grafo è stato demolito. Non inoltrato alle applicazioni.                                 |
| [**EC \_ USERABORT**](ec-userabort.md)                                   | L'utente ha terminato la riproduzione.                                                                                         |
| [**DIMENSIONI \_ VIDEO \_ EC \_ MODIFICATE**](ec-video-size-changed.md)               | Le dimensioni del video nativo sono state modificate.                                                                                        |
| [**EC \_ VIDEOFRAMEREADY**](ec-videoframeready.md)                       | Un fotogramma video è pronto per la visualizzazione.                                                                                       |
| [**\_RICONNESSIONE DI EC VMR NON \_ \_ RIUSCITA**](ec-vmr-reconnection-failed.md)     | Inviato da VMR-7 e VMR-9 quando non è stato in grado di accettare una richiesta di modifica del formato dinamico dal decodificatore upstream.   |
| [**EC \_ VMR \_ RENDERDEVICE \_ SET**](ec-vmr-renderdevice-set.md)           | Inviato quando la macchina virtuale ha selezionato il meccanismo di rendering.                                                                   |
| [**SUPERFICIE \_ VMR \_ EC \_ CAPOVOLTA**](ec-vmr-surface-flipped.md)             | Inviato quando l'allocatore presenter di VMR-7 ha chiamato il metodo Flip DirectDraw sulla superficie visualizzata.           |
| [**FINESTRA \_ EC \_ DISTRUTTA**](ec-window-destroyed.md)                    | Il renderer video è stato eliminato o eliminato dal grafo.                                                               |
| [**EVENTO \_ EC WMT \_**](ec-wmt-event.md)                                  | Inviato dal filtro WM ASF Reader quando legge i file ASF protetti da DRM (Digital Rights Management).                    |
| [**EVENTO \_ EC WMT \_ \_ INDEX**](ec-wmt-index-event.md)                     | Inviato quando un'applicazione usa WM ASF Writer per indicizzare Windows file video multimediali.                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



