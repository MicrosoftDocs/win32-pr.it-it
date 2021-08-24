---
description: Questo argomento illustra come ruotare un oggetto IWICBitmapSource usando un componente IWICBitmapFlipRotator.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Come capovolgere e ruotare un'origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a61a1546f5a0191d2e20cc3079af3e4d772e6d2c3c07a5dd1e1e4aa331dc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331547"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a>Come capovolgere e ruotare un'origine bitmap

Questo argomento illustra come ruotare [**un oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando un [**componente IWICBitmapFlipRotator.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)

Per capovolgere e ruotare un'origine bitmap

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
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

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

4.  Creare [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) da usare per capovolgere l'immagine.

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  Inizializzare l'oggetto flip/rotator con i dati dell'immagine della cornice bitmap capovolti orizzontalmente (lungo l'asse y verticale).

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    Per altre rotazioni e opzioni di capovolgimento, vedere [**WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

6.  Disegnare o elaborare l'origine bitmap capovolta.

    > [!Note]  
    > [**L'interfaccia IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) eredita dall'interfaccia [**IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) quindi è possibile usare l'oggetto flip/rotator inizializzato ovunque accetti **un oggetto IWICBitmapSource.**

     

    Nella figura seguente viene illustrato come capovolgere orizzontalmente un'immagine lungo l'asse x verticale.

    ![Figura che mostra un capovolgimento orizzontale (lungo l'asse x veritale) di un'immagine](graphics/fliphorizontal.png)

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


 

 



