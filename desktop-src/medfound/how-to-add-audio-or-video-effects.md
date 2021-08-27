---
description: Questo argomento descrive come usare gli effetti audio/video con MFPlay.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Come aggiungere effetti audio o video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af2bb310ab4818cac5dd2804d2bb696c284fdd868d916e4e543a205328e909e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061551"
---
# <a name="how-to-add-audio-or-video-effects"></a>Come aggiungere effetti audio o video

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

Questo argomento descrive come usare gli effetti audio/video con MFPlay.

Per usare un effetto con MFPlay, l'effetto deve essere implementato come trasformazione Media Foundation (MFT). Per altre informazioni, vedere [Media Foundation Transforms.](media-foundation-transforms.md)

**Per aggiungere un effetto audio o video**

1.  Creare un'istanza di MFT che implementa l'effetto.
2.  Chiamare [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).

Chiamare [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) prima di aprire il file multimediale per la riproduzione. MFPlay determina automaticamente se l'effetto è un effetto video o audio.

Il [**metodo InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) accetta anche un parametro booleano che specifica se l'effetto è facoltativo o obbligatorio. Se MFPlay non può aggiungere un effetto obbligatorio (ad esempio, perché il formato del flusso non è compatibile), si verifica un errore di riproduzione. Nella maggior parte dei casi, è meglio impostare un effetto come facoltativo.

MFPlay continua a usare l'effetto per tutta la riproduzione successiva. Per rimuovere l'effetto, chiamare [**IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) o [**IMFPMediaPlayer::RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



