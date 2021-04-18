---
description: Questo argomento descrive come usare MFPlay per visualizzare l'anteprima del video da una videocamera video.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Anteprima video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308977"
---
# <a name="video-preview"></a>Anteprima video

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

Questo argomento descrive come usare MFPlay per visualizzare l'anteprima del video da una videocamera video.

MFPlay fornisce il modo più semplice per Microsoft Media Foundation di visualizzare in anteprima i video da un dispositivo di acquisizione. È consigliabile utilizzare MFPlay se si verificano tutte le condizioni seguenti:

-   Non è necessario acquisire il video in un file.
-   Non è necessario un controllo con granularità fine sulla modalità di rendering del video. Non è ad esempio necessario controllare la creazione del dispositivo Direct3D.
-   Non è necessario elaborare i dati video dalla fotocamera prima del rendering.

In caso contrario, il [lettore di origine](source-reader.md) potrebbe essere un'opzione migliore.

Per usare MFPlay con un dispositivo di acquisizione video, seguire questa procedura:

1.  Creare un'origine multimediale per il dispositivo di acquisizione. Vedere [enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).
2.  Chiamare [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) per creare un'istanza dell'oggetto Player.
3.  Chiamare il metodo [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) . Passare un puntatore all'interfaccia IMFMediaSource dell'origine multimediale. Il metodo riceve un puntatore all'interfaccia [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .
4.  Chiamare [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).
5.  Chiamare [**IMFPMediaPlayer::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) per iniziare l'anteprima.

Il codice seguente illustra questi passaggi:


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



In una tipica applicazione, si fornirebbe un puntatore a un'interfaccia di callback nella funzione [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) e si userà l'interfaccia di callback per ottenere gli eventi dal lettore. Per semplicità, il codice illustrato di seguito Ignora questa procedura. Per ulteriori informazioni, vedere [Introduzione con MFPlay](getting-started-with-mfplay.md).

### <a name="shutting-down"></a>Chiusura in corso

Prima di uscire dall'applicazione, arrestare l'origine del supporto e l'oggetto Player come indicato di seguito:

1.  Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine multimediale.
2.  Chiamare [**IMFPMediaPlayer:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) sull'oggetto Player.


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MFPlay](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[Acquisizione video](audio-video-capture.md)
</dt> </dl>

 

 



