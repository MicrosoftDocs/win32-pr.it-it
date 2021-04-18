---
description: Questo argomento è il passaggio 7 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 'Passaggio 7: controlli di trasporto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b974ccc8c186b1915d2a6564870a0b177073544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316312"
---
# <a name="step-7-transport-controls"></a><span data-ttu-id="d59b8-103">Passaggio 7: controlli di trasporto</span><span class="sxs-lookup"><span data-stu-id="d59b8-103">Step 7: Transport Controls</span></span>

<span data-ttu-id="d59b8-104">Questo argomento è il passaggio 7 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="d59b8-104">This topic is step 7 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="d59b8-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="d59b8-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="d59b8-106">L'ultimo passaggio consiste nell'aggiungere controlli di trasporto (riproduzione, pausa e arresto).</span><span class="sxs-lookup"><span data-stu-id="d59b8-106">The last step is to add transport controls (play, pause, and stop).</span></span> <span data-ttu-id="d59b8-107">Per riprodurre il file, chiamare [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span><span class="sxs-lookup"><span data-stu-id="d59b8-107">To play the file, call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span></span>


```C++
HRESULT DShowPlayer::Play()
{
    if (m_state != STATE_PAUSED && m_state != STATE_STOPPED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Run();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_RUNNING;
    }
    return hr;
}
```



<span data-ttu-id="d59b8-108">Per sospendere, chiamare [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span><span class="sxs-lookup"><span data-stu-id="d59b8-108">To pause, call [**IMediaControl::Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span></span>


```C++
HRESULT DShowPlayer::Pause()
{
    if (m_state != STATE_RUNNING)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_PAUSED;
    }
    return hr;
}
```



<span data-ttu-id="d59b8-109">Per arrestare, chiamare [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="d59b8-109">To stop, call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>


```C++
HRESULT DShowPlayer::Stop()
{
    if (m_state != STATE_RUNNING && m_state != STATE_PAUSED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_STOPPED;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d59b8-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d59b8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d59b8-111">Riproduzione audio/video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d59b8-111">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d59b8-112">Esempio di riproduzione DirectShow</span><span class="sxs-lookup"><span data-stu-id="d59b8-112">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="d59b8-113">Stati filtro</span><span class="sxs-lookup"><span data-stu-id="d59b8-113">Filter States</span></span>](filter-states.md)
</dt> </dl>

 

 



