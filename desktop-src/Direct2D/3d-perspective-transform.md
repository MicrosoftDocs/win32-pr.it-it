---
title: Effetto con trasformazione prospettica 3D
description: Usare l'effetto di trasformazione prospettiva 3D per ruotare l'immagine in 3 dimensioni come se fosse visualizzata da una distanza.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- effetto trasformazione prospettiva 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874654"
---
# <a name="3d-perspective-transform-effect"></a><span data-ttu-id="a32b0-104">Effetto con trasformazione prospettica 3D</span><span class="sxs-lookup"><span data-stu-id="a32b0-104">3D perspective transform effect</span></span>

<span data-ttu-id="a32b0-105">Usare l'effetto di trasformazione prospettiva 3D per ruotare l'immagine in 3 dimensioni come se fosse visualizzata da una distanza.</span><span class="sxs-lookup"><span data-stu-id="a32b0-105">Use the 3D perspective transform effect to rotate the image in 3 dimensions as if viewed from a distance.</span></span>

<span data-ttu-id="a32b0-106">La trasformazione prospettiva 3D è più comoda rispetto all'effetto trasformazione 3D, ma espone solo un subset della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a32b0-106">The 3D perspective transform is more convenient than the 3D transform effect, but only exposes a subset of the functionality.</span></span> <span data-ttu-id="a32b0-107">È possibile calcolare una matrice di trasformazione 3D completa e applicare una matrice di trasformazione più arbitraria a un'immagine usando l'effetto di [trasformazione 3D](3d-transform.md) .</span><span class="sxs-lookup"><span data-stu-id="a32b0-107">You can compute a full 3D transformation matrix and apply a more arbitrary transform matrix to an image using the [3D transform](3d-transform.md) effect.</span></span>

<span data-ttu-id="a32b0-108">Il CLSID per questo effetto è CLSID \_ D2D13DPerspectiveTransform.</span><span class="sxs-lookup"><span data-stu-id="a32b0-108">The CLSID for this effect is CLSID\_D2D13DPerspectiveTransform.</span></span>

-   [<span data-ttu-id="a32b0-109">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="a32b0-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="a32b0-110">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="a32b0-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="a32b0-111">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="a32b0-111">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="a32b0-112">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="a32b0-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="a32b0-113">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="a32b0-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="a32b0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a32b0-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a32b0-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a32b0-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="a32b0-116">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="a32b0-116">Example image</span></span>



| <span data-ttu-id="a32b0-117">Prima</span><span class="sxs-lookup"><span data-stu-id="a32b0-117">Before</span></span>                                                               |
|----------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)           |
| <span data-ttu-id="a32b0-119">After</span><span class="sxs-lookup"><span data-stu-id="a32b0-119">After</span></span>                                                                |
| ![immagine dopo l'effetto.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="a32b0-121">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="a32b0-121">Effect properties</span></span>



| <span data-ttu-id="a32b0-122">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="a32b0-122">Display name and index enumeration</span></span>                                                              | <span data-ttu-id="a32b0-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a32b0-123">Description</span></span>                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a32b0-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="a32b0-124">InterpolationMode</span></span><br/> <span data-ttu-id="a32b0-125">\_Modalità di \_ \_ interpolazione della prop 3DPERSPECTIVETRANSFORM d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="a32b0-125">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="a32b0-126">Modalità di interpolazione utilizzata dall'effetto sull'immagine.</span><span class="sxs-lookup"><span data-stu-id="a32b0-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="a32b0-127">Sono disponibili 5 modalità di ridimensionamento che variano in qualità e velocità.</span><span class="sxs-lookup"><span data-stu-id="a32b0-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="a32b0-128">Il tipo è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ Interpolation \_ mode.</span><span class="sxs-lookup"><span data-stu-id="a32b0-128">Type is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="a32b0-129">Il valore predefinito è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modalità di interpolazione \_ \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="a32b0-129">Default value is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span><br/>              |
| <span data-ttu-id="a32b0-130">BorderMode</span><span class="sxs-lookup"><span data-stu-id="a32b0-130">BorderMode</span></span><br/> <span data-ttu-id="a32b0-131">\_ \_ \_ Modalità bordo prop 3DPERSPECTIVETRANSFORM \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="a32b0-131">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="a32b0-132">Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard.</span><span class="sxs-lookup"><span data-stu-id="a32b0-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="a32b0-133">Per altre informazioni, vedere [Border modes](https://www.bing.com/search?q=Border+modes) .</span><span class="sxs-lookup"><span data-stu-id="a32b0-133">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span><br/> <span data-ttu-id="a32b0-134">Il tipo è D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="a32b0-134">Type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="a32b0-135">Il valore predefinito è D2D1 \_ Border \_ mode \_ .</span><span class="sxs-lookup"><span data-stu-id="a32b0-135">Default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                              |
| <span data-ttu-id="a32b0-136">Profondità</span><span class="sxs-lookup"><span data-stu-id="a32b0-136">Depth</span></span><br/> <span data-ttu-id="a32b0-137">\_Profondità della \_ prop \_ 3DPERSPECTIVETRANSFORM d2d1</span><span class="sxs-lookup"><span data-stu-id="a32b0-137">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_DEPTH</span></span><br/>                           | <span data-ttu-id="a32b0-138">Distanza tra il *PerspectiveOrigin* e il piano di proiezione.</span><span class="sxs-lookup"><span data-stu-id="a32b0-138">The distance from the *PerspectiveOrigin* to the projection plane.</span></span> <span data-ttu-id="a32b0-139">Il valore specificato in DIP e deve essere maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="a32b0-139">The value specified in DIPs and must be greater than 0.</span></span><br/> <span data-ttu-id="a32b0-140">Il tipo è FLOAT.</span><span class="sxs-lookup"><span data-stu-id="a32b0-140">Type is FLOAT.</span></span><br/> <span data-ttu-id="a32b0-141">Il valore predefinito è 1000.0 f.</span><span class="sxs-lookup"><span data-stu-id="a32b0-141">Default value is 1000.0f.</span></span><br/>                                                                                               |
| <span data-ttu-id="a32b0-142">PerspectiveOrigin</span><span class="sxs-lookup"><span data-stu-id="a32b0-142">PerspectiveOrigin</span></span><br/> <span data-ttu-id="a32b0-143">\_ \_ \_ Origine prospettiva d2d1 3DPERSPECTIVETRANSFORM \_ prop</span><span class="sxs-lookup"><span data-stu-id="a32b0-143">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_PERSPECTIVE\_ORIGIN</span></span><br/> | <span data-ttu-id="a32b0-144">Posizione X e Y del visualizzatore nella scena 3D.</span><span class="sxs-lookup"><span data-stu-id="a32b0-144">The X and Y location of the viewer in the 3D scene.</span></span> <span data-ttu-id="a32b0-145">Questa proprietà è un D2D1 \_ vector \_ 2F definito come: (punto X, punto Y).</span><span class="sxs-lookup"><span data-stu-id="a32b0-145">This property is a D2D1\_VECTOR\_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="a32b0-146">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="a32b0-146">The units are in DIPs.</span></span><br/> <span data-ttu-id="a32b0-147">Il valore Z viene impostato con la proprietà *Depth* .</span><span class="sxs-lookup"><span data-stu-id="a32b0-147">You set the Z value with the *Depth* property.</span></span><br/> <span data-ttu-id="a32b0-148">Il tipo è D2D1 \_ vector \_ 2F.</span><span class="sxs-lookup"><span data-stu-id="a32b0-148">Type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="a32b0-149">Il valore predefinito è {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="a32b0-149">Default value is {0.0f, 0.0f}.</span></span><br/> |
| <span data-ttu-id="a32b0-150">LocalOffset</span><span class="sxs-lookup"><span data-stu-id="a32b0-150">LocalOffset</span></span><br/> <span data-ttu-id="a32b0-151">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ Local \_ offset</span><span class="sxs-lookup"><span data-stu-id="a32b0-151">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_LOCAL\_OFFSET</span></span><br/>             | <span data-ttu-id="a32b0-152">Una traduzione che l'effetto esegue prima di ruotare il piano di proiezione.</span><span class="sxs-lookup"><span data-stu-id="a32b0-152">A translation the effect performs before it rotates the projection plane.</span></span> <span data-ttu-id="a32b0-153">Questa proprietà è un \_ vettore d2d1 \_ 3F definito come: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="a32b0-153">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="a32b0-154">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="a32b0-154">The units are in DIPs.</span></span><br/> <span data-ttu-id="a32b0-155">Il tipo è D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="a32b0-155">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="a32b0-156">Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="a32b0-156">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                        |
| <span data-ttu-id="a32b0-157">GlobalOffset</span><span class="sxs-lookup"><span data-stu-id="a32b0-157">GlobalOffset</span></span><br/> <span data-ttu-id="a32b0-158">\_ \_ \_ Offset globale d2d1 3DPERSPECTIVETRANSFORM \_ prop</span><span class="sxs-lookup"><span data-stu-id="a32b0-158">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_GLOBAL\_OFFSET</span></span><br/>           | <span data-ttu-id="a32b0-159">Una traduzione che l'effetto esegue dopo la rotazione del piano di proiezione.</span><span class="sxs-lookup"><span data-stu-id="a32b0-159">A translation the effect performs after it rotates the projection plane.</span></span> <span data-ttu-id="a32b0-160">Questa proprietà è un \_ vettore d2d1 \_ 3F definito come: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="a32b0-160">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="a32b0-161">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="a32b0-161">The units are in DIPs.</span></span><br/> <span data-ttu-id="a32b0-162">Il tipo è D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="a32b0-162">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="a32b0-163">Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="a32b0-163">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                         |
| <span data-ttu-id="a32b0-164">RotationOrigin</span><span class="sxs-lookup"><span data-stu-id="a32b0-164">RotationOrigin</span></span><br/> <span data-ttu-id="a32b0-165">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ Rotation \_ Origin</span><span class="sxs-lookup"><span data-stu-id="a32b0-165">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION\_ORIGIN</span></span><br/>       | <span data-ttu-id="a32b0-166">Punto centrale della rotazione eseguita dall'effetto.</span><span class="sxs-lookup"><span data-stu-id="a32b0-166">The center point of the rotation the effect performs.</span></span> <span data-ttu-id="a32b0-167">Questa proprietà è un \_ vettore d2d1 \_ 3F definito come: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="a32b0-167">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="a32b0-168">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="a32b0-168">The units are in DIPs.</span></span><br/> <span data-ttu-id="a32b0-169">Il tipo è D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="a32b0-169">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="a32b0-170">Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="a32b0-170">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                            |
| <span data-ttu-id="a32b0-171">Rotazione</span><span class="sxs-lookup"><span data-stu-id="a32b0-171">Rotation</span></span><br/> <span data-ttu-id="a32b0-172">\_Rotazione della \_ prop \_ 3DPERSPECTIVETRANSFORM d2d1</span><span class="sxs-lookup"><span data-stu-id="a32b0-172">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION</span></span><br/>                     | <span data-ttu-id="a32b0-173">Angoli di rotazione per ogni asse.</span><span class="sxs-lookup"><span data-stu-id="a32b0-173">The angles of rotation for each axis.</span></span> <span data-ttu-id="a32b0-174">Questa proprietà è un \_ vettore d2d1 \_ 3F definito come: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="a32b0-174">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="a32b0-175">Le unità sono in gradi.</span><span class="sxs-lookup"><span data-stu-id="a32b0-175">The units are in degrees.</span></span><br/> <span data-ttu-id="a32b0-176">Il tipo è D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="a32b0-176">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="a32b0-177">Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="a32b0-177">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="a32b0-178">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="a32b0-178">Interpolation modes</span></span>



| <span data-ttu-id="a32b0-179">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="a32b0-179">Enumeration</span></span>                                                              | <span data-ttu-id="a32b0-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a32b0-180">Description</span></span>                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a32b0-181">D2D1 \_ 3DPERSPECTIVETRANSFORM- \_ modalità di interpolazione \_ \_ più vicina \_</span><span class="sxs-lookup"><span data-stu-id="a32b0-181">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="a32b0-182">Campiona il punto singolo più vicino e lo utilizza.</span><span class="sxs-lookup"><span data-stu-id="a32b0-182">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="a32b0-183">In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.</span><span class="sxs-lookup"><span data-stu-id="a32b0-183">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="a32b0-184">D2D1 \_ 3DPERSPECTIVETRANSFORM- \_ modalità di interpolazione \_ \_ lineare</span><span class="sxs-lookup"><span data-stu-id="a32b0-184">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="a32b0-185">Usa un esempio a quattro punti e un'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="a32b0-185">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="a32b0-186">Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="a32b0-186">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="a32b0-187">D2D1 \_ 3DPERSPECTIVETRANSFORM- \_ modalità di interpolazione \_ \_ cubica</span><span class="sxs-lookup"><span data-stu-id="a32b0-187">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="a32b0-188">Usa un kernel cubico di esempio 16 per l'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="a32b0-188">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="a32b0-189">Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="a32b0-189">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="a32b0-190">D2D1 \_ 3DPERSPECTIVETRANSFORM- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_</span><span class="sxs-lookup"><span data-stu-id="a32b0-190">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="a32b0-191">USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi.</span><span class="sxs-lookup"><span data-stu-id="a32b0-191">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="a32b0-192">Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.</span><span class="sxs-lookup"><span data-stu-id="a32b0-192">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="a32b0-193">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modalità di interpolazione \_ \_ anisotropico</span><span class="sxs-lookup"><span data-stu-id="a32b0-193">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="a32b0-194">Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.</span><span class="sxs-lookup"><span data-stu-id="a32b0-194">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="a32b0-195">Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modalità di interpolazione \_ \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="a32b0-195">If you don't select a mode, the effect defaults to D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="a32b0-196">La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che vengono inseriti in questo effetto, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.</span><span class="sxs-lookup"><span data-stu-id="a32b0-196">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="a32b0-197">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="a32b0-197">Border modes</span></span>



| <span data-ttu-id="a32b0-198">Nome</span><span class="sxs-lookup"><span data-stu-id="a32b0-198">Name</span></span>                     | <span data-ttu-id="a32b0-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a32b0-199">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a32b0-200">\_Modalità bordo \_ d2d1 \_ Soft</span><span class="sxs-lookup"><span data-stu-id="a32b0-200">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="a32b0-201">L'effetto riempie l'immagine con i pixel neri trasparenti durante l'interpolazione, ottenendo un bordo flessibile.</span><span class="sxs-lookup"><span data-stu-id="a32b0-201">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="a32b0-202">\_Modalità bordo \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="a32b0-202">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="a32b0-203">L'effetto fissa l'output alla dimensione dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="a32b0-203">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="output-bitmap"></a><span data-ttu-id="a32b0-204">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="a32b0-204">Output bitmap</span></span>

<span data-ttu-id="a32b0-205">Le dimensioni della bitmap di output dipendono dalla matrice di trasformazione applicata all'immagine.</span><span class="sxs-lookup"><span data-stu-id="a32b0-205">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="a32b0-206">L'effetto esegue l'operazione di trasformazione e quindi applica un rettangolo di delimitazione intorno al risultato.</span><span class="sxs-lookup"><span data-stu-id="a32b0-206">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="a32b0-207">La bitmap di output corrisponde alla dimensione del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="a32b0-207">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32b0-208">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a32b0-208">Requirements</span></span>



| <span data-ttu-id="a32b0-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="a32b0-209">Requirement</span></span> | <span data-ttu-id="a32b0-210">Valore</span><span class="sxs-lookup"><span data-stu-id="a32b0-210">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a32b0-211">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a32b0-211">Minimum supported client</span></span> | <span data-ttu-id="a32b0-212">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="a32b0-212">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a32b0-213">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a32b0-213">Minimum supported server</span></span> | <span data-ttu-id="a32b0-214">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="a32b0-214">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a32b0-215">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a32b0-215">Header</span></span>                   | <span data-ttu-id="a32b0-216">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="a32b0-216">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="a32b0-217">Libreria</span><span class="sxs-lookup"><span data-stu-id="a32b0-217">Library</span></span>                  | <span data-ttu-id="a32b0-218">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="a32b0-218">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="a32b0-219">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a32b0-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a32b0-220">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="a32b0-220">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

