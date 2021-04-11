---
description: Questo argomento illustra come ridimensionare un IWICBitmapSource usando il componente IWICBitmapScaler.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Come ridimensionare un'origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737f72014929065bc63ec9c6021b05e38799d06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128975"
---
# <a name="how-to-scale-a-bitmap-source"></a><span data-ttu-id="e68be-103">Come ridimensionare un'origine bitmap</span><span class="sxs-lookup"><span data-stu-id="e68be-103">How to Scale a Bitmap Source</span></span>

<span data-ttu-id="e68be-104">Questo argomento illustra come ridimensionare un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando il componente [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="e68be-104">This topic demonstrates how to scale an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) component.</span></span>

<span data-ttu-id="e68be-105">Per ridimensionare un'origine bitmap</span><span class="sxs-lookup"><span data-stu-id="e68be-105">To scale a bitmap source</span></span>

1.  <span data-ttu-id="e68be-106">Creare un oggetto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) per creare oggetti di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="e68be-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="e68be-107">Usare il metodo [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) per creare un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) da un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e68be-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapScaler *pIScaler = NULL;


    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="e68be-108">Ottiene il primo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e68be-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="e68be-109">Il formato del file JPEG supporta solo un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="e68be-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="e68be-110">Poiché il file in questo esempio è un file JPEG, viene usato il primo frame ( `0` ).</span><span class="sxs-lookup"><span data-stu-id="e68be-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="e68be-111">Per i formati di immagine con più frame, vedere [How to retrieve the Frames of an image to](-wic-bitmapsources-howto-retrieveimageframes.md) accessing Each frame of the image.</span><span class="sxs-lookup"><span data-stu-id="e68be-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="e68be-112">Creare il [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) da usare per il ridimensionamento dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e68be-112">Create the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) to use for the image scaling.</span></span>

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  <span data-ttu-id="e68be-113">Inizializzare l'oggetto scaler con i dati dell'immagine della cornice bitmap a metà delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e68be-113">Initialize the scaler object with the image data of the bitmap frame at half the size.</span></span>

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  <span data-ttu-id="e68be-114">Creare o elaborare l'origine bitmap ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="e68be-114">Draw or process the scaled bitmap source.</span></span>

    <span data-ttu-id="e68be-115">La figura seguente illustra il ridimensionamento della creazione di immagini.</span><span class="sxs-lookup"><span data-stu-id="e68be-115">The following illustration demonstrates imaging scaling.</span></span> <span data-ttu-id="e68be-116">L'immagine originale a sinistra è 200 x 130 pixel.</span><span class="sxs-lookup"><span data-stu-id="e68be-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="e68be-117">L'immagine a destra è l'immagine originale ridimensionata alla metà della dimensione.</span><span class="sxs-lookup"><span data-stu-id="e68be-117">The image on the right is the original image scaled to half the size.</span></span>

    ![illustrazione che mostra il ridimensionamento di un'immagine a dimensioni inferiori](graphics/scaledregion.png)

## <a name="see-also"></a><span data-ttu-id="e68be-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e68be-119">See Also</span></span>

[<span data-ttu-id="e68be-120">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="e68be-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="e68be-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e68be-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="e68be-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="e68be-122">Samples</span></span>](-wic-samples.md)


 

 



