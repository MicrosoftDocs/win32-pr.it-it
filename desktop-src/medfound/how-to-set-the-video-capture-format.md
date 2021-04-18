---
description: Un dispositivo di acquisizione video potrebbe supportare diversi formati di acquisizione. I formati generalmente variano in base al tipo di compressione, allo spazio colore (YUV o RGB), alle dimensioni del frame o alla frequenza dei fotogrammi.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Come impostare il formato di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310841"
---
# <a name="how-to-set-the-video-capture-format"></a>Come impostare il formato di acquisizione video

Un dispositivo di acquisizione video potrebbe supportare diversi formati di acquisizione. I formati generalmente variano in base al tipo di compressione, allo spazio colore (YUV o RGB), alle dimensioni del frame o alla frequenza dei fotogrammi.

L'elenco dei formati supportati è contenuto nel *descrittore della presentazione*. Per ulteriori informazioni, vedere [descrittori di presentazione](presentation-descriptors.md).

Per enumerare i formati supportati:

1.  Creare l'origine multimediale per il dispositivo di acquisizione. Vedere [enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).
2.  Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine del supporto per ottenere il descrittore della presentazione.
3.  Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per ottenere il descrittore del flusso per il flusso video.
4.  Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore del flusso.
5.  Chiamare [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) per ottenere il numero di formati supportati.
6.  In un ciclo, chiamare [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) per ottenere ogni formato. Il formato è rappresentato da un *tipo di supporto*. Per ulteriori informazioni, vedere [tipi di supporti video](video-media-types.md).

Nell'esempio seguente vengono enumerati i formati di acquisizione per un dispositivo:


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



La `LogMediaType` funzione utilizzata in questo esempio è elencata nell'argomento [codice di debug del tipo di supporto](media-type-debugging-code.md).

Per impostare il formato di acquisizione:

1.  Ottenere un puntatore all'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , come illustrato nell'esempio precedente.
2.  Chiamare [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) per ottenere il formato desiderato, specificato dall'indice.
3.  Chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) per impostare il formato.

Se non si imposta il formato di acquisizione, il dispositivo utilizzerà il formato predefinito.

Nell'esempio seguente viene impostato il formato di acquisizione:


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



L'ordine in cui vengono restituiti i formati dipende dal dispositivo. Vengono in genere raggruppati per primo in base al tipo di compressione o allo spazio dei colori; e quindi dalla dimensione minima del fotogramma alla dimensione massima del fotogramma all'interno di ogni gruppo.

La frequenza dei fotogrammi viene gestita in modo leggermente diverso rispetto agli altri attributi di formato. Per altre informazioni, vedere [How to set the video Capture frame rate](how-to-set-the-video-capture-frame-rate.md).

> [!Note]  
> In alcuni dispositivi, l'elenco di formato conterrà una voce duplicata per ogni formato. Se, ad esempio, il dispositivo supporta 15 formati di acquisizione distinti, l'elenco conterrà 30 voci. All'interno di ogni coppia uno dei tipi di supporto avrà l'attributo [**MF \_ mt \_ am \_ \_ tipo di formato**](mf-mt-am-format-type-attribute.md) uguale a **Format \_ videoinfo** e l'altro avrà il **tipo di \_ formato MF mt \_ \_ \_ am** uguale a **Format \_ VideoInfo2**. Questi due valori vengono definiti nel file di intestazione UUIDs. h. Il secondo tipo può inoltre contenere informazioni sui colori aggiuntive ([informazioni sui colori estese](extended-color-information.md)) o visualizzare un valore diverso per l'interlacciamento ([**\_ \_ \_ modalità di interpolazione MF mt**](mf-mt-interlace-mode-attribute.md)). Questi tipi duplicati sono disponibili per supportare le applicazioni DirectShow precedenti. In un'applicazione Media Foundation è consigliabile ignorare il **formato \_ videoinfo** ogni volta che viene elencato un tipo **\_ VideoInfo2 di formato** duplicato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



