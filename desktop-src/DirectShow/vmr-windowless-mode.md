---
description: Modalità senza finestra VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Modalità senza finestra VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344371"
---
# <a name="vmr-windowless-mode"></a>Modalità senza finestra VMR

La modalità senza finestra è il modo migliore per le applicazioni per eseguire il rendering di video all'interno di una finestra dell'applicazione. In modalità senza finestra, il renderer di mixaggio video non carica il componente Window Manager e pertanto non supporta le interfacce [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) o [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Al contrario, l'applicazione fornisce la finestra di riproduzione e imposta un rettangolo di destinazione nell'area client per VMR per creare il video. VMR usa un oggetto di DirectDraw Clipper per garantire che il video venga ritagliato nella finestra dell'applicazione e non venga visualizzato in altre finestre. Il VMR non esegue la sottoclasse della finestra dell'applicazione né installa alcun hook di sistema/processo.

In modalità senza finestra, la sequenza di eventi durante la connessione e la transizione allo stato di esecuzione è la seguente:

-   Il filtro upstream propone un tipo di supporto, che il VMR accetta o rifiuta.
-   Se il tipo di supporto è accettato, il VMR chiama Allocator-Presenter per ottenere una superficie DirectDraw. Se la superficie viene creata correttamente, i pin Connect e VMR sono pronti per la transizione allo stato di esecuzione.
-   Quando viene eseguito il grafico dei filtri, il decodificatore chiama **GetBuffer** per ottenere un esempio di supporto dall'allocatore. VMR esegue una query su Allocator-Presenter per assicurarsi che la profondità dei pixel, le dimensioni del rettangolo e altri parametri sulla relativa superficie DirectDraw siano compatibili con il video in arrivo. Se sono compatibili, VMR restituisce la superficie DirectDraw al decodificatore. Dopo la decodifica della superficie del decodificatore, l'unità di sincronizzazione principale di VMR convalida i timestamp. Questa unità blocca la chiamata di **ricezione** fino a quando non arriva l'ora di presentazione. A questo punto, VMR chiama **PresentImage** su Allocator-Presenter, che presenta la superficie alla scheda grafica.

La figura seguente mostra il VMR in modalità senza finestra con più flussi di input.

![VMR in modalità senza finestra](images/vmr-windowless-mult-streams.png)

**Configurazione di VMR-7 per la modalità senza finestra**

Per configurare VMR-7 per la modalità senza finestra, eseguire tutti i passaggi seguenti prima di connettere i pin di input di VMR:

1.  Creare il filtro e aggiungerlo al grafico.
2.  Chiamare il metodo [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) con il flag VMRMode senza \_ finestra.
3.  Facoltativamente, configurare VMR per più flussi di input chiamando [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). VMR crea un pin di input per ogni flusso. Usare l'interfaccia [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) per impostare l'ordine Z e altri parametri per il flusso. Per altre informazioni, vedere [VMR con più flussi (modalità di combinazione)](vmr-with-multiple-streams--mixing-mode.md).

    Se non si chiama **SetNumberOfStreams**, il valore predefinito di VMR-7 è un pin di input. Una volta connessi i pin di input, il numero di pin non può essere modificato.

4.  Chiamare [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) per specificare la finestra in cui verrà visualizzato il video di cui è stato eseguito il rendering.

Una volta completati questi passaggi, è possibile connettere i pin di input del filtro VMR. Esistono diversi modi per creare il grafico, ad esempio la connessione diretta dei pin, l'uso di metodi di connessione intelligenti, ad esempio [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), o l'uso del metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) del generatore di grafici di acquisizione. Per ulteriori informazioni, vedere [General Graph-Building Techniques](general-graph-building-techniques.md).

Per impostare la posizione del video all'interno della finestra dell'applicazione, chiamare il metodo [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) . Il metodo [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) restituisce le dimensioni del video nativo. Durante la riproduzione, l'applicazione deve notificare al VMR i messaggi di Windows seguenti:

-   \_Disegno WM: chiamare [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) per ridisegnare l'immagine.
-   WM \_ DISPLAYCHANGE: chiamata [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). Il VMR esegue le azioni necessarie per visualizzare il video alla nuova risoluzione o alla profondità del colore.
-   \_Dimensioni WM: ricalcolare la posizione del video e chiamare di nuovo [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) , se necessario.

> [!Note]  
> Le applicazioni MFC devono definire un \_ gestore di messaggi WM ERASEBKGND vuoto oppure l'area di visualizzazione del video non viene ridisegnata correttamente.

 

**Configurazione di VMR-9 per la modalità senza finestra**

Per configurare VMR-9 per la modalità senza finestra, usare la procedura descritta per VMR-7 per la modalità senza finestra, ma usare le interfacce [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) e [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) . L'unica differenza significativa è che VMR-9 crea quattro pin di input per impostazione predefinita, anziché un pin di input. Pertanto, è necessario chiamare **SetNumberOfStreams** solo se si combinano più di quattro flussi video.

**Codice di esempio**

Il codice seguente illustra come creare un filtro VMR-7, aggiungerlo al grafo del filtro DirectShow e quindi inserire il VMR in modalità senza finestra. Per VMR-9 usare CLSID \_ VideoMixingRenderer9 in **CoCreateInstance** e le corrispondenti interfacce VMR-9.


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

 

 



