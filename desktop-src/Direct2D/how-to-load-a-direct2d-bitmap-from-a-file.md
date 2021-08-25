---
title: Come caricare una bitmap da un file
description: Illustra come caricare una bitmap Direct2D da un file di immagine.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: a330f0e32ee4abf62eb7df1c1d6a00b3f217e6f04502cebae6c489aa01eaaa9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824561"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a>Come caricare una bitmap da un file

Direct2D usa il Windows di creazione dell'immagine (WIC) per caricare le bitmap. Per caricare una bitmap da un file, usare prima gli oggetti WIC per caricare l'immagine e convertirla in un formato compatibile con Direct2D, quindi usare il [**metodo CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) per creare un oggetto [**ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

1.  Creare un [**oggetto IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) usando il [**metodo IWICImagingFactory::CreateDecoderFromFileName.**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)

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

    

2.  Recuperare un frame dall'immagine e archiviare il frame in un [**oggetto IWICBitmapFrameDecode.**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode)

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  La bitmap deve essere convertita in un formato che Direct2D può usare, quindi convertire il formato pixel dell'immagine in 32bppPBGRA. Per un elenco dei formati supportati, vedere [Formati di pixel e modalità alfa.](supported-pixel-formats-and-alpha-modes.md) Chiamare il [**metodo IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) per creare un oggetto [**IWICFormatConverter,**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) quindi chiamare il metodo [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) dell'oggetto **IWICFormatConverter** per eseguire la conversione.
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

    

4.  Chiamare il [**metodo CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) per creare un oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) che può essere disegnato da una destinazione di rendering e usato con altri oggetti Direct2D.
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

    

In questo esempio è stato omesso codice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[Come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 