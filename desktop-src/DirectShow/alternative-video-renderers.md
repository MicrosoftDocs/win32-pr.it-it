---
description: Questo argomento descrive come scrivere un renderer video personalizzato per DirectShow.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Renderer video alternativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd105f406e1b39d998a027a915621f214ec2e769f373912a1e9e8525573f31aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074805"
---
# <a name="alternative-video-renderers"></a>Renderer video alternativi

Questo argomento descrive come scrivere un renderer video personalizzato per DirectShow.

> [!Note]  
> Invece di scrivere un renderer video personalizzato, è consigliabile scrivere un allocatore-presenter plug-in per il renderer di combinazione video (VMR) o il [**renderer video**](enhanced-video-renderer-filter.md) avanzato (EVR). Questo approccio offre tutti i vantaggi di VMR/EVR, incluso il supporto per l'accelerazione video DirectX (DXVA), il denterlacciamento hardware e l'esecuzione passo a passo dei fotogrammi ed è probabilmente più affidabile rispetto a un renderer video personalizzato. Per altre informazioni, vedere i seguenti argomenti:
>
> -   [Modalità di riproduzione senza rendering di VMR (allocator-presenter personalizzati)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Come scrivere un presentatore EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Scrittura di un renderer alternativo

Microsoft DirectShow fornisce un renderer video basato su finestra; fornisce anche un renderer a schermo intero nell'installazione in fase di esecuzione. È possibile usare le classi DirectShow base per scrivere renderer video alternativi. Perché i renderer alternativi interagiscano correttamente con le DirectShow basate su DirectShow, i renderer devono rispettare le linee guida descritte in questo articolo. È possibile usare le [**classi CBaseRenderer**](cbaserenderer.md) e [**CBaseVideoRenderer**](cbasevideorenderer.md) per seguire queste linee guida quando si implementa un rendering video alternativo. A causa dello sviluppo continuo di DirectShow, esaminare periodicamente l'implementazione per assicurarsi che i renderer siano compatibili con la versione più recente di DirectShow.

In questo argomento vengono illustrate molte notifiche che un renderer è responsabile della gestione. Una breve revisione delle DirectShow può essere utile per impostare la fase. Esistono essenzialmente tre tipi di notifiche che si verificano in DirectShow:

-   *Notifiche di flusso,* che sono eventi che si verificano nel flusso multimediale e vengono passati da un filtro a quello successivo. Possono essere notifiche di inizio scaricamento, scaricamento finale o fine flusso e vengono inviate chiamando il metodo appropriato sul pin di input del filtro downstream (ad esempio [**IPin::BeginFlush).**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)
-   *Filtrare le notifiche del* grafico, che sono eventi inviati da un filtro a Filter Graph Manager, ad esempio [**EC \_ COMPLETE.**](ec-complete.md) Questa operazione viene eseguita chiamando il [**metodo IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) in Filter Graph Manager.
-   *Notifiche dell'applicazione*, recuperate da Filter Graph Manager dall'applicazione di controllo. Un'applicazione chiama [**il metodo IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in Filter Graph Manager per recuperare questi eventi. Spesso, l'Graph gestione filtri passa gli eventi ricevuti all'applicazione.

In questo argomento viene illustrata la responsabilità del filtro del renderer nella gestione delle notifiche di flusso ricevute e nell'invio di notifiche appropriate del grafico dei filtri.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Gestione delle notifiche di fine flusso e scaricamento

Una notifica di fine flusso inizia in corrispondenza di un filtro upstream,ad esempio il filtro di origine, quando tale filtro rileva che non può inviare altri dati. Viene passato attraverso ogni filtro nel grafico e alla fine termina in corrispondenza del renderer, responsabile dell'invio successivo di una notifica [**EC \_ COMPLETE**](ec-complete.md) a Filter Graph Manager. I renderer hanno responsabilità speciali quando si tratta di gestire queste notifiche.

Un renderer riceve una notifica di fine flusso quando il metodo [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) del pin di input viene chiamato dal filtro upstream. Un renderer deve prendere nota di questa notifica e continuare a eseguire il rendering dei dati già ricevuti. Dopo che tutti i dati rimanenti sono stati ricevuti, il renderer deve inviare una notifica [**EC \_ COMPLETE**](ec-complete.md) a Filter Graph Manager. La **notifica EC \_ COMPLETE** deve essere inviata una sola volta da un renderer ogni volta che raggiunge la fine di un flusso. Inoltre, le **notifiche EC \_ COMPLETE** non devono mai essere inviate tranne quando il grafico dei filtri è in esecuzione. Pertanto, se il grafico dei filtri viene sospeso quando un filtro di origine invia una notifica di fine flusso, **EC \_ COMPLETE** non deve essere inviato fino a quando il grafico del filtro non viene eseguito.

Tutte le chiamate ai metodi [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) dopo la segnalazione di una notifica di fine flusso devono essere rifiutate. **E \_ UNEXPECTED** è il messaggio di errore più appropriato da restituire in questo caso.

Quando un grafo del filtro viene arrestato, qualsiasi notifica di fine flusso memorizzata nella cache deve essere cancellata e non inviata di nuovo all'avvio successivo. Questo avviene perché Filter Graph Manager sospende sempre tutti i filtri appena prima di eseguire i filtri in modo che si verifichi lo scaricamento corretto. Pertanto, ad esempio, se il grafico dei filtri viene sospeso e viene ricevuta una notifica di fine flusso e quindi il grafico dei filtri viene arrestato, il renderer non deve inviare una notifica [**EC \_ COMPLETE**](ec-complete.md) quando viene eseguito successivamente. Se non è stata eseguita alcuna ricerca, il filtro di origine invierà automaticamente un'altra notifica di fine flusso durante lo stato di sospensione che precede uno stato di esecuzione. Se, d'altra parte, si è verificata una ricerca mentre il grafico dei filtri è arrestato, il filtro di origine potrebbe avere dati da inviare, quindi non invierà una notifica di fine flusso.

I renderer video spesso dipendono dalle notifiche di fine flusso per un tempo maggiore rispetto all'invio di [**notifiche EC \_ COMPLETE.**](ec-complete.md) Ad esempio, se la riproduzione di un flusso è terminata (ovvero viene inviata una notifica di fine flusso) e un'altra finestra viene trascinata su una finestra del renderer video, verranno generati alcuni messaggi della finestra [**WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) La procedura tipica per l'esecuzione di renderer video consiste nell'evitare di ridisegnare il fotogramma corrente alla ricezione di messaggi **WM \_ PAINT** (in base al presupposto che verrà ricevuto un altro fotogramma da disegnare). Tuttavia, quando viene inviata la notifica di fine flusso, il renderer è in uno stato di attesa. è ancora in esecuzione, ma è consapevole che non riceverà dati aggiuntivi. In queste circostanze, il renderer disegna in modo personalizzato l'area di riproduzione nera.

La gestione dello scaricamento è una complicazione aggiuntiva per i renderer. Lo scaricamento viene eseguito tramite una coppia di [**metodi IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) denominati [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) [**ed EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) Lo scaricamento è essenzialmente uno stato aggiuntivo che il renderer deve gestire. Non è valido che un filtro di origine chiami **BeginFlush** senza **chiamare EndFlush,** quindi lo stato dovrebbe essere breve e discreto. Tuttavia, il renderer deve gestire correttamente i dati o le notifiche ricevute durante la transizione di scaricamento.

Tutti i dati ricevuti dopo [**la chiamata a BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) devono essere rifiutati immediatamente con la restituzione **di S \_ FALSE.** Inoltre, qualsiasi notifica di fine flusso memorizzata nella cache deve essere cancellata anche quando un renderer viene scaricato. Un renderer viene in genere scaricato in risposta a una ricerca. Lo scaricamento garantisce che i dati precedenti siano cancellati dal grafico dei filtri prima dell'invio di nuovi campioni. In genere, la riproduzione di due sezioni di un flusso, una dopo l'altra, viene gestita meglio tramite comandi posticimanti anziché attendere il completamento di una sezione e quindi l'esecuzione di un comando di ricerca.

## <a name="handling-state-changes-and-pause-completion"></a>Gestione delle modifiche di stato e sospensione del completamento

Un filtro renderer si comporta come qualsiasi altro filtro nel grafico dei filtri quando ne viene modificato lo stato, con l'eccezione seguente. Dopo la sospensione, il renderer avrà alcuni dati in coda, pronti per il rendering quando verranno eseguiti successivamente. Quando il renderer video viene arrestato, mantiene i dati in coda. Si tratta di un'eccezione alla regola DirectShow che nessuna risorsa deve essere mantenuta dai filtri mentre il grafico dei filtri viene arrestato.

Il motivo di questa eccezione è che, mantenendo le risorse, il renderer avrà sempre un'immagine con cui ridisegnare la finestra se riceve un [**messaggio WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) Include anche un'immagine per soddisfare i metodi, ad esempio [**CBaseControlVideo::GetStaticImage**](cbasecontrolvideo-getstaticimage.md), che richiedono una copia dell'immagine corrente. Un altro effetto della gestione delle risorse è che l'allocazione dell'immagine impedisce il discommitted dell'allocatore, che a sua volta rende la successiva modifica dello stato molto più veloce perché i buffer dell'immagine sono già allocati.

Un renderer video deve eseguire il rendering e rilasciare gli esempi solo durante l'esecuzione. Mentre è in pausa, il filtro potrebbe eseguirne il rendering (ad esempio, quando si disegna un'immagine poster statica in una finestra), ma non deve rilasciarli. I renderer audio non eseguiranno il rendering mentre sono in pausa,anche se possono eseguire altre attività, ad esempio la preparazione del dispositivo audio. L'ora in cui eseguire il rendering degli esempi viene ottenuta combinando l'ora del flusso nell'esempio con l'ora di riferimento passata come parametro al [**metodo IMediaControl::Run.**](/windows/desktop/api/Control/nf-control-imediacontrol-run) I renderer devono rifiutare i campioni con orari di inizio inferiori o uguali all'ora di fine.

Quando un'applicazione sospende un grafico dei filtri, il grafico dei filtri non viene restituito dal relativo metodo [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) finché non vengono accodati i dati nei renderer. Per garantire questo risultato, quando un renderer viene sospeso, deve restituire S FALSE se non sono presenti dati \_ in attesa di rendering. Se i dati sono accodati, può restituire **S \_ OK**.

Gestione filtri Graph controlla tutti i valori restituiti durante la sospensione di un grafico di filtro, per assicurarsi che i renderer siano accodati. Se uno o più filtri non sono pronti, Filter Graph Manager esegue il polling dei filtri nel grafico chiamando [**IMediaFilter::GetState.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) Il **metodo GetState** accetta un parametro di timeout. Un filtro (in genere un renderer) che è ancora in attesa dell'arrivo dei dati prima di completare la modifica dello stato restituisce **VFW \_ S \_ STATE \_ INTERMEDIATE** se il **metodo GetState** scade. Quando i dati arrivano al renderer, **GetState** deve essere restituito immediatamente con **S \_ OK.**

Sia nello stato intermedio che in quello completato, lo stato del filtro segnalato sarà Stato \_ sospeso. Solo il valore restituito indica se il filtro è effettivamente pronto o meno. Se, mentre un renderer è in attesa dell'arrivo dei dati, il filtro di origine invia una notifica di fine flusso, che dovrebbe completare anche la modifica dello stato.

Quando tutti i filtri hanno effettivamente i dati in attesa di essere sottoposti a rendering, il grafico dei filtri completerà la modifica dello stato di sospensione.

## <a name="handling-termination"></a>Gestione della terminazione

I renderer video devono gestire correttamente gli eventi di terminazione dell'utente. Ciò implica che la finestra viene nascosta correttamente e si sa cosa fare se successivamente viene forzata la visualizzazione di una finestra. Inoltre, i renderer video devono notificare a Filter Graph Manager quando la relativa finestra viene eliminata definitivamente (o, più precisamente, quando il renderer viene rimosso dal grafico dei filtri) per liberare risorse.

Se l'utente chiude la finestra video,ad esempio premendo ALT+F4, la convenzione è nascondere immediatamente la finestra e inviare una notifica [**\_ EC USERABORT**](ec-userabort.md) a Filter Graph Manager. Questa notifica viene passata all'applicazione, che interrompe la riproduzione del grafo. Dopo **\_ l'invio di EC USERABORT,** un renderer video deve rifiutare eventuali campioni aggiuntivi recapitati.

Il flag graph-stopped deve essere lasciato in esecuzione dal renderer fino a quando non viene successivamente arrestato, a quel punto deve essere reimpostato in modo che un'applicazione possa eseguire l'override dell'azione dell'utente e continuare a riprodurre il grafico, se lo desidera. Se si preme ALT+F4 mentre il video è in esecuzione, la finestra verrà nascosta e tutti gli altri campioni recapitati verranno rifiutati. Se la finestra viene visualizzata successivamente (ad esempio tramite [**IVideoWindow::p ut \_ Visible),**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)non deve essere generata alcuna notifica [**EC \_ REPAINT.**](ec-repaint.md)

Il renderer video deve anche inviare la notifica [**EC \_ WINDOW \_ DESTROYED**](ec-window-destroyed.md) al grafico dei filtri quando il renderer video viene terminato. In realtà, è meglio gestirlo quando il metodo [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del renderer viene chiamato con un parametro Null (che indica che il renderer sta per essere rimosso dal grafico del filtro), anziché attendere che la finestra video effettiva venga eliminata definitivamente. L'invio di questa notifica consente al distributore di plug-in in Filter Graph Manager di passare le risorse che dipendono dalla finestra attiva ad altri filtri, ad esempio i dispositivi audio.

## <a name="handling-dynamic-format-changes"></a>Gestione delle modifiche al formato dinamico

In alcuni casi, il filtro upstream del renderer potrebbe provare a modificare il formato video durante la riproduzione del video. Nella maggior parte dei casi è il decompressore video ad avviare una modifica del formato dinamico.

Un filtro upstream che tenta di modificare dinamicamente i formati deve sempre chiamare il metodo [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di input del renderer. Un renderer video ha un certo grado di disaveglianza per i tipi di modifiche al formato dinamico che deve supportare. Come minimo, deve consentire al filtro upstream di modificare i palette. Quando un filtro upstream modifica i tipi di supporti, collega il tipo di supporto al primo esempio fornito nel nuovo formato. Se il renderer contiene esempi in una coda per il rendering, non deve modificare il formato finché non esegue il rendering dell'esempio con la modifica del tipo.

Un renderer video può anche richiedere una modifica del formato dal decodificatore. Ad esempio, potrebbe chiedere al decodificatore di fornire un formato compatibile con DirectDraw con **un valore biHeight negativo.** Quando il renderer viene sospeso, deve chiamare [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin upstream per vedere i formati che il decodificatore può fornire. Tuttavia, il decodificatore potrebbe non enumerare tutti i tipi che può accettare, quindi il renderer deve offrire alcuni tipi anche se il decodificatore non li annuncia.

Se il decodificatore può passare al formato richiesto, restituisce **S \_ OK** da [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept). Il renderer collega quindi il nuovo tipo di supporto all'esempio di supporti successivo nell'allocatore upstream. Per il funzionamento, il renderer deve fornire un allocatore personalizzato che implementa un metodo privato per associare il tipo di supporto all'esempio successivo. All'interno di questo metodo privato chiamare [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) per impostare il tipo.

Il pin di input del renderer deve restituire l'allocatore personalizzato del renderer nel [**metodo IMemInputPin::GetAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) Eseguire [**l'override di IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) in modo che non riesca se il filtro upstream non usa l'allocatore del renderer.

Con alcuni decodificatori, impostando **biHeight** su un numero positivo per i tipi YUV, il decodificatore disegna l'immagine capovolta. Questo non è corretto e deve essere considerato un bug nel decodificatore.

Ogni volta che il renderer video rileva una modifica del formato, deve inviare una [**notifica EC \_ DISPLAY \_ CHANGED.**](ec-display-changed.md) La maggior parte dei renderer video seleziona un formato durante la connessione in modo che il formato possa essere disegnato in modo efficiente tramite GDI. Se l'utente modifica la modalità di visualizzazione corrente senza riavviare il computer, è possibile che un renderer si trovi con una connessione in formato immagine non valido e invii questa notifica. Il primo parametro deve essere il pin che deve essere riconnesso. La gestione Graph filtro disporrà l'arresto del grafo del filtro e la riconnessione del segnaposto. Durante la riconnessione successiva, il renderer può accettare un formato più appropriato.

Ogni volta che un renderer video rileva una modifica della tavolozza nel flusso, deve inviare la notifica [**EC \_ PALETTE \_ CHANGED**](ec-palette-changed.md) a Filter Graph Manager. I DirectShow renderer video rilevano se una tavolozza è cambiata o meno in formato dinamico. I renderer video lo fanno non solo per filtrare il numero di notifiche **EC \_ PALETTE \_ CHANGED** inviate, ma anche per ridurre la quantità di creazione, installazione ed eliminazione del riquadro richiesto.

Infine, il renderer video potrebbe anche rilevare che le dimensioni del video sono cambiate, nel qual caso deve inviare la notifica [**EC \_ VIDEO SIZE \_ \_ CHANGED.**](ec-video-size-changed.md) Un'applicazione potrebbe usare questa notifica per negoziare lo spazio in un documento composto. Le dimensioni video effettive sono disponibili tramite l'interfaccia di controllo [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) I DirectShow renderer rilevano se le dimensioni del video sono cambiate o meno prima di inviare questi eventi.

## <a name="handling-persistent-properties"></a>Gestione delle proprietà persistenti

Tutte le proprietà impostate tramite [**le interfacce IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) e [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) devono essere persistenti tra le connessioni. Di conseguenza, la disconnessione e la riconnessione di un renderer non dovrebbero mostrare effetti sulle dimensioni, sulla posizione o sugli stili della finestra. Tuttavia, se le dimensioni del video cambiano tra le connessioni, il renderer deve reimpostare i rettangoli di origine e di destinazione sui valori predefiniti. Le posizioni di origine e di destinazione vengono impostate tramite **l'interfaccia IBasicVideo.**

Sia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) che [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) forniscono accesso sufficiente alle proprietà per consentire a un'applicazione di salvare e ripristinare tutti i dati nell'interfaccia in un formato permanente. Ciò sarà utile per le applicazioni che devono salvare la configurazione e le proprietà esatte dei grafici di filtro durante una sessione di modifica e ripristinarli in un secondo momento.

## <a name="handling-ec_repaint-notifications"></a>Gestione delle notifiche EC \_ REPAINT

La [**notifica EC \_ REPAINT**](ec-repaint.md) viene inviata solo quando il renderer viene sospeso o arrestato. Questa notifica segnala a Filter Graph Manager che il renderer necessita di dati. Se il grafico dei filtri viene arrestato quando riceve una di queste notifiche, sospende il grafico dei filtri, attende che tutti i filtri ricevano i dati (chiamando [**GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)) e quindi lo arresta nuovamente. Quando viene arrestato, un renderer video deve mantenere l'immagine in modo che i messaggi [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) successivi possano essere gestiti.

Pertanto, se un renderer video riceve un messaggio [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) quando viene arrestato o sospeso e non ha nulla con cui disegnare la finestra, deve inviare [**EC \_ REPAINT**](ec-repaint.md) a Filter Graph Manager. Se durante la sospensione viene ricevuta una notifica **EC \_ REPAINT,** Filter Graph Manager chiama [**IMediaPosition::p ut \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) con la posizione corrente, ovvero cerca la posizione corrente. In questo modo, i filtri di origine scaricano il grafico dei filtri e determinano l'invio di nuovi dati tramite il grafico dei filtri.

Un renderer deve inviare solo una di queste notifiche alla volta. Pertanto, dopo che il renderer ha inviato una notifica, deve assicurarsi che non ne siano stati inviati altri fino a quando non vengono recapitati alcuni campioni. Il modo convenzionale per eseguire questa operazione è avere un flag che indica che è possibile inviare un ridisegno, che viene disattivato dopo l'invio di una notifica [**EC \_ REPAINT.**](ec-repaint.md) Questo flag deve essere reimpostato quando i dati vengono recapitati o quando il pin di input viene scaricato, ma non se la fine del flusso viene segnalata sul pin di input.

Se il renderer non monitora le notifiche [**EC \_ REPAINT,**](ec-repaint.md) inonda filter Graph Manager con richieste **EC \_ REPAINT** (che sono relativamente costose da elaborare). Ad esempio, se un renderer non ha immagini da disegnare e un'altra finestra viene trascinata nella finestra del renderer in un'operazione di trascinamento completo, il renderer riceve più messaggi [**WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) Solo il primo di questi deve generare una notifica **dell'evento EC \_ REPAINT** dal renderer a Filter Graph Manager.

Un renderer deve inviare il pin di input come primo parametro alla [**notifica EC \_ REPAINT.**](ec-repaint.md) In questo modo, verrà eseguita una query sul pin di output collegato per [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)e, se supportato, la notifica **EC \_ REPAINT** verrà inviata per prima. In questo modo i segnaposto di output possono gestire i ridisegni prima che il grafico dei filtri venga toccato. Questa operazione non verrà eseguita se il grafo del filtro viene arrestato, perché non sono disponibili buffer dall'allocatore del renderer di cui è stato eseguito il discommitted.

Se il pin di output non è in grado di gestire la richiesta e il grafico dei filtri è in esecuzione, la notifica [**EC \_ REPAINT**](ec-repaint.md) viene ignorata. Un pin di output deve restituire **S \_ OK** da [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) per segnalare che la richiesta di ridisegno è stata elaborata correttamente. Il pin di output verrà chiamato nel thread di lavoro di Filter Graph Manager, che evita che il renderer chiami direttamente il pin di output e quindi esere evita eventuali problemi di deadlock. Se il grafico dei filtri viene arrestato o sospeso e l'output non gestisce la richiesta, viene eseguita l'elaborazione predefinita.

## <a name="handling-notifications-in-full-screen-mode"></a>Gestione delle notifiche in modalità Full-Screen predefinita

Il distributore plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) nel grafico dei filtri gestisce la riproduzione a schermo intero. Verrà scambiato un renderer video per un renderer a schermo intero specializzato, si estenderà una finestra di un renderer a schermo intero o il renderer implementerà direttamente la riproduzione a schermo intero. Per interagire con protocolli a schermo intero, un renderer video deve inviare una notifica [**EC \_ ACTIVATE**](ec-activate.md) ogni volta che la relativa finestra viene attivata o disattivata. In altre parole, deve essere inviata una notifica **EC \_ ACTIVATE** per ogni messaggio WM ACTIVATEAPP ricevuto \_ da un renderer.

Quando un renderer viene usato in modalità schermo intero, queste notifiche gestiscono il passaggio da e verso tale modalità a schermo intero. La disattivazione della finestra si verifica in genere quando un utente preme ALT+TAB per passare a un'altra finestra, che il renderer DirectShow schermo intero usa come segnale per tornare alla modalità di rendering tipica.

Quando la notifica [**EC \_ ACTIVATE**](ec-activate.md) viene inviata a Filter Graph Manager quando si esce dalla modalità schermo intero, Filter Graph Manager invia una notifica [**EC \_ FULLSCREEN \_ LOST**](ec-fullscreen-lost.md) all'applicazione di controllo. L'applicazione potrebbe usare questa notifica per ripristinare lo stato di un pulsante a schermo intero, ad esempio. Le **notifiche \_ EC ACTIVATE** vengono usate internamente da DirectShow per gestire il passaggio a schermo intero sui segnali dai renderer video.

## <a name="summary-of-notifications"></a>Riepilogo delle notifiche

In questa sezione sono elencate le notifiche del grafico dei filtri che un renderer può inviare.



| Notifica degli eventi                                        | Descrizione                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ ACTIVATE**](ec-activate.md)                       | Inviati dai renderer video in modalità di rendering a schermo intero per ogni messaggio WM \_ ACTIVATEAPP ricevuto.                                                                                                  |
| [**COMPLETAMENTO \_ EC**](ec-complete.md)                       | Inviato dai renderer dopo il rendering di tutti i dati.                                                                                                                                               |
| [**VISUALIZZAZIONE \_ EC \_ MODIFICATA**](ec-display-changed.md)        | Inviato dai renderer video quando cambia il formato di visualizzazione.                                                                                                                                            |
| [**TAVOLOZZA \_ EC \_ MODIFICATA**](ec-palette-changed.md)        | Inviato ogni volta che un renderer video rileva una modifica della tavolozza nel flusso.                                                                                                                            |
| [**EC \_ REPAINT**](ec-repaint.md)                         | Inviati dai renderer video arrestati o sospesi quando viene ricevuto un messaggio WM \_ PAINT e non sono presenti dati da visualizzare. In questo modo, gestione Graph filtro genera un frame da disegnare sulla visualizzazione. |
| [**EC \_ USERABORT**](ec-userabort.md)                     | Inviati dai renderer video per segnalare una chiusura richiesta dall'utente(ad esempio, un utente che chiude la finestra video).                                                                               |
| [**DIMENSIONI \_ VIDEO \_ EC \_ MODIFICATE**](ec-video-size-changed.md) | Inviato dai renderer video ogni volta che viene rilevata una modifica nelle dimensioni native del video.                                                                                                                       |
| [**FINESTRA \_ EC \_ DISTRUTTA**](ec-window-destroyed.md)      | Inviati dai renderer video quando il filtro viene rimosso o eliminato definitivamente in modo che le risorse che dipendono dallo stato attivo della finestra possano essere passate ad altri filtri.                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di renderer video](writing-video-renderers.md)
</dt> </dl>

 

 
