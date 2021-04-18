---
description: In questo argomento viene descritto come creare un decodificatore bitmap utilizzando un flusso.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Come creare un decodificatore usando un flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319115"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a>Come creare un decodificatore usando un flusso

In questo argomento viene descritto come creare un decodificatore bitmap utilizzando un flusso.

Per creare un decodificatore bitmap utilizzando un flusso

1.  Caricare un file di immagine in un flusso. In questo esempio viene creato un flusso per una risorsa dell'applicazione.

    Nel file di definizione della risorsa dell'applicazione (RC) definire la risorsa. Nell'esempio seguente viene definita una `Image` risorsa denominata `IDR_SAMPLE_IMAGE` .

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

    

4.  Creare un [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti di Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  Utilizzare il metodo [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) per creare un oggetto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inizializzarlo utilizzando il puntatore memoria immagine.

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

    

6.  Creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) dal nuovo oggetto flusso usando il metodo [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

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

    

7.  Ottiene il primo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dell'immagine.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Il formato del file JPEG supporta solo un singolo frame. Poiché il file in questo esempio è un file JPEG, viene usato il primo frame ( `0` ). Per i formati di immagine con più frame, vedere [How to retrieve the Frames of an image to](-wic-bitmapsources-howto-retrieveimageframes.md) accessing Each frame of the image.

8.  Elaborare il frame dell'immagine. Per ulteriori informazioni sugli oggetti [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).

## <a name="see-also"></a>Vedere anche

[Guida per programmatori](-wic-programming-guide.md)


[Riferimento](-wic-codec-reference.md)


[Esempi](-wic-samples.md)


 

 



