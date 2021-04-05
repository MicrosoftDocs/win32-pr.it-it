---
description: Creazione del grafico del filtro DVD
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: Creazione del grafico del filtro DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d15c7d84ec138771e1f5da8be4270faae049cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125313"
---
# <a name="building-the-dvd-filter-graph"></a>Creazione del grafico del filtro DVD

Come per qualsiasi applicazione DirectShow, un'applicazione di riproduzione DVD inizia con la creazione di un grafico di filtro. DirectShow fornisce i componenti seguenti per la riproduzione DVD:

-   [Generatore di grafici DVD](dvd-graph-builder.md). Oggetto helper che costruisce il grafico del filtro. Espone l'interfaccia [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .
-   Filtro del [navigatore DVD](dvd-navigator-filter.md) . Filtro DirectShow che gestisce la riproduzione DVD, la navigazione e altri comandi.

La riproduzione DVD richiede anche un decodificatore MPEG-2. I decodificatori MPEG-2 hardware e software sono disponibili da terze parti. Per prima cosa, creare un'istanza dell'oggetto generatore di grafici DVD.


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



A questo punto, è possibile selezionare e configurare il renderer video prima di compilare il resto del grafo. Questo passaggio, facoltativo, viene descritto più dettagliatamente nella sezione successiva. Se si omette questo passaggio, il generatore di DVD Graph seleziona un renderer predefinito. Compilare quindi il grafo chiamando il metodo [**IDvdGraphBuilder:: RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) .


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



Il primo parametro è il nome di una directory che contiene i file DVD. In un disco DVD questi file si trovano in una directory denominata VIDEO \_ TS. Se il primo parametro è **null**, il generatore di DVD Graph usa la prima unità che contiene un volume DVD.

Il secondo parametro contiene diversi flag facoltativi per la scelta del tipo di decodificatore (hardware o software) e di altre opzioni.

Il terzo parametro è una [**struttura \_ \_ RENDERSTATUS DVD**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) che riceve informazioni sullo stato. Se il metodo [**RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) restituisce \_ false, significa che la chiamata è parzialmente riuscita (o parzialmente non riuscita, se si è un pessimistico). Ad esempio, il metodo potrebbe non essere in grado di eseguire il rendering del flusso dell'immagine, anche se gli altri flussi sono stati visualizzati correttamente. Se il metodo **RenderDvdVideoVolume** restituisce un codice di errore o il valore di \_ false, è possibile esaminare la struttura di **\_ \_ RENDERSTATUS per DVD** per informazioni dettagliate sull'errore.

Ottenere quindi un puntatore al gestore del grafico del filtro chiamando [**IDvdGraphBuilder:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph). Questo metodo restituisce un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gestore del grafico dei filtri.


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



Usare il metodo [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) per recuperare le interfacce correlate a DVD, incluse le seguenti:

-   [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2). Controlla i comandi di riproduzione e DVD
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2). Restituisce informazioni sullo stato corrente del navigatore DVD.
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder). Controlla la visualizzazione della didascalia chiusa. La visualizzazione didascalia chiusa è abilitata per impostazione predefinita. Per disabilitarla, chiamare [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) con il \_ flag AM L21 \_ CCSTATE \_ off.
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio). Controlla il volume e il bilanciamento audio.

Il codice seguente, ad esempio, restituisce l'interfaccia [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



Il modo consigliato per creare il grafico del filtro per la riproduzione DVD consiste nel fare in modo che un oggetto [Generatore di grafici DVD](dvd-graph-builder.md) esegua automaticamente questa operazione. Questo approccio è illustrato di seguito e nell'applicazione di esempio DVD. Se è necessario creare manualmente il grafico del filtro DVD, è possibile eseguire questa operazione seguendo le regole di base della creazione di un grafico illustrate altrove nella documentazione di DirectShow. In genere, è consigliabile non aggiungere, rimuovere, connettere o disconnettere manualmente i singoli filtri nel grafico creato dal generatore di DVD Graph, perché questa operazione potrebbe confondere il codice di pulizia.

Configurazione del renderer video

DirectShow offre diversi filtri per renderer video. Prima di compilare il grafico, è possibile scegliere quale renderer video si preferisce. Selezionare il renderer chiamando [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) e richiedendo un'interfaccia specifica per il renderer:

-   Filtro del mixer sovrapposto: [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).
-   Renderer di video mixing 7 (VMR-7): [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).
-   Renderer di video mixing 9 (VMR-9): [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).
-   Renderer video migliorato (EVR): [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).

Se si richiede una di queste interfacce prima di creare il grafico del filtro, il generatore di DVD Graph crea il renderer video corrispondente. Successivamente, quando si compila il grafico, il generatore di DVD Graph tenterà di usare il renderer. Tuttavia, se non è possibile compilare il grafo utilizzando il renderer selezionato, può passare a un altro renderer. Ad esempio, il decodificatore MPEG-2 potrebbe non essere compatibile con il filtro VMR, nel qual caso il generatore di DVD Graph utilizzerà per impostazione predefinita il mixer sovrapposto.

Queste interfacce offrono inoltre la possibilità di configurare il renderer prima che sia connesso al decodificatore. Ad esempio, è possibile impostare VMR per usare la modalità senza finestra anziché la modalità finestra predefinita. Per ulteriori informazioni sui renderer video, vedere l'argomento [relativo al rendering video in DirectShow](about-video-rendering-in-directshow.md).

In Windows XP e versioni successive, il generatore di grafici DVD usa sempre il [renderer di mixaggio video 7](video-mixing-renderer-filter-7.md) (VMR-7), a meno che non sia:

-   Le interfacce di query del chiamante hanno trovato solo il [mixer overlay](overlay-mixer-filter.md), ad esempio [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). In questo modo viene inviato un suggerimento al generatore di grafici DVD che l'applicazione vuole usare il mixer overlay e non il VMR. Windows Media Player dispone inoltre di un'opzione della finestra di dialogo per forzare l'utilizzo del mixer overlay.
-   Il decoder installato non è compatibile con VMR. Durante la creazione del grafico, la nuova interfaccia [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) viene utilizzata per verificare il supporto VMR del decodificatore. Se non è presente, il generatore di grafici DVD utilizzerà il mixer sovrapposto.
-   Quando si utilizza un decodificatore hardware, il decodificatore non è in grado di connettersi a [video Port Manager](video-port-manager.md) (VPM). Se un decodificatore hardware non è in grado di utilizzare VPM, non potrà utilizzare VMR e quindi il generatore di DVD Graph tenterà di compilare un grafo utilizzando il mixer overlay.
-   La scheda video è nota per avere risorse e/o funzionalità insufficienti per supportare il VMR, ma non segnala correttamente questo problema nel driver. (Alcuni casi noti sono esclusi in modo specifico dal generatore di grafici DVD).
-   La connessione tra il decodificatore e il VMR non riesce per qualsiasi motivo, in genere a causa della mancanza di VRAM per creare le superfici necessarie. In questi casi, il generatore di DVD Graph disattiva l'uso di VMR e prova a usare il mixer overlay per compilare un grafo.

Modalità finestra

In modalità finestra (mixer sovrapposto o VMR), il renderer crea la propria finestra video. Per rendere questa finestra un elemento figlio della finestra dell'applicazione, chiamare [**IVideoWindow::p \_ proprietario UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un handle per l'applicazione. Chiamare anche [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) per impostare gli \_ stili WS Child e WS \_ CLIPSIBLINGS nella finestra video del renderer. Per ottenere i messaggi del mouse dalla finestra video del renderer, chiamare [**IVideoWindow::p UT \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) con un handle per la finestra dell'applicazione. Questo metodo imposta un "svuotamento del messaggio": la finestra del video inoltra tutti i messaggi del mouse ricevuti alla finestra di svuotamento del messaggio.


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



Lo svuotamento del messaggio semplifica la selezione dei pulsanti di menu DVD. Supponendo che la finestra del video non riempia l'intera area client dell'applicazione, alcuni eventi del mouse rientrano all'esterno della finestra del video. Quando si ottiene un evento del mouse *dalla finestra* video, è necessario elaborarlo per la navigazione nel menu DVD. Gli eventi del mouse dall' *esterno* della finestra video non devono essere elaborati. Con lo svuotamento del messaggio, non è possibile distinguere tra i due. Inoltre, le coordinate per gli eventi del mouse dalla finestra video sono relative all'area client della finestra video; ma gli eventi del mouse dall'esterno della finestra video sono relativi all'area client dell'applicazione.

Modalità senza finestra

La modalità senza finestra evita i problemi con i messaggi del mouse. Non è necessario un svuotamento dei messaggi perché VMR (o EVR) non crea la propria finestra in modalità senza finestra. Viene invece disegnato direttamente nella finestra dell'applicazione. Se il rettangolo di destinazione è più piccolo dell'area client dell'applicazione, il navigatore DVD prende in considerazione questo aspetto quando calcola le posizioni dei pulsanti DVD. Pertanto, quando si riceve un messaggio del mouse, è possibile passare le coordinate direttamente al navigatore DVD, come descritto nella sezione navigazione dei menu.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 
