---
description: In questo argomento viene descritto come riprodurre un segmento di un file multimediale in MFPlay, impostando le ore di inizio e di fine per la riproduzione.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Come riprodurre una clip di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879934"
---
# <a name="how-to-play-a-file-clip"></a>Come riprodurre una clip di file

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

In questo argomento viene descritto come riprodurre un segmento di un file multimediale in MFPlay, impostando le ore di inizio e di fine per la riproduzione.

**Per riprodurre una clip di file**

1.  Chiamare [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) per creare un elemento multimediale per il file.
2.  Facoltativamente, ottenere la durata totale del file, come descritto in [come ottenere la durata della riproduzione](how-to-get-the-playback-duration.md).
3.  Chiamare [**IMFPMediaItem:: SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) per impostare l'ora di inizio e di fine. L'ora di arresto non deve superare la durata del file.
4.  Chiamare [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) per avviare la riproduzione.

Nell'esempio seguente viene utilizzata la versione di blocco di [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl). Se viene usata la versione non bloccante, il codice visualizzato dopo **CreateMediaItemFromURL** deve essere inserito nel gestore per il tipo di **\_ evento MFP \_ \_ MEDIAITEM \_ creato** evento. Per ulteriori informazioni sugli eventi in MFPlay, vedere [ricezione di eventi dal lettore](getting-started-with-mfplay.md).

Per ottenere la durata del file, in questo esempio viene chiamata la `GetPlaybackDuration` funzione illustrata nell'argomento [come ottenere la durata della riproduzione](how-to-get-the-playback-duration.md).


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



