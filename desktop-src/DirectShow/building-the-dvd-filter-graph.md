---
description: Compilazione del filtro DVD Graph
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: Compilazione del filtro DVD Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049c8bc52fd382be863cdf5a0e6b124534e0b9280d28536abc58a6f4e64e81e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662647"
---
# <a name="building-the-dvd-filter-graph"></a>Compilazione del filtro DVD Graph

Come per qualsiasi applicazione DirectShow, un'applicazione per la riproduzione di DVD inizia creando un grafo di filtro. DirectShow fornisce i componenti seguenti per la riproduzione di DVD:

-   [DVD Graph Builder](dvd-graph-builder.md). Oggetto helper che costruisce il grafico dei filtri. Espone [**l'interfaccia IDvdGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)
-   [Filtro DVD Navigator.](dvd-navigator-filter.md) Filtro DirectShow che gestisce la riproduzione, la navigazione e altri comandi dei DVD.

La riproduzione di DVD richiede anche un decodificatore MPEG-2. I decodificatori MPEG-2 hardware e software sono disponibili da terze parti. Creare prima di tutto un'istanza del DVD Graph Builder.


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



A questo punto, è possibile selezionare e configurare il renderer video prima di compilare il resto del grafico. Questo passaggio, facoltativo, viene descritto in modo più dettagliato nella sezione successiva. Se si omette questo passaggio, il DVD Graph Builder seleziona un renderer predefinito. Compilare quindi il grafo chiamando [**il metodo IDvdGraphBuilder::RenderDvdVideoVolume.**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume)


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



Il primo parametro è il nome di una directory che contiene i file DVD. Su un disco DVD questi file si trovano in una directory denominata VIDEO \_ TS. Se il primo parametro è **NULL,** il DVD Graph Builder usa la prima unità che contiene un volume DVD.

Il secondo parametro contiene vari flag facoltativi per la scelta del tipo di decodificatore (hardware o software) e altre opzioni.

Il terzo parametro è una [**struttura \_ AM DVD \_ RENDERSTATUS**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) che riceve informazioni sullo stato. Se il [**metodo RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) restituisce S FALSE, significa che la chiamata ha avuto esito positivo parziale (o parzialmente non riuscita, se si \_ è pessimisti). Ad esempio, il metodo potrebbe non riuscire a eseguire il rendering del flusso di immagini secondarie, anche se il rendering degli altri flussi ha esito positivo. Se il **metodo RenderDvdVideoVolume** restituisce un codice di errore o il valore S FALSE, è possibile esaminare la struttura AM DVD \_ **\_ \_ RENDERSTATUS** per informazioni dettagliate sull'errore.

Ottenere quindi un puntatore a Filter Graph Manager chiamando [**IDvdGraphBuilder::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph). Questo metodo restituisce un puntatore all'interfaccia [**Graph'interfaccia IGraphBuilder di Filter**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) Manager.


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



Usare il [**metodo IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) per recuperare le interfacce correlate al DVD, incluse le seguenti:

-   [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2). Controlla la riproduzione e i comandi DVD
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2). Restituisce informazioni sullo stato corrente dello strumento di navigazione DVD.
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder). Controlla la visualizzazione di sottotitoli codificati. La visualizzazione di sottotitoli codificati è abilitata per impostazione predefinita. Per disabilitarlo, chiamare [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) con il flag AM \_ L21 \_ CCSTATE \_ Off.
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio). Controlla il volume e il bilanciamento dell'audio.

Ad esempio, il codice seguente restituisce [**l'interfaccia IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



Il modo consigliato per creare il grafico del filtro di riproduzione DVD è fare in modo che un [oggetto DVD Graph Builder](dvd-graph-builder.md) eseere automaticamente. Questo approccio è illustrato di seguito e nell'applicazione di esempio DVD. Se è necessario compilare manualmente il grafico dei filtri DVD, è possibile farlo seguendo le regole di base per la creazione di grafi illustrate altrove nella documentazione DirectShow. In genere, non è consigliabile aggiungere, rimuovere, connettere o disconnettere manualmente singoli filtri nel grafico creato da DVD Graph Builder, perché in questo modo si potrebbe confondere il codice di pulizia.

Configurazione del renderer video

DirectShow fornisce diversi filtri di renderer video. Prima di compilare il grafo, è possibile scegliere il renderer video preferito. Selezionare il renderer chiamando [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) e richiedendo un'interfaccia specifica del renderer:

-   Overlay Mixer Filter: [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).
-   Video Mixing Renderer 7 (VMR-7): [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).
-   Video Mixing Renderer 9 (VMR-9): [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).
-   Enhanced Video Renderer (EVR): [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).

Se si richiede una di queste interfacce prima di compilare il grafico dei filtri, dvd Graph Builder crea il renderer video corrispondente. In seguito, quando si compila il grafo, il DVD Graph Builder tenterà di usare tale renderer. Tuttavia, se non è in grado di compilare il grafo usando il renderer selezionato, è possibile che si commuti a un altro renderer. Ad esempio, il decodificatore MPEG-2 potrebbe non essere compatibile con il filtro VMR, nel qual caso il DVD Graph Builder verrebbe utilizzato per impostazione predefinita la sovrimpressione Mixer.

Queste interfacce offrono anche la possibilità di configurare il renderer prima di essere connesso al decodificatore. Ad esempio, è possibile impostare la macchina virtuale per l'uso della modalità senza finestra anziché della modalità finestra predefinita. Per altre informazioni sui renderer video, vedere l'argomento [About Video Rendering in DirectShow](about-video-rendering-in-directshow.md).

In Windows XP e versioni successive, DVD Graph Builder usa sempre [il renderer](video-mixing-renderer-filter-7.md) di combinazione video 7 (VMR-7), a meno che:

-   Il chiamante esegue una query sulle interfacce e trova solo il [Mixer,](overlay-mixer-filter.md)ad [**esempio IMixerPinConfig2.**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) In questo modo viene inviato un suggerimento al DVD Graph Builder che l'applicazione vuole usare il Mixer sovrimpressione e non il VMR. Windows Media Player è disponibile anche un'opzione della finestra di dialogo per forzare l'uso del comando Sovrimpressione Mixer.
-   Il decodificatore installato non è compatibile con VMR. Durante la compilazione del grafo, viene usata la nuova interfaccia [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) per verificare il supporto vmr del decodificatore. Se non è presente, il DVD Graph Builder userà il comando Overlay Mixer.
-   Quando si usa un decodificatore hardware, il decodificatore non può connettersi a [Video Port Manager](video-port-manager.md) (VPM). Se un decodificatore hardware non può usare il VPM, non può usare la macchina virtuale e quindi DVD Graph Builder prova a creare un grafo usando il comando Overlay Mixer.
-   È noto che la scheda video non dispone di risorse e/o funzionalità sufficienti per supportare il ripristino della macchina virtuale, ma non segnala correttamente questo problema nel driver. Alcuni casi noti sono esclusi in modo specifico dal DVD Graph Builder.
-   La connessione tra il decodificatore e il VMR non riesce per qualsiasi motivo, in genere a causa della mancanza di VRAM per creare le superfici necessarie. In questi casi, IL DVD Graph Builder disattiva l'uso di VMR e tenta di usare la funzionalità di sovrapposizione Mixer creare un grafo.

Modalità finestra

In modalità finestra (overlay Mixer o VMR), il renderer crea la propria finestra video. Per rendere questa finestra figlio della finestra dell'applicazione, chiamare [**IVideoWindow::p ut \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un handle per l'applicazione. Chiamare anche [**IVideoWindow::p ut \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) per impostare gli stili WS CHILD e \_ WS CLIPSIBLINGS nella finestra \_ video del renderer. Per ottenere i messaggi del mouse dalla finestra video del renderer, chiamare [**IVideoWindow::p ut \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) con un handle per la finestra dell'applicazione. Questo metodo configura uno "svuotamento dei messaggi": la finestra video inoltra i messaggi del mouse ricevuti alla finestra di svuotamento dei messaggi.


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



Lo svuotamento dei messaggi rende più complicata la selezione dei pulsanti del menu DVD. Supponendo che la finestra video non riempia l'intera area client dell'applicazione, alcuni eventi del mouse non rientrano nella finestra video. Quando si ottiene un evento del mouse *dall'interno* della finestra video, è necessario elaborarlo per la navigazione nei menu dei DVD. Gli eventi del mouse *dall'esterno* della finestra video non devono essere elaborati. Con lo svuotamento dei messaggi, non è possibile distinguere tra i due. Inoltre, le coordinate per gli eventi del mouse dalla finestra video sono relative all'area client della finestra video; ma gli eventi del mouse dall'esterno della finestra video sono relativi all'area client dell'applicazione.

Modalità senza finestra

La modalità senza finestra evita completamente i problemi relativi ai messaggi del mouse. Non è necessario svuotare i messaggi, perché la macchina virtuale (o EVR) non crea la propria finestra in modalità senza finestra. Viene invece disegnata direttamente nella finestra dell'applicazione. Se il rettangolo di destinazione è più piccolo dell'area client dell'applicazione, lo Strumento di navigazione DVD prende in considerazione questo valore quando calcola le posizioni dei pulsanti DVD. Pertanto, quando viene visualizzato un messaggio del mouse, è possibile passare le coordinate direttamente a DVD Navigator, come descritto nella sezione Navigazione nei menu.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 
