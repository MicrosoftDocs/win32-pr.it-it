---
description: Come individuare la durata di un file multimediale.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Come individuare la durata di un file multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530504"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>Come individuare la durata di un file multimediale

Per trovare la durata di un file multimediale, seguire questa procedura:

1.  Usare il [resolver di origine](source-resolver.md) per creare un'origine multimediale in grado di analizzare il file multimediale.
2.  Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine supporto. Questo metodo restituisce il descrittore di presentazione che descrive il contenuto del file multimediale.
3.  Eseguire una query sul descrittore di presentazione per l'attributo della [ \_ \_ durata MF PD](mf-pd-duration-attribute.md) chiamando il metodo [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) . Il valore dell'attributo, se presente, è la durata del file in unità 100-nanosecondi.


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

 

 



