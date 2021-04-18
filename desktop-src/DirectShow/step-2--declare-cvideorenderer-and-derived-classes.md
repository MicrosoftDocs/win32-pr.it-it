---
description: Questo argomento è il passaggio 2 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Passaggio 2: dichiarare CVideoRenderer e classi derivate'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315533"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a><span data-ttu-id="91411-103">Passaggio 2: dichiarare CVideoRenderer e classi derivate</span><span class="sxs-lookup"><span data-stu-id="91411-103">Step 2: Declare CVideoRenderer and Derived Classes</span></span>

<span data-ttu-id="91411-104">Questo argomento è il passaggio 2 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="91411-104">This topic is step 2 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="91411-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="91411-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="91411-106">DirectShow fornisce diversi filtri che eseguono il rendering del video:</span><span class="sxs-lookup"><span data-stu-id="91411-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="91411-107">[**Filtro renderer video migliorato**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="91411-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="91411-108">[Filtro renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="91411-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="91411-109">[Filtro renderer video mixing 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="91411-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="91411-110">Per ulteriori informazioni sulle differenze tra questi filtri, vedere [scelta del renderer video appropriato](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="91411-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="91411-111">In questa esercitazione viene usata la classe astratta seguente per eseguire il wrapping del filtro renderer video.</span><span class="sxs-lookup"><span data-stu-id="91411-111">In this tutorial, the following abstract class is used to wrap the video renderer filter.</span></span>


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



<span data-ttu-id="91411-112">Note:</span><span class="sxs-lookup"><span data-stu-id="91411-112">Notes:</span></span>

-   <span data-ttu-id="91411-113">Il `HasVideo` metodo restituisce **true** se il renderer video è stato creato.</span><span class="sxs-lookup"><span data-stu-id="91411-113">The `HasVideo` method returns **TRUE** if the video renderer has been created.</span></span>
-   <span data-ttu-id="91411-114">Il `AddToGraph` metodo aggiunge il renderer video al grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="91411-114">The `AddToGraph` method adds the video renderer to the filter graph.</span></span>
-   <span data-ttu-id="91411-115">Il `FinalizeGraph` metodo completa il passaggio di compilazione del grafico.</span><span class="sxs-lookup"><span data-stu-id="91411-115">The `FinalizeGraph` method completes the graph-building step.</span></span>
-   <span data-ttu-id="91411-116">Il `UpdateVideoWindow` metodo aggiorna il rettangolo di destinazione del video.</span><span class="sxs-lookup"><span data-stu-id="91411-116">The `UpdateVideoWindow` method updates the video destination rectangle.</span></span>
-   <span data-ttu-id="91411-117">Il `Repaint` Metodo ridisegnato il fotogramma video corrente.</span><span class="sxs-lookup"><span data-stu-id="91411-117">The `Repaint` method redraws the current video frame.</span></span>
-   <span data-ttu-id="91411-118">Il `DisplayModeChanged` metodo gestisce le modifiche della modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="91411-118">The `DisplayModeChanged` method handles display-mode changes.</span></span>

<span data-ttu-id="91411-119">Ognuno di questi metodi è descritto in dettaglio più avanti in questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="91411-119">Each of these methods is described in detail later in this tutorial.</span></span>

<span data-ttu-id="91411-120">Dichiarare quindi una classe derivata per eseguire il wrapping di ognuno dei tre renderer video, ovvero EVR, VMR-9 e VMR-7.</span><span class="sxs-lookup"><span data-stu-id="91411-120">Next, declare a derived class to wrap each of the three video renderers: the EVR, the VMR-9, and the VMR-7.</span></span>

### <a name="cevr-class"></a><span data-ttu-id="91411-121">Classe CEVR</span><span class="sxs-lookup"><span data-stu-id="91411-121">CEVR Class</span></span>

<span data-ttu-id="91411-122">La `CEVR` classe gestisce l'EVR.</span><span class="sxs-lookup"><span data-stu-id="91411-122">The `CEVR` class manages the EVR.</span></span> <span data-ttu-id="91411-123">Contiene un puntatore alle interfacce [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) di EVR.</span><span class="sxs-lookup"><span data-stu-id="91411-123">It contains a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) and [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interfaces of the EVR.</span></span>


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a><span data-ttu-id="91411-124">Classe CVMR9</span><span class="sxs-lookup"><span data-stu-id="91411-124">CVMR9 Class</span></span>

<span data-ttu-id="91411-125">La `CVMR9` classe gestisce VMR-9.</span><span class="sxs-lookup"><span data-stu-id="91411-125">The `CVMR9` class manages the VMR-9.</span></span> <span data-ttu-id="91411-126">Contiene un puntatore all'interfaccia [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="91411-126">It contains a pointer to the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a><span data-ttu-id="91411-127">Classe CVMR7</span><span class="sxs-lookup"><span data-stu-id="91411-127">CVMR7 Class</span></span>

<span data-ttu-id="91411-128">La `CVMR7` classe gestisce VMR-7.</span><span class="sxs-lookup"><span data-stu-id="91411-128">The `CVMR7` class manages the VMR-7.</span></span> <span data-ttu-id="91411-129">Contiene un puntatore all'interfaccia [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="91411-129">It contains a pointer to the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



<span data-ttu-id="91411-130">[Passaggio 3: creare il grafico dei filtri](step-3--build-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="91411-130">Next: [Step 3: Build the Filter Graph](step-3--build-the-filter-graph.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="91411-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91411-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91411-132">Riproduzione audio/video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="91411-132">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="91411-133">Uso del renderer video mixing</span><span class="sxs-lookup"><span data-stu-id="91411-133">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="91411-134">Rendering video</span><span class="sxs-lookup"><span data-stu-id="91411-134">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
