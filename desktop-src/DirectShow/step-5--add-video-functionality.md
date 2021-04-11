---
description: Questo argomento è il passaggio 5 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Passaggio 5: aggiungere funzionalità video'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f5ccf1ae3ca24a705506bc41620ac53a13d7e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232986"
---
# <a name="step-5-add-video-functionality"></a><span data-ttu-id="628b4-103">Passaggio 5: aggiungere funzionalità video</span><span class="sxs-lookup"><span data-stu-id="628b4-103">Step 5: Add Video Functionality</span></span>

<span data-ttu-id="628b4-104">Questo argomento è il passaggio 5 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="628b4-104">This topic is step 5 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="628b4-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="628b4-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="628b4-106">Per assicurarsi che il video venga visualizzato correttamente, l'applicazione deve rispondere ai messaggi [**WM \_ Paint**](../gdi/wm-paint.md), [**WM \_ size**](../winmsg/wm-size.md)e [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="628b4-106">To ensure that video displays correctly, the application must respond to [**WM\_PAINT**](../gdi/wm-paint.md), [**WM\_SIZE**](../winmsg/wm-size.md), and [**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md) messages as follows.</span></span>

### <a name="handle-wm_paint-messages"></a><span data-ttu-id="628b4-107">Gestire \_ i messaggi di disegno WM</span><span class="sxs-lookup"><span data-stu-id="628b4-107">Handle WM\_PAINT Messages</span></span>

<span data-ttu-id="628b4-108">Quando l'applicazione riceve un messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) , il renderer video potrebbe dover ridisegnare l'ultimo fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="628b4-108">When the application receives a [**WM\_PAINT**](../gdi/wm-paint.md) message, the video renderer might need to redraw the last video frame.</span></span> <span data-ttu-id="628b4-109">Per il filtro EVR ( [**Enhanced video renderer**](enhanced-video-renderer-filter.md) ), chiamare [**IMFVideoDisplayControl:: RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="628b4-109">For the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter, call [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>


```C++
HRESULT CEVR::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="628b4-110">Per il [filtro del renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9), chiamare [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="628b4-110">For the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span>


```C++
HRESULT CVMR9::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="628b4-111">Per il [filtro del renderer di video mixing 7](video-mixing-renderer-filter-7.md) (VMR-7), chiamare [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="628b4-111">For the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7), call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span>


```C++
HRESULT CVMR7::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



### <a name="handle-wm_size-messages"></a><span data-ttu-id="628b4-112">Gestire \_ i messaggi di dimensioni WM</span><span class="sxs-lookup"><span data-stu-id="628b4-112">Handle WM\_SIZE Messages</span></span>

<span data-ttu-id="628b4-113">Se le dimensioni della finestra video cambiano, inviare una notifica al renderer video per ridimensionare il video.</span><span class="sxs-lookup"><span data-stu-id="628b4-113">If the size of the video window changes, notify the video renderer to resize the video.</span></span> <span data-ttu-id="628b4-114">Per EVR, chiamare [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="628b4-114">For the EVR, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>


```C++
HRESULT CEVR::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pVideoDisplay == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pVideoDisplay->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pVideoDisplay->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="628b4-115">Per VMR-9, chiamare [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="628b4-115">For the VMR-9, call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span></span>


```C++
HRESULT CVMR9::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="628b4-116">Per VMR-7, chiamare [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="628b4-116">For the VMR-7, call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span></span>


```C++
HRESULT CVMR7::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {
        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



### <a name="handle-wm_displaychange-messages"></a><span data-ttu-id="628b4-117">Gestire \_ i messaggi WM DISPLAYCHANGE</span><span class="sxs-lookup"><span data-stu-id="628b4-117">Handle WM\_DISPLAYCHANGE Messages</span></span>

<span data-ttu-id="628b4-118">Se la modalità di visualizzazione viene modificata, è necessario inviare una notifica al filtro VMR-9 o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="628b4-118">If the display mode changes, you must notify the VMR-9 or VMR-7 filter.</span></span> <span data-ttu-id="628b4-119">Per VMR-9, chiamare [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="628b4-119">For the VMR-9, call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span>


```C++
HRESULT CVMR9::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="628b4-120">Per VMR-7, chiamare [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="628b4-120">For the VMR-7, call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span>


```C++
HRESULT CVMR7::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="628b4-121">Il EVR non deve essere notificato quando cambia la modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="628b4-121">The EVR does not need to be notified when the display mode changes.</span></span>

<span data-ttu-id="628b4-122">[Passaggio 6: gestire gli eventi del grafo](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="628b4-122">Next: [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="628b4-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="628b4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="628b4-124">Riproduzione audio/video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="628b4-124">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="628b4-125">Esempio di riproduzione DirectShow</span><span class="sxs-lookup"><span data-stu-id="628b4-125">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="628b4-126">Uso del filtro EVR DirectShow</span><span class="sxs-lookup"><span data-stu-id="628b4-126">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="628b4-127">Uso del renderer video mixing</span><span class="sxs-lookup"><span data-stu-id="628b4-127">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
