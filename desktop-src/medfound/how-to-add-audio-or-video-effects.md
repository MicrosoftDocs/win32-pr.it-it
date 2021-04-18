---
description: Questo argomento descrive come usare gli effetti audio/video con MFPlay.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Come aggiungere effetti audio o video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310847"
---
# <a name="how-to-add-audio-or-video-effects"></a>Come aggiungere effetti audio o video

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

Questo argomento descrive come usare gli effetti audio/video con MFPlay.

Per usare un effetto con MFPlay, è necessario implementare l'effetto come trasformazione Media Foundation (MFT). Per ulteriori informazioni, vedere [trasformazioni Media Foundation](media-foundation-transforms.md).

**Per aggiungere un effetto audio o video**

1.  Creare un'istanza del MFT che implementi l'effetto.
2.  Chiamare [**IMFPMediaPlayer:: InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).

Chiamare [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) prima di aprire il file multimediale per la riproduzione. MFPlay determina automaticamente se l'effetto è un effetto video o un effetto audio.

Il metodo [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) accetta anche un parametro booleano che specifica se l'effetto è facoltativo o obbligatorio. Se MFPlay non è in grado di aggiungere un effetto obbligatorio, ad esempio perché il formato del flusso è incompatibile, si verifica un errore di riproduzione. Nella maggior parte dei casi, è preferibile impostare un effetto come facoltativo.

MFPlay continua a usare l'effetto per tutta la riproduzione successiva. Per rimuovere l'effetto, chiamare [**IMFPMediaPlayer:: RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) o [**IMFPMediaPlayer:: RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).


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

 

 



