---
description: Questo argomento è il passaggio 4 dell'esercitazione come riprodurre file multimediali con Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Passaggio 4: creare la sessione multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968976"
---
# <a name="step-4-create-the-media-session"></a><span data-ttu-id="c6875-103">Passaggio 4: creare la sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="c6875-103">Step 4: Create the Media Session</span></span>

<span data-ttu-id="c6875-104">Questo argomento è il passaggio 4 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="c6875-104">This topic is step 4 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="c6875-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="c6875-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="c6875-106">`CPlayer::CreateSession`Crea una nuova istanza della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c6875-106">The `CPlayer::CreateSession` creates a new instance of the Media Session.</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



<span data-ttu-id="c6875-107">Questo metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6875-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="c6875-108">Chiama `CPlayer::CloseSession` per chiudere qualsiasi istanza precedente della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c6875-108">Calls `CPlayer::CloseSession` to close any previous instance of the Media Session.</span></span>
2.  <span data-ttu-id="c6875-109">Chiama [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare una nuova istanza della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c6875-109">Calls [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="c6875-110">Chiama il metodo [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) per richiedere l'evento successivo dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c6875-110">Calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method to request the next event from the Media Session.</span></span> <span data-ttu-id="c6875-111">Il primo parametro di **BeginGetEvent** è un puntatore all'oggetto **CPlayer** stesso, che implents l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="c6875-111">The first parameter to **BeginGetEvent** is a pointer to the **CPlayer** object itself, which implents the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>

<span data-ttu-id="c6875-112">La gestione degli eventi è descritta nel passaggio 5.</span><span class="sxs-lookup"><span data-stu-id="c6875-112">Event handling is described in step 5.</span></span>

<span data-ttu-id="c6875-113">[Passaggio 5: gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md)</span><span class="sxs-lookup"><span data-stu-id="c6875-113">Next: [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6875-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6875-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6875-115">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="c6875-115">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="c6875-116">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6875-116">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



