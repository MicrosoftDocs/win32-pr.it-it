---
description: Un dispositivo di acquisizione video potrebbe supportare un intervallo di frequenza dei fotogrammi.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Come impostare la frequenza dei fotogrammi di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308755"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Come impostare la frequenza dei fotogrammi di acquisizione video

Un dispositivo di acquisizione video potrebbe supportare un intervallo di frequenza dei fotogrammi. Se queste informazioni sono disponibili, le frequenze dei fotogrammi minime e massime vengono archiviate come attributi di tipo multimediale:



| Attributo                                                         | Descrizione         |
|-------------------------------------------------------------------|---------------------|
| [\_intervallo di \_ frequenza frame MF mt \_ \_ \_ Max](mf-mt-frame-rate-range-max.md) | Frequenza massima di fotogrammi. |
| [\_intervallo di \_ \_ frequenza frame \_ MF \_ mt](mf-mt-frame-rate-range-min.md) | Frequenza minima del fotogramma. |



 

L'intervallo può variare a seconda del formato di acquisizione. Ad esempio, in dimensioni di frame più grandi, la frequenza massima dei frame potrebbe essere ridotta.

Per impostare la frequenza dei fotogrammi:

1.  Creare l'origine multimediale per il dispositivo di acquisizione. Vedere [enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).
2.  Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine del supporto per ottenere il descrittore della presentazione.
3.  Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per ottenere il descrittore del flusso per il flusso video.
4.  Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore del flusso.
5.  Enumerare i formati di acquisizione, come descritto in [come impostare il formato di acquisizione video](how-to-set-the-video-capture-format.md).
6.  Selezionare il formato di output desiderato nell'elenco.
7.  Eseguire una query sul tipo di supporto per gli attributi [MF \_ mt \_ frame \_ rate \_ \_ Max](mf-mt-frame-rate-range-max.md) e [MF \_ mt \_ frame \_ rate \_ Range \_ min](mf-mt-frame-rate-range-min.md) . Questi valori forniscono la gamma di frequenze dei frame supportate. Il dispositivo potrebbe supportare altre frequenze dei fotogrammi all'interno di questo intervallo.
8.  Impostare l'attributo [**MF \_ mt \_ frame**](mf-mt-frame-rate-attribute.md) sul tipo di supporto per specificare la frequenza dei fotogrammi desiderata.
9.  Chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) con il tipo di supporto modificato.

Nell'esempio seguente viene impostata la frequenza dei fotogrammi uguale alla frequenza massima di frame supportata dal dispositivo:


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

 

 



