---
description: Come trovare la durata di un file multimediale.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Come trovare la durata di un file multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1885d356be54875079341eabc7433c9753792daf01c4848a00ee4ed4fbb343ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878845"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>Come trovare la durata di un file multimediale

Per trovare la durata di un file multimediale, seguire questa procedura:

1.  Usare il [sistema di risoluzione dell'origine](source-resolver.md) per creare un'origine multimediale in grado di analizzare il file multimediale.
2.  Chiamare [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) nell'origine multimediale. Questo metodo restituisce il descrittore di presentazione che descrive il contenuto del file multimediale.
3.  Eseguire una query sul descrittore di presentazione per [l'attributo \_ MF PD \_ DURATION](mf-pd-duration-attribute.md) chiamando il [**metodo IMFAttributes::GetUINT64.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) Il valore dell'attributo, se presente, è la durata del file in unità da 100 nanosecondi.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> </dl>

 

 



