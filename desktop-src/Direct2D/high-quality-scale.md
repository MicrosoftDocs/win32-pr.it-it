---
title: Effetto di scalabilità
description: Utilizzare questo effetto per ridimensionare un'immagine verso l'alto o verso il basso. L'effetto è costituito da sei modalità di ridimensionamento adiacenti, lineari, cubici, multicampionamento lineare, anisotropico e cubi di alta qualità.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- effetto scala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400542"
---
# <a name="scale-effect"></a><span data-ttu-id="865e9-105">Effetto di scalabilità</span><span class="sxs-lookup"><span data-stu-id="865e9-105">Scale effect</span></span>

<span data-ttu-id="865e9-106">Utilizzare questo effetto per ridimensionare un'immagine verso l'alto o verso il basso.</span><span class="sxs-lookup"><span data-stu-id="865e9-106">Use this effect to scale an image up or down.</span></span> <span data-ttu-id="865e9-107">L'effetto è costituito da sei modalità di ridimensionamento: adiacente più vicino, lineare, cubico, lineare a più campioni, anisotropico e cubi di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="865e9-107">The effect has six scaling modes: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

<span data-ttu-id="865e9-108">Il CLSID per questo effetto è CLSID \_ D2D1Scale.</span><span class="sxs-lookup"><span data-stu-id="865e9-108">The CLSID for this effect is CLSID\_D2D1Scale.</span></span>

-   [<span data-ttu-id="865e9-109">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="865e9-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="865e9-110">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="865e9-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="865e9-111">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="865e9-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="865e9-112">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="865e9-112">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="865e9-113">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="865e9-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="865e9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="865e9-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="865e9-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="865e9-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="865e9-116">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="865e9-116">Example image</span></span>

<span data-ttu-id="865e9-117">Questo esempio mostra lo zoom dell'effetto di scala in 2 volte l'input e il ritaglio alle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="865e9-117">This example shows the scale effect zooming in 2 times the input and cropping to the original size.</span></span>



| <span data-ttu-id="865e9-118">Prima</span><span class="sxs-lookup"><span data-stu-id="865e9-118">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| <span data-ttu-id="865e9-120">After</span><span class="sxs-lookup"><span data-stu-id="865e9-120">After</span></span>                                                      |
| ![immagine dopo la trasformazione.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="865e9-122">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="865e9-122">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="865e9-123">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="865e9-123">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="865e9-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="865e9-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="865e9-125">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="865e9-125">Scale</span></span><br/> <span data-ttu-id="865e9-126">D2D1_SCALE_PROP_SCALE</span><span class="sxs-lookup"><span data-stu-id="865e9-126">D2D1_SCALE_PROP_SCALE</span></span><br/></td>
<td><span data-ttu-id="865e9-127">Quantità di scala nella direzione X e Y come rapporto tra le dimensioni di output e le dimensioni di input.</span><span class="sxs-lookup"><span data-stu-id="865e9-127">The scale amount in the X and Y direction as a ratio of the output size to the input size.</span></span> <span data-ttu-id="865e9-128">Questa proprietà a D2D1_VECTOR_2Fdefined come: (scala X, scala Y).</span><span class="sxs-lookup"><span data-stu-id="865e9-128">This property a D2D1_VECTOR_2Fdefined as: (X scale, Y scale).</span></span> <span data-ttu-id="865e9-129">Gli importi di scala sono FLOAT, unità e devono essere positivi o 0.</span><span class="sxs-lookup"><span data-stu-id="865e9-129">The scale amounts are FLOAT, unitless, and must be positive or 0.</span></span><br/> <span data-ttu-id="865e9-130">Il tipo è D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="865e9-130">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="865e9-131">Il valore predefinito è {1.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="865e9-131">The default value is {1.0f, 1.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="865e9-132">CenterPoint</span><span class="sxs-lookup"><span data-stu-id="865e9-132">CenterPoint</span></span><br/> <span data-ttu-id="865e9-133">D2D1_SCALE_PROP_CENTER_POINT</span><span class="sxs-lookup"><span data-stu-id="865e9-133">D2D1_SCALE_PROP_CENTER_POINT</span></span><br/></td>
<td><span data-ttu-id="865e9-134">Punto centrale di ridimensionamento dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="865e9-134">The image scaling center point.</span></span> <span data-ttu-id="865e9-135">Questa proprietà è un D2D1_VECTOR_2F definito come: (punto X, punto Y).</span><span class="sxs-lookup"><span data-stu-id="865e9-135">This property is a D2D1_VECTOR_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="865e9-136">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="865e9-136">The units are in DIPs.</span></span><br/> <span data-ttu-id="865e9-137">Usare la proprietà punto centrale per ridimensionare un punto diverso dall'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="865e9-137">Use the center point property to scale around a point other than the upper-left corner.</span></span><br/> <span data-ttu-id="865e9-138">Il tipo è D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="865e9-138">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="865e9-139">Il valore predefinito è {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="865e9-139">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="865e9-140">BorderMode</span><span class="sxs-lookup"><span data-stu-id="865e9-140">BorderMode</span></span><br/> <span data-ttu-id="865e9-141">D2D1_SCALE_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="865e9-141">D2D1_SCALE_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="865e9-142">Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard.</span><span class="sxs-lookup"><span data-stu-id="865e9-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="865e9-143">Per altre informazioni, vedere <a href="#border-modes">Border modes</a> .</span><span class="sxs-lookup"><span data-stu-id="865e9-143">See <a href="#border-modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="865e9-144">Il tipo è D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="865e9-144">The type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="865e9-145">Il valore predefinito è D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="865e9-145">The default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="865e9-146">Nitidezza</span><span class="sxs-lookup"><span data-stu-id="865e9-146">Sharpness</span></span><br/> <span data-ttu-id="865e9-147">D2D1_SCALE_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="865e9-147">D2D1_SCALE_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="865e9-148">Nella modalità di interpolazione cubica di alta qualità, il livello di nitidezza del filtro di ridimensionamento come float compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="865e9-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="865e9-149">I valori sono di unità.</span><span class="sxs-lookup"><span data-stu-id="865e9-149">The values are unitless.</span></span> <span data-ttu-id="865e9-150">È possibile usare la nitidezza per regolare la qualità di un'immagine quando si ridimensiona l'immagine verso il basso.</span><span class="sxs-lookup"><span data-stu-id="865e9-150">You can use sharpness to adjust the quality of an image when you scale the image down.</span></span><br/> <span data-ttu-id="865e9-151">Il fattore di nitidezza influiscono sulla forma del kernel.</span><span class="sxs-lookup"><span data-stu-id="865e9-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="865e9-152">Maggiore è il fattore di nitidezza, minore è il kernel.</span><span class="sxs-lookup"><span data-stu-id="865e9-152">The higher the sharpness factor, the smaller the kernel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="865e9-153">Questa proprietà ha effetto solo sulla modalità di interpolazione cubica di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="865e9-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="865e9-154">Il tipo è FLOAT.</span><span class="sxs-lookup"><span data-stu-id="865e9-154">The type is FLOAT.</span></span><br/> <span data-ttu-id="865e9-155">Il valore predefinito è 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="865e9-155">The default value is 0.0f.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="865e9-156">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="865e9-156">InterpolationMode</span></span><br/> <span data-ttu-id="865e9-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="865e9-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="865e9-158">Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="865e9-158">The interpolation mode the effect uses to scale the image.</span></span> <span data-ttu-id="865e9-159">Sono disponibili 6 modalità di ridimensionamento che variano in qualità e velocità.</span><span class="sxs-lookup"><span data-stu-id="865e9-159">There are 6 scale modes that range in quality and speed.</span></span> <span data-ttu-id="865e9-160">Per altre informazioni, vedere <a href="#interpolation-modes">modalità di interpolazione</a> .</span><span class="sxs-lookup"><span data-stu-id="865e9-160">See <a href="#interpolation-modes">Interpolation modes</a> for more info.</span></span> <br/> <span data-ttu-id="865e9-161">Il tipo è D2D1_SCALE_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="865e9-161">The type is D2D1_SCALE_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="865e9-162">Il valore predefinito è D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="865e9-162">The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a><span data-ttu-id="865e9-163">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="865e9-163">Border modes</span></span>



| <span data-ttu-id="865e9-164">Nome</span><span class="sxs-lookup"><span data-stu-id="865e9-164">Name</span></span>                     | <span data-ttu-id="865e9-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="865e9-165">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="865e9-166">\_Modalità bordo \_ d2d1 \_ Soft</span><span class="sxs-lookup"><span data-stu-id="865e9-166">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="865e9-167">L'effetto riempie l'immagine di input con i pixel neri trasparenti per i campioni all'esterno dei limiti di input quando applica il kernel di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="865e9-167">The effect pads the input image with transparent black pixels for samples outside of the input bounds when it applies the convolution kernel.</span></span> <span data-ttu-id="865e9-168">Viene creato un bordo flessibile per l'immagine e il processo espande la bitmap di output in base alla dimensione del kernel.</span><span class="sxs-lookup"><span data-stu-id="865e9-168">This creates a soft edge for the image, and in the process expands the output bitmap by the size of the kernel.</span></span><br/> |
| <span data-ttu-id="865e9-169">\_Modalità bordo \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="865e9-169">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="865e9-170">L'effetto estende l'immagine di input con una trasformazione del bordo di tipo mirror per i campioni all'esterno dei limiti di input.</span><span class="sxs-lookup"><span data-stu-id="865e9-170">The effect extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span> <span data-ttu-id="865e9-171">La dimensione della bitmap di output è uguale alla dimensione della bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="865e9-171">The size of the output bitmap is equal to the size of the input bitmap.</span></span><br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a><span data-ttu-id="865e9-172">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="865e9-172">Interpolation modes</span></span>



| <span data-ttu-id="865e9-173">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="865e9-173">Enumeration</span></span>                                             | <span data-ttu-id="865e9-174">Descrizione</span><span class="sxs-lookup"><span data-stu-id="865e9-174">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="865e9-175">\_Modalità di \_ interpolazione scala d2d1 \_ \_ più \_ vicina</span><span class="sxs-lookup"><span data-stu-id="865e9-175">D2D1\_SCALE\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="865e9-176">Campiona il punto singolo più vicino e lo utilizza.</span><span class="sxs-lookup"><span data-stu-id="865e9-176">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="865e9-177">In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.</span><span class="sxs-lookup"><span data-stu-id="865e9-177">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="865e9-178">\_Modalità di \_ interpolazione scala d2d1 \_ \_ lineare</span><span class="sxs-lookup"><span data-stu-id="865e9-178">D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="865e9-179">Usa un esempio a quattro punti e un'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="865e9-179">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="865e9-180">Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="865e9-180">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="865e9-181">\_Modalità di \_ interpolazione scala d2d1 \_ \_ cubica</span><span class="sxs-lookup"><span data-stu-id="865e9-181">D2D1\_SCALE\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="865e9-182">Usa un kernel cubico di esempio 16 per l'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="865e9-182">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="865e9-183">Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="865e9-183">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="865e9-184">\_Modalità di \_ interpolazione con SCALAbilità d2d1 \_ \_ \_ multicampione \_ lineare</span><span class="sxs-lookup"><span data-stu-id="865e9-184">D2D1\_SCALE\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="865e9-185">USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi.</span><span class="sxs-lookup"><span data-stu-id="865e9-185">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="865e9-186">Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.</span><span class="sxs-lookup"><span data-stu-id="865e9-186">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="865e9-187">\_Modalità di \_ interpolazione con SCALAbilità d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="865e9-187">D2D1\_SCALE\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="865e9-188">Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.</span><span class="sxs-lookup"><span data-stu-id="865e9-188">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="865e9-189">D2D1 \_ di \_ \_ \_ alta \_ qualità in modalità interpolazione \_</span><span class="sxs-lookup"><span data-stu-id="865e9-189">D2D1\_SCALE\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="865e9-190">Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="865e9-190">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="865e9-191">USA quindi la modalità di interpolazione cubica per l'output finale.</span><span class="sxs-lookup"><span data-stu-id="865e9-191">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="865e9-192">Se non si seleziona una modalità, l'effetto viene impostato sul valore predefinito D2D1 \_ \_ modalità di interpolazione \_ \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="865e9-192">If you don't select a mode, the effect defaults to D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="865e9-193">La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che vengono inseriti in questo effetto, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.</span><span class="sxs-lookup"><span data-stu-id="865e9-193">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="865e9-194">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="865e9-194">Output bitmap</span></span>

<span data-ttu-id="865e9-195">La posizione e le dimensioni della bitmap di output dipendono dal fattore di scala e dal punto centrale specificati.</span><span class="sxs-lookup"><span data-stu-id="865e9-195">The location and size of the output bitmap depends on the specified scale factor and the center point.</span></span>

<span data-ttu-id="865e9-196">È possibile calcolare le dimensioni della bitmap di output usando questa equazione:</span><span class="sxs-lookup"><span data-stu-id="865e9-196">You can calculate the size of the output bitmap using this equation:</span></span><dl> <span data-ttu-id="865e9-197">BitmapSize? (Pixel) = scala? \* Dimensioni originali della bitmap?</span><span class="sxs-lookup"><span data-stu-id="865e9-197">BitmapSize?(Pixels)=Scale?\*Original Bitmap Size?</span></span> <span data-ttu-id="865e9-198">(DIP) \* (UserDPI/96)</span><span class="sxs-lookup"><span data-stu-id="865e9-198">(DIPs)\*(UserDPI/96)</span></span>  
<span data-ttu-id="865e9-199">BitmapSize<sub>y</sub>(pixel) = scala<sub>y</sub> \* dimensioni bitmap originali<sub>y</sub> (DIP) \* (UserDPI/96)</span><span class="sxs-lookup"><span data-stu-id="865e9-199">BitmapSize<sub>y</sub>(Pixels)=Scale<sub>y</sub>\*Original Bitmap Size<sub>y</sub> (DIPs)\*(UserDPI/96)</span></span>  
</dl>

<span data-ttu-id="865e9-200">L'effetto Arrotonda le frazioni di pixel fino al pixel intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="865e9-200">The effect rounds fractions of pixels up to the nearest whole pixel.</span></span>

<span data-ttu-id="865e9-201">Il percorso della bitmap è (0, 0) o il valore della proprietà del punto centrale.</span><span class="sxs-lookup"><span data-stu-id="865e9-201">The location of the bitmap is (0, 0) or the value of the center point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="865e9-202">Requisiti</span><span class="sxs-lookup"><span data-stu-id="865e9-202">Requirements</span></span>



| <span data-ttu-id="865e9-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="865e9-203">Requirement</span></span> | <span data-ttu-id="865e9-204">Valore</span><span class="sxs-lookup"><span data-stu-id="865e9-204">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="865e9-205">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="865e9-205">Minimum supported client</span></span> | <span data-ttu-id="865e9-206">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="865e9-206">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="865e9-207">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="865e9-207">Minimum supported server</span></span> | <span data-ttu-id="865e9-208">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="865e9-208">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="865e9-209">Intestazione</span><span class="sxs-lookup"><span data-stu-id="865e9-209">Header</span></span>                   | <span data-ttu-id="865e9-210">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="865e9-210">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="865e9-211">Libreria</span><span class="sxs-lookup"><span data-stu-id="865e9-211">Library</span></span>                  | <span data-ttu-id="865e9-212">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="865e9-212">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="865e9-213">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="865e9-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="865e9-214">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="865e9-214">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

