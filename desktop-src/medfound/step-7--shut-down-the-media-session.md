---
description: Questo argomento è il passaggio 7 dell'esercitazione come riprodurre file multimediali con Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Passaggio 7: arrestare la sessione multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9fd11cde51b06d932b212f4effabf315deecb7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132187"
---
# <a name="step-7-shut-down-the-media-session"></a><span data-ttu-id="42177-103">Passaggio 7: arrestare la sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="42177-103">Step 7: Shut Down the Media Session</span></span>

<span data-ttu-id="42177-104">Questo argomento è il passaggio 7 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="42177-104">This topic is step 7 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="42177-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="42177-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="42177-106">Per arrestare la [sessione multimediale](media-session.md), seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="42177-106">To shut down the [Media Session](media-session.md), perform the following steps:</span></span>

1.  <span data-ttu-id="42177-107">Chiamare [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="42177-107">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the current presentation.</span></span>
2.  <span data-ttu-id="42177-108">Attendere l'evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="42177-108">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="42177-109">Questo evento è sicuramente l'ultimo evento della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="42177-109">This event is guaranteed to be the last event from the Media Session.</span></span>
3.  <span data-ttu-id="42177-110">Chiamare [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="42177-110">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="42177-111">Questo metodo fa sì che le sessioni multimediali rilascino le risorse.</span><span class="sxs-lookup"><span data-stu-id="42177-111">This method causes the Media Sessions to release resources.</span></span>
4.  <span data-ttu-id="42177-112">Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="42177-112">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the current media source.</span></span>

<span data-ttu-id="42177-113">Il metodo seguente arresta la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="42177-113">The following method shuts down the Media Session.</span></span> <span data-ttu-id="42177-114">Usa un handle di evento (*m \_ hCloseEvent*) per attendere l'evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="42177-114">It uses an event handle (*m\_hCloseEvent*) to wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="42177-115">Vedere [passaggio 5: gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="42177-115">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>


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



<span data-ttu-id="42177-116">Prima di uscire dall'applicazione, arrestare la sessione multimediale e chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare la piattaforma Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="42177-116">Before the application exits, shut down the Media Session, and then call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Microsoft Media Foundation platform.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="42177-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42177-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42177-118">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="42177-118">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="42177-119">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42177-119">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



