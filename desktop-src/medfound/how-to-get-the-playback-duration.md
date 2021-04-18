---
description: Questo argomento descrive come ottenere la durata di riproduzione di un file multimediale usando MFPlay.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Come ottenere la durata della riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308764"
---
# <a name="how-to-get-the-playback-duration"></a>Come ottenere la durata della riproduzione

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

Questo argomento descrive come ottenere la durata di riproduzione di un file multimediale usando MFPlay.

**Per ottenere la durata della riproduzione**

1.  Chiamare [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) per creare un elemento multimediale per il file.
2.  Chiamare [**IMFPMediaItem:: GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration). Specificare **MFP \_ POSITIONTYPE \_ 100 ns** per il primo parametro. La durata viene restituita come **PROPVARIANT** che contiene un **valore \_ Integer grande** . La durata è indicata in unità da 100 nanosecondi.

Nell'esempio seguente viene illustrato il passaggio 2:


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



