---
title: Effetto con trasformazione affine 2D
description: L'effetto di trasformazione affine 2D applica una trasformazione spaziale a un'immagine basata su una matrice 3X2 usando la trasformazione della matrice Direct2D e una delle sei modalità di interpolazione.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Effetto con trasformazione affine 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121694"
---
# <a name="2d-affine-transform-effect"></a><span data-ttu-id="4bf72-104">Effetto con trasformazione affine 2D</span><span class="sxs-lookup"><span data-stu-id="4bf72-104">2D affine transform effect</span></span>

<span data-ttu-id="4bf72-105">L'effetto di trasformazione affine 2D applica una trasformazione spaziale a un'immagine basata su una matrice 3X2 usando la [trasformazione](direct2d-transforms-overview.md) della matrice Direct2D e una delle sei modalità di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="4bf72-105">The 2D affine transform effect applies a spatial transform to a image based on a 3X2 matrix using the Direct2D matrix [transform](direct2d-transforms-overview.md) and any of six interpolation modes.</span></span> <span data-ttu-id="4bf72-106">È possibile utilizzare questo effetto per ruotare, ridimensionare, inclinare o tradurre un'immagine.</span><span class="sxs-lookup"><span data-stu-id="4bf72-106">You can use this effect to rotate, scale, skew, or translate an image.</span></span> <span data-ttu-id="4bf72-107">In alternativa, è possibile combinare queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="4bf72-107">Or, you can combine these operations.</span></span> <span data-ttu-id="4bf72-108">I trasferimenti affini conservano linee parallele e il rapporto tra tre punti di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="4bf72-108">Affine transfers preserve parallel lines and the ratio of distances between any three points in an image.</span></span>

<span data-ttu-id="4bf72-109">Il CLSID per questo effetto è CLSID \_ D2D12DAffineTransform.</span><span class="sxs-lookup"><span data-stu-id="4bf72-109">The CLSID for this effect is CLSID\_D2D12DAffineTransform.</span></span>

-   [<span data-ttu-id="4bf72-110">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="4bf72-110">Example image</span></span>](#example-image)
-   [<span data-ttu-id="4bf72-111">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="4bf72-111">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="4bf72-112">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="4bf72-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="4bf72-113">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="4bf72-113">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="4bf72-114">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="4bf72-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="4bf72-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bf72-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4bf72-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4bf72-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="4bf72-117">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="4bf72-117">Example image</span></span>



| <span data-ttu-id="4bf72-118">Prima</span><span class="sxs-lookup"><span data-stu-id="4bf72-118">Before</span></span>                                                             |
|--------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)         |
| <span data-ttu-id="4bf72-120">After</span><span class="sxs-lookup"><span data-stu-id="4bf72-120">After</span></span>                                                              |
| ![immagine dopo la trasformazione.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="4bf72-122">Questo effetto esegue questa operazione della matrice:</span><span class="sxs-lookup"><span data-stu-id="4bf72-122">This effect performs this matrix operation:</span></span>

![operazione di matrice affine](images/affine-matrix-calculation.png)

<span data-ttu-id="4bf72-124">Sebbene la matrice di input sia definita come matrice 3x2, l'ultima colonna viene riempita con 0, 0 e 1 per produrre una matrice quadrata.</span><span class="sxs-lookup"><span data-stu-id="4bf72-124">Although the input matrix is defined as a 3x2 matrix, the last column is padded with 0, 0 and 1 to produce a square matrix.</span></span> <span data-ttu-id="4bf72-125">Questo consente la moltiplicazione di matrici, in modo che le trasformazioni possano essere concatenate in una singola matrice.</span><span class="sxs-lookup"><span data-stu-id="4bf72-125">This allows for matrix multiplication, so that transforms can be concatenated into a single matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="4bf72-126">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="4bf72-126">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bf72-127">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="4bf72-127">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="4bf72-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bf72-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bf72-129">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="4bf72-129">InterpolationMode</span></span><br/> <span data-ttu-id="4bf72-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="4bf72-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="4bf72-131">Modalità di interpolazione utilizzata per ridimensionare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="4bf72-131">The interpolation mode used to scale the image.</span></span> <span data-ttu-id="4bf72-132">Sono disponibili 6 modalità di ridimensionamento che variano in qualità e velocità.</span><span class="sxs-lookup"><span data-stu-id="4bf72-132">There are 6 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="4bf72-133">Il tipo è D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="4bf72-133">Type is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="4bf72-134">Il valore predefinito è D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="4bf72-134">Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bf72-135">BorderMode</span><span class="sxs-lookup"><span data-stu-id="4bf72-135">BorderMode</span></span><br/> <span data-ttu-id="4bf72-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="4bf72-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="4bf72-137">Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard.</span><span class="sxs-lookup"><span data-stu-id="4bf72-137">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="4bf72-138">Per altre informazioni, vedere <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> .</span><span class="sxs-lookup"><span data-stu-id="4bf72-138">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="4bf72-139">Il tipo è D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="4bf72-139">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="4bf72-140">Il valore predefinito è D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="4bf72-140">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bf72-141">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="4bf72-141">TransformMatrix</span></span><br/> <span data-ttu-id="4bf72-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="4bf72-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="4bf72-143">Matrice 3x2 per trasformare l'immagine utilizzando la <a href="direct2d-transforms-overview.md">trasformazione</a>della matrice Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4bf72-143">The 3x2 matrix to transform the image using the Direct2D matrix <a href="direct2d-transforms-overview.md">transform</a>.</span></span> <br/> <span data-ttu-id="4bf72-144">Il tipo è D2D1_MATRIX_3X2_F.</span><span class="sxs-lookup"><span data-stu-id="4bf72-144">Type is D2D1_MATRIX_3X2_F.</span></span><br/> <span data-ttu-id="4bf72-145">Il valore predefinito è Matrix3x2F:: Identity ().</span><span class="sxs-lookup"><span data-stu-id="4bf72-145">Default value is Matrix3x2F::Identity().</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bf72-146">Nitidezza</span><span class="sxs-lookup"><span data-stu-id="4bf72-146">Sharpness</span></span><br/> <span data-ttu-id="4bf72-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="4bf72-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="4bf72-148">Nella modalità di interpolazione cubica di alta qualità, il livello di nitidezza del filtro di ridimensionamento come float compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="4bf72-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="4bf72-149">I valori sono di unità.</span><span class="sxs-lookup"><span data-stu-id="4bf72-149">The values are unitless.</span></span> <span data-ttu-id="4bf72-150">È possibile usare la nitidezza per regolare la qualità di un'immagine quando si ridimensiona l'immagine.</span><span class="sxs-lookup"><span data-stu-id="4bf72-150">You can use sharpness to adjust the quality of an image when you scale the image.</span></span><br/> <span data-ttu-id="4bf72-151">Il fattore di nitidezza influiscono sulla forma del kernel.</span><span class="sxs-lookup"><span data-stu-id="4bf72-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="4bf72-152">Maggiore è il fattore di nitidezza, minore è il kernel.</span><span class="sxs-lookup"><span data-stu-id="4bf72-152">The higher the sharpness factor, the smaller the kernel.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4bf72-153">Questa proprietà ha effetto solo sulla modalità di interpolazione cubica di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="4bf72-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="4bf72-154">Il tipo è FLOAT.</span><span class="sxs-lookup"><span data-stu-id="4bf72-154">Type is FLOAT.</span></span><br/> <span data-ttu-id="4bf72-155">Il valore predefinito è 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="4bf72-155">Default value is 1.0f.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a><span data-ttu-id="4bf72-156">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="4bf72-156">Border modes</span></span>



| <span data-ttu-id="4bf72-157">Nome</span><span class="sxs-lookup"><span data-stu-id="4bf72-157">Name</span></span>                     | <span data-ttu-id="4bf72-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bf72-158">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf72-159">\_Modalità bordo \_ d2d1 \_ Soft</span><span class="sxs-lookup"><span data-stu-id="4bf72-159">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="4bf72-160">L'effetto riempie l'immagine con i pixel neri trasparenti durante l'interpolazione, ottenendo un bordo flessibile.</span><span class="sxs-lookup"><span data-stu-id="4bf72-160">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="4bf72-161">\_Modalità bordo \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="4bf72-161">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="4bf72-162">L'effetto fissa l'output alla dimensione dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="4bf72-162">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="4bf72-163">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="4bf72-163">Interpolation modes</span></span>



| <span data-ttu-id="4bf72-164">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="4bf72-164">Enumeration</span></span>                                                         | <span data-ttu-id="4bf72-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bf72-165">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf72-166">D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione \_ \_ più vicina \_</span><span class="sxs-lookup"><span data-stu-id="4bf72-166">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="4bf72-167">Campiona il punto singolo più vicino e lo utilizza.</span><span class="sxs-lookup"><span data-stu-id="4bf72-167">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="4bf72-168">In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.</span><span class="sxs-lookup"><span data-stu-id="4bf72-168">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="4bf72-169">D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione \_ \_ lineare</span><span class="sxs-lookup"><span data-stu-id="4bf72-169">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="4bf72-170">Usa un esempio a quattro punti e un'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="4bf72-170">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="4bf72-171">Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="4bf72-171">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="4bf72-172">D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione \_ \_ cubica</span><span class="sxs-lookup"><span data-stu-id="4bf72-172">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="4bf72-173">Usa un kernel cubico di esempio 16 per l'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="4bf72-173">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="4bf72-174">Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="4bf72-174">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="4bf72-175">D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_</span><span class="sxs-lookup"><span data-stu-id="4bf72-175">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="4bf72-176">USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi.</span><span class="sxs-lookup"><span data-stu-id="4bf72-176">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="4bf72-177">Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.</span><span class="sxs-lookup"><span data-stu-id="4bf72-177">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="4bf72-178">D2D1 \_ 2DAFFINETRANSFORM \_ modalità di interpolazione \_ \_ anisotropico</span><span class="sxs-lookup"><span data-stu-id="4bf72-178">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="4bf72-179">Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.</span><span class="sxs-lookup"><span data-stu-id="4bf72-179">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="4bf72-180">D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione \_ \_ alta \_ qualità \_ cubica</span><span class="sxs-lookup"><span data-stu-id="4bf72-180">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="4bf72-181">Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="4bf72-181">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="4bf72-182">USA quindi la modalità di interpolazione cubica per l'output finale.</span><span class="sxs-lookup"><span data-stu-id="4bf72-182">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="4bf72-183">Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ 2DAFFINETRANSFORM \_ modalità di interpolazione \_ \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="4bf72-183">If you don't select a mode, the effect defaults to D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="4bf72-184">La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che vengono inseriti in questo effetto, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.</span><span class="sxs-lookup"><span data-stu-id="4bf72-184">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="4bf72-185">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="4bf72-185">Output bitmap</span></span>

<span data-ttu-id="4bf72-186">Le dimensioni della bitmap di output dipendono dalla matrice di trasformazione applicata all'immagine.</span><span class="sxs-lookup"><span data-stu-id="4bf72-186">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="4bf72-187">L'effetto esegue l'operazione di trasformazione e quindi applica un rettangolo di delimitazione intorno al risultato.</span><span class="sxs-lookup"><span data-stu-id="4bf72-187">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="4bf72-188">La bitmap di output corrisponde alla dimensione del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="4bf72-188">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf72-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bf72-189">Requirements</span></span>



| <span data-ttu-id="4bf72-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bf72-190">Requirement</span></span> | <span data-ttu-id="4bf72-191">Valore</span><span class="sxs-lookup"><span data-stu-id="4bf72-191">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf72-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bf72-192">Minimum supported client</span></span> | <span data-ttu-id="4bf72-193">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="4bf72-193">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4bf72-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bf72-194">Minimum supported server</span></span> | <span data-ttu-id="4bf72-195">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="4bf72-195">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4bf72-196">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4bf72-196">Header</span></span>                   | <span data-ttu-id="4bf72-197">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="4bf72-197">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="4bf72-198">Libreria</span><span class="sxs-lookup"><span data-stu-id="4bf72-198">Library</span></span>                  | <span data-ttu-id="4bf72-199">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="4bf72-199">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="4bf72-200">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4bf72-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bf72-201">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="4bf72-201">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

