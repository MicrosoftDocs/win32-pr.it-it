---
description: Questo argomento è il passaggio 2 dell'esercitazione come riprodurre file multimediali con Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: "Passaggio 2: creare l'oggetto CPlayer"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308992"
---
# <a name="step-2-create-the-cplayer-object"></a><span data-ttu-id="c4434-103">Passaggio 2: creare l'oggetto CPlayer</span><span class="sxs-lookup"><span data-stu-id="c4434-103">Step 2: Create the CPlayer Object</span></span>

<span data-ttu-id="c4434-104">Questo argomento è il passaggio 2 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="c4434-104">This topic is step 2 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="c4434-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="c4434-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="c4434-106">Per creare un'istanza della `CPlayer` classe, l'applicazione chiama il metodo statico `CPlayer::CreateInstance` .</span><span class="sxs-lookup"><span data-stu-id="c4434-106">To create an instance of the `CPlayer` class, the application calls the static `CPlayer::CreateInstance` method.</span></span> <span data-ttu-id="c4434-107">Questo metodo accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4434-107">This method takes the following parameters:</span></span>

-   <span data-ttu-id="c4434-108">*hVideo* specifica la finestra per la visualizzazione del video.</span><span class="sxs-lookup"><span data-stu-id="c4434-108">*hVideo* specifies the window to display video.</span></span>
-   <span data-ttu-id="c4434-109">*hEvent* specifica una finestra per la ricezione di eventi.</span><span class="sxs-lookup"><span data-stu-id="c4434-109">*hEvent* specifies a window to receive events.</span></span> <span data-ttu-id="c4434-110">È possibile passare lo stesso handle per entrambi gli handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="c4434-110">It is valid to pass the same handle for both window handles.</span></span>
-   <span data-ttu-id="c4434-111">*ppPlayer* riceve un puntatore a una nuova `CPlayer` istanza.</span><span class="sxs-lookup"><span data-stu-id="c4434-111">*ppPlayer* receives a pointer to a new `CPlayer` instance.</span></span>

<span data-ttu-id="c4434-112">Nel codice seguente viene illustrato il metodo `CreateInstance`.</span><span class="sxs-lookup"><span data-stu-id="c4434-112">The following code shows the `CreateInstance` method:</span></span>


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



<span data-ttu-id="c4434-113">Il codice seguente illustra il `CPlayer` costruttore:</span><span class="sxs-lookup"><span data-stu-id="c4434-113">The following code shows the `CPlayer` constructor:</span></span>


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



<span data-ttu-id="c4434-114">Il costruttore esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4434-114">The constructor does the following:</span></span>

1.  <span data-ttu-id="c4434-115">Chiama [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare la piattaforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c4434-115">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="c4434-116">Crea un evento di reimpostazione automatica.</span><span class="sxs-lookup"><span data-stu-id="c4434-116">Creates an auto-reset event.</span></span> <span data-ttu-id="c4434-117">Questo evento viene utilizzato quando si chiude la sessione multimediale. vedere [passaggio 7: arrestare la sessione multimediale](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="c4434-117">This event is used when closing the Media Session; see [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>

<span data-ttu-id="c4434-118">Il distruttore arresta la sessione multimediale, come descritto in [passaggio 7: arrestare la sessione multimediale](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="c4434-118">The destructor shuts down the Media Session, as described in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



<span data-ttu-id="c4434-119">Si noti che il costruttore e il distruttore sono entrambi metodi di classe protetti.</span><span class="sxs-lookup"><span data-stu-id="c4434-119">Note that the constructor and destructor are both protected class methods.</span></span> <span data-ttu-id="c4434-120">L'applicazione crea l'oggetto usando il `CreateInstance` metodo statico.</span><span class="sxs-lookup"><span data-stu-id="c4434-120">The application creates the object using the static `CreateInstance` method.</span></span> <span data-ttu-id="c4434-121">Elimina l'oggetto chiamando **IUnknown:: Release**, anziché usando esplicitamente **Delete**.</span><span class="sxs-lookup"><span data-stu-id="c4434-121">It destroys the object by calling **IUnknown::Release**, rather than explicitly using **delete**.</span></span>

<span data-ttu-id="c4434-122">[Passaggio 3: aprire un file multimediale](step-3--open-a-media-file.md)</span><span class="sxs-lookup"><span data-stu-id="c4434-122">Next: [Step 3: Open a Media File](step-3--open-a-media-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4434-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4434-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4434-124">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="c4434-124">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="c4434-125">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c4434-125">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



