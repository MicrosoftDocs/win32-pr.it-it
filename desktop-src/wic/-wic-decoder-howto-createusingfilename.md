---
description: In questo argomento viene descritto come creare un decodificatore bitmap utilizzando un nome file di immagine.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Come creare un decodificatore usando un nome file di immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317893"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a><span data-ttu-id="558db-103">Come creare un decodificatore usando un nome file di immagine</span><span class="sxs-lookup"><span data-stu-id="558db-103">How to Create a Decoder Using an Image Filename</span></span>

<span data-ttu-id="558db-104">In questo argomento viene descritto come creare un decodificatore bitmap utilizzando un nome file di immagine.</span><span class="sxs-lookup"><span data-stu-id="558db-104">This topic describes how to create a bitmap decoder by using an image filename.</span></span>

<span data-ttu-id="558db-105">Per creare un decodificatore bitmap utilizzando un nome file di immagine</span><span class="sxs-lookup"><span data-stu-id="558db-105">To create a bitmap decoder by using an image filename</span></span>

1.  <span data-ttu-id="558db-106">Creare un oggetto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="558db-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="558db-107">Usare il metodo [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) per creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) da un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="558db-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="558db-108">Ottiene il primo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="558db-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="558db-109">Il formato del file JPEG supporta solo un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="558db-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="558db-110">Poiché il file in questo esempio è un file JPEG, viene usato il primo frame ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="558db-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="558db-111">Per i formati di immagine con più frame, vedere [How to retrieve the Frames of an image to](-wic-bitmapsources-howto-retrieveimageframes.md) accessing Each frame of the image.</span><span class="sxs-lookup"><span data-stu-id="558db-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="558db-112">Elaborare il frame dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="558db-112">Process the image frame.</span></span> <span data-ttu-id="558db-113">Per ulteriori informazioni sugli oggetti [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="558db-113">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="558db-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="558db-114">See Also</span></span>

[<span data-ttu-id="558db-115">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="558db-115">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="558db-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="558db-116">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="558db-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="558db-117">Samples</span></span>](-wic-samples.md)


 

 



