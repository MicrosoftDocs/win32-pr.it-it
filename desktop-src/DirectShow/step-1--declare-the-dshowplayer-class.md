---
description: Questo argomento è il passaggio 1 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 'Passaggio 1: dichiarare la classe DShowPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314409"
---
# <a name="step-1-declare-the-dshowplayer-class"></a><span data-ttu-id="43bcb-103">Passaggio 1: dichiarare la classe DShowPlayer</span><span class="sxs-lookup"><span data-stu-id="43bcb-103">Step 1: Declare the DShowPlayer Class</span></span>

<span data-ttu-id="43bcb-104">Questo argomento è il passaggio 1 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="43bcb-104">This topic is step 1 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="43bcb-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="43bcb-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="43bcb-106">In questa esercitazione la `DShowPlayer` classe gestisce tutte le funzionalità DirectShow.</span><span class="sxs-lookup"><span data-stu-id="43bcb-106">In this tutorial, the `DShowPlayer` class manages all DirectShow functionality.</span></span> <span data-ttu-id="43bcb-107">Questa classe è dichiarata come folows.</span><span class="sxs-lookup"><span data-stu-id="43bcb-107">This class is declared as folows.</span></span>


```C++
#include <new>
#include <windows.h>
#include <dshow.h>


enum PlaybackState
{
    STATE_NO_GRAPH,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED,
};

const UINT WM_GRAPH_EVENT = WM_APP + 1;

typedef void (CALLBACK *GraphEventFN)(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);

class DShowPlayer
{
public:
    DShowPlayer(HWND hwnd);
    ~DShowPlayer();

    PlaybackState State() const { return m_state; }

    HRESULT OpenFile(PCWSTR pszFileName);
    
    HRESULT Play();
    HRESULT Pause();
    HRESULT Stop();

    BOOL    HasVideo() const;
    HRESULT UpdateVideoWindow(const LPRECT prc);
    HRESULT Repaint(HDC hdc);
    HRESULT DisplayModeChanged();

    HRESULT HandleGraphEvent(GraphEventFN pfnOnGraphEvent);

private:
    HRESULT InitializeGraph();
    void    TearDownGraph();
    HRESULT CreateVideoRenderer();
    HRESULT RenderStreams(IBaseFilter *pSource);

    PlaybackState   m_state;

    HWND m_hwnd; // Video window. This window also receives graph events.

    IGraphBuilder   *m_pGraph;
    IMediaControl   *m_pControl;
    IMediaEventEx   *m_pEvent;
    CVideoRenderer  *m_pVideo;
};
```





<span data-ttu-id="43bcb-108">Note:</span><span class="sxs-lookup"><span data-stu-id="43bcb-108">Notes:</span></span>

-   <span data-ttu-id="43bcb-109">L' `PlaybackState` enumerazione descrive lo stato corrente dell' `DShowPlayer` oggetto.</span><span class="sxs-lookup"><span data-stu-id="43bcb-109">The `PlaybackState` enumeration describes the current state of the `DShowPlayer` object.</span></span>
-   <span data-ttu-id="43bcb-110">L'evento costante WM \_ Graph \_ definisce un messaggio di finestra privata.</span><span class="sxs-lookup"><span data-stu-id="43bcb-110">The constant WM\_GRAPH\_EVENT defines a private window message.</span></span> <span data-ttu-id="43bcb-111">Questo messaggio viene utilizzato per notificare all'applicazione gli eventi del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="43bcb-111">This message is used to notify the application about filter graph events.</span></span> <span data-ttu-id="43bcb-112">Vedere [passaggio 6: gestire gli eventi del grafo](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="43bcb-112">See [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>
-   <span data-ttu-id="43bcb-113">`GraphEventFN` puntatore a una funzione di callback per la gestione degli eventi del grafo del filtro.</span><span class="sxs-lookup"><span data-stu-id="43bcb-113">`GraphEventFN` is a pointer to a callback function for handling filter graph events.</span></span> <span data-ttu-id="43bcb-114">Questa funzione di callback viene implementata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43bcb-114">The application implements this callback function.</span></span>
-   <span data-ttu-id="43bcb-115">La variabile membro *\_ pVideo m* fornisce un wrapper per i diversi renderer video DirectShow.</span><span class="sxs-lookup"><span data-stu-id="43bcb-115">The *m\_pVideo* member variable provides a wrapper for the various DirectShow video renderers.</span></span> <span data-ttu-id="43bcb-116">Vedere [passaggio 2: dichiarare CVideoRenderer e classi derivate](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="43bcb-116">See [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>
-   <span data-ttu-id="43bcb-117">In questa esercitazione, la funzione [SafeRelease](../medfound/saferelease.md) viene usata per rilasciare i puntatori di interfaccia com.</span><span class="sxs-lookup"><span data-stu-id="43bcb-117">Throughout this tutorial, the [SafeRelease](../medfound/saferelease.md) function is used to release COM interface pointers.</span></span>

<span data-ttu-id="43bcb-118">[Passaggio 2: dichiarare CVideoRenderer e le classi derivate](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="43bcb-118">Next: [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43bcb-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43bcb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43bcb-120">Riproduzione audio/video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="43bcb-120">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
