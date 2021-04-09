---
description: In questo argomento viene illustrato come decodificare un'immagine a più frame e come recuperare ogni frame per l'elaborazione.
ms.assetid: e4f69608-7bf1-4d54-b586-b749526700c9
title: Come recuperare i frame da un'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeeb19e0a0ac69f75673df0736fd0bd4987b3423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128978"
---
# <a name="how-to-retrieve-the-frames-from-an-image"></a><span data-ttu-id="51134-103">Come recuperare i frame da un'immagine</span><span class="sxs-lookup"><span data-stu-id="51134-103">How to Retrieve the Frames from an Image</span></span>

<span data-ttu-id="51134-104">In questo argomento viene illustrato come decodificare un'immagine a più frame e come recuperare ogni frame per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="51134-104">This topic demonstrates how to decode a multi-frame image and retrieve each frame for processing.</span></span>

<span data-ttu-id="51134-105">Per recuperare i frame di un'immagine</span><span class="sxs-lookup"><span data-stu-id="51134-105">To retrieve the frames of an image</span></span>

1.  <span data-ttu-id="51134-106">Creare un [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="51134-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="51134-107">Usare il metodo [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) per creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) da un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="51134-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    UINT nFrameCount = 0;
    UINT uiWidth, uiHeight;

    // Create decoder for an image.
    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"creek.tiff",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="51134-108">Recuperare il numero di frame nelle immagini.</span><span class="sxs-lookup"><span data-stu-id="51134-108">Retrieve the number of frames in the images.</span></span>

    ```C++
    // Retrieve the frame count of the image.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrameCount(&nFrameCount);
    }
    ```

    

4.  <span data-ttu-id="51134-109">Elaborare ogni frame ottenendo un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) per ogni frame nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="51134-109">Process each frame by obtaining an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) for each frame in the image.</span></span>

    ```C++
    // Process each frame in the image.
    for (UINT i=0; i < nFrameCount; i++)
    {
       // Retrieve the next bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoder->GetFrame(i, &pIDecoderFrame);
       }

       // Retrieve the size of the bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoderFrame->GetSize(&uiWidth, &uiHeight);
       }

       // Additional frame processing.
       // ...

       SafeRelease(&pIDecoderFrame);
    }
    ```

    

## <a name="see-also"></a><span data-ttu-id="51134-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="51134-110">See Also</span></span>

[<span data-ttu-id="51134-111">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="51134-111">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="51134-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="51134-112">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="51134-113">Esempi</span><span class="sxs-lookup"><span data-stu-id="51134-113">Samples</span></span>](-wic-samples.md)


 

 



