---
description: Questo argomento è il passaggio 1 dell'esercitazione come riprodurre file multimediali con Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 'Passaggio 1: dichiarare la classe CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1593842ecece68fcd3c4cca35a7e2e28eac503c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308993"
---
# <a name="step-1-declare-the-cplayer-class"></a><span data-ttu-id="650b3-103">Passaggio 1: dichiarare la classe CPlayer</span><span class="sxs-lookup"><span data-stu-id="650b3-103">Step 1: Declare the CPlayer Class</span></span>

<span data-ttu-id="650b3-104">Questo argomento è il passaggio 1 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="650b3-104">This topic is step 1 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="650b3-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="650b3-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="650b3-106">In questa esercitazione la funzionalità di riproduzione è incapsulata nella `CPlayer` classe.</span><span class="sxs-lookup"><span data-stu-id="650b3-106">In this tutorial, playback functionality is encapsulated in the `CPlayer` class.</span></span> <span data-ttu-id="650b3-107">La classe `CPlayer` viene dichiarata nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="650b3-107">The `CPlayer` class is declared as follows:</span></span>


```C++
const UINT WM_APP_PLAYER_EVENT = WM_APP + 1;   

    // WPARAM = IMFMediaEvent*, WPARAM = MediaEventType

enum PlayerState
{
    Closed = 0,     // No session.
    Ready,          // Session was created, ready to open a file. 
    OpenPending,    // Session is opening a file.
    Started,        // Session is playing a file.
    Paused,         // Session is paused.
    Stopped,        // Session is stopped (ready to play). 
    Closing         // Application has closed the session, but is waiting for MESessionClosed.
};

class CPlayer : public IMFAsyncCallback
{
public:
    static HRESULT CreateInstance(HWND hVideo, HWND hEvent, CPlayer **ppPlayer);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP  GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP  Invoke(IMFAsyncResult* pAsyncResult);

    // Playback
    HRESULT       OpenURL(const WCHAR *sURL);
    HRESULT       Play();
    HRESULT       Pause();
    HRESULT       Stop();
    HRESULT       Shutdown();
    HRESULT       HandleEvent(UINT_PTR pUnkPtr);
    PlayerState   GetState() const { return m_state; }

    // Video functionality
    HRESULT       Repaint();
    HRESULT       ResizeVideo(WORD width, WORD height);
    
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }

protected:
    
    // Constructor is private. Use static CreateInstance method to instantiate.
    CPlayer(HWND hVideo, HWND hEvent);

    // Destructor is private. Caller should call Release.
    virtual ~CPlayer(); 

    HRESULT Initialize();
    HRESULT CreateSession();
    HRESULT CloseSession();
    HRESULT StartPlayback();

    // Media event handlers
    virtual HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    virtual HRESULT OnPresentationEnded(IMFMediaEvent *pEvent);
    virtual HRESULT OnNewPresentation(IMFMediaEvent *pEvent);

    // Override to handle additional session events.
    virtual HRESULT OnSessionEvent(IMFMediaEvent*, MediaEventType) 
    { 
        return S_OK; 
    }

protected:
    long                    m_nRefCount;        // Reference count.

    IMFMediaSession         *m_pSession;
    IMFMediaSource          *m_pSource;
    IMFVideoDisplayControl  *m_pVideoDisplay;

    HWND                    m_hwndVideo;        // Video window.
    HWND                    m_hwndEvent;        // App window to receive events.
    PlayerState             m_state;            // Current state of the media session.
    HANDLE                  m_hCloseEvent;      // Event to wait on while closing.
};
```



<span data-ttu-id="650b3-108">Di seguito sono riportati alcuni aspetti da considerare `CPlayer` :</span><span class="sxs-lookup"><span data-stu-id="650b3-108">Here are some things to note about `CPlayer`:</span></span>

-   <span data-ttu-id="650b3-109">L' **evento costante \_ WM \_ app \_ Player** definisce un messaggio di finestra privata.</span><span class="sxs-lookup"><span data-stu-id="650b3-109">The constant **WM\_APP\_PLAYER\_EVENT** defines a private window message.</span></span> <span data-ttu-id="650b3-110">Questo messaggio viene utilizzato per notificare all'applicazione gli eventi della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="650b3-110">This message is used to notify the application about Media Session events.</span></span> <span data-ttu-id="650b3-111">Vedere [passaggio 5: gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="650b3-111">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>
-   <span data-ttu-id="650b3-112">L' `PlayerState` enumerazione definisce gli stati possibili dell' `CPlayer` oggetto.</span><span class="sxs-lookup"><span data-stu-id="650b3-112">The `PlayerState` enumeration defines the possible states of the `CPlayer` object.</span></span>
-   <span data-ttu-id="650b3-113">La `CPlayer` classe implementa l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , che viene usata per ottenere le notifiche degli eventi dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="650b3-113">The `CPlayer` class implements the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which is used to get event notifications from the Media Session.</span></span>
-   <span data-ttu-id="650b3-114">Il `CPlayer` costruttore è privato.</span><span class="sxs-lookup"><span data-stu-id="650b3-114">The `CPlayer` constructor is private.</span></span> <span data-ttu-id="650b3-115">L'applicazione chiama il `CreateInstance` metodo statico per creare un'istanza della `CPlayer` classe.</span><span class="sxs-lookup"><span data-stu-id="650b3-115">The application calls the static `CreateInstance` method to create an instance of the `CPlayer` class.</span></span>
-   <span data-ttu-id="650b3-116">`CPlayer`Anche il distruttore è privato.</span><span class="sxs-lookup"><span data-stu-id="650b3-116">The `CPlayer` destructor is also private.</span></span> <span data-ttu-id="650b3-117">La `CPlayer` classe implementa **IUnknown**, quindi la durata dell'oggetto viene controllata tramite il conteggio dei riferimenti (*m \_ nRefCount*).</span><span class="sxs-lookup"><span data-stu-id="650b3-117">The `CPlayer` class implements **IUnknown**, so the object's lifetime is controlled through its reference count (*m\_nRefCount*).</span></span> <span data-ttu-id="650b3-118">Per eliminare definitivamente l'oggetto, l'applicazione chiama **IUnknown:: Release**, non **Delete**.</span><span class="sxs-lookup"><span data-stu-id="650b3-118">To destroy the object, the application calls **IUnknown::Release**, not **delete**.</span></span>
-   <span data-ttu-id="650b3-119">L' `CPlayer` oggetto gestisce sia la sessione multimediale che l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="650b3-119">The `CPlayer` object manages both the Media Session and the media source.</span></span>

## <a name="implement-iunknown"></a><span data-ttu-id="650b3-120">Implementare IUnknown</span><span class="sxs-lookup"><span data-stu-id="650b3-120">Implement IUnknown</span></span>

<span data-ttu-id="650b3-121">La `CPlayer` classe implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), che eredita **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="650b3-121">The `CPlayer` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), which inherits **IUnknown**.</span></span>

<span data-ttu-id="650b3-122">Il codice illustrato di seguito è un'implementazione piuttosto standard di **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="650b3-122">The code shown here is a fairly standard implementation of **IUnknown**.</span></span> <span data-ttu-id="650b3-123">Se si preferisce, è possibile utilizzare il Active Template Library (ATL) per implementare questi metodi.</span><span class="sxs-lookup"><span data-stu-id="650b3-123">If you prefer, you can use the Active Template Library (ATL) to implement these methods.</span></span> <span data-ttu-id="650b3-124">Tuttavia, non `CPlayer` supporta [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o le funzionalità com avanzate, quindi non esiste alcun motivo per cui utilizzare ATL.</span><span class="sxs-lookup"><span data-stu-id="650b3-124">However, `CPlayer` does not support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or any advanced COM features, so there is no overwhelming reason to use ATL here.</span></span>


```C++
HRESULT CPlayer::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CPlayer, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

ULONG CPlayer::AddRef()
{
    return InterlockedIncrement(&m_nRefCount);
}

ULONG CPlayer::Release()
{
    ULONG uCount = InterlockedDecrement(&m_nRefCount);
    if (uCount == 0)
    {
        delete this;
    }
    return uCount;
}
```



<span data-ttu-id="650b3-125">[Passaggio 2: creare l'oggetto CPlayer](step-2--create-the-cplayer-object.md)</span><span class="sxs-lookup"><span data-stu-id="650b3-125">Next: [Step 2: Create the CPlayer Object](step-2--create-the-cplayer-object.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="650b3-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="650b3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="650b3-127">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="650b3-127">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="650b3-128">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="650b3-128">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
