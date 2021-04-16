---
description: Stride immagine
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Stride immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556888"
---
# <a name="image-stride"></a><span data-ttu-id="efddf-103">Stride immagine</span><span class="sxs-lookup"><span data-stu-id="efddf-103">Image Stride</span></span>

<span data-ttu-id="efddf-104">Quando un'immagine video è archiviata in memoria, il buffer di memoria potrebbe contenere byte di riempimento aggiuntivi dopo ogni riga di pixel.</span><span class="sxs-lookup"><span data-stu-id="efddf-104">When a video image is stored in memory, the memory buffer might contain extra padding bytes after each row of pixels.</span></span> <span data-ttu-id="efddf-105">I byte di riempimento influiscono sulla modalità di archiviazione dell'immagine in memoria, ma non influiscono sulla modalità di visualizzazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="efddf-105">The padding bytes affect how the image is stored in memory, but do not affect how the image is displayed.</span></span>

<span data-ttu-id="efddf-106">Lo *stride* è il numero di byte da una riga di pixel in memoria alla riga successiva di pixel in memoria.</span><span class="sxs-lookup"><span data-stu-id="efddf-106">The *stride* is the number of bytes from one row of pixels in memory to the next row of pixels in memory.</span></span> <span data-ttu-id="efddf-107">Stride viene anche chiamato *pitch*.</span><span class="sxs-lookup"><span data-stu-id="efddf-107">Stride is also called *pitch*.</span></span> <span data-ttu-id="efddf-108">Se sono presenti byte di riempimento, lo stride è più ampio della larghezza dell'immagine, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="efddf-108">If padding bytes are present, the stride is wider than the width of the image, as shown in the following illustration.</span></span>

![diagramma che mostra un'immagine più la spaziatura interna.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

<span data-ttu-id="efddf-110">Due buffer che contengono fotogrammi video con dimensioni uguali possono avere due diversi stride.</span><span class="sxs-lookup"><span data-stu-id="efddf-110">Two buffers that contain video frames with equal dimensions can have two different strides.</span></span> <span data-ttu-id="efddf-111">Se si elabora un'immagine video, è necessario tenere conto dello stride.</span><span class="sxs-lookup"><span data-stu-id="efddf-111">If you process a video image, you must take the stride into account.</span></span>

<span data-ttu-id="efddf-112">Inoltre, è possibile disporre in memoria di un'immagine in due modi.</span><span class="sxs-lookup"><span data-stu-id="efddf-112">In addition, there are two ways that an image can be arranged in memory.</span></span> <span data-ttu-id="efddf-113">In un'immagine dall' *alto verso il basso* , la prima riga di pixel nell'immagine viene visualizzata per prima in memoria.</span><span class="sxs-lookup"><span data-stu-id="efddf-113">In a *top-down* image, the top row of pixels in the image appears first in memory.</span></span> <span data-ttu-id="efddf-114">In un'immagine dal *basso in alto* , l'ultima riga di pixel viene visualizzata per prima nella memoria.</span><span class="sxs-lookup"><span data-stu-id="efddf-114">In a *bottom-up* image, the last row of pixels appears first in memory.</span></span> <span data-ttu-id="efddf-115">Nella figura seguente viene illustrata la differenza tra un'immagine dall'alto verso il basso e un'immagine dal basso in alto.</span><span class="sxs-lookup"><span data-stu-id="efddf-115">The following illustration shows the difference between a top-down image and a bottom-up image.</span></span>

![diagramma che mostra le immagini dall'alto verso il basso e dal basso verso l'alto.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

<span data-ttu-id="efddf-117">Un'immagine dal basso verso l'alto ha un stride negativo, perché lo stride viene definito come il numero di byte necessario per spostarsi verso il basso di una riga di pixel rispetto all'immagine visualizzata.</span><span class="sxs-lookup"><span data-stu-id="efddf-117">A bottom-up image has a negative stride, because stride is defined as the number of bytes need to move down a row of pixels, relative to the displayed image.</span></span> <span data-ttu-id="efddf-118">Le immagini YUV devono sempre essere dall'alto verso il basso e qualsiasi immagine contenuta in una superficie Direct3D deve essere dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="efddf-118">YUV images should always be top-down, and any image that is contained in a Direct3D surface must be top-down.</span></span> <span data-ttu-id="efddf-119">Le immagini RGB nella memoria di sistema sono in genere dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="efddf-119">RGB images in system memory are usually bottom-up.</span></span>

<span data-ttu-id="efddf-120">Le trasformazioni video in particolare devono gestire i buffer con stride non corrispondenti, perché il buffer di input potrebbe non corrispondere al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="efddf-120">Video transforms in particular need to handle buffers with mismatched strides, because the input buffer might not match the output buffer.</span></span> <span data-ttu-id="efddf-121">Si supponga, ad esempio, di voler convertire un'immagine di origine e scrivere il risultato in un'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efddf-121">For example, suppose that you want to convert a source image and write the result to a destination image.</span></span> <span data-ttu-id="efddf-122">Si supponga che entrambe le immagini abbiano la stessa larghezza e altezza, ma che potrebbero non avere lo stesso formato pixel o lo stesso stride di immagine.</span><span class="sxs-lookup"><span data-stu-id="efddf-122">Assume that both images have the same width and height, but might not have the same pixel format or the same image stride.</span></span>

<span data-ttu-id="efddf-123">Nell'esempio di codice riportato di seguito viene illustrato un approccio generalizzato per la scrittura di questo tipo di funzione.</span><span class="sxs-lookup"><span data-stu-id="efddf-123">The following example code shows a generalized approach for writing this kind of function.</span></span> <span data-ttu-id="efddf-124">Non si tratta di un esempio di funzionamento completo, perché astrae molti dei dettagli specifici.</span><span class="sxs-lookup"><span data-stu-id="efddf-124">This is not a complete working example, because it abstracts many of the specific details.</span></span>


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



<span data-ttu-id="efddf-125">Questa funzione accetta sei parametri:</span><span class="sxs-lookup"><span data-stu-id="efddf-125">This function takes six parameters:</span></span>

-   <span data-ttu-id="efddf-126">Puntatore all'inizio della riga di analisi 0 nell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efddf-126">A pointer to the start of scan line 0 in the destination image.</span></span>
-   <span data-ttu-id="efddf-127">Stride dell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efddf-127">The stride of the destination image.</span></span>
-   <span data-ttu-id="efddf-128">Puntatore all'inizio della riga di analisi 0 nell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="efddf-128">A pointer to the start of scan line 0 in the source image.</span></span>
-   <span data-ttu-id="efddf-129">Stride dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="efddf-129">The stride of the source image.</span></span>
-   <span data-ttu-id="efddf-130">Larghezza dell'immagine in pixel.</span><span class="sxs-lookup"><span data-stu-id="efddf-130">The width of the image in pixels.</span></span>
-   <span data-ttu-id="efddf-131">Altezza dell'immagine in pixel.</span><span class="sxs-lookup"><span data-stu-id="efddf-131">The height of the image in pixels.</span></span>

<span data-ttu-id="efddf-132">L'idea generale è elaborare una riga alla volta, scorrendo ogni pixel della riga.</span><span class="sxs-lookup"><span data-stu-id="efddf-132">The general idea is to process one row at a time, iterating over each pixel in the row.</span></span> <span data-ttu-id="efddf-133">Si supponga che il tipo di pixel di origine \_ \_ e il \_ \_ tipo di pixel dest siano strutture che rappresentano rispettivamente il layout dei pixel per le immagini di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efddf-133">Assume that SOURCE\_PIXEL\_TYPE and DEST\_PIXEL\_TYPE are structures representing the pixel layout for the source and destination images, respectively.</span></span> <span data-ttu-id="efddf-134">Ad esempio, RGB a 32 bit usa la struttura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) .</span><span class="sxs-lookup"><span data-stu-id="efddf-134">(For example, 32-bit RGB uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure.</span></span> <span data-ttu-id="efddf-135">Non ogni formato pixel ha una struttura predefinita.) Il cast del puntatore di matrice al tipo di struttura consente di accedere ai componenti RGB o YUV di ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="efddf-135">Not every pixel format has a predefined structure.) Casting the array pointer to the structure type enables you to access the RGB or YUV components of each pixel.</span></span> <span data-ttu-id="efddf-136">All'inizio di ogni riga, la funzione Archivia un puntatore alla riga.</span><span class="sxs-lookup"><span data-stu-id="efddf-136">At the start of each row, the function stores a pointer to the row.</span></span> <span data-ttu-id="efddf-137">Alla fine della riga, il puntatore viene incrementato in base alla larghezza dello stride dell'immagine, che sposta il puntatore alla riga successiva.</span><span class="sxs-lookup"><span data-stu-id="efddf-137">At the end of the row, it increments the pointer by the width of the image stride, which advances the pointer to the next row.</span></span>

<span data-ttu-id="efddf-138">In questo esempio viene chiamata una funzione ipotetica denominata TransformPixelValue per ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="efddf-138">This example calls a hypothetical function named TransformPixelValue for each pixel.</span></span> <span data-ttu-id="efddf-139">Potrebbe trattarsi di qualsiasi funzione che calcola un pixel di destinazione da un pixel di origine.</span><span class="sxs-lookup"><span data-stu-id="efddf-139">This could be any function that calculates a target pixel from a source pixel.</span></span> <span data-ttu-id="efddf-140">Naturalmente, i dettagli esatti dipenderanno dall'attività specifica.</span><span class="sxs-lookup"><span data-stu-id="efddf-140">Of course, the exact details will depend on the particular task.</span></span> <span data-ttu-id="efddf-141">Se, ad esempio, si dispone di un formato YUV planare, è necessario accedere ai piani Chroma indipendentemente dal piano Luma; con video interlacciato, potrebbe essere necessario elaborare i campi separatamente. e così via.</span><span class="sxs-lookup"><span data-stu-id="efddf-141">For example, if you have a planar YUV format, you must access the chroma planes independently from the luma plane; with interlaced video, you might need to process the fields separately; and so forth.</span></span>

<span data-ttu-id="efddf-142">Per fornire un esempio più concreto, il codice seguente converte un'immagine RGB a 32 bit in un'immagine AYUV.</span><span class="sxs-lookup"><span data-stu-id="efddf-142">To give a more concrete example, the following code converts a 32-bit RGB image into an AYUV image.</span></span> <span data-ttu-id="efddf-143">È possibile accedere ai pixel RGB usando una struttura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) e si accede ai pixel AYUV usando una struttura della struttura [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .</span><span class="sxs-lookup"><span data-stu-id="efddf-143">The RGB pixels are accessed using an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, and the AYUV pixels are accessed using a [**DXVA2\_AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) structure structure.</span></span>


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



<span data-ttu-id="efddf-144">Nell'esempio seguente viene convertita un'immagine RGB a 32 bit in un'immagine YV12.</span><span class="sxs-lookup"><span data-stu-id="efddf-144">The next example converts a 32-bit RGB image to a YV12 image.</span></span> <span data-ttu-id="efddf-145">Questo esempio illustra come gestire un formato YUV planare.</span><span class="sxs-lookup"><span data-stu-id="efddf-145">This example shows how to handle a planar YUV format.</span></span> <span data-ttu-id="efddf-146">(YV12 è un formato Planar 4:2:0). In questo esempio, la funzione mantiene tre puntatori distinti per i tre piani nell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efddf-146">(YV12 is a planar 4:2:0 format.) In this example, the function maintains three separate pointers for the three planes in the target image.</span></span> <span data-ttu-id="efddf-147">Tuttavia, l'approccio di base è identico a quello dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="efddf-147">However, the basic approach is the same as the previous example.</span></span>


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



<span data-ttu-id="efddf-148">In tutti questi esempi, si presuppone che l'applicazione abbia già determinato lo stride dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="efddf-148">In all of these examples, it is assumed that the application has already determined the image stride.</span></span> <span data-ttu-id="efddf-149">A volte è possibile ottenere queste informazioni dal buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="efddf-149">You can sometimes get this information from the media buffer.</span></span> <span data-ttu-id="efddf-150">In caso contrario, è necessario calcolarlo in base al formato video.</span><span class="sxs-lookup"><span data-stu-id="efddf-150">Otherwise, you must calculate it based on the video format.</span></span> <span data-ttu-id="efddf-151">Per altre informazioni sul calcolo dello stride dell'immagine e sull'uso di buffer multimediali per video, vedere [buffer video non compressi](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="efddf-151">For more information about calculating image stride and working with media buffers for video, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="efddf-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efddf-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efddf-153">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="efddf-153">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="efddf-154">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="efddf-154">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
