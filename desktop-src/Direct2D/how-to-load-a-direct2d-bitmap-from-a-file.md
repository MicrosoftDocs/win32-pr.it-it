---
title: Come caricare una bitmap da un file
description: Viene illustrato come caricare una bitmap Direct2D da un file di immagine.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: c9590e799e71e92056157b75573565cf79b9236b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728898"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a>Come caricare una bitmap da un file

Direct2D utilizza Windows Imaging Component (WIC) per caricare le bitmap. Per caricare una bitmap da un file, usare prima di tutto gli oggetti WIC per caricare l'immagine e convertirla in un formato compatibile con Direct2D, quindi usare il metodo [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) per creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

1.  Creare un [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) usando il metodo [**IWICImagingFactory:: CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .

    ```C++
    HRESULT DemoApp::LoadBitmapFromFile(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR uri,
        UINT destinationWidth,
        UINT destinationHeight,
        ID2D1Bitmap **ppBitmap
        )
    {
        IWICBitmapDecoder *pDecoder = NULL;
        IWICBitmapFrameDecode *pSource = NULL;
        IWICStream *pStream = NULL;
        IWICFormatConverter *pConverter = NULL;
        IWICBitmapScaler *pScaler = NULL;

        HRESULT hr = pIWICFactory->CreateDecoderFromFilename(
            uri,
            NULL,
            GENERIC_READ,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
            
    ```

    

2.  Recuperare un frame dall'immagine e archiviare il frame in un oggetto [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  La bitmap deve essere convertita in un formato che può essere usato da Direct2D, quindi convertire il formato pixel dell'immagine in 32bppPBGRA. Per un elenco dei formati supportati, vedere [formati pixel e modalità Alpha](supported-pixel-formats-and-alpha-modes.md). Chiamare il metodo [**IWICImagingFactory:: CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) per creare un oggetto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , quindi chiamare il metodo [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) dell'oggetto **IWICFormatConverter** per eseguire la conversione.
    ```C++
        if (SUCCEEDED(hr))
        {

            // Convert the image format to 32bppPBGRA
            // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
            hr = pIWICFactory->CreateFormatConverter(&pConverter);

        }
     
     
        if (SUCCEEDED(hr))
        {
            hr = pConverter->Initialize(
                pSource,
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                NULL,
                0.f,
                WICBitmapPaletteTypeMedianCut
                );
    ```

    

4.  Chiamare il metodo [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) per creare un oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) che può essere disegnato da una destinazione di rendering e utilizzato con altri oggetti Direct2D.
    ```C++
        if (SUCCEEDED(hr))
        {
        
            // Create a Direct2D bitmap from the WIC bitmap.
            hr = pRenderTarget->CreateBitmapFromWicBitmap(
                pConverter,
                NULL,
                ppBitmap
                );
        }

        SafeRelease(&pDecoder);
        SafeRelease(&pSource);
        SafeRelease(&pStream);
        SafeRelease(&pConverter);
        SafeRelease(&pScaler);

        return hr;
    }
    ```

    

Il codice è stato omesso da questo esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[Come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 