---
description: Codici di notifica degli eventi
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Codici di notifica degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c41abc3ffc7a93a39e7a97fb210b491ad4fc58
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304395"
---
# <a name="event-notification-codes"></a>Codici di notifica degli eventi

Questa sezione elenca gli eventi di DirectShow che non sono specifici del DVD. Per gli eventi specifici del DVD, vedere la pagina relativa ai [codici di notifica degli eventi DVD](dvd-notification-codes.md).

I filtri inviano gli eventi al gestore del grafico dei filtri chiamando il metodo [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) . Il gestore del grafico del filtro gestisce alcuni eventi e ne accoda altri per l'applicazione. L'applicazione li recupera chiamando il metodo [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) .

Nelle sezioni riportate di seguito, ogni voce elenca il codice evento, il significato dei parametri dell'evento e l'azione predefinita del gestore del grafico di filtro per l'evento, se presente. Per eseguire l'override dell'azione predefinita, chiamare [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling). I codici evento vengono definiti nei file di intestazione Evcode. h e Audevcod. h. Se non è presente alcuna azione predefinita, il gestore del grafico del filtro lo trasmette automaticamente all'applicazione (tramite la coda degli eventi).

**Eventi personalizzati**

I filtri possono definire eventi personalizzati con i codici evento nell'intervallo EC \_ utente e versioni successive. Il gestore del grafico dei filtri li inserirà direttamente nella coda degli eventi. Tuttavia, si applicano le avvertenze seguenti:

-   Filter Graph Manager non può liberare i parametri dell'evento usando il metodo [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) normale. L'applicazione deve liberare i conteggi di memoria o di riferimento associati ai parametri dell'evento.
-   Il filtro deve solo inviare l'evento all'interno di un'applicazione preparata per la gestione dell'evento. (Probabilmente l'applicazione può impostare una proprietà personalizzata sul filtro per indicare che è sicuro inviare l'evento).



| Codice di notifica degli eventi                                                 | Descrizione                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**\_attivazione EC**](ec-activate.md)                                     | È in corso l'attivazione o la disattivazione di una finestra video.                                                                         |
| [**\_BANDWIDTHCHANGE EC**](ec-bandwidthchange.md)                       | Non supportata.                                                                                                            |
| [**\_dati di buffering EC \_**](ec-buffering-data.md)                        | Il grafico memorizza nel buffer i dati o ha interrotto il buffering dei dati.                                                               |
| [**EC \_ compilata**](ec-built.md)                                           | Inviare dal controllo video quando è stato compilato un grafo. Non è stato inviato ad applicazioni.                                     |
| [**\_orologio EC \_ modificato**](ec-clock-changed.md)                          | L'orologio di riferimento è stato modificato.                                                                                          |
| [**orologio EC non \_ \_ impostato**](ec-clock-unset.md)                              | Il provider Clock è stato disconnesso.                                                                                      |
| [**\_evento CODEcapite EC \_**](ec-codecapi-event.md)                        | Inviato da un codificatore per segnalare un evento di codifica.                                                                           |
| [**EC \_ completato**](ec-complete.md)                                     | È stato eseguito il rendering di tutti i dati di un flusso specifico.                                                                      |
| [**\_tipo CONTENTPROPERTY EC \_ modificato**](ec-contentproperty-changed.md)      | Non supportata.                                                                                                            |
| [**\_dispositivo EC \_ perso**](ec-device-lost.md)                              | Un dispositivo Plug and Play è stato rimosso o è stato nuovamente disponibile.                                                         |
| [**visualizzazione di EC \_ \_ modificata**](ec-display-changed.md)                      | La modalità di visualizzazione è cambiata.                                                                                             |
| [**\_fine \_ del \_ segmento EC**](ec-end-of-segment.md)                       | È stata raggiunta la fine di un segmento.                                                                                    |
| [**EC \_ EOS a \_ breve**](ec-eos-soon.md)                                    | Non supportata.                                                                                                            |
| [**\_STILLPLAYING errore \_ EC**](ec-error-stillplaying.md)                | Un comando asincrono per eseguire il grafo non è riuscito.                                                                      |
| [**\_ERRORABORT EC**](ec-errorabort.md)                                 | Un'operazione è stata interrotta a causa di un errore.                                                                             |
| [**\_ERRORABORTEX EC**](ec-errorabortex.md)                             | Un'operazione è stata interrotta a causa di un errore.                                                                             |
| [**\_modifica della \_ modalità \_ EXTDEVICE EC**](ec-extdevice-mode-change.md)         | Non supportata.                                                                                                            |
| [**\_file EC \_ chiuso**](ec-file-closed.md)                              | Il file di origine è stato chiuso a causa di un evento imprevisto.                                                                |
| [**EC \_ FullScreen \_ perso**](ec-fullscreen-lost.md)                      | Il renderer video sta per uscire dalla modalità schermo intero.                                                                  |
| [**\_grafico EC \_ modificato**](ec-graph-changed.md)                          | Il grafico del filtro è stato modificato.                                                                                             |
| [**lunghezza di EC \_ \_ modificata**](ec-length-changed.md)                        | La lunghezza di un'origine è cambiata.                                                                                       |
| [**\_LOADSTATUS EC**](ec-loadstatus.md)                                 | Notifica all'applicazione lo stato di avanzamento all'apertura di un file di rete.                                                         |
| [**\_hit indicatore \_ EC**](ec-marker-hit.md)                                | Non supportata.                                                                                                            |
| [**EC \_ necessario \_ riavvio**](ec-need-restart.md)                            | Un filtro richiede che il grafico venga riavviato.                                                                       |
| [**\_nuovo \_ pin EC**](ec-new-pin.md)                                      | Non supportata.                                                                                                            |
| [**\_finestra notifica \_ EC**](ec-notify-window.md)                          | Invia una notifica a un filtro della finestra del renderer video.                                                                         |
| [**\_evento OLE \_ EC**](ec-ole-event.md)                                  | Un filtro passa una stringa di testo all'applicazione.                                                                     |
| [**\_file di apertura EC \_**](ec-opening-file.md)                            | Il grafico apre un file o ha terminato l'apertura di un file.                                                              |
| [**\_tavolozza EC \_ modificata**](ec-palette-changed.md)                      | La tavolozza video è cambiata.                                                                                            |
| [**EC \_ sospeso**](ec-paused.md)                                         | Una richiesta di sospensione è stata completata.                                                                                            |
| [**EC \_ \_ riapri**](ec-please-reopen.md)                          | Il file di origine è stato modificato.                                                                                              |
| [**\_pre-elaborazione EC \_ completata**](ec-preprocess-complete.md)              | Inviato dal filtro del [writer ASF WM](wm-asf-writer-filter.md) quando completa la pre-elaborazione per la codifica Multipass. |
| [**\_latenza di elaborazione EC \_**](ec-processing-latency.md)                | Indica la quantità di tempo che un componente sta prendendo per elaborare ogni campione.                                           |
| [**\_modifica della qualità EC \_**](ec-quality-change.md)                        | Il grafico sta eliminando gli esempi per il controllo qualità.                                                                       |
| [**\_rendering EC \_ completato**](ec-render-finished.md)                      | Non supportata.                                                                                                            |
| [**ridisegno EC \_**](ec-repaint.md)                                       | Un renderer video richiede un oggetto Repaint.                                                                                      |
| [**\_ \_ latenza campione EC**](ec-sample-latency.md)                        | Specifica la distanza di pianificazione di un componente per l'elaborazione degli esempi.                                                  |
| [**\_esempio EC \_ necessario**](ec-sample-needed.md)                          | Richiede un nuovo esempio di input dal filtro renderer video avanzato (EVR).                                                |
| [**\_tempo di scrub EC \_**](ec-scrub-time.md)                                | Specifica il timestamp per il passaggio del frame più recente.                                                                  |
| [**\_segmento EC \_ avviato**](ec-segment-started.md)                      | Un nuovo segmento è stato avviato.                                                                                                |
| [**\_arresto di EC \_**](ec-shutting-down.md)                          | È in corso l'arresto del grafico del filtro prima di essere eliminato definitivamente.                                                              |
| [**EC \_ SNDDEV \_ in \_ errore**](ec-snddev-in-error.md)                     | Si è verificato un errore del dispositivo in un filtro di acquisizione audio.                                                                   |
| [**\_errore SNDDEV \_ EC \_**](ec-snddev-out-error.md)                   | Si è verificato un errore del dispositivo in un filtro renderer audio.                                                                  |
| [**scadenza \_ EC**](ec-starvation.md)                                 | Un filtro non riceve dati sufficienti.                                                                                    |
| [**\_modifica dello stato EC \_**](ec-state-change.md)                            | Lo stato del grafico filtro è stato modificato.                                                                                       |
| [**\_stato EC**](ec-status.md)                                         | Contiene due stringhe di stato arbitrarie.                                                                                    |
| [**\_passaggio EC \_ completato**](ec-step-complete.md)                          | Un filtro che esegue lo stepping del frame ha superato il numero di frame specificato.                                            |
| [**\_controllo flusso \_ EC \_ avviato**](ec-stream-control-started.md)       | È stato applicato un comando di avvio del controllo di flusso.                                                                          |
| [**\_controllo flusso \_ EC \_ arrestato**](ec-stream-control-stopped.md)       | È stato applicato un comando di interruzione del controllo del flusso.                                                                           |
| [**\_errore di flusso EC \_ \_ STILLPLAYING**](ec-stream-error-stillplaying.md) | Si è verificato un errore in un flusso. Il flusso è ancora in riproduzione.                                                           |
| [**\_errore di flusso EC \_ \_ arrestato**](ec-stream-error-stopped.md)           | Un flusso è stato interrotto a causa di un errore.                                                                                 |
| [**\_timecode EC \_ disponibile**](ec-timecode-available.md)                | Non supportata.                                                                                                            |
| [**EC non \_ compilato**](ec-unbuilt.md)                                       | Inviare dal controllo video quando un grafo è stato eliminato. Non è stato inviato ad applicazioni.                                 |
| [**\_USERABORT EC**](ec-userabort.md)                                   | L'utente ha terminato la riproduzione.                                                                                         |
| [**\_dimensioni del video EC \_ \_ modificate**](ec-video-size-changed.md)               | Le dimensioni del video nativo sono state modificate.                                                                                        |
| [**\_VIDEOFRAMEREADY EC**](ec-videoframeready.md)                       | Un frame video è pronto per la visualizzazione.                                                                                       |
| [**\_riconnessione VMR EC \_ \_ non riuscita**](ec-vmr-reconnection-failed.md)     | Inviato da VMR-7 e VMR-9 quando non è stato in grado di accettare una richiesta di modifica del formato dinamico dal decodificatore upstream.   |
| [**\_set di \_ RENDERDEVICE \_ VMR EC**](ec-vmr-renderdevice-set.md)           | Inviato quando VMR ha selezionato il meccanismo di rendering.                                                                   |
| [**\_superficie VMR \_ EC \_ capovolta**](ec-vmr-surface-flipped.md)             | Inviato quando il relatore dell'allocatore VMR-7 ha chiamato il metodo di capovolgimento DirectDraw sulla superficie visualizzata.           |
| [**\_finestra EC \_ distrutta**](ec-window-destroyed.md)                    | Il renderer video è stato eliminato o rimosso dal grafico.                                                               |
| [**\_evento WMT \_ EC**](ec-wmt-event.md)                                  | Inviato dal filtro di lettura ASF WM quando legge i file ASF protetti da Digital Rights Management (DRM).                    |
| [**\_evento di \_ indice \_ WMT EC**](ec-wmt-index-event.md)                     | Inviato quando un'applicazione usa il writer ASF WM per indicizzare i file di Windows Media Video.                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



