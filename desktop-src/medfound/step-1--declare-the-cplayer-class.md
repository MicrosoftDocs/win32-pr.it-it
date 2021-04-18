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
# <a name="step-1-declare-the-cplayer-class"></a>Passaggio 1: dichiarare la classe CPlayer

Questo argomento è il passaggio 1 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).

In questa esercitazione la funzionalità di riproduzione è incapsulata nella `CPlayer` classe. La classe `CPlayer` viene dichiarata nel modo seguente:


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



Di seguito sono riportati alcuni aspetti da considerare `CPlayer` :

-   L' **evento costante \_ WM \_ app \_ Player** definisce un messaggio di finestra privata. Questo messaggio viene utilizzato per notificare all'applicazione gli eventi della sessione multimediale. Vedere [passaggio 5: gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md).
-   L' `PlayerState` enumerazione definisce gli stati possibili dell' `CPlayer` oggetto.
-   La `CPlayer` classe implementa l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , che viene usata per ottenere le notifiche degli eventi dalla sessione multimediale.
-   Il `CPlayer` costruttore è privato. L'applicazione chiama il `CreateInstance` metodo statico per creare un'istanza della `CPlayer` classe.
-   `CPlayer`Anche il distruttore è privato. La `CPlayer` classe implementa **IUnknown**, quindi la durata dell'oggetto viene controllata tramite il conteggio dei riferimenti (*m \_ nRefCount*). Per eliminare definitivamente l'oggetto, l'applicazione chiama **IUnknown:: Release**, non **Delete**.
-   L' `CPlayer` oggetto gestisce sia la sessione multimediale che l'origine del supporto.

## <a name="implement-iunknown"></a>Implementare IUnknown

La `CPlayer` classe implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), che eredita **IUnknown**.

Il codice illustrato di seguito è un'implementazione piuttosto standard di **IUnknown**. Se si preferisce, è possibile utilizzare il Active Template Library (ATL) per implementare questi metodi. Tuttavia, non `CPlayer` supporta [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o le funzionalità com avanzate, quindi non esiste alcun motivo per cui utilizzare ATL.


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



[Passaggio 2: creare l'oggetto CPlayer](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
