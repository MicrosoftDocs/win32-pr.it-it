---
description: Questo argomento è il passaggio 3 dell'esercitazione Come riprodurre file multimediali con Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Passaggio 3: Aprire un file multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c198b07358ebbf5d8da591d75d44f4687b600f6bb387c4f55901974397308dc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012354"
---
# <a name="step-3-open-a-media-file"></a>Passaggio 3: Aprire un file multimediale

Questo argomento è il passaggio 3 dell'esercitazione [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'argomento [Esempio di riproduzione di sessioni multimediali](media-session-playback-example.md).

Il `CPlayer::OpenURL` metodo apre un file multimediale da un URL.


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



Questo metodo esegue la procedura seguente:

1.  Chiama **CPlayer::CreateSession** per creare una nuova istanza della sessione multimediale. Vedere [Passaggio 4: Creare la sessione multimediale](step-4--create-the-media-session.md).
2.  Crea un'origine multimediale dall'URL. Il codice completo per questo passaggio è illustrato nell'argomento [Using the Source Resolver](using-the-source-resolver.md).
3.  Chiama [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) per ottenere il descrittore di presentazione dell'origine multimediale. Il descrittore di presentazione descrive ogni flusso nel file di origine.
4.  Crea la topologia di riproduzione. Il codice per questo passaggio è illustrato nell'argomento [Creazione di topologie di riproduzione](creating-playback-topologies.md).
5.  Chiama [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.

Il [**metodo SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) viene completato in modo asincrono. Al termine, viene chiamato il metodo [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'oggetto CPlayer. Vedere [Passaggio 5: Gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md).

Passaggio [4: Creare la sessione multimediale](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



