---
description: Questo argomento è il passaggio 4 dell'esercitazione Come riprodurre file multimediali con Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Passaggio 4: Creare la sessione multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9c31d4c5e07abe8f088aad38fec9f91046a7d4338905dbd917de9d414fd4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847771"
---
# <a name="step-4-create-the-media-session"></a>Passaggio 4: Creare la sessione multimediale

Questo argomento è il passaggio 4 dell'esercitazione [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'argomento [Esempio di riproduzione di sessioni multimediali](media-session-playback-example.md).

Crea `CPlayer::CreateSession` una nuova istanza della sessione multimediale.


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



Questo metodo esegue la procedura seguente:

1.  Chiama `CPlayer::CloseSession` per chiudere qualsiasi istanza precedente della sessione multimediale.
2.  Chiama [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare una nuova istanza della sessione multimediale.
3.  Chiama il [**metodo IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) per richiedere l'evento successivo dalla sessione multimediale. Il primo parametro di **BeginGetEvent** è un puntatore all'oggetto **CPlayer** stesso, che implaca [**l'interfaccia IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)

La gestione degli eventi è descritta nel passaggio 5.

Passaggio [5: Gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



