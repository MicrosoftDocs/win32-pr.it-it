---
description: Questo argomento descrive come scrivere un renderer video personalizzato per DirectShow.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Renderer video alternativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070e55375d9d1d5a32c306853aafcb431a76c368
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747279"
---
# <a name="alternative-video-renderers"></a>Renderer video alternativi

Questo argomento descrive come scrivere un renderer video personalizzato per DirectShow.

> [!Note]  
> Anziché scrivere un renderer video personalizzato, è consigliabile scrivere un plug-in Allocator-Presenter per il renderer video mixing (VMR) o il [**renderer video avanzato**](enhanced-video-renderer-filter.md) (EVR). Questo approccio offre tutti i vantaggi di VMR/EVR, incluso il supporto per l'accelerazione video DirectX (DXVA), la deinterlacciamento hardware e l'esecuzione del frame, ed è probabile che sia più affidabile rispetto a un renderer video personalizzato. Per altre informazioni, vedere i seguenti argomenti:
>
> -   [Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Come scrivere un presentatore EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Scrittura di un Renderer alternativo

Microsoft DirectShow fornisce un renderer video basato su finestra; fornisce inoltre un renderer a schermo intero nell'installazione di run-time. È possibile usare le classi base di DirectShow per scrivere renderer video alternativi. Affinché i renderer alternativi possano interagire correttamente con le applicazioni basate su DirectShow, i renderer devono rispettare le linee guida descritte in questo articolo. È possibile usare le classi [**CBaseRenderer**](cbaserenderer.md) e [**CBaseVideoRenderer**](cbasevideorenderer.md) per seguire queste linee guida durante l'implementazione di un rendering video alternativo. A causa dello sviluppo continuo di DirectShow, esaminare periodicamente l'implementazione per assicurarsi che i renderer siano compatibili con la versione più recente di DirectShow.

In questo argomento vengono descritte molte notifiche che un renderer è responsabile della gestione di. Una breve revisione delle notifiche DirectShow potrebbe contribuire a impostare la fase. In DirectShow sono essenzialmente presenti tre tipi di notifiche:

-   *Notifiche di flusso*, ovvero eventi che si verificano nel flusso multimediale e passati da un filtro a quello successivo. Possono essere le notifiche di inizio-svuotamento, di svuotamento finale o di fine flusso e vengono inviate chiamando il metodo appropriato sul pin di input del filtro downstream (ad esempio [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)).
-   *Filtrare le notifiche dei grafici*, ovvero gli eventi inviati da un filtro al gestore del grafico del filtro, ad esempio [**EC \_ complete**](ec-complete.md). Questa operazione viene eseguita chiamando il metodo [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) in gestione grafico dei filtri.
-   *Notifiche dell'applicazione*, che vengono recuperate da Filter Graph Manager dall'applicazione di controllo. Un'applicazione chiama il metodo [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) su Filter Graph Manager per recuperare questi eventi. Spesso, il gestore del grafo dei filtri passa attraverso gli eventi che riceve all'applicazione.

In questo argomento viene illustrata la responsabilità del filtro renderer per la gestione delle notifiche di flusso ricevute e per l'invio di notifiche del grafico di filtro appropriate.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Gestione delle notifiche di fine flusso e scaricamento

Una notifica di fine flusso inizia da un filtro upstream, ad esempio il filtro di origine, quando tale filtro rileva che può inviare altri dati. Viene passato attraverso ogni filtro nel grafico e infine termina nel renderer, che è responsabile della successiva invio di una notifica di [**\_ completamento EC**](ec-complete.md) al gestore del grafico dei filtri. I renderer hanno responsabilità particolari quando si tratta di gestire queste notifiche.

Un renderer riceve una notifica di fine flusso quando il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) del PIN di input viene chiamato dal filtro upstream. Un renderer deve prendere nota della notifica e continuare a eseguire il rendering dei dati già ricevuti. Una volta ricevuti tutti i dati rimanenti, il renderer deve inviare una notifica di [**\_ completamento EC**](ec-complete.md) al gestore del grafo dei filtri. La notifica di **\_ completamento EC** deve essere inviata una sola volta da un renderer ogni volta che raggiunge la fine di un flusso. Inoltre, le notifiche **\_ complete EC** non devono mai essere inviate tranne quando il grafico del filtro è in esecuzione. Se, pertanto, il grafico del filtro viene sospeso quando un filtro di origine invia una notifica di fine flusso, è necessario che **EC \_ complete** non venga inviato fino a quando non viene infine eseguito il grafico dei filtri.

Qualsiasi chiamata al metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) dopo una notifica di fine del flusso viene segnalata come deve essere rifiutata. **E \_** Il messaggio di errore più appropriato da restituire in questo caso è imprevisto.

Quando un grafico a filtro viene arrestato, eventuali notifiche di fine flusso memorizzate nella cache devono essere cancellate e non inviate nuovamente al successivo avvio. Questo è dovuto al fatto che il gestore del grafico dei filtri sospende sempre tutti i filtri immediatamente prima di eseguirli, in modo che si verifichi lo svuotamento appropriato. Se, ad esempio, il grafico del filtro è sospeso e viene ricevuta una notifica di fine del flusso, quindi il grafico del filtro viene arrestato, il renderer non deve inviare una notifica di [**\_ completamento EC**](ec-complete.md) quando viene eseguita successivamente. Se non si è verificata alcuna ricerca, il filtro di origine invierà automaticamente un'altra notifica di fine flusso durante lo stato di sospensione che precede uno stato di esecuzione. Se, invece, si è verificata una ricerca durante l'arresto del grafico del filtro, il filtro di origine potrebbe avere dati da inviare, quindi non invierà una notifica di fine del flusso.

I renderer video spesso dipendono dalle notifiche di fine flusso per un numero maggiore di notifiche di [**\_ completamento**](ec-complete.md) dell'invio di EC. Ad esempio, se un flusso ha terminato la riproduzione, ovvero viene inviata una notifica di fine flusso, e un'altra finestra viene trascinata su una finestra renderer video, verranno generati alcuni messaggi della finestra di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) . La procedura tipica per l'esecuzione di renderer video è evitare di ridisegnare il frame corrente alla ricezione dei messaggi di **\_ disegno WM** (in base al presupposto che venga ricevuto un altro frame da disegnare). Tuttavia, quando è stata inviata la notifica di fine flusso, il renderer è in uno stato di attesa. è ancora in esecuzione, ma è consapevole del mancato ricevimento di dati aggiuntivi. In queste circostanze, il renderer disegna normalmente l'area di riproduzione nera.

La gestione dello svuotamento è una complicazione aggiuntiva per i renderer. Lo scaricamento viene eseguito tramite una coppia di metodi [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) denominati [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush). Lo svuotamento è essenzialmente uno stato aggiuntivo che deve essere gestito dal renderer. Non è consentito per un filtro di origine chiamare **BeginFlush** senza chiamare **EndFlush**, quindi è possibile che lo stato sia breve e discreto; Tuttavia, il renderer deve gestire correttamente i dati o le notifiche ricevute durante la transizione di svuotamento.

Qualsiasi dato ricevuto dopo la chiamata a [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) deve essere rifiutato immediatamente restituendo **S \_ false**. Inoltre, qualsiasi notifica di fine flusso memorizzata nella cache deve essere cancellata anche quando viene scaricato un renderer. Un renderer viene in genere scaricato in risposta a una ricerca. Lo scaricamento garantisce che i dati obsoleti vengano cancellati dal grafico filtro prima che vengano inviati nuovi esempi. In genere, la riproduzione di due sezioni di un flusso, una dopo l'altra, viene gestita in modo ottimale tramite comandi posticipati invece di attendere il completamento di una sezione e quindi di emettere un comando seek.

## <a name="handling-state-changes-and-pause-completion"></a>Gestione delle modifiche di stato e completamento della sospensione

Un filtro renderer si comporta allo stesso modo di qualsiasi altro filtro nel grafico filtro quando viene modificato lo stato, con la seguente eccezione. Dopo la sospensione, il renderer avrà alcuni dati in coda, pronti per essere sottoposti a rendering quando vengono eseguiti successivamente. Quando il renderer video viene arrestato, lo utilizza per i dati in coda. Si tratta di un'eccezione alla regola DirectShow che non deve essere mantenuta da filtri quando il grafico del filtro viene arrestato.

Il motivo di questa eccezione è che, mantenendo le risorse, il renderer avrà sempre un'immagine con cui ridisegnare la finestra se riceve un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) . Dispone inoltre di un'immagine per soddisfare i metodi, ad esempio [**CBaseControlVideo:: GetStaticImage**](cbasecontrolvideo-getstaticimage.md), che richiedono una copia dell'immagine corrente. Un altro effetto del contenimento delle risorse consiste nel fatto che l'allocazione dell'allocatore si interrompe, il che a sua volta rende più veloce la modifica dello stato successivo perché i buffer delle immagini sono già allocati.

Un renderer video deve eseguire il rendering e rilasciare campioni solo durante l'esecuzione. Durante la pausa, il filtro potrebbe eseguirne il rendering, ad esempio durante il disegno di un'immagine del poster statica in una finestra, ma non deve essere rilasciata. I renderer audio non eseguiranno il rendering mentre sono sospesi (anche se possono eseguire altre attività, ad esempio la preparazione del dispositivo Wave). L'ora in cui deve essere eseguito il rendering degli esempi viene ottenuta combinando l'ora del flusso nell'esempio con l'ora di riferimento passata come parametro al metodo [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) . I renderer devono rifiutare campioni con orari di inizio inferiori o uguali a quelli di fine.

Quando un'applicazione sospende un grafico di filtro, il grafico del filtro non restituisce alcun risultato dal metodo [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) fino a quando non sono presenti dati in coda nei renderer. Per garantire questo aspetto, quando un renderer viene sospeso, deve restituire S \_ false se non sono presenti dati in attesa di essere sottoposti a rendering. Se sono presenti dati in coda, può restituire **S \_ OK**.

Filter Graph Manager controlla tutti i valori restituiti durante la sospensione di un grafico di filtro per assicurarsi che i renderer dispongano di dati in coda. Se uno o più filtri non sono pronti, il gestore del grafico dei filtri esegue il polling dei filtri nel grafico chiamando [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate). Il metodo **GetState** accetta un parametro di timeout. Un filtro (in genere un renderer) che è ancora in attesa dell'arrivo dei dati prima di completare la modifica dello stato restituisce l' **\_ \_ \_ intermediario dello stato VFW S** se il metodo **GetState** scade. Quando i dati arrivano al renderer, **GetState** deve essere restituito immediatamente con **S \_ OK**.

Sia nello stato intermedio che completato lo stato del filtro indicato sarà \_ sospeso. Solo il valore restituito indica se il filtro è effettivamente pronto o meno. Se, mentre un renderer è in attesa dell'arrivo dei dati, il relativo filtro di origine invia una notifica di fine flusso, che dovrebbe anche completare la modifica dello stato.

Quando tutti i filtri hanno effettivamente dati in attesa di essere sottoposti a rendering, il grafico del filtro completerà la modifica dello stato di sospensione.

## <a name="handling-termination"></a>Gestione della terminazione

I renderer video devono gestire correttamente gli eventi di terminazione dall'utente. Ciò implica la corretta mascheramento della finestra e la conoscenza delle operazioni da eseguire se successivamente viene forzata la visualizzazione di una finestra. Inoltre, i renderer video devono notificare a Filter Graph Manager quando la finestra viene distrutta (o più accuratamente quando il renderer viene rimosso dal grafico di filtro) per liberare risorse.

Se l'utente chiude la finestra del video (ad esempio premendo ALT + F4), la convenzione consiste nel nascondere immediatamente la finestra e inviare una notifica di [**\_ USERABORT EC**](ec-userabort.md) a Filter Graph Manager. Questa notifica viene passata all'applicazione, in modo da arrestare la riproduzione del grafo. Dopo l'invio di **\_ USERABORT EC**, un renderer video deve rifiutare eventuali altri esempi recapitati.

Il flag arrestato dal grafico deve rimanere attivo dal renderer fino a quando non viene arrestato, quindi deve essere reimpostato in modo che un'applicazione possa eseguire l'override dell'azione dell'utente e continuare a riprodurre il grafico se lo desidera. Se si preme ALT + F4 mentre è in esecuzione il video, la finestra sarà nascosta e tutti gli altri campioni recapitati verranno rifiutati. Se successivamente viene visualizzata la finestra (ad esempio tramite [**IVideoWindow::p UT \_ visibile**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)), non è necessario generare alcuna notifica di [**\_ Repaint EC**](ec-repaint.md) .

Il renderer video deve anche inviare la notifica della [**\_ finestra EC \_ distrutta**](ec-window-destroyed.md) al grafico del filtro quando il renderer video viene terminato. In realtà, è consigliabile gestire questa situazione quando il metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del renderer viene chiamato con un parametro null (che indica che il renderer sta per essere rimosso dal grafico di filtro), anziché attendere che la finestra video effettiva venga distrutta. L'invio di questa notifica consente al server di distribuzione dei plug-in di filtrare Graph Manager di passare le risorse che dipendono dallo stato attivo della finestra ad altri filtri, ad esempio i dispositivi audio.

## <a name="handling-dynamic-format-changes"></a>Gestione delle modifiche al formato dinamico

In alcuni casi, il filtro upstream del renderer potrebbe provare a modificare il formato video durante la riproduzione del video. Spesso è il decompressore video che avvia una modifica di formato dinamico.

Un filtro upstream che tenta di modificare i formati in modo dinamico deve sempre chiamare il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input del renderer. Un renderer video ha alcuni margini relativi ai tipi di modifiche del formato dinamico che deve supportare. Come minimo, deve consentire al filtro upstream di modificare le tavolozze. Quando un filtro upstream modifica i tipi di supporto, collega il tipo di supporto al primo campione fornito nel nuovo formato. Se il renderer include esempi in una coda per il rendering, non dovrebbe modificare il formato fino a quando non viene eseguito il rendering dell'esempio con la modifica del tipo.

Un renderer video può anche richiedere una modifica di formato dal decodificatore. Ad esempio, potrebbe chiedere al decodificatore di fornire un formato compatibile con DirectDraw con una **bialtezza** negativa. Quando il renderer viene sospeso, deve chiamare [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin upstream per vedere quali formati possono essere forniti dal decodificatore. Il decodificatore potrebbe non enumerare tutti i tipi che è in grado di accettare, quindi il renderer dovrebbe offrire alcuni tipi anche se il decodificatore non li annuncia.

Se il decodificatore può passare al formato richiesto, restituisce **S \_ OK** da [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept). Il renderer connette quindi il nuovo tipo di supporto all'esempio multimediale successivo nell'allocatore upstream. Per funzionare, il renderer deve fornire un allocatore personalizzato che implementi un metodo privato per il fissaggio del tipo di supporto all'esempio successivo. (All'interno di questo metodo privato, chiamare [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) per impostare il tipo).

Il pin di input del renderer deve restituire l'allocatore personalizzato del renderer nel metodo [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) . Eseguire l'override di [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) in modo che abbia esito negativo se il filtro upstream non usa l'allocatore del renderer.

Con alcuni decodificatori, l'impostazione di **biHeight** su un numero positivo sui tipi YUV fa sì che il decodificatore disegni l'immagine capovolto. (Questo non è corretto e deve essere considerato un bug nel decodificatore).

Ogni volta che viene rilevata una modifica del formato dal renderer video, deve inviare una notifica di [**\_ \_ modifica della visualizzazione della EC**](ec-display-changed.md) . La maggior parte dei renderer video sceglie un formato durante la connessione in modo da poter disegnare il formato in modo efficiente tramite GDI. Se l'utente modifica la modalità di visualizzazione corrente senza riavviare il computer, un renderer potrebbe trovarsi in una connessione con formato di immagine non valido e deve inviare la notifica. Il primo parametro deve essere il pin che richiede la riconnessione. Il gestore del grafico del filtro disporrà l'arresto del grafico del filtro e la riconnessione del PIN. Durante la successiva riconnessione, il renderer può accettare un formato più appropriato.

Ogni volta che un renderer video rileva una modifica della tavolozza nel flusso, deve inviare la notifica di modifica della [**\_ \_ tavolozza EC**](ec-palette-changed.md) alla gestione del grafo del filtro. I renderer video DirectShow rilevano se una tavolozza è effettivamente cambiata in formato dinamico o meno. I renderer video eseguono questa operazione non solo per filtrare il numero di notifiche **di \_ \_ modifica della tavolozza EC** inviate ma anche per ridurre la quantità di creazione, installazione ed eliminazione della tavolozza necessaria.

Infine, il renderer video potrebbe rilevare anche che la dimensione del video è cambiata, nel qual caso deve inviare la notifica di [**modifica delle \_ \_ dimensioni del \_ video EC**](ec-video-size-changed.md) . Questa notifica può essere utilizzata da un'applicazione per negoziare lo spazio in un documento composto. Le dimensioni effettive del video sono disponibili tramite l'interfaccia di controllo [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . I renderer DirectShow rilevano se la dimensione del video è effettivamente cambiata o meno prima dell'invio di questi eventi.

## <a name="handling-persistent-properties"></a>Gestione delle proprietà permanenti

Tutte le proprietà impostate tramite le interfacce [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) sono destinate a essere persistenti tra le connessioni. Pertanto, la disconnessione e la riconnessione di un renderer non dovrebbero mostrare effetti sulle dimensioni, sulla posizione o sugli stili della finestra. Tuttavia, se le dimensioni del video cambiano tra le connessioni, il renderer deve reimpostare i rettangoli di origine e di destinazione sulle impostazioni predefinite. Le posizioni di origine e di destinazione vengono impostate tramite l'interfaccia **IBasicVideo** .

Sia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) che [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) forniscono un accesso sufficiente alle proprietà per consentire a un'applicazione di salvare e ripristinare tutti i dati nell'interfaccia in un formato permanente. Questa operazione sarà utile per le applicazioni che devono salvare la configurazione e le proprietà esatte dei grafici di filtro durante una sessione di modifica e ripristinarle in un secondo momento.

## <a name="handling-ec_repaint-notifications"></a>Gestione delle \_ notifiche di ridisegno EC

La notifica di [**\_ ridisegno EC**](ec-repaint.md) viene inviata solo quando il renderer viene sospeso o arrestato. Questa notifica segnala al gestore di filtri Graph che il renderer necessita di dati. Se il grafico del filtro viene arrestato quando riceve una di queste notifiche, sospenderà il grafico del filtro, attenderà la ricezione dei dati da parte di tutti i filtri (chiamando [**GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)), quindi verrà arrestato nuovamente. Quando viene arrestato, un renderer video deve rimanere in attesa dell'immagine in modo che i messaggi di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) successivi possano essere gestiti.

Pertanto, se un renderer video riceve un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) quando viene arrestato o sospeso e non ha nulla con cui disegnare la finestra, deve inviare il [**\_ ridisegno EC**](ec-repaint.md) al gestore del grafico del filtro. Se viene ricevuta una notifica di **\_ ridisegno EC** mentre è in pausa, il gestore del grafo del filtro chiama [**IMediaPosition::p UT \_ currentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) con la posizione corrente, ovvero cerca la posizione corrente. In questo modo, i filtri di origine scaricano il grafico del filtro e generano nuovi dati da inviare tramite il grafico dei filtri.

Un renderer deve inviare solo una di queste notifiche alla volta. Pertanto, una volta che il renderer invia una notifica, è necessario assicurarsi che non vengano più inviati fino a quando alcuni campioni non vengono recapitati. Il modo convenzionale per eseguire questa operazione è avere un flag per indicare che è possibile inviare un Repaint, che è disattivato dopo l'invio di una notifica di [**\_ Repaint EC**](ec-repaint.md) . Questo flag deve essere reimpostato quando i dati vengono recapitati o quando viene scaricato il pin di input, ma non se la fine del flusso viene segnalata sul pin di input.

Se il renderer non monitora le notifiche [**di \_ ridisegno EC**](ec-repaint.md) , comporterà la gestione del grafo del filtro con le richieste di **\_ ridisegno EC** (relativamente costose da elaborare). Se, ad esempio, un renderer non ha un'immagine da disegnare e un'altra finestra viene trascinata nella finestra del renderer in un'operazione di trascinamento completo, il renderer riceve più messaggi di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) . Solo il primo di questi deve generare una notifica degli eventi di **\_ Repaint EC** dal renderer al gestore del grafico dei filtri.

Un renderer deve inviare il pin di input come primo parametro alla notifica [**di \_ ridisegno EC**](ec-repaint.md) . In tal caso, verrà eseguita una query sul pin di output associato per [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)e, se supportato, la notifica di **\_ ridisegno EC** verrà inviata prima. Questo consente ai pin di output di gestire i ridisegnamenti prima che il grafico di filtro debba essere toccato. Questa operazione non verrà eseguita se il grafo del filtro viene arrestato, perché non sono disponibili buffer dall'allocatore renderer di cui è stato eseguito il commit.

Se il pin di output non è in grado di gestire la richiesta e il grafico del filtro è in esecuzione, la notifica di [**\_ ridisegno EC**](ec-repaint.md) verrà ignorata. Un pin di output deve restituire **S \_ OK** da [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) per segnalare che la richiesta di ridisegno è stata elaborata correttamente. Il pin di output verrà chiamato sul thread di lavoro Filter Graph Manager, evitando che il renderer chiami direttamente il pin di output, quindi elude eventuali problemi di deadlock. Se il grafico del filtro viene arrestato o sospeso e l'output non gestisce la richiesta, viene eseguita l'elaborazione predefinita.

## <a name="handling-notifications-in-full-screen-mode"></a>Gestione delle notifiche in modalità Full-Screen

Il server di distribuzione plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) nel grafico del filtro gestisce la riproduzione a schermo intero. Verrà scambiato un renderer video per un renderer a schermo intero specializzato, si estenderà una finestra di un renderer a schermo intero oppure il renderer implementerà direttamente la riproduzione a schermo intero. Per interagire con i protocolli a schermo intero, un renderer video deve inviare una notifica di [**\_ attivazione EC**](ec-activate.md) ogni volta che la finestra viene attivata o disattivata. In altre parole, deve essere inviata una notifica di **\_ attivazione EC** per ogni \_ messaggio WM ACTIVATEAPP ricevuto da un renderer.

Quando un renderer viene usato in modalità schermo intero, queste notifiche gestiscono l'invio e la disattivazione della modalità schermo intero. La disattivazione della finestra si verifica in genere quando un utente preme ALT + TAB per passare a un'altra finestra, che il renderer a schermo intero DirectShow USA come spunto per tornare alla modalità di rendering tipica.

Quando la notifica di [**\_ attivazione della EC**](ec-activate.md) viene inviata a Filter Graph Manager quando si esce dalla modalità a schermo intero, Filter Graph Manager invia una notifica a schermo intero [**EC \_ \_ persa**](ec-fullscreen-lost.md) per l'applicazione di controllo. L'applicazione può usare questa notifica per ripristinare lo stato di un pulsante a schermo intero, ad esempio. Le notifiche di **\_ attivazione EC** vengono utilizzate internamente da DirectShow per gestire l'attivazione a schermo intero di suggerimenti dai renderer video.

## <a name="summary-of-notifications"></a>Riepilogo delle notifiche

In questa sezione sono elencate le notifiche del grafico di filtro che un renderer può inviare.



| Notifica degli eventi                                        | Descrizione                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_attivazione EC**](ec-activate.md)                       | Inviato dai renderer video in modalità di rendering a schermo intero per ogni \_ messaggio WM ACTIVATEAPP ricevuto.                                                                                                  |
| [**EC \_ completato**](ec-complete.md)                       | Inviato dai renderer dopo che è stato eseguito il rendering di tutti i dati.                                                                                                                                               |
| [**visualizzazione di EC \_ \_ modificata**](ec-display-changed.md)        | Inviato dai renderer video quando cambia il formato di visualizzazione.                                                                                                                                            |
| [**\_tavolozza EC \_ modificata**](ec-palette-changed.md)        | Inviato ogni volta che un renderer video rileva una modifica della tavolozza nel flusso.                                                                                                                            |
| [**ridisegno EC \_**](ec-repaint.md)                         | Inviato dai renderer video interrotti o sospesi quando \_ viene ricevuto un messaggio di disegno WM e non sono presenti dati da visualizzare. In questo modo, il gestore del grafico dei filtri genera un frame da disegnare sullo schermo. |
| [**\_USERABORT EC**](ec-userabort.md)                     | Inviato dai renderer video per segnalare una chiusura richiesta dall'utente, ad esempio un utente che chiude la finestra del video.                                                                               |
| [**\_dimensioni del video EC \_ \_ modificate**](ec-video-size-changed.md) | Inviato dai renderer video ogni volta che viene rilevata una modifica nelle dimensioni del video nativo.                                                                                                                       |
| [**\_finestra EC \_ distrutta**](ec-window-destroyed.md)      | Inviato dai renderer video quando il filtro viene rimosso o eliminato in modo che le risorse che dipendono dallo stato attivo della finestra possano essere passate ad altri filtri.                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di renderer video](writing-video-renderers.md)
</dt> </dl>

 

 
