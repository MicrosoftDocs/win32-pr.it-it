---
description: Implementazione di IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementazione di IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347186"
---
# <a name="implementing-iwicbitmapsourcetransform"></a><span data-ttu-id="c87b9-103">Implementazione di IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="c87b9-103">Implementing IWICBitmapSourceTransform</span></span>

## <a name="iwicbitmapsourcetransform"></a><span data-ttu-id="c87b9-104">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="c87b9-104">IWICBitmapSourceTransform</span></span>

<span data-ttu-id="c87b9-105">Sebbene sia facoltativo, è consigliabile che ogni decodificatore implementi questa interfaccia sulla classe di decodifica a livello di frame, in quanto può offrire notevoli vantaggi a livello di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c87b9-105">Though optional, we highly recommend that every decoder implement this interface on your frame-level decoding class, because it can provide major performance benefits.</span></span> <span data-ttu-id="c87b9-106">Quando un'applicazione richiede un'area specifica di interesse, dimensioni, orientamento o formato pixel, anziché semplicemente decodificare l'intera immagine alla risoluzione completa e quindi applicare le trasformazioni richieste, Windows Imaging Component (WIC) chiama [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per questa interfaccia nell'oggetto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="c87b9-106">When an application requests a specific region of interest, size, orientation, or pixel format, instead of just decoding the whole image at full resolution and then applying the requested transforms, Windows Imaging Component (WIC) calls [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for this interface on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span> <span data-ttu-id="c87b9-107">Se il decodificatore di frame lo supporta, WIC chiama il metodo o i metodi appropriati per determinare se il decodificatore di frame può eseguire la trasformazione richiesta o determinare il formato pixel o dimensioni più vicino che il decodificatore può fornire a quello richiesto.</span><span class="sxs-lookup"><span data-stu-id="c87b9-107">If the frame decoder supports it, WIC calls the appropriate method or methods to determine whether the frame decoder can perform the requested transform or determine the closest size or pixel format the decoder can provide to the one requested.</span></span> <span data-ttu-id="c87b9-108">Se il decodificatore è in grado di eseguire la trasformazione o le trasformazioni richieste, WIC richiama [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con i parametri appropriati.</span><span class="sxs-lookup"><span data-stu-id="c87b9-108">If the decoder can perform the requested transform or transforms, WIC invokes [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the appropriate parameters.</span></span> <span data-ttu-id="c87b9-109">Se il decodificatore è in grado di eseguire alcune, ma non tutte le trasformazioni richieste, WIC chiede al decodificatore di eseguire quelle che possono e utilizza gli oggetti di trasformazione WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) per eseguire le trasformazioni rimanenti che non possono essere eseguite dal decodificatore del frame sul risultato della chiamata **CopyPixels** .</span><span class="sxs-lookup"><span data-stu-id="c87b9-109">If the decoder can perform some, but not all of the requested transforms, WIC asks the decoder to perform those that it can, and uses the WIC transform objects ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) to perform the remaining transforms that could not be performed by the frame decoder on the result of the **CopyPixels** call.</span></span> <span data-ttu-id="c87b9-110">Se il decodificatore non supporta [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), è necessario che WIC usi gli oggetti Transform per eseguire tutte le trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="c87b9-110">If the decoder doesn’t support [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), then WIC must use the transform objects to perform all of the transforms.</span></span> <span data-ttu-id="c87b9-111">È in genere molto più efficiente per il decodificatore eseguire trasformazioni durante il processo di decodifica rispetto a decodificare l'intera immagine e quindi eseguire le trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="c87b9-111">It’s usually much more efficient for the decoder to perform transforms during the decoding process than it is to decode the entire image and then perform the transforms.</span></span> <span data-ttu-id="c87b9-112">Ciò vale soprattutto per le operazioni, ad esempio il ridimensionamento a una dimensione molto più piccola o le conversioni di formato pixel.</span><span class="sxs-lookup"><span data-stu-id="c87b9-112">This is especially true for operations such as scaling to a much smaller size or pixel format conversions.</span></span>


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [<span data-ttu-id="c87b9-113">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="c87b9-113">DoesSupportTransform</span></span>](#doessupporttransform)
-   [<span data-ttu-id="c87b9-114">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="c87b9-114">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="c87b9-115">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="c87b9-115">GetClosestSize</span></span>](#getclosestsize)
-   [<span data-ttu-id="c87b9-116">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="c87b9-116">GetClosestPixelFormat</span></span>](#getclosestpixelformat)

### <a name="doessupporttransform"></a><span data-ttu-id="c87b9-117">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="c87b9-117">DoesSupportTransform</span></span>

<span data-ttu-id="c87b9-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) chiede se il decodificatore supporta la rotazione o l'operazione di capovolgimento richiesta.</span><span class="sxs-lookup"><span data-stu-id="c87b9-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) asks whether the decoder supports the requested rotation or flipping operation.</span></span> <span data-ttu-id="c87b9-119">I [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) che possono essere richiesti sono:</span><span class="sxs-lookup"><span data-stu-id="c87b9-119">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) that may be requested are:</span></span>


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a><span data-ttu-id="c87b9-120">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="c87b9-120">CopyPixels</span></span>

<span data-ttu-id="c87b9-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) esegue il lavoro effettivo di decodifica dei bit dell'immagine, ad esempio il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sull'interfaccia [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , ma il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) su [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) è molto più potente e può migliorare significativamente le prestazioni di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="c87b9-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) performs the actual work of decoding the image bits, such as the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, but the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method on [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) is much more powerful, and can improve image processing performance significantly.</span></span>

<span data-ttu-id="c87b9-122">Quando vengono richieste più operazioni di trasformazione, il risultato dipende dall'ordine in cui vengono eseguite le operazioni.</span><span class="sxs-lookup"><span data-stu-id="c87b9-122">When multiple transform operations are requested, the result is dependent on the order in which the operations are performed.</span></span> <span data-ttu-id="c87b9-123">Per garantire la prevedibilità e la coerenza tra i codec, è importante che tutti i codec eseguano queste operazioni nello stesso ordine.</span><span class="sxs-lookup"><span data-stu-id="c87b9-123">To ensure predictability and consistency across codecs, it’s important that all codecs perform these operations in the same order.</span></span> <span data-ttu-id="c87b9-124">Questo è l'ordine canonico per l'esecuzione di queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="c87b9-124">This is the canonical order for performing these operations.</span></span>

1.  <span data-ttu-id="c87b9-125">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="c87b9-125">Scale</span></span>
2.  <span data-ttu-id="c87b9-126">Ritaglia</span><span class="sxs-lookup"><span data-stu-id="c87b9-126">Crop</span></span>
3.  <span data-ttu-id="c87b9-127">Ruota</span><span class="sxs-lookup"><span data-stu-id="c87b9-127">Rotate</span></span>

<span data-ttu-id="c87b9-128">La conversione del formato pixel può essere eseguita in qualsiasi momento, perché non ha alcun effetto sulle altre trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="c87b9-128">Pixel format conversion can be performed at any time, because it has no effect on the other transforms.</span></span>

<span data-ttu-id="c87b9-129">Il primo parametro, *prcSrc*, viene usato per specificare l'area di interesse per il ritaglio dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c87b9-129">The first parameter, *prcSrc*, is used to specify the region of interest for clipping the image.</span></span> <span data-ttu-id="c87b9-130">Poiché il ridimensionamento viene eseguito prima del ritaglio per convenzione, se l'immagine deve essere ridimensionata e ritagliata, è necessario determinare l'area di interesse dopo che l'immagine è stata ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="c87b9-130">Because scaling is performed before clipping by convention, if the image is to be scaled as well as clipped, the region of interest should be determined after the image has been scaled.</span></span>

<span data-ttu-id="c87b9-131">Il secondo e il terzo parametro indicano le dimensioni a cui ridimensionare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="c87b9-131">The second and third parameters indicate the size to which to scale the image.</span></span>

<span data-ttu-id="c87b9-132">Il parametro *pguidDstFormat* indica il formato pixel richiesto per l'immagine decodificata.</span><span class="sxs-lookup"><span data-stu-id="c87b9-132">The *pguidDstFormat* parameter indicates the requested pixel format for the decoded image.</span></span> <span data-ttu-id="c87b9-133">Poiché WIC ha già chiamato [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), deve essere un formato pixel che il decodificatore ha indicato che supporta.</span><span class="sxs-lookup"><span data-stu-id="c87b9-133">Because WIC has already called [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), this should be a pixel format that the decoder has indicated that it supports.</span></span>

<span data-ttu-id="c87b9-134">Il parametro *dstTransform* indica l'angolo di rotazione richiesto e se capovolgere l'immagine verticalmente, orizzontalmente o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c87b9-134">The *dstTransform* parameter indicates the requested rotation angle, and whether to flip the image vertically, horizontally, or both.</span></span> <span data-ttu-id="c87b9-135">Anche in questo caso, poiché WIC avrà già chiamato [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), la trasformazione richiesta dovrebbe essere una delle quali il decodificatore ha già indicato che supporta.</span><span class="sxs-lookup"><span data-stu-id="c87b9-135">Again, because WIC will have already called [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), the requested transform should be one that the decoder has already indicated that it supports.</span></span> <span data-ttu-id="c87b9-136">Tenere presente che la rotazione deve sempre essere eseguita dopo il ridimensionamento e il ritaglio.</span><span class="sxs-lookup"><span data-stu-id="c87b9-136">Remember that rotation should always be performed after scaling and clipping.</span></span>

### <a name="getclosestsize"></a><span data-ttu-id="c87b9-137">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="c87b9-137">GetClosestSize</span></span>

<span data-ttu-id="c87b9-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) accetta due parametri in/out.</span><span class="sxs-lookup"><span data-stu-id="c87b9-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) takes two in/out parameters.</span></span> <span data-ttu-id="c87b9-139">Il chiamante utilizza i parametri *puiWidth* e *puiHeight* per specificare le dimensioni in base alle quali il chiamante preferisce l'immagine da decodificare.</span><span class="sxs-lookup"><span data-stu-id="c87b9-139">The caller uses the *puiWidth* and *puiHeight* parameters to specify the size at which that the caller prefers the image to be decoded.</span></span> <span data-ttu-id="c87b9-140">Tuttavia, un decodificatore può decodificare un'immagine solo in una dimensione che è un multiplo delle dimensioni DCT e formati di immagine diversi possono avere dimensioni DCT diverse.</span><span class="sxs-lookup"><span data-stu-id="c87b9-140">However, a decoder can decode an image only to a size that’s a multiple of its DCT size, and different image formats can have different DCT sizes.</span></span> <span data-ttu-id="c87b9-141">Il decodificatore deve determinare, in base alle proprie dimensioni DCT, il più vicino possibile alla dimensione richiesta e impostare *puiWidth* e *puiHeight* su tali dimensioni alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="c87b9-141">The decoder should determine, based on its own DCT size, the closest it can come to the requested size, and set the *puiWidth* and *puiHeight* to those dimensions on return.</span></span> <span data-ttu-id="c87b9-142">Se è richiesta una dimensione maggiore, ma il codec non supporta il ridimensionamento, verrà restituito il valore originale.</span><span class="sxs-lookup"><span data-stu-id="c87b9-142">If a larger size is requested, but the codec doesn’t support upscaling, the original should be returned.</span></span>

### <a name="getclosestpixelformat"></a><span data-ttu-id="c87b9-143">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="c87b9-143">GetClosestPixelFormat</span></span>

<span data-ttu-id="c87b9-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) viene usato per determinare il formato pixel più vicino al formato pixel richiesto che può essere fornito dal decodificatore senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="c87b9-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) is used to determine the closest pixel format to the requested pixel format that the decoder can provide without loss of data.</span></span> <span data-ttu-id="c87b9-145">È sempre preferibile eseguire la conversione in un formato pixel più ampio rispetto a uno più piccolo, anche se aumenterà le dimensioni dell'immagine, perché può sempre essere riconvertito in un formato più restrittivo, se necessario.</span><span class="sxs-lookup"><span data-stu-id="c87b9-145">It’s always preferable to convert to a wider pixel format than a narrower one, even though it will increase the size of the image, because it can always be reconverted to a more restrictive format if necessary.</span></span> <span data-ttu-id="c87b9-146">Tuttavia, una volta persi, i dati non possono essere recuperati.</span><span class="sxs-lookup"><span data-stu-id="c87b9-146">However, after the data is lost, it can’t be recovered.</span></span>

## <a name="continued-reading"></a><span data-ttu-id="c87b9-147">Continua lettura</span><span class="sxs-lookup"><span data-stu-id="c87b9-147">Continued Reading</span></span>

<span data-ttu-id="c87b9-148">Per ulteriori informazioni su come creare un codec abilitato per WIC, vedere [implementazione di IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span><span class="sxs-lookup"><span data-stu-id="c87b9-148">To learn more about how to create a WIC-enabled codec, see [Implementing IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c87b9-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c87b9-149">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c87b9-150">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c87b9-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c87b9-151">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="c87b9-151">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[<span data-ttu-id="c87b9-152">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="c87b9-152">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="c87b9-153">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c87b9-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c87b9-154">Implementazione di IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="c87b9-154">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="c87b9-155">Implementazione di IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="c87b9-155">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="c87b9-156">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c87b9-156">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c87b9-157">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="c87b9-157">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
