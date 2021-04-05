---
description: In questo argomento viene illustrato come caricare un IWICBitmapFrameDecode da una risorsa dell'applicazione.
ms.assetid: 2260ad3a-44d4-4fe2-aa8c-608ffc11fbfb
title: Come caricare una bitmap da una risorsa (componente di Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb33ad57b3b9dac1cb5d98719c681adb38c11de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882453"
---
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a>Come caricare una bitmap da una risorsa (componente di Windows Imaging)

In questo argomento viene illustrato come caricare un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da una risorsa dell'applicazione.

1.  Nel file di definizione della risorsa dell'applicazione (RC) definire la risorsa. Nell'esempio seguente viene definita una `Image` risorsa denominata `IDR_SAMPLE_IMAGE` .

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    La risorsa verrà aggiunta alle risorse dell'applicazione quando viene compilata l'applicazione.

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

    

4.  Utilizzare il metodo [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) per creare un oggetto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inizializzarlo utilizzando il puntatore memoria immagine.

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

    

5.  Creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) dal nuovo oggetto flusso usando il metodo [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

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

    

    Questo codice recupera solo il primo `0` frame () dell'immagine. Per le immagini multiframe, usare [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) per determinare il numero di frame nell'immagine.

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


 

 



