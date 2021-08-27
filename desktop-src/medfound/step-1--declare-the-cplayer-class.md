---
description: Questo argomento è il passaggio 1 dell'esercitazione Come riprodurre file multimediali con Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 'Passaggio 1: Dichiarare la classe CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61f03a9054e96769414320811d32a549027defb80ff929aba2c27ad4aa5b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112911"
---
# <a name="step-1-declare-the-cplayer-class"></a>Passaggio 1: Dichiarare la classe CPlayer

Questo argomento è il passaggio 1 dell'esercitazione [Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'argomento [Esempio di riproduzione di sessioni multimediali](media-session-playback-example.md).

In questa esercitazione la funzionalità di riproduzione viene incapsulata nella `CPlayer` classe . La classe `CPlayer` viene dichiarata nel modo seguente:


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



Di seguito sono riportati alcuni aspetti da tenere presenti `CPlayer` in :

-   La costante **WM \_ APP PLAYER \_ \_ EVENT** definisce un messaggio di finestra privata. Questo messaggio viene usato per notificare all'applicazione gli eventi della sessione multimediale. Vedere [Passaggio 5: Gestire gli eventi della sessione multimediale.](step-5--handle-media-session-events.md)
-   `PlayerState`L'enumerazione definisce i possibili stati dell'oggetto `CPlayer` .
-   La `CPlayer` classe implementa [**l'interfaccia IMFAsyncCallback,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) che viene usata per ottenere le notifiche degli eventi dalla sessione multimediale.
-   Il `CPlayer` costruttore è privato. L'applicazione chiama il `CreateInstance` metodo statico per creare un'istanza della classe `CPlayer` .
-   Anche `CPlayer` il distruttore è privato. La `CPlayer` classe implementa **IUnknown,** quindi la durata dell'oggetto viene controllata tramite il relativo conteggio dei riferimenti (*m \_ nRefCount*). Per eliminare definitivamente l'oggetto, l'applicazione chiama **IUnknown::Release** e non **elimina**.
-   `CPlayer`L'oggetto gestisce sia la sessione multimediale che l'origine multimediale.

## <a name="implement-iunknown"></a>Implementare IUnknown

La `CPlayer` classe implementa [**IMFAsyncCallback,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)che eredita **IUnknown.**

Il codice illustrato di seguito è un'implementazione piuttosto standard **di IUnknown.** Se si preferisce, è possibile usare Active Template Library (ATL) per implementare questi metodi. Tuttavia, non supporta CoCreateInstance o alcuna funzionalità COM avanzata, quindi non esiste un motivo `CPlayer` eccessivo per usare ATL in questo [](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) caso.


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



Passaggio [2: Creare l'oggetto CPlayer](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
