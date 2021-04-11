---
description: Questo argomento illustra come ridimensionare un IWICBitmapSource usando il componente IWICBitmapScaler.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Come ridimensionare un'origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737f72014929065bc63ec9c6021b05e38799d06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128975"
---
# <a name="how-to-scale-a-bitmap-source"></a>Come ridimensionare un'origine bitmap

Questo argomento illustra come ridimensionare un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando il componente [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .

Per ridimensionare un'origine bitmap

1.  Creare un oggetto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti di Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Usare il metodo [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) per creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) da un file di immagine.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapScaler *pIScaler = NULL;


    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Ottiene il primo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dell'immagine.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Il formato del file JPEG supporta solo un singolo frame. Poiché il file in questo esempio è un file JPEG, viene usato il primo frame ( `0` ). Per i formati di immagine con più frame, vedere [How to retrieve the Frames of an image to](-wic-bitmapsources-howto-retrieveimageframes.md) accessing Each frame of the image.

4.  Creare il [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) da usare per il ridimensionamento dell'immagine.

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  Inizializzare l'oggetto scaler con i dati dell'immagine della cornice bitmap a metà delle dimensioni.

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  Creare o elaborare l'origine bitmap ridimensionata.

    La figura seguente illustra il ridimensionamento della creazione di immagini. L'immagine originale a sinistra è 200 x 130 pixel. L'immagine a destra è l'immagine originale ridimensionata alla metà della dimensione.

    ![illustrazione che mostra il ridimensionamento di un'immagine a dimensioni inferiori](graphics/scaledregion.png)

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


 

 



