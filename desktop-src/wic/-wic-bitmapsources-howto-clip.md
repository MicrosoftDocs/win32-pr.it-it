---
description: In questo argomento viene illustrato come ottenere una parte rettangolare di un IWICBitmapSource utilizzando un componente di IWICBitmapClipper.
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: Come ritagliare un'origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554660"
---
# <a name="how-to-clip-a-bitmap-source"></a>Come ritagliare un'origine bitmap

In questo argomento viene illustrato come ottenere una parte rettangolare di un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) utilizzando un componente di [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .

Per ritagliare un'origine bitmap

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

4.  Creare il [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) da usare per il ritaglio dell'immagine.

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  Inizializzare l'oggetto Clipper con i dati dell'immagine all'interno del rettangolo specificato del frame bitmap.

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  Creare o elaborare l'immagine ritagliata.

    Nella figura seguente viene illustrato il ritaglio della creazione di immagini. L'immagine originale a sinistra è 200 x 130 pixel. L'immagine a destra è l'immagine originale ritagliata in un rettangolo definito come `{20,20,100,100}` .

    ![illustrazione del ritaglio di immagini](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


 

 



