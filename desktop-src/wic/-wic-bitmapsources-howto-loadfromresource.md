---
description: Questo argomento illustra come caricare un IWICBitmapFrameDecode da una risorsa dell'applicazione.
ms.assetid: 2260ad3a-44d4-4fe2-aa8c-608ffc11fbfb
title: Come caricare una bitmap da una risorsa (Windows Imaging Component)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88bc10766ed6720e60dd85a9600107c883da80d7b326ddd810b6261e509915da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034743"
---
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a>Come caricare una bitmap da una risorsa (Windows Imaging Component)

Questo argomento illustra come caricare un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da una risorsa dell'applicazione.

1.  Nel file di definizione della risorsa dell'applicazione (RC) definire la risorsa. Nell'esempio seguente viene definita `Image` una risorsa denominata `IDR_SAMPLE_IMAGE` .

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    La risorsa verrà aggiunta alle risorse dell'applicazione quando l'applicazione viene compilata.

2.  Caricare la risorsa dall'applicazione.

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  Bloccare la risorsa e ottenere le dimensioni.

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  Usare il [**metodo CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) per creare un [**oggetto IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inizializzarlo usando il puntatore di memoria dell'immagine.

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

5.  Creare un [**oggetto IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) dal nuovo oggetto flusso usando il [**metodo CreateDecoderFromStream.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

6.  Recuperare un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dall'immagine decodificata.

    ```C++
    // Retrieve the initial frame.
    if (SUCCEEDED(hr)){
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Questo codice recupera solo il primo frame ( `0` ) dell'immagine. Per le immagini con più frame, usare [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) per determinare il numero di fotogrammi nell'immagine.

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


 

 



