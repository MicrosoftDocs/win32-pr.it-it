---
description: Uso della modalità senza finestra
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Uso della modalità senza finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883093"
---
# <a name="using-windowless-mode"></a><span data-ttu-id="5dd74-103">Uso della modalità senza finestra</span><span class="sxs-lookup"><span data-stu-id="5dd74-103">Using Windowless Mode</span></span>

<span data-ttu-id="5dd74-104">Sia il [filtro del renderer video mixing 7](video-mixing-renderer-filter-7.md) (VMR-7) che il [filtro del renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9) supportano la *modalità senza finestra*, che rappresenta un miglioramento significativo rispetto all'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="5dd74-104">Both the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) support *windowless mode*, which represents a major improvement over the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="5dd74-105">In questo argomento vengono descritte le differenze tra la modalità senza finestra e la modalità finestra e come utilizzare la modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="5dd74-105">This topic describes the differences between windowless mode and windowed mode, and how to use windowless mode.</span></span>

<span data-ttu-id="5dd74-106">Per mantenere la compatibilità con le applicazioni esistenti, il valore predefinito di VMR è la modalità con finestra.</span><span class="sxs-lookup"><span data-stu-id="5dd74-106">To remain backward-compatible with existing applications, the VMR defaults to windowed mode.</span></span> <span data-ttu-id="5dd74-107">In modalità finestra, il renderer crea la propria finestra per visualizzare il video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-107">In windowed mode, the renderer creates its own window to display the video.</span></span> <span data-ttu-id="5dd74-108">In genere, l'applicazione imposta la finestra video come figlio della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5dd74-108">Typically the application sets the video window to be a child of the application window.</span></span> <span data-ttu-id="5dd74-109">L'esistenza di una finestra video separata comporta tuttavia alcuni problemi:</span><span class="sxs-lookup"><span data-stu-id="5dd74-109">The existence of a separate video window causes some problems, however:</span></span>

-   <span data-ttu-id="5dd74-110">In particolare, è possibile che si verifichino deadlock se i messaggi della finestra vengono inviati tra i thread.</span><span class="sxs-lookup"><span data-stu-id="5dd74-110">Most importantly, there is a potential for deadlocks if window messages are sent between threads.</span></span>
-   <span data-ttu-id="5dd74-111">Il gestore del grafo del filtro deve trasmettere al renderer video alcuni messaggi della finestra, ad esempio WM \_ Paint.</span><span class="sxs-lookup"><span data-stu-id="5dd74-111">The Filter Graph Manager must forward certain window messages, such as WM\_PAINT, to the Video Renderer.</span></span> <span data-ttu-id="5dd74-112">L'applicazione deve usare l'implementazione del gestore del grafo del filtro di [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (e non il renderer video), in modo che il gestore del grafico del filtro mantenga lo stato interno corretto.</span><span class="sxs-lookup"><span data-stu-id="5dd74-112">The application must use the Filter Graph Manager's implementation of [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (and not the Video Renderer's), so that the Filter Graph Manager maintains the correct internal state.</span></span>
-   <span data-ttu-id="5dd74-113">Per ricevere gli eventi del mouse o della tastiera dalla finestra del video, l'applicazione deve impostare un *svuotamento del messaggio*, facendo sì che la finestra video inoltri tali messaggi all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5dd74-113">To receive mouse or keyboard events from the video window, the application must set a *message drain*, causing the video window to forward these messages to the application.</span></span>
-   <span data-ttu-id="5dd74-114">Per evitare problemi di ritaglio, la finestra video deve avere gli stili della finestra corretti.</span><span class="sxs-lookup"><span data-stu-id="5dd74-114">To prevent clipping problems, the video window must have the right window styles.</span></span>

<span data-ttu-id="5dd74-115">La modalità senza finestra consente di evitare questi problemi VMR direttamente sull'area client della finestra dell'applicazione, utilizzando DirectDraw per ritagliare il rettangolo del video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-115">Windowless mode avoids these problems by having the VMR draw directly on the application window's client area, using DirectDraw to clip the video rectangle.</span></span> <span data-ttu-id="5dd74-116">La modalità senza finestra riduce significativamente la probabilità di deadlock.</span><span class="sxs-lookup"><span data-stu-id="5dd74-116">Windowless mode significantly reduces the chance of deadlocks.</span></span> <span data-ttu-id="5dd74-117">Inoltre, l'applicazione non deve impostare la finestra proprietaria né gli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="5dd74-117">Also, the application does not have to set the owner window or the window styles.</span></span> <span data-ttu-id="5dd74-118">Infatti, quando il VMR è in modalità senza finestra, non espone anche l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , che non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="5dd74-118">In fact, when the VMR is in windowless mode, it does not even expose the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, which is no longer needed.</span></span>

<span data-ttu-id="5dd74-119">Per usare la modalità senza finestra, è necessario configurare in modo esplicito VMR.</span><span class="sxs-lookup"><span data-stu-id="5dd74-119">To use windowless mode, you must explicitly configure the VMR.</span></span> <span data-ttu-id="5dd74-120">Tuttavia, si noterà che è più flessibile e più semplice da usare rispetto alla modalità Window.</span><span class="sxs-lookup"><span data-stu-id="5dd74-120">However, you will find that is more flexible and easier to use than windowed mode.</span></span>

<span data-ttu-id="5dd74-121">Il filtro VMR-7 e il filtro VMR-9 espongono interfacce diverse, ma i passaggi sono equivalenti per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="5dd74-121">The VMR-7 filter and the VMR-9 filter expose different interfaces, but the steps are equivalent for each.</span></span>

## <a name="configure-the-vmr-for-windowless-mode"></a><span data-ttu-id="5dd74-122">Configurare VMR per la modalità senza finestra</span><span class="sxs-lookup"><span data-stu-id="5dd74-122">Configure the VMR for Windowless Mode</span></span>

<span data-ttu-id="5dd74-123">Per eseguire l'override del comportamento predefinito di VMR, configurare VMR prima di compilare il grafico del filtro:</span><span class="sxs-lookup"><span data-stu-id="5dd74-123">To override the VMR's default behavior, configure the VMR before building the filter graph:</span></span>

<span data-ttu-id="5dd74-124">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="5dd74-124">**VMR-7**</span></span>

1.  <span data-ttu-id="5dd74-125">Creare il gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="5dd74-125">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="5dd74-126">Creare VMR-7 e aggiungerlo al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="5dd74-126">Create the VMR-7 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="5dd74-127">Chiamare [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) in VMR-7 con il flag **VMRMode senza \_ finestra** .</span><span class="sxs-lookup"><span data-stu-id="5dd74-127">Call [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) on the VMR-7 with the **VMRMode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="5dd74-128">Eseguire una query su VMR-7 per l'interfaccia [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="5dd74-128">Query the VMR-7 for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
5.  <span data-ttu-id="5dd74-129">Chiamare [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) in VMR-7.</span><span class="sxs-lookup"><span data-stu-id="5dd74-129">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) on the VMR-7.</span></span> <span data-ttu-id="5dd74-130">Specificare un handle per la finestra in cui deve essere visualizzato il video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-130">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="5dd74-131">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="5dd74-131">**VMR-9**</span></span>

1.  <span data-ttu-id="5dd74-132">Creare il gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="5dd74-132">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="5dd74-133">Creare VMR-9 e aggiungerlo al grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="5dd74-133">Create the VMR-9 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="5dd74-134">Chiamare [**IVMRFilterConfig9:: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) in VMR-9 con il flag **VMR9Mode senza \_ finestra** .</span><span class="sxs-lookup"><span data-stu-id="5dd74-134">Call [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) on the VMR-9 with the **VMR9Mode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="5dd74-135">Eseguire una query su VMR-9 per l'interfaccia [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="5dd74-135">Query the VMR-9 for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
5.  <span data-ttu-id="5dd74-136">Chiamare [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) in VMR-9.</span><span class="sxs-lookup"><span data-stu-id="5dd74-136">Call [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) on the VMR-9.</span></span> <span data-ttu-id="5dd74-137">Specificare un handle per la finestra in cui deve essere visualizzato il video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-137">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="5dd74-138">A questo punto, compilare il resto del grafo del filtro chiamando [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o altri metodi di creazione di grafici.</span><span class="sxs-lookup"><span data-stu-id="5dd74-138">Now build the rest of the filter graph by calling [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or other graph-building methods.</span></span> <span data-ttu-id="5dd74-139">Filter Graph Manager usa automaticamente l'istanza di VMR aggiunta al grafo.</span><span class="sxs-lookup"><span data-stu-id="5dd74-139">The Filter Graph Manager automatically uses the instance of the VMR that you added to the graph.</span></span> <span data-ttu-id="5dd74-140">Per informazioni dettagliate sul motivo per cui si verifica questo problema, vedere la pagina relativa alla [connessione intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="5dd74-140">(For details on why this happens, see [Intelligent Connect](intelligent-connect.md).)</span></span>

<span data-ttu-id="5dd74-141">Il codice seguente illustra una funzione helper che crea VMR-7, la aggiunge al grafo e imposta la modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="5dd74-141">The following code shows a helper function that creates the VMR-7, adds it to the graph, and sets up windowless mode.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



<span data-ttu-id="5dd74-142">Questa funzione presuppone che venga visualizzato un solo flusso video e che non si mescoli una bitmap statica sul video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-142">This function assumes that are displaying only one video stream and are not mixing a static bitmap over the video.</span></span> <span data-ttu-id="5dd74-143">Per informazioni dettagliate, vedere [modalità senza finestra VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="5dd74-143">For details, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span> <span data-ttu-id="5dd74-144">Questa funzione verrà chiamata come segue:</span><span class="sxs-lookup"><span data-stu-id="5dd74-144">You would call this function as follows:</span></span>


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a><span data-ttu-id="5dd74-145">Posizionare il video</span><span class="sxs-lookup"><span data-stu-id="5dd74-145">Position the Video</span></span>

<span data-ttu-id="5dd74-146">Dopo aver configurato il VMR, il passaggio successivo consiste nell'impostare la posizione del video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-146">After configuring the VMR, the next step is to set the position of the video.</span></span> <span data-ttu-id="5dd74-147">È necessario considerare due rettangoli, il rettangolo di *origine* e il rettangolo di *destinazione* .</span><span class="sxs-lookup"><span data-stu-id="5dd74-147">There are two rectangles to consider, the *source* rectangle and the *destination* rectangle.</span></span> <span data-ttu-id="5dd74-148">Il rettangolo di origine definisce la parte del video da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="5dd74-148">The source rectangle defines which portion of the video to display.</span></span> <span data-ttu-id="5dd74-149">Il rettangolo di destinazione specifica l'area dell'area client della finestra che conterrà il video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-149">The destination rectangle specifies the region in the window's client area that will contain the video.</span></span> <span data-ttu-id="5dd74-150">VMR consente di ritagliare l'immagine del video nel rettangolo di origine e di allungare l'immagine ritagliata per adattarla al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5dd74-150">The VMR crops the video image to the source rectangle and stretches the cropped image to fit the destination rectangle.</span></span>

<span data-ttu-id="5dd74-151">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="5dd74-151">**VMR-7**</span></span>

1.  <span data-ttu-id="5dd74-152">Chiamare il metodo [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) per specificare entrambi i rettangoli.</span><span class="sxs-lookup"><span data-stu-id="5dd74-152">Call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="5dd74-153">Il rettangolo di origine deve essere minore o uguale alla dimensione del video nativa; è possibile usare il metodo [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) per ottenere la dimensione del video nativa.</span><span class="sxs-lookup"><span data-stu-id="5dd74-153">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="5dd74-154">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="5dd74-154">**VMR-9**</span></span>

1.  <span data-ttu-id="5dd74-155">Chiamare il metodo [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) per specificare entrambi i rettangoli.</span><span class="sxs-lookup"><span data-stu-id="5dd74-155">Call the [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="5dd74-156">Il rettangolo di origine deve essere minore o uguale alla dimensione del video nativa; è possibile usare il metodo [**IVMRWindowlessControl9:: GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) per ottenere la dimensione del video nativa.</span><span class="sxs-lookup"><span data-stu-id="5dd74-156">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="5dd74-157">Il codice seguente, ad esempio, imposta i rettangoli di origine e di destinazione per VMR-7.</span><span class="sxs-lookup"><span data-stu-id="5dd74-157">For example, the following code sets the source and destination rectangles for the VMR-7.</span></span> <span data-ttu-id="5dd74-158">Imposta il rettangolo di origine uguale all'intera immagine video e il rettangolo di destinazione è uguale all'intera area client della finestra:</span><span class="sxs-lookup"><span data-stu-id="5dd74-158">It sets the source rectangle equal to the entire video image, and the destination rectangle equal to the entire window client area:</span></span>


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



<span data-ttu-id="5dd74-159">Se si vuole che il video occupi una parte più piccola dell'area client, modificare il parametro *rcDest* .</span><span class="sxs-lookup"><span data-stu-id="5dd74-159">If you want to video to occupy a smaller portion of the client area, modify the *rcDest* parameter.</span></span> <span data-ttu-id="5dd74-160">Se si vuole ritagliare l'immagine video, modificare il parametro *rcSrc* .</span><span class="sxs-lookup"><span data-stu-id="5dd74-160">If you want to crop the video image, modify the *rcSrc* parameter.</span></span>

## <a name="handle-window-messages"></a><span data-ttu-id="5dd74-161">Gestire i messaggi della finestra</span><span class="sxs-lookup"><span data-stu-id="5dd74-161">Handle Window Messages</span></span>

<span data-ttu-id="5dd74-162">Poiché VMR non dispone di una propria finestra, è necessario ricevere una notifica se è necessario ridisegnare o ridimensionare il video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-162">Because the VMR does not have its own window, it must be notified if it need to repaint or resize the video.</span></span> <span data-ttu-id="5dd74-163">Per rispondere ai messaggi della finestra seguenti, chiamare i metodi VMR elencati.</span><span class="sxs-lookup"><span data-stu-id="5dd74-163">Respond to the following window messages by calling the VMR methods listed.</span></span>

<span data-ttu-id="5dd74-164">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="5dd74-164">**VMR-7**</span></span>

1.  <span data-ttu-id="5dd74-165">[**WM \_ Disegna**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="5dd74-165">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="5dd74-166">Chiamare [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="5dd74-166">Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span> <span data-ttu-id="5dd74-167">Questo metodo fa in modo che VMR-7 ridisegni il frame video più recente.</span><span class="sxs-lookup"><span data-stu-id="5dd74-167">This method causes the VMR-7 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="5dd74-168">[**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): chiama [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="5dd74-168">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="5dd74-169">Questo metodo notifica a VMR-7 che il video deve essere visualizzato con una nuova risoluzione o profondità del colore.</span><span class="sxs-lookup"><span data-stu-id="5dd74-169">This method notifies the VMR-7 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="5dd74-170">[**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): ricalcolare la posizione del video e chiamare [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) per aggiornare la posizione, se necessario.</span><span class="sxs-lookup"><span data-stu-id="5dd74-170">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) to update the position, if needed.</span></span>

<span data-ttu-id="5dd74-171">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="5dd74-171">**VMR-9**</span></span>

1.  <span data-ttu-id="5dd74-172">[**WM \_ Disegna**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="5dd74-172">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="5dd74-173">Chiamare [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="5dd74-173">Call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span> <span data-ttu-id="5dd74-174">Questo metodo fa in modo che VMR-9 ridisegni il frame video più recente.</span><span class="sxs-lookup"><span data-stu-id="5dd74-174">This method causes the VMR-9 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="5dd74-175">[**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): chiama [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="5dd74-175">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span> <span data-ttu-id="5dd74-176">Questo metodo notifica a VMR-9 che il video deve essere visualizzato con una nuova risoluzione o profondità del colore.</span><span class="sxs-lookup"><span data-stu-id="5dd74-176">This method notifies the VMR-9 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="5dd74-177">[**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): ricalcolare la posizione del video e chiamare [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) per aggiornare la posizione, se necessario.</span><span class="sxs-lookup"><span data-stu-id="5dd74-177">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) to update the position, if needed.</span></span>

> [!Note]  
> <span data-ttu-id="5dd74-178">Il gestore predefinito per il messaggio [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) Invia un messaggio di [**\_ dimensioni WM**](../winmsg/wm-size.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd74-178">The default handler for the [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) message sends a [**WM\_SIZE**](../winmsg/wm-size.md) message.</span></span> <span data-ttu-id="5dd74-179">Tuttavia, se l'applicazione intercetta **WM \_ WINDOWPOSCHANGED** e non la passa a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), è necessario chiamare **SetVideoPosition** nel gestore **WM \_ WINDOWPOSCHANGED** , oltre al gestore **\_ dimensioni WM** .</span><span class="sxs-lookup"><span data-stu-id="5dd74-179">But if your application intercepts **WM\_WINDOWPOSCHANGED** and does not pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), you should call **SetVideoPosition** in your **WM\_WINDOWPOSCHANGED** handler, in addition to your **WM\_SIZE** handler.</span></span>

 

<span data-ttu-id="5dd74-180">Nell'esempio seguente viene illustrato un gestore di messaggi di [**\_ disegno WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd74-180">The following example shows a [**WM\_PAINT**](../gdi/wm-paint.md) message handler.</span></span> <span data-ttu-id="5dd74-181">Disegna un'area definita dal rettangolo client meno il rettangolo del video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-181">It paints a region defined by the client rectangle minus the video rectangle.</span></span> <span data-ttu-id="5dd74-182">Non disegnare sul rettangolo video, perché il VMR ne eseguirà il disegno, causando lo sfarfallio.</span><span class="sxs-lookup"><span data-stu-id="5dd74-182">Do not draw onto the video rectangle, because the VMR will paint over it, causing flickering.</span></span> <span data-ttu-id="5dd74-183">Per lo stesso motivo, non impostare un pennello per lo sfondo nella classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="5dd74-183">For the same reason, do not set a background brush in your window class.</span></span>


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



<span data-ttu-id="5dd74-184">Sebbene sia necessario rispondere ai messaggi di [**\_ disegno WM**](../gdi/wm-paint.md) , non è necessario eseguire alcuna operazione tra i messaggi di **\_ disegno WM** per aggiornare il video.</span><span class="sxs-lookup"><span data-stu-id="5dd74-184">Although you must respond to [**WM\_PAINT**](../gdi/wm-paint.md) messages, there is nothing you need to do between **WM\_PAINT** messages to update the video.</span></span> <span data-ttu-id="5dd74-185">Come illustrato in questo esempio, la modalità senza finestra consente di gestire l'immagine video semplicemente come area di disegno automatico nella finestra.</span><span class="sxs-lookup"><span data-stu-id="5dd74-185">As this example shows, windowless mode lets you treat the video image simply as a self-drawing region on the window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dd74-186">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5dd74-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dd74-187">Uso del renderer video mixing</span><span class="sxs-lookup"><span data-stu-id="5dd74-187">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="5dd74-188">Rendering video</span><span class="sxs-lookup"><span data-stu-id="5dd74-188">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
