---
description: In questo argomento viene illustrato come ottenere una parte rettangolare di un IWICBitmapSource utilizzando un componente di IWICBitmapClipper.
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: Come ritagliare un'origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554660"
---
# <a name="how-to-clip-a-bitmap-source"></a><span data-ttu-id="8e98a-103">Come ritagliare un'origine bitmap</span><span class="sxs-lookup"><span data-stu-id="8e98a-103">How to Clip a Bitmap Source</span></span>

<span data-ttu-id="8e98a-104">In questo argomento viene illustrato come ottenere una parte rettangolare di un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) utilizzando un componente di [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="8e98a-104">This topic demonstrates how to obtain a rectangular portion of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using an [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) component.</span></span>

<span data-ttu-id="8e98a-105">Per ritagliare un'origine bitmap</span><span class="sxs-lookup"><span data-stu-id="8e98a-105">To clip a bitmap source</span></span>

1.  <span data-ttu-id="8e98a-106">Creare un oggetto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="8e98a-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="8e98a-107">Usare il metodo [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) per creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) da un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="8e98a-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="8e98a-108">Ottiene il primo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="8e98a-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="8e98a-109">Il formato del file JPEG supporta solo un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="8e98a-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="8e98a-110">Poiché il file in questo esempio è un file JPEG, viene usato il primo frame ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="8e98a-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="8e98a-111">Per i formati di immagine con più frame, vedere [How to retrieve the Frames of an image to](-wic-bitmapsources-howto-retrieveimageframes.md) accessing Each frame of the image.</span><span class="sxs-lookup"><span data-stu-id="8e98a-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="8e98a-112">Creare il [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) da usare per il ritaglio dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="8e98a-112">Create the [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) to use for the image clipping.</span></span>

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  <span data-ttu-id="8e98a-113">Inizializzare l'oggetto Clipper con i dati dell'immagine all'interno del rettangolo specificato del frame bitmap.</span><span class="sxs-lookup"><span data-stu-id="8e98a-113">Initialize the clipper object with the image data within the given rectangle of the bitmap frame.</span></span>

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  <span data-ttu-id="8e98a-114">Creare o elaborare l'immagine ritagliata.</span><span class="sxs-lookup"><span data-stu-id="8e98a-114">Draw or process the clipped image.</span></span>

    <span data-ttu-id="8e98a-115">Nella figura seguente viene illustrato il ritaglio della creazione di immagini.</span><span class="sxs-lookup"><span data-stu-id="8e98a-115">The following illustration demonstrates imaging clipping.</span></span> <span data-ttu-id="8e98a-116">L'immagine originale a sinistra è 200 x 130 pixel.</span><span class="sxs-lookup"><span data-stu-id="8e98a-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="8e98a-117">L'immagine a destra è l'immagine originale ritagliata in un rettangolo definito come `{20,20,100,100}` .</span><span class="sxs-lookup"><span data-stu-id="8e98a-117">The image on the right is the original image clipped to a rectangle defined as `{20,20,100,100}`.</span></span>

    ![illustrazione del ritaglio di immagini](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a><span data-ttu-id="8e98a-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8e98a-119">See Also</span></span>

[<span data-ttu-id="8e98a-120">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="8e98a-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="8e98a-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8e98a-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="8e98a-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="8e98a-122">Samples</span></span>](-wic-samples.md)


 

 



