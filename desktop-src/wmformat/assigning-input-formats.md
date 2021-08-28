---
title: Assegnazione di formati di input
description: Assegnazione di formati di input
ms.assetid: 44c4ed7e-b35e-4ab5-9975-021f343dab6a
keywords:
- Advanced Systems Format (ASF), assegnazione di formati di input
- ASF (Advanced Systems Format), assegnazione di formati di input
- profili, assegnazione di formati di input
- codec, assegnazione di formati di input
- Advanced Systems Format (ASF), assegnazioni di formato di input
- ASF (Advanced Systems Format), assegnazioni di formato di input
- profili, assegnazioni di formato di input
- codec, assegnazioni di formato di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6f87ec74bc5d3750d65ecc91e2df4640a6ed02c9e9a9425b27897e70f825983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840331"
---
# <a name="assigning-input-formats"></a>Assegnazione di formati di input

Dopo aver identificato il formato di input corrispondente ai dati, è possibile impostarlo per l'uso da parte del writer chiamando [**IWMWriter::SetInputProps.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)

Per i flussi video, è necessario impostare le dimensioni dei fotogrammi negli esempi di input. Il codice di esempio seguente illustra come configurare e impostare un input video. Usa la **funzione FindInputFormat** definita nella sezione Per enumerare i formati di [input](to-enumerate-input-formats.md) per ottenere il formato di input per video RGB a 24 bit. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice.](using-the-code-examples.md)


```C++
HRESULT ConfigureVideoInput(IWMWriter* pWriter,
                            DWORD dwInput,
                            GUID guidSubType,
                            LONG lFrameWidth,
                            LONG lFrameHeight)
{
    DWORD   cbSize = 0;
    LONG    lStride = 0;

    IWMInputMediaProps* pProps  = NULL;
    WM_MEDIA_TYPE*      pType   = NULL;
    WMVIDEOINFOHEADER*  pVidHdr = NULL;
    BITMAPINFOHEADER*   pbmi    = NULL;

    // Get the base input format for the required subtype.
    HRESULT hr = FindInputFormat(pWriter, dwInput, guidSubType, &pProps);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Get the size of the media type structure.
    hr = pProps->GetMediaType(NULL, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Allocate memory for the media type structure.
    pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
    if (pType == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }
    
    // Get the media type structure.
    hr = pProps->GetMediaType(pType, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Adjust the format to match your source images.

    // First set pointers to the video structures.
    pVidHdr = (WMVIDEOINFOHEADER*) pType->pbFormat;
    pbmi  = &(pVidHdr->bmiHeader);
        
    pbmi->biWidth  = lFrameWidth;  
    pbmi->biHeight = lFrameHeight;
    
    // Stride = (width * bytes/pixel), rounded to the next DWORD boundary.
    lStride = (lFrameWidth * (pbmi->biBitCount / 8) + 3) & ~3;


    // Image size = stride * height. 
    pbmi->biSizeImage = lFrameHeight * lStride;

    // Apply the adjusted type to the video input. 
    hr = pProps->SetMediaType(pType);
    if (FAILED(hr))
    {
        goto Exit;
    }

    hr = pWriter->SetInputProps(dwInput, pProps);

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```





## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso degli input**](working-with-inputs.md)
</dt> </dl>

 

 




