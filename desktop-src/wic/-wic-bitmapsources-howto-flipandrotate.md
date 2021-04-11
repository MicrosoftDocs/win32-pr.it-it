---
description: In questo argomento viene illustrato come ruotare un IWICBitmapSource tramite un componente di IWICBitmapFlipRotator.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Come capovolgere e ruotare un'origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f6a805144025f185a4f4793fc4fafb27d7695a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128979"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a><span data-ttu-id="eabb8-103">Come capovolgere e ruotare un'origine bitmap</span><span class="sxs-lookup"><span data-stu-id="eabb8-103">How to Flip and Rotate a Bitmap Source</span></span>

<span data-ttu-id="eabb8-104">In questo argomento viene illustrato come ruotare un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) tramite un componente di [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="eabb8-104">This topic demonstrates how to rotate an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using an [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) component.</span></span>

<span data-ttu-id="eabb8-105">Per capovolgere e ruotare un'origine bitmap</span><span class="sxs-lookup"><span data-stu-id="eabb8-105">To flip and rotate a bitmap source</span></span>

1.  <span data-ttu-id="eabb8-106">Creare un oggetto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="eabb8-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="eabb8-107">Usare il metodo [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) per creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) da un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="eabb8-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="eabb8-108">Ottiene il primo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="eabb8-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="eabb8-109">Il formato del file JPEG supporta solo un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="eabb8-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="eabb8-110">Poiché il file in questo esempio è un file JPEG, viene usato il primo frame ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="eabb8-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="eabb8-111">Per i formati di immagine con più frame, vedere [How to retrieve the Frames of an image to](-wic-bitmapsources-howto-retrieveimageframes.md) accessing Each frame of the image.</span><span class="sxs-lookup"><span data-stu-id="eabb8-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="eabb8-112">Creare il [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) da utilizzare per capovolgere l'immagine.</span><span class="sxs-lookup"><span data-stu-id="eabb8-112">Create the [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) to use for flipping the image.</span></span>

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  <span data-ttu-id="eabb8-113">Inizializzare l'oggetto Flip/rotatorio con i dati dell'immagine del frame bitmap capovolto orizzontalmente (lungo l'asse y verticale).</span><span class="sxs-lookup"><span data-stu-id="eabb8-113">Initialize the flip/rotator object with the image data of the bitmap frame flipped horizontally (along the vertical y-axis).</span></span>

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    <span data-ttu-id="eabb8-114">Per ulteriori rotazioni e opzioni di capovolgimento, vedere [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="eabb8-114">See [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) for additional rotations and flipping options.</span></span>

6.  <span data-ttu-id="eabb8-115">Creare o elaborare l'origine della bitmap capovolta.</span><span class="sxs-lookup"><span data-stu-id="eabb8-115">Draw or process the flipped bitmap source.</span></span>

    > [!Note]  
    > <span data-ttu-id="eabb8-116">L'interfaccia [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) eredita dall'interfaccia [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , quindi è possibile usare l'oggetto Flip/Rotator inizializzato in un punto qualsiasi che accetti un **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="eabb8-116">The [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) interface inherits from the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, so you can use the initialized flip/rotator object anywhere that accepts a **IWICBitmapSource**.</span></span>

     

    <span data-ttu-id="eabb8-117">Nella figura seguente viene illustrato il capovolgimento orizzontale di un'immagine (lungo l'asse x verticale).</span><span class="sxs-lookup"><span data-stu-id="eabb8-117">The following illustration demonstrates flipping an imaging horizontally (along the vertical x-axis).</span></span>

    ![illustrazione che mostra un capovolgimento orizzontale (lungo l'asse x autentico) di un'immagine](graphics/fliphorizontal.png)

## <a name="see-also"></a><span data-ttu-id="eabb8-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eabb8-119">See Also</span></span>

[<span data-ttu-id="eabb8-120">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="eabb8-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="eabb8-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="eabb8-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="eabb8-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="eabb8-122">Samples</span></span>](-wic-samples.md)


 

 



