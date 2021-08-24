---
description: Questo argomento è il passaggio 7 dell'esercitazione Come riprodurre file multimediali con Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Passaggio 7: Arrestare la sessione multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1eec6e798ee260c83fc1532c2012aed8a53625b12195848ac00fcdcf8fae3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721946"
---
# <a name="step-7-shut-down-the-media-session"></a>Passaggio 7: Arrestare la sessione multimediale

Questo argomento è il passaggio 7 dell'esercitazione [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'argomento [Esempio di riproduzione di sessioni multimediali](media-session-playback-example.md).

Per arrestare la [sessione multimediale,](media-session.md)seguire questa procedura:

1.  Chiamare [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la presentazione corrente.
2.  Attendere [l'evento MESessionClosed.](mesessionclosed.md) Questo evento è garantito come ultimo evento della sessione multimediale.
3.  Chiamare [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Questo metodo fa in modo che le sessioni multimediali rilascino le risorse.
4.  Chiamare [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine multimediale corrente.

Il metodo seguente arresta la sessione multimediale. Usa un handle di evento (*m \_ hCloseEvent*) per attendere l'evento [MESessionClosed.](mesessionclosed.md) Vedere [Passaggio 5: Gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md).


```C++
//  Close the media session. 
HRESULT CPlayer::CloseSession()
{
    //  The IMFMediaSession::Close method is asynchronous, but the 
    //  CPlayer::CloseSession method waits on the MESessionClosed event.
    //  
    //  MESessionClosed is guaranteed to be the last event that the 
    //  media session fires.

    HRESULT hr = S_OK;

    SafeRelease(&m_pVideoDisplay);

    // First close the media session.
    if (m_pSession)
    {
        DWORD dwWaitResult = 0;

        m_state = Closing;
           
        hr = m_pSession->Close();
        // Wait for the close operation to complete
        if (SUCCEEDED(hr))
        {
            dwWaitResult = WaitForSingleObject(m_hCloseEvent, 5000);
            if (dwWaitResult == WAIT_TIMEOUT)
            {
                assert(FALSE);
            }
            // Now there will be no more events from this session.
        }
    }

    // Complete shutdown operations.
    if (SUCCEEDED(hr))
    {
        // Shut down the media source. (Synchronous operation, no events.)
        if (m_pSource)
        {
            (void)m_pSource->Shutdown();
        }
        // Shut down the media session. (Synchronous operation, no events.)
        if (m_pSession)
        {
            (void)m_pSession->Shutdown();
        }
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pSession);
    m_state = Closed;
    return hr;
}
```



Prima che l'applicazione venga chiusa, arrestare la sessione multimediale e quindi chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare la Microsoft Media Foundation piattaforma.


```C++
//  Release all resources held by this object.
HRESULT CPlayer::Shutdown()
{
    // Close the session
    HRESULT hr = CloseSession();

    // Shutdown the Media Foundation platform
    MFShutdown();

    if (m_hCloseEvent)
    {
        CloseHandle(m_hCloseEvent);
        m_hCloseEvent = NULL;
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



