---
description: PIN della porta video
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: PIN della porta video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883078"
---
# <a name="video-port-pins"></a><span data-ttu-id="03f76-103">PIN della porta video</span><span class="sxs-lookup"><span data-stu-id="03f76-103">Video Port Pins</span></span>

<span data-ttu-id="03f76-104">Un dispositivo di acquisizione con una porta video hardware può usare VPE (video Port Extensions) in Microsoft® DirectX®.</span><span class="sxs-lookup"><span data-stu-id="03f76-104">A capture device with a hardware video port might use the video port extensions (VPE) in Microsoft® DirectX®.</span></span> <span data-ttu-id="03f76-105">In tal caso, il filtro di acquisizione avrà un PIN della porta video (VP).</span><span class="sxs-lookup"><span data-stu-id="03f76-105">If so, the capture filter will have a video port (VP) pin.</span></span> <span data-ttu-id="03f76-106">Nessun dato video passa dal perno VP al grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="03f76-106">No video data travels from the VP pin through the filter graph.</span></span> <span data-ttu-id="03f76-107">Al contrario, i frame video vengono prodotti nell'hardware e inviati direttamente alla memoria del video.</span><span class="sxs-lookup"><span data-stu-id="03f76-107">Instead, video frames are produced in hardware and sent directly to video memory.</span></span> <span data-ttu-id="03f76-108">Il pin VP consente l'invio di messaggi di controllo all'hardware.</span><span class="sxs-lookup"><span data-stu-id="03f76-108">The VP pin allows control messages to be sent to the hardware.</span></span>

<span data-ttu-id="03f76-109">È importante connettere il pin VP, anche se l'applicazione esegue solo l'acquisizione di file senza anteprima.</span><span class="sxs-lookup"><span data-stu-id="03f76-109">It is important to connect the VP pin, even if your application only performs file capture with no preview.</span></span> <span data-ttu-id="03f76-110">Se si lascia il PIN non connesso, il grafico non viene eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="03f76-110">If you leave the pin unconnected, the graph will not run correctly.</span></span> <span data-ttu-id="03f76-111">Questo comportamento è diverso dai pin di anteprima, che non devono essere connessi.</span><span class="sxs-lookup"><span data-stu-id="03f76-111">This is different from preview pins, which do not have to be connected.</span></span>

<span data-ttu-id="03f76-112">I diversi renderer video DirectShow offrono un supporto variabile per i pin VP:</span><span class="sxs-lookup"><span data-stu-id="03f76-112">The different DirectShow video renderers provide varying support for VP pins:</span></span>

-   <span data-ttu-id="03f76-113">Renderer video: connettere il pin VP al pin 0 nel filtro [sovrimpressione](overlay-mixer-filter.md) e connettere il filtro del mixer sovrapposto al renderer video.</span><span class="sxs-lookup"><span data-stu-id="03f76-113">Video Renderer: Connect the VP pin to pin 0 on the [Overlay Mixer](overlay-mixer-filter.md) filter, and connect the Overlay Mixer filter to the Video Renderer.</span></span>
-   <span data-ttu-id="03f76-114">VMR-7: connettere il pin VP al filtro di [Gestione porte video](video-port-manager.md) e connettere Gestione porta video a VMR-7.</span><span class="sxs-lookup"><span data-stu-id="03f76-114">VMR-7: Connect the VP pin to the [Video Port Manager](video-port-manager.md) filter, and connect the Video Port Manager to the VMR-7.</span></span>
-   <span data-ttu-id="03f76-115">VMR-9: non è possibile usare VMR-9 se il dispositivo ha un pin VP, perché Direct3D 9 non supporta le porte video.</span><span class="sxs-lookup"><span data-stu-id="03f76-115">VMR-9: You cannot use the VMR-9 if the device has a VP pin, because Direct3D 9 does not support video ports.</span></span> <span data-ttu-id="03f76-116">Usare il renderer video o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="03f76-116">Use either the Video Renderer or the VMR-7.</span></span>

<span data-ttu-id="03f76-117">Per gli scenari di porta video, il mixer overlay e il renderer video sono consigliati rispetto a gestione porta video e VMR-7, perché non tutti i driver supportano il gestore della porta video.</span><span class="sxs-lookup"><span data-stu-id="03f76-117">For video port scenarios, the Overlay Mixer and Video Renderer are recommended over the Video Port Manager and VMR-7, because not all drivers support the Video Port Manager.</span></span> <span data-ttu-id="03f76-118">In generale, il mixer overlay è l'opzione più affidabile per le porte video.</span><span class="sxs-lookup"><span data-stu-id="03f76-118">In general, the Overlay Mixer is the most reliable option for video ports.</span></span>

<span data-ttu-id="03f76-119">Il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserisce automaticamente il mixer della sovrimpressione se è presente un pin VP.</span><span class="sxs-lookup"><span data-stu-id="03f76-119">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Overlay Mixer if there is a VP pin.</span></span> <span data-ttu-id="03f76-120">Se si compila il grafico senza usare questo metodo, è necessario verificare la presenza di un PIN della porta video nel filtro di acquisizione e, se presente, connetterlo al filtro della sovrimpressione, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="03f76-120">If you are building the graph without using this method, you should check for a video port pin on the capture filter, and if one is present, connect it to the Overlay Mixer filter, as shown in the following diagram.</span></span>

![connessione di un PIN della porta video al filtro della sovrimpressione.](images/vidcap11.png)

<span data-ttu-id="03f76-122">È possibile usare il metodo [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) per cercare un pin VP sul filtro di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="03f76-122">You can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to search for a VP pin on the capture filter:</span></span>


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="03f76-123">Dopo aver aggiunto il mixer della sovrimpressione al grafo, chiamare di nuovo **FindPin** per trovare il pin 0 nel mixer della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="03f76-123">After you add the Overlay Mixer to the graph, call **FindPin** again to find pin 0 on the Overlay Mixer.</span></span> <span data-ttu-id="03f76-124">Il pin 0 è sempre il primo pin di input sul filtro.</span><span class="sxs-lookup"><span data-stu-id="03f76-124">Pin 0 is always the first input pin on the filter.</span></span>


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



<span data-ttu-id="03f76-125">Connettere i due pin chiamando [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span><span class="sxs-lookup"><span data-stu-id="03f76-125">Connect the two pins by calling [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span></span>


```C++
pGraph->Connect(pVPPin, pOvPin);
```



<span data-ttu-id="03f76-126">Quindi connettere il pin di output del mixer overlay al filtro renderer video.</span><span class="sxs-lookup"><span data-stu-id="03f76-126">Then connect the Overlay Mixer's output pin to the Video Renderer filter.</span></span> <span data-ttu-id="03f76-127">È possibile nascondere il video chiamando il [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) e [**IVideoWindow::p UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="03f76-127">You can hide the video by calling the [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) and [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.</span></span>

<span data-ttu-id="03f76-128">Per i sintonizzatori TV, il filtro di acquisizione potrebbe avere anche una porta video VBI pin (PIN \_ Category \_ VIDEOPORT \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="03f76-128">For TV tuners, the capture filter might also have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="03f76-129">In tal caso, connettere il PIN al filtro [VBI Surface allocator](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="03f76-129">If so, connect that pin to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="03f76-130">Per ulteriori informazioni, vedere [visualizzazione di didascalie chiuse](viewing-closed-captions.md).</span><span class="sxs-lookup"><span data-stu-id="03f76-130">For more information, see [Viewing Closed Captions](viewing-closed-captions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03f76-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03f76-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03f76-132">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="03f76-132">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="03f76-133">Uso del mixer overlay in acquisizione video</span><span class="sxs-lookup"><span data-stu-id="03f76-133">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



