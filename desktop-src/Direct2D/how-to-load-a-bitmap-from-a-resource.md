---
title: Come caricare una bitmap da una risorsa (Direct2D)
description: Viene illustrato come caricare una bitmap Direct2D archiviata come risorsa dell'applicazione.
ms.assetid: 7285e6ea-ebc7-4693-8a77-99bff0b5d0d1
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: fe96ba4e0674392333173df7daeb5a354a379343
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300740"
---
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a>Come caricare una bitmap da una risorsa (Direct2D)

Come descritto in [come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D usa Windows Imaging Component (WIC) per caricare le bitmap. Per caricare una bitmap da una risorsa, usare oggetti WIC per caricare l'immagine e convertirla in un formato compatibile con Direct2D; quindi, usare il metodo [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) per creare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

1.  Nel [file di definizione della risorsa dell'applicazione](/windows/desktop/menurc/about-resource-files)definire la risorsa. Nell'esempio seguente viene definita una risorsa denominata "SampleImage".

    ```C++
    // THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
    // ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
    // THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
    // PARTICULAR PURPOSE.
    //
    // Copyright (c) Microsoft Corporation. All rights reserved
    #include "windows.h"

    SampleImage Image "sampleImage.jpg"
    ```

Questa risorsa verrà aggiunta al file di risorse dell'applicazione quando viene compilata l'applicazione.

2.  Caricare l'immagine dal file di risorse dell'applicazione.

    ```C++
    HRESULT DemoApp::LoadResourceBitmap(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR resourceName,
        PCWSTR resourceType,
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

        HRSRC imageResHandle = NULL;
        HGLOBAL imageResDataHandle = NULL;
        void *pImageFile = NULL;
        DWORD imageFileSize = 0;

        // Locate the resource.
        imageResHandle = FindResourceW(HINST_THISCOMPONENT, resourceName, resourceType);
        HRESULT hr = imageResHandle ? S_OK : E_FAIL;
        if (SUCCEEDED(hr))
        {
            // Load the resource.
            imageResDataHandle = LoadResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageResDataHandle ? S_OK : E_FAIL;
        }
    ```

    

3.  Blocca la risorsa e calcola la dimensione dell'immagine.
    ```C++
        if (SUCCEEDED(hr))
        {
            // Lock it to get a system memory pointer.
            pImageFile = LockResource(imageResDataHandle);

            hr = pImageFile ? S_OK : E_FAIL;
        }
        if (SUCCEEDED(hr))
        {
            // Calculate the size.
            imageFileSize = SizeofResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageFileSize ? S_OK : E_FAIL;
            
        }
    ```

    

4.  Usare il metodo [**IWICImagingFactory:: CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) per creare un oggetto [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) .
    ```C++
        if (SUCCEEDED(hr))
        {
              // Create a WIC stream to map onto the memory.
            hr = pIWICFactory->CreateStream(&pStream);
        }
        if (SUCCEEDED(hr))
        {
            // Initialize the stream with the memory pointer and size.
            hr = pStream->InitializeFromMemory(
                reinterpret_cast<BYTE*>(pImageFile),
                imageFileSize
                );
        }
    ```

    

5.  Usare il metodo [**IWICImagingFactory:: CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) per creare un [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create a decoder for the stream.
            hr = pIWICFactory->CreateDecoderFromStream(
                pStream,
                NULL,
                WICDecodeMetadataCacheOnLoad,
                &pDecoder
                );
        }
    ```

    

6.  Recuperare un frame dall'immagine e archiviarlo in un oggetto [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  Prima che Direct2D possa usare l'immagine, è necessario convertirla nel formato pixel 32bppPBGRA. Per convertire il formato di immagine, usare il metodo [**IWICImagingFactory:: CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) per creare un oggetto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , quindi usare il metodo [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) dell'oggetto **IWICFormatConverter** per eseguire la conversione.
 
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

    

8.  Infine, utilizzare il metodo [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) per creare un oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) che può essere disegnato da una destinazione di rendering e utilizzato con altri oggetti Direct2D.
    ```C++
        if (SUCCEEDED(hr))
        {
            //create a Direct2D bitmap from the WIC bitmap.
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

[Come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 
