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
# <a name="step-2-create-the-cplayer-object"></a>Passaggio 2: creare l'oggetto CPlayer

Questo argomento è il passaggio 2 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).

Per creare un'istanza della `CPlayer` classe, l'applicazione chiama il metodo statico `CPlayer::CreateInstance` . Questo metodo accetta i parametri seguenti:

-   *hVideo* specifica la finestra per la visualizzazione del video.
-   *hEvent* specifica una finestra per la ricezione di eventi. È possibile passare lo stesso handle per entrambi gli handle di finestra.
-   *ppPlayer* riceve un puntatore a una nuova `CPlayer` istanza.

Nel codice seguente viene illustrato il metodo `CreateInstance`.


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



Il codice seguente illustra il `CPlayer` costruttore:


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



Il costruttore esegue le operazioni seguenti:

1.  Chiama [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare la piattaforma Media Foundation.
2.  Crea un evento di reimpostazione automatica. Questo evento viene utilizzato quando si chiude la sessione multimediale. vedere [passaggio 7: arrestare la sessione multimediale](step-7--shut-down-the-media-session.md).

Il distruttore arresta la sessione multimediale, come descritto in [passaggio 7: arrestare la sessione multimediale](step-7--shut-down-the-media-session.md).


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



Si noti che il costruttore e il distruttore sono entrambi metodi di classe protetti. L'applicazione crea l'oggetto usando il `CreateInstance` metodo statico. Elimina l'oggetto chiamando **IUnknown:: Release**, anziché usando esplicitamente **Delete**.

[Passaggio 3: aprire un file multimediale](step-3--open-a-media-file.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



