---
description: Un dispositivo di acquisizione video potrebbe supportare un intervallo di frequenze fotogrammi.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Come impostare la frequenza fotogrammi di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0e80c26c5a53a89cbc87ca509f25db1ebccf4571b4dda2e83ea63717c7d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827971"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Come impostare la frequenza fotogrammi di acquisizione video

Un dispositivo di acquisizione video potrebbe supportare un intervallo di frequenze fotogrammi. Se queste informazioni sono disponibili, le frequenze fotogrammi minime e massime vengono archiviate come attributi del tipo di supporto:



| Attributo                                                         | Descrizione         |
|-------------------------------------------------------------------|---------------------|
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MAX](mf-mt-frame-rate-range-max.md) | Frequenza massima dei fotogrammi. |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md) | Frequenza fotogrammi minima. |



 

L'intervallo può variare a seconda del formato di acquisizione. Ad esempio, con dimensioni di fotogrammi maggiori, la frequenza massima dei fotogrammi potrebbe essere ridotta.

Per impostare la frequenza dei fotogrammi:

1.  Creare l'origine multimediale per il dispositivo di acquisizione. Vedere [Enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).
2.  Chiamare [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine multimediale per ottenere il descrittore di presentazione.
3.  Chiamare [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per ottenere il descrittore di flusso per il flusso video.
4.  Chiamare [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore di flusso.
5.  Enumerare i formati di acquisizione, come descritto in [Come impostare il formato di acquisizione video](how-to-set-the-video-capture-format.md).
6.  Selezionare il formato di output desiderato nell'elenco.
7.  Eseguire una query sul tipo di supporto per gli attributi [ \_ MF MT \_ FRAME RATE \_ RANGE \_ \_ MAX](mf-mt-frame-rate-range-max.md) e [MF MT FRAME RATE \_ \_ RANGE \_ \_ \_ MIN.](mf-mt-frame-rate-range-min.md) Questi valori forniscono l'intervallo di frequenze dei fotogrammi supportate. Il dispositivo potrebbe supportare altre frequenze fotogrammi all'interno di questo intervallo.
8.  Impostare [**l'attributo \_ MF MT \_ FRAME**](mf-mt-frame-rate-attribute.md) sul tipo di supporto per specificare la frequenza fotogrammi desiderata.
9.  Chiamare [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) con il tipo di supporto modificato.

L'esempio seguente imposta la frequenza dei fotogrammi uguale alla frequenza fotogrammi massima che il dispositivo supporta:


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



