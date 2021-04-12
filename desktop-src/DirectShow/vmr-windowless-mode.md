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
# <a name="vmr-windowless-mode"></a><span data-ttu-id="d0740-103">Modalità senza finestra VMR</span><span class="sxs-lookup"><span data-stu-id="d0740-103">VMR Windowless Mode</span></span>

<span data-ttu-id="d0740-104">La modalità senza finestra è il modo migliore per le applicazioni per eseguire il rendering di video all'interno di una finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d0740-104">Windowless mode is the preferred way for applications to render video inside an application window.</span></span> <span data-ttu-id="d0740-105">In modalità senza finestra, il renderer di mixaggio video non carica il componente Window Manager e pertanto non supporta le interfacce [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) o [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="d0740-105">In windowless mode, the Video Mixing Renderer does not load its Window Manager component, and therefore does not support the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) or [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interfaces.</span></span> <span data-ttu-id="d0740-106">Al contrario, l'applicazione fornisce la finestra di riproduzione e imposta un rettangolo di destinazione nell'area client per VMR per creare il video.</span><span class="sxs-lookup"><span data-stu-id="d0740-106">Instead, the application provides the playback window and sets a destination rectangle in the client area for the VMR to draw the video.</span></span> <span data-ttu-id="d0740-107">VMR usa un oggetto di DirectDraw Clipper per garantire che il video venga ritagliato nella finestra dell'applicazione e non venga visualizzato in altre finestre.</span><span class="sxs-lookup"><span data-stu-id="d0740-107">The VMR uses a DirectDraw clipper object to ensure that the video is clipped to the application's window and does not appear on any other windows.</span></span> <span data-ttu-id="d0740-108">Il VMR non esegue la sottoclasse della finestra dell'applicazione né installa alcun hook di sistema/processo.</span><span class="sxs-lookup"><span data-stu-id="d0740-108">The VMR does not subclass the application's window or install any system/process hooks.</span></span>

<span data-ttu-id="d0740-109">In modalità senza finestra, la sequenza di eventi durante la connessione e la transizione allo stato di esecuzione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="d0740-109">In windowless mode, the sequence of events during connection and transition to the run state is as follows:</span></span>

-   <span data-ttu-id="d0740-110">Il filtro upstream propone un tipo di supporto, che il VMR accetta o rifiuta.</span><span class="sxs-lookup"><span data-stu-id="d0740-110">The upstream filter proposes a media type, which the VMR either accepts or rejects.</span></span>
-   <span data-ttu-id="d0740-111">Se il tipo di supporto è accettato, il VMR chiama Allocator-Presenter per ottenere una superficie DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="d0740-111">If the media type is accepted, the VMR calls the allocator-presenter to obtain a DirectDraw surface.</span></span> <span data-ttu-id="d0740-112">Se la superficie viene creata correttamente, i pin Connect e VMR sono pronti per la transizione allo stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d0740-112">If the surface is created successfully, the pins connect and the VMR is ready to transition into the run state.</span></span>
-   <span data-ttu-id="d0740-113">Quando viene eseguito il grafico dei filtri, il decodificatore chiama **GetBuffer** per ottenere un esempio di supporto dall'allocatore.</span><span class="sxs-lookup"><span data-stu-id="d0740-113">When the filter graph runs, the decoder calls **GetBuffer** to get a media sample from the allocator.</span></span> <span data-ttu-id="d0740-114">VMR esegue una query su Allocator-Presenter per assicurarsi che la profondità dei pixel, le dimensioni del rettangolo e altri parametri sulla relativa superficie DirectDraw siano compatibili con il video in arrivo.</span><span class="sxs-lookup"><span data-stu-id="d0740-114">The VMR queries the allocator-presenter to ensure that the pixel depth, rectangle size, and other parameters on its DirectDraw surface are compatible with the incoming video.</span></span> <span data-ttu-id="d0740-115">Se sono compatibili, VMR restituisce la superficie DirectDraw al decodificatore.</span><span class="sxs-lookup"><span data-stu-id="d0740-115">If they are compatible, the VMR returns the DirectDraw surface to the decoder.</span></span> <span data-ttu-id="d0740-116">Dopo la decodifica della superficie del decodificatore, l'unità di sincronizzazione principale di VMR convalida i timestamp.</span><span class="sxs-lookup"><span data-stu-id="d0740-116">After the decoder has decoded into the surface, the VMR's Core Synchronization Unit validates the time stamps.</span></span> <span data-ttu-id="d0740-117">Questa unità blocca la chiamata di **ricezione** fino a quando non arriva l'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="d0740-117">This unit blocks the **Receive** call until the presentation time arrives.</span></span> <span data-ttu-id="d0740-118">A questo punto, VMR chiama **PresentImage** su Allocator-Presenter, che presenta la superficie alla scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="d0740-118">At that point, the VMR calls **PresentImage** on the allocator-presenter, which presents the surface to the graphics card.</span></span>

<span data-ttu-id="d0740-119">La figura seguente mostra il VMR in modalità senza finestra con più flussi di input.</span><span class="sxs-lookup"><span data-stu-id="d0740-119">The following illustration shows the VMR in windowless mode with multiple input streams.</span></span>

![VMR in modalità senza finestra](images/vmr-windowless-mult-streams.png)

<span data-ttu-id="d0740-121">**Configurazione di VMR-7 per la modalità senza finestra**</span><span class="sxs-lookup"><span data-stu-id="d0740-121">**Configuring the VMR-7 for Windowless Mode**</span></span>

<span data-ttu-id="d0740-122">Per configurare VMR-7 per la modalità senza finestra, eseguire tutti i passaggi seguenti prima di connettere i pin di input di VMR:</span><span class="sxs-lookup"><span data-stu-id="d0740-122">To configure the VMR-7 for windowless mode, perform all of the following steps before connecting any of the VMR's input pins:</span></span>

1.  <span data-ttu-id="d0740-123">Creare il filtro e aggiungerlo al grafico.</span><span class="sxs-lookup"><span data-stu-id="d0740-123">Create the filter and add it to the graph.</span></span>
2.  <span data-ttu-id="d0740-124">Chiamare il metodo [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) con il flag VMRMode senza \_ finestra.</span><span class="sxs-lookup"><span data-stu-id="d0740-124">Call the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method with the VMRMode\_Windowless flag.</span></span>
3.  <span data-ttu-id="d0740-125">Facoltativamente, configurare VMR per più flussi di input chiamando [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="d0740-125">Optionally, configure the VMR for multiple input streams by calling [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="d0740-126">VMR crea un pin di input per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="d0740-126">The VMR creates an input pin for each stream.</span></span> <span data-ttu-id="d0740-127">Usare l'interfaccia [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) per impostare l'ordine Z e altri parametri per il flusso.</span><span class="sxs-lookup"><span data-stu-id="d0740-127">Use the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) interface to set the Z-order and other parameters for the stream.</span></span> <span data-ttu-id="d0740-128">Per altre informazioni, vedere [VMR con più flussi (modalità di combinazione)](vmr-with-multiple-streams--mixing-mode.md).</span><span class="sxs-lookup"><span data-stu-id="d0740-128">For more information, see [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span>

    <span data-ttu-id="d0740-129">Se non si chiama **SetNumberOfStreams**, il valore predefinito di VMR-7 è un pin di input.</span><span class="sxs-lookup"><span data-stu-id="d0740-129">If you do not call **SetNumberOfStreams**, the VMR-7 defaults to one input pin.</span></span> <span data-ttu-id="d0740-130">Una volta connessi i pin di input, il numero di pin non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="d0740-130">After the input pins are connected, the number of pins cannot be changed.</span></span>

4.  <span data-ttu-id="d0740-131">Chiamare [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) per specificare la finestra in cui verrà visualizzato il video di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="d0740-131">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) to specify the window in which the rendered video will appear.</span></span>

<span data-ttu-id="d0740-132">Una volta completati questi passaggi, è possibile connettere i pin di input del filtro VMR.</span><span class="sxs-lookup"><span data-stu-id="d0740-132">Once these steps are completed, you can connect the VMR filter's input pins.</span></span> <span data-ttu-id="d0740-133">Esistono diversi modi per creare il grafico, ad esempio la connessione diretta dei pin, l'uso di metodi di connessione intelligenti, ad esempio [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), o l'uso del metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) del generatore di grafici di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d0740-133">There are various ways to build the graph, such as connecting pins directly, using Intelligent Connect methods such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), or using the Capture Graph Builder's [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="d0740-134">Per ulteriori informazioni, vedere [General Graph-Building Techniques](general-graph-building-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="d0740-134">For more information, see [General Graph-Building Techniques](general-graph-building-techniques.md).</span></span>

<span data-ttu-id="d0740-135">Per impostare la posizione del video all'interno della finestra dell'applicazione, chiamare il metodo [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="d0740-135">To set the position of the video within the application window, call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method.</span></span> <span data-ttu-id="d0740-136">Il metodo [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) restituisce le dimensioni del video nativo.</span><span class="sxs-lookup"><span data-stu-id="d0740-136">The [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method returns the native video size.</span></span> <span data-ttu-id="d0740-137">Durante la riproduzione, l'applicazione deve notificare al VMR i messaggi di Windows seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0740-137">During playback, the application should notify the VMR of the following Windows messages:</span></span>

-   <span data-ttu-id="d0740-138">\_Disegno WM: chiamare [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) per ridisegnare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="d0740-138">WM\_PAINT: Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) to repaint the image.</span></span>
-   <span data-ttu-id="d0740-139">WM \_ DISPLAYCHANGE: chiamata [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="d0740-139">WM\_DISPLAYCHANGE: Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="d0740-140">Il VMR esegue le azioni necessarie per visualizzare il video alla nuova risoluzione o alla profondità del colore.</span><span class="sxs-lookup"><span data-stu-id="d0740-140">The VMR takes any actions that are needed to display the video at the new resolution or color depth.</span></span>
-   <span data-ttu-id="d0740-141">\_Dimensioni WM: ricalcolare la posizione del video e chiamare di nuovo [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) , se necessario.</span><span class="sxs-lookup"><span data-stu-id="d0740-141">WM\_SIZE: Recalculate the position of the video and call [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) again if necessary.</span></span>

> [!Note]  
> <span data-ttu-id="d0740-142">Le applicazioni MFC devono definire un \_ gestore di messaggi WM ERASEBKGND vuoto oppure l'area di visualizzazione del video non viene ridisegnata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d0740-142">MFC applications must define an empty WM\_ERASEBKGND message handler, or the video display area will not repaint correctly.</span></span>

 

<span data-ttu-id="d0740-143">**Configurazione di VMR-9 per la modalità senza finestra**</span><span class="sxs-lookup"><span data-stu-id="d0740-143">**Configuring the VMR-9 for Windowless Mode**</span></span>

<span data-ttu-id="d0740-144">Per configurare VMR-9 per la modalità senza finestra, usare la procedura descritta per VMR-7 per la modalità senza finestra, ma usare le interfacce [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) e [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="d0740-144">To configure the VMR-9 for windowless mode, use the steps described for the VMR-7 for Windowless mode, but use the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) and [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interfaces.</span></span> <span data-ttu-id="d0740-145">L'unica differenza significativa è che VMR-9 crea quattro pin di input per impostazione predefinita, anziché un pin di input.</span><span class="sxs-lookup"><span data-stu-id="d0740-145">The only significant difference is that the VMR-9 creates four input pins by default, rather than one input pin.</span></span> <span data-ttu-id="d0740-146">Pertanto, è necessario chiamare **SetNumberOfStreams** solo se si combinano più di quattro flussi video.</span><span class="sxs-lookup"><span data-stu-id="d0740-146">Therefore, you only need to call **SetNumberOfStreams** if you are mixing more than four video streams.</span></span>

<span data-ttu-id="d0740-147">**Codice di esempio**</span><span class="sxs-lookup"><span data-stu-id="d0740-147">**Example Code**</span></span>

<span data-ttu-id="d0740-148">Il codice seguente illustra come creare un filtro VMR-7, aggiungerlo al grafo del filtro DirectShow e quindi inserire il VMR in modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="d0740-148">The following code shows how to create a VMR-7 filter, add it to the DirectShow filter graph, and then put the VMR into windowless mode.</span></span> <span data-ttu-id="d0740-149">Per VMR-9 usare CLSID \_ VideoMixingRenderer9 in **CoCreateInstance** e le corrispondenti interfacce VMR-9.</span><span class="sxs-lookup"><span data-stu-id="d0740-149">For the VMR-9, use CLSID\_VideoMixingRenderer9 in **CoCreateInstance** and the corresponding VMR-9 interfaces.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d0740-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0740-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0740-151">Uso della modalità senza finestra</span><span class="sxs-lookup"><span data-stu-id="d0740-151">Using Windowless Mode</span></span>](using-windowless-mode.md)
</dt> </dl>

 

 



