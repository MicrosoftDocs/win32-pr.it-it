---
title: Assegnazione di formati di input
description: Assegnazione di formati di input
ms.assetid: 44c4ed7e-b35e-4ab5-9975-021f343dab6a
keywords:
- Formato di sistemi avanzati (ASF), assegnazione dei formati di input
- ASF (Advanced Systems Format), assegnazione dei formati di input
- profili, assegnazione di formati di input
- codec, assegnazione di formati di input
- ASF (Advanced Systems Format), assegnazioni di formato di input
- ASF (formato avanzato dei sistemi), assegnazioni di formato di input
- profili, assegnazioni di formato di input
- codec, assegnazioni di formato di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c6ad1bcdf161b335d9367d7de4df84b7eb2e6ea
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516573"
---
# <a name="assigning-input-formats"></a>Assegnazione di formati di input

Dopo aver identificato il formato di input corrispondente ai dati, è possibile impostarlo per l'uso da parte del writer chiamando [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).

Per i flussi video, è necessario impostare la dimensione dei frame negli esempi di input. Nell'esempio di codice seguente viene illustrato come configurare e impostare un input video. Usa la funzione **FindInputFormat** definita nella sezione [per enumerare i formati di input](to-enumerate-input-formats.md) per ottenere il formato di input per il video RGB a 24 bit. Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).


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

[**Utilizzo degli input**](working-with-inputs.md)
</dt> </dl>

 

 




