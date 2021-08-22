---
description: Questo argomento è il passaggio 7 dell'esercitazione Riproduzione audio/video in DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 'Passaggio 7: Controlli di trasporto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8253efab566f5dc14a0d0210a26e84cb0a50113389d54b7a871d818a17296ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072415"
---
# <a name="step-7-transport-controls"></a>Passaggio 7: Controlli di trasporto

Questo argomento è il passaggio 7 dell'esercitazione [Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md). Il codice completo è illustrato nell'argomento DirectShow [Esempio di riproduzione](directshow-playback-example.md).

L'ultimo passaggio consiste nell'aggiungere controlli di trasporto (riproduzione, pausa e arresto). Per riprodurre il file, chiamare [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).


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



Per sospendere, chiamare [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).


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



Per arrestare, chiamare [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Esempio di riproduzione](directshow-playback-example.md)
</dt> <dt>

[Stati di filtro](filter-states.md)
</dt> </dl>

 

 



