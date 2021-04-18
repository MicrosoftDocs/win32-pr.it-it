---
description: In questo argomento viene illustrato il processo di creazione di un IWICBitmapSource tramite Direct2D.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Come creare un oggetto BitmapSource tramite Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6dfdddb7cd6f7ab7341eb3c13a9fe40b797f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312395"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a>Come creare un oggetto BitmapSource tramite Direct2D

In questo argomento viene illustrato il processo di creazione di un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) tramite Direct2D.

Per creare un'origine bitmap tramite Direct2D

1.  Decodificare un'immagine di origine e ottenere un'origine bitmap. In questo esempio viene usato un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) per decodificare l'immagine e viene recuperato il primo fotogramma immagine.

    ```C++
       // Create a decoder
       IWICBitmapDecoder *pDecoder = NULL;

       hr = m_pIWICFactory->CreateDecoderFromFilename(
           szFileName,                      // Image to be decoded
           NULL,                            // Do not prefer a particular vendor
           GENERIC_READ,                    // Desired read access to the file
           WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
           &pDecoder                        // Pointer to the decoder
           );

       // Retrieve the first frame of the image from the decoder
       IWICBitmapFrameDecode *pFrame = NULL;

       if (SUCCEEDED(hr))
       {
           hr = pDecoder->GetFrame(0, &pFrame);
       }
    ```

    

    Per ulteriori tipi di origini bitmap da creare, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

2.  Converte l'origine bitmap in un formato pixel 32bppPBGRA.

    Prima che Direct2D possa usare un'immagine, è necessario convertirlo nel formato pixel 32bppPBGRA. Per convertire il formato di immagine, usare il metodo [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) per creare un oggetto [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) . Una volta creati, usare il metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) per eseguire la conversione.

    ```C++
       // Format convert the frame to 32bppPBGRA
       if (SUCCEEDED(hr))
       {
           SafeRelease(&m_pConvertedSourceBitmap);
           hr = m_pIWICFactory->CreateFormatConverter(&m_pConvertedSourceBitmap);
       }

       if (SUCCEEDED(hr))
       {
           hr = m_pConvertedSourceBitmap->Initialize(
               pFrame,                          // Input bitmap to convert
               GUID_WICPixelFormat32bppPBGRA,   // Destination pixel format
               WICBitmapDitherTypeNone,         // Specified dither pattern
               NULL,                            // Specify a particular palette 
               0.f,                             // Alpha threshold
               WICBitmapPaletteTypeCustom       // Palette translation type
               );
       }
    ```

    

3.  Creare un oggetto [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) per il rendering in un handle di finestra.

    ```C++
       // Create a D2D render target properties
       D2D1_RENDER_TARGET_PROPERTIES renderTargetProperties = D2D1::RenderTargetProperties();

       // Set the DPI to be the default system DPI to allow direct mapping
       // between image pixels and desktop pixels in different system DPI settings
       renderTargetProperties.dpiX = DEFAULT_DPI;
       renderTargetProperties.dpiY = DEFAULT_DPI;

       // Create a D2D render target
       D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

       hr = m_pD2DFactory->CreateHwndRenderTarget(
           renderTargetProperties,
           D2D1::HwndRenderTargetProperties(hWnd, size),
           &m_pRT
           );
    ```

    

    Per altre informazioni sulle destinazioni di rendering, vedere [Cenni preliminari sulle destinazioni di rendering](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Direct2D.

4.  Creare un oggetto [ID2D1Bitmap](../direct2d/render-targets-overview.md) usando il metodo [ID2D1RenderTarget:: CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) .

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  Creare [ID2D1Bitmap](../direct2d/render-targets-overview.md) usando D2D [ID2D1RenderTarget::D Metodo rawbitmap](../direct2d/id2d1rendertarget-drawbitmap.md) .

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

Il codice è stato omesso da questo esempio. Per il codice completo, vedere il [Visualizzatore di immagini WIC usando l'esempio Direct2D](-wic-sample-d2d-viewer.md).

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


[Direct2D](../direct2d/direct2d-portal.md)


 

 
