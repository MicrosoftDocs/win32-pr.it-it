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
# <a name="how-to-create-a-decoder-using-a-stream"></a><span data-ttu-id="7c37d-103">Come creare un decodificatore usando un flusso</span><span class="sxs-lookup"><span data-stu-id="7c37d-103">How to Create a Decoder Using a Stream</span></span>

<span data-ttu-id="7c37d-104">In questo argomento viene descritto come creare un decodificatore bitmap utilizzando un flusso.</span><span class="sxs-lookup"><span data-stu-id="7c37d-104">This topic describes how to create a bitmap decoder by using a stream.</span></span>

<span data-ttu-id="7c37d-105">Per creare un decodificatore bitmap utilizzando un flusso</span><span class="sxs-lookup"><span data-stu-id="7c37d-105">To create a bitmap decoder by using a stream</span></span>

1.  <span data-ttu-id="7c37d-106">Caricare un file di immagine in un flusso.</span><span class="sxs-lookup"><span data-stu-id="7c37d-106">Load an image file into a stream.</span></span> <span data-ttu-id="7c37d-107">In questo esempio viene creato un flusso per una risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c37d-107">In this example, a stream is created for an application resource.</span></span>

    <span data-ttu-id="7c37d-108">Nel file di definizione della risorsa dell'applicazione (RC) definire la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c37d-108">In the application resource definition (.rc) file, define the resource.</span></span> <span data-ttu-id="7c37d-109">Nell'esempio seguente viene definita una `Image` risorsa denominata `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="7c37d-109">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="7c37d-110">La risorsa verrà aggiunta alle risorse dell'applicazione quando viene compilata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c37d-110">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="7c37d-111">Caricare la risorsa dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c37d-111">Load the resource from the application.</span></span>

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

    

3.  <span data-ttu-id="7c37d-112">Bloccare la risorsa e ottenere le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="7c37d-112">Lock the resource and get the size.</span></span>

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

    

4.  <span data-ttu-id="7c37d-113">Creare un [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="7c37d-113">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  <span data-ttu-id="7c37d-114">Utilizzare il metodo [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) per creare un oggetto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inizializzarlo utilizzando il puntatore memoria immagine.</span><span class="sxs-lookup"><span data-stu-id="7c37d-114">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

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

    

6.  <span data-ttu-id="7c37d-115">Creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) dal nuovo oggetto flusso usando il metodo [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="7c37d-115">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

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

    

7.  <span data-ttu-id="7c37d-116">Ottiene il primo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c37d-116">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="7c37d-117">Il formato del file JPEG supporta solo un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="7c37d-117">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="7c37d-118">Poiché il file in questo esempio è un file JPEG, viene usato il primo frame ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="7c37d-118">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="7c37d-119">Per i formati di immagine con più frame, vedere [How to retrieve the Frames of an image to](-wic-bitmapsources-howto-retrieveimageframes.md) accessing Each frame of the image.</span><span class="sxs-lookup"><span data-stu-id="7c37d-119">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

8.  <span data-ttu-id="7c37d-120">Elaborare il frame dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c37d-120">Process the image frame.</span></span> <span data-ttu-id="7c37d-121">Per ulteriori informazioni sugli oggetti [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="7c37d-121">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7c37d-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7c37d-122">See Also</span></span>

[<span data-ttu-id="7c37d-123">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="7c37d-123">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="7c37d-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7c37d-124">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="7c37d-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="7c37d-125">Samples</span></span>](-wic-samples.md)


 

 



