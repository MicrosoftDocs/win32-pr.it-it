---
description: Un dispositivo di acquisizione video potrebbe supportare diversi formati di acquisizione. I formati in genere differiscono per tipo di compressione, spazio colore (YUV o RGB), dimensioni dei fotogrammi o frequenza dei fotogrammi.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Come impostare il formato di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0968560772345bea91f5acfb79e7157a6376f388a5c0065634a273196b7552cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974400"
---
# <a name="how-to-set-the-video-capture-format"></a>Come impostare il formato di acquisizione video

Un dispositivo di acquisizione video potrebbe supportare diversi formati di acquisizione. I formati in genere differiscono per tipo di compressione, spazio colore (YUV o RGB), dimensioni dei fotogrammi o frequenza dei fotogrammi.

L'elenco dei formati supportati è contenuto nel *descrittore di presentazione*. Per altre informazioni, vedere [Descrittori di presentazione](presentation-descriptors.md).

Per enumerare i formati supportati:

1.  Creare l'origine multimediale per il dispositivo di acquisizione. Vedere [Enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).
2.  Chiamare [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine multimediale per ottenere il descrittore di presentazione.
3.  Chiamare [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per ottenere il descrittore di flusso per il flusso video.
4.  Chiamare [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore di flusso.
5.  Chiamare [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) per ottenere il numero di formati supportati.
6.  In un ciclo chiamare [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) per ottenere ogni formato. Il formato è rappresentato da un *tipo di supporto*. Per altre informazioni, vedere [Tipi di supporti video](video-media-types.md).

L'esempio seguente enumera i formati di acquisizione per un dispositivo:


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



La `LogMediaType` funzione usata in questo esempio è elencata nell'argomento Codice di debug del tipo di [supporto](media-type-debugging-code.md).

Per impostare il formato di acquisizione:

1.  Ottenere un puntatore [**all'interfaccia IMFMediaTypeHandler,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) come illustrato nell'esempio precedente.
2.  Chiamare [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) per ottenere il formato desiderato, specificato dall'indice.
3.  Chiamare [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) per impostare il formato.

Se non si imposta il formato di acquisizione, il dispositivo userà il formato predefinito.

L'esempio seguente imposta il formato di acquisizione:


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



L'ordine in cui vengono restituiti i formati dipende dal dispositivo. In genere, vengono raggruppati per primi in base al tipo di compressione o allo spazio colore; e quindi dalle dimensioni del frame più piccole alle dimensioni più grandi del frame all'interno di ogni gruppo.

La frequenza dei fotogrammi viene gestita in modo leggermente diverso rispetto agli altri attributi di formato. Per altre informazioni, vedere [Come impostare la frequenza fotogrammi di acquisizione video](how-to-set-the-video-capture-frame-rate.md).

> [!Note]  
> In alcuni dispositivi l'elenco dei formati conterrà una voce duplicata per ogni formato. Ad esempio, se il dispositivo supporta 15 formati di acquisizione distinti, l'elenco conterrà 30 voci. All'interno di ogni coppia, uno dei tipi di supporti avrà l'attributo [**MF \_ MT AM FORMAT \_ \_ \_ TYPE**](mf-mt-am-format-type-attribute.md) uguale a **FORMAT \_ VideoInfo** e l'altro avrà **MF MT AM FORMAT \_ \_ \_ \_ TYPE** uguale a **FORMAT \_ VideoInfo2.** Questi due valori sono definiti nel file di intestazione uuids.h. Il secondo tipo può anche contenere informazioni aggiuntive sul colore ([Extended Color Information](extended-color-information.md)) o visualizzare un valore diverso per l'interlacciamento ([**MF MT \_ \_ INTERLACE \_ MODE**](mf-mt-interlace-mode-attribute.md)). Questi tipi duplicati esistono per supportare le applicazioni DirectShow precedenti. In un'Media Foundation, è necessario ignorare il tipo **FORMAT \_ VideoInfo** ogni volta che viene elencato un tipo **\_ VIDEOInfo2** FORMAT duplicato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



