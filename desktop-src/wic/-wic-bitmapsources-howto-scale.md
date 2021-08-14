---
description: Questo argomento illustra come ridimensionare un oggetto IWICBitmapSource usando il componente IWICBitmapScaler.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Come ridimensionare un'origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2771ed13c23fdb3d74cf9c24899bea7a355efefcb5e541ac21aff53f372ded0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439694"
---
# <a name="how-to-scale-a-bitmap-source"></a>Come ridimensionare un'origine bitmap

Questo argomento illustra come ridimensionare un [**oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando il [**componente IWICBitmapScaler.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)

Per ridimensionare un'origine bitmap

1.  Creare un [**oggetto IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare Windows oggetti WIC (Imaging Component).

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
    IWICBitmapScaler *pIScaler = NULL;


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

    

    Il formato di file JPEG supporta solo un singolo frame. Poiché il file in questo esempio è un file JPEG, viene usato il primo frame ( `0` ). Per i formati di immagine con più fotogrammi, vedere How to Retrieve the Frames of an Image for accessing each frame of the image [(Come](-wic-bitmapsources-howto-retrieveimageframes.md) recuperare i fotogrammi di un'immagine per accedere a ogni fotogramma dell'immagine).

4.  Creare [**L'oggetto IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) da usare per il ridimensionamento dell'immagine.

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  Inizializzare l'oggetto scaler con i dati dell'immagine del frame bitmap a metà delle dimensioni.

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

    

6.  Disegnare o elaborare l'origine bitmap ridimensionata.

    Nella figura seguente viene illustrato il ridimensionamento dell'immagine. L'immagine originale a sinistra è 200 x 130 pixel. L'immagine a destra è l'immagine originale ridimensionata a metà delle dimensioni.

    ![illustrazione che mostra il ridimensionamento di un'immagine a dimensioni inferiori](graphics/scaledregion.png)

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


 

 



