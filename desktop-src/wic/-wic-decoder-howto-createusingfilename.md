---
description: Questo argomento descrive come creare un decodificatore bitmap usando un nome file di immagine.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Come creare un decodificatore usando un nome file di immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867581e06692188913e4bb1af4956956c462c46bc189a4983f3c5d24bc38c986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811991"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a>Come creare un decodificatore usando un nome file di immagine

Questo argomento descrive come creare un decodificatore bitmap usando un nome file di immagine.

Per creare un decodificatore bitmap usando un nome file di immagine

1.  Creare un [**oggetto IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Usare il [**metodo CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) per creare un [**oggetto IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) da un file di immagine.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Ottenere il primo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dell'immagine.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Il formato di file JPEG supporta solo un singolo frame. Poiché il file in questo esempio è un file JPEG, viene usato il primo fotogramma ( `0` ). Per i formati di immagine con più fotogrammi, vedere [Come recuperare i](-wic-bitmapsources-howto-retrieveimageframes.md) fotogrammi di un'immagine per accedere a ogni fotogramma dell'immagine.

4.  Elaborare la cornice dell'immagine. Per altre informazioni sugli [**oggetti IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) vedere Cenni preliminari sulle [origini bitmap](-wic-bitmapsources.md).

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


 

 



