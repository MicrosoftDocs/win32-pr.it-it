---
description: Questo argomento è il passaggio 3 dell'esercitazione come riprodurre file multimediali con Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Passaggio 3: aprire un file multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058454"
---
# <a name="step-3-open-a-media-file"></a>Passaggio 3: aprire un file multimediale

Questo argomento è il passaggio 3 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).

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



Questo metodo esegue i passaggi seguenti:

1.  Chiama **CPlayer:: CreateSession** per creare una nuova istanza della sessione multimediale. Vedere [passaggio 4: creare la sessione multimediale](step-4--create-the-media-session.md).
2.  Crea un'origine multimediale dall'URL. Il codice completo per questo passaggio è illustrato nell'argomento [utilizzo del](using-the-source-resolver.md)sistema di risoluzione di origine.
3.  Chiama [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) per ottenere il descrittore di presentazione dell'origine multimediale. Il descrittore della presentazione descrive tutti i flussi nel file di origine.
4.  Crea la topologia di riproduzione. Il codice per questo passaggio è illustrato nell'argomento [creazione di topologie di riproduzione](creating-playback-topologies.md).
5.  Chiama [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.

Il metodo di [**topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) viene completato in modo asincrono. Al termine, viene chiamato il metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'oggetto CPlayer. vedere [passaggio 5: gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md).

[Passaggio 4: creare la sessione multimediale](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



