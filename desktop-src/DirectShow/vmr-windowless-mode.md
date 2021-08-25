---
description: Modalità senza finestra vmr
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Modalità senza finestra vmr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193f672e0fc1e3dced4bdff16da0e85123079eb94f2ac3c5fdb302b67c9432b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830586"
---
# <a name="vmr-windowless-mode"></a>Modalità senza finestra vmr

La modalità senza finestra è il modo preferito per le applicazioni di eseguire il rendering di video all'interno di una finestra dell'applicazione. In modalità senza finestra, il renderer di combinazione video non carica il componente Gestione finestre e pertanto non supporta le [**interfacce IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) o [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Al contrario, l'applicazione fornisce la finestra di riproduzione e imposta un rettangolo di destinazione nell'area client per il vmr per disegnare il video. La macchina virtuale usa un oggetto clipper DirectDraw per assicurarsi che il video venga ritagliato nella finestra dell'applicazione e non venga visualizzato in altre finestre. La macchina virtuale non sottoclassa la finestra dell'applicazione né installa alcun hook di sistema/processo.

In modalità senza finestra, la sequenza di eventi durante la connessione e la transizione allo stato di esecuzione è la seguente:

-   Il filtro upstream propone un tipo di supporto, che il vmr accetta o rifiuta.
-   Se il tipo di supporto viene accettato, la macchina virtuale chiama allocator-presenter per ottenere una superficie DirectDraw. Se la superficie viene creata correttamente, i pin si connettono e la macchina virtuale è pronta per la transizione allo stato di esecuzione.
-   Quando viene eseguito il grafo del filtro, il decodificatore chiama **GetBuffer** per ottenere un campione multimediale dall'allocatore. La macchina virtuale esegue una query sull'allocatore-presentatore per verificare che la profondità in pixel, le dimensioni del rettangolo e altri parametri sulla superficie DirectDraw siano compatibili con il video in ingresso. Se sono compatibili, la macchina virtuale restituisce la superficie DirectDraw al decodificatore. Dopo che il decodificatore è stato decodificato in superficie, l'unità di sincronizzazione principale della macchina virtuale convalida i timestamp. Questa unità blocca la **chiamata Receive** fino all'arrivo dell'ora di presentazione. A questo punto, la macchina virtuale chiama **PresentImage** sull'allocator-presenter, che presenta la superficie alla scheda grafica.

La figura seguente mostra la macchina virtuale in modalità senza finestra con più flussi di input.

![vmr in modalità senza finestra](images/vmr-windowless-mult-streams.png)

**Configurazione di VMR-7 per la modalità senza finestra**

Per configurare VMR-7 per la modalità senza finestra, eseguire tutti i passaggi seguenti prima di connettere uno dei pin di input della macchina virtuale:

1.  Creare il filtro e aggiungerlo al grafico.
2.  Chiamare il [**metodo IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) con il flag senza finestra VMRMode. \_
3.  Facoltativamente, configurare la macchina virtuale per più flussi di input chiamando [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). La macchina virtuale crea un pin di input per ogni flusso. Usare [**l'interfaccia IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) per impostare l'ordine Z e altri parametri per il flusso. Per altre informazioni, vedere VMR con più [Flussi (modalità di combinazione).](vmr-with-multiple-streams--mixing-mode.md)

    Se non si chiama **SetNumberOfStreams,** il valore predefinito di VMR-7 è un pin di input. Dopo la connessione dei pin di input, il numero di pin non può essere modificato.

4.  Chiamare [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) per specificare la finestra in cui verrà visualizzato il video sottoposto a rendering.

Al termine di questi passaggi, è possibile connettere i pin di input del filtro VMR. Esistono diversi modi per compilare il grafo, ad esempio connettendo i pin direttamente, usando metodi intelligent Connessione come [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)o usando il metodo [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) di Capture Graph Builder. Per altre informazioni, vedere [General Graph-Building Techniques](general-graph-building-techniques.md).

Per impostare la posizione del video all'interno della finestra dell'applicazione, chiamare il metodo [**IVMRWindowlessControl::SetVideoPosition.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) Il [**metodo IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) restituisce le dimensioni native del video. Durante la riproduzione, l'applicazione deve inviare una notifica al VMR dei messaggi Windows seguenti:

-   WM \_ PAINT: chiamare [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) per ridisegnare l'immagine.
-   WM \_ DISPLAYCHANGE: chiamare [**IVMRWindowlessControl::D isplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). La macchina virtuale prende tutte le azioni necessarie per visualizzare il video alla nuova risoluzione o profondità del colore.
-   WM \_ SIZE: ricalcolare la posizione del video e chiamare di nuovo [**SetVideoPosition,**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) se necessario.

> [!Note]  
> Le applicazioni MFC devono definire un gestore di messaggi WM \_ ERASEBKGND vuoto oppure l'area di visualizzazione video non verrà ridisegnata correttamente.

 

**Configurazione di VMR-9 per la modalità senza finestra**

Per configurare VMR-9 per la modalità senza finestra, seguire la procedura descritta per vmr-7 per la modalità senza finestra, ma usare le [**interfacce IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) e [**IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) L'unica differenza significativa è che vmr-9 crea quattro pin di input per impostazione predefinita, anziché un pin di input. Pertanto, è necessario chiamare **SetNumberOfStreams** solo se si combinano più di quattro flussi video.

**Codice di esempio**

Il codice seguente illustra come creare un filtro VMR-7, aggiungerlo al grafo del filtro DirectShow e quindi impostare la vmr in modalità senza finestra. Per VMR-9, usare CLSID \_ VideoMixingRenderer9 in **CoCreateInstance** e le interfacce VMR-9 corrispondenti.


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità senza finestra](using-windowless-mode.md)
</dt> </dl>

 

 



