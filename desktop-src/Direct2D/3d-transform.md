---
title: Effetto con trasformazione 3D
description: Usare l'effetto di trasformazione 3D per applicare una matrice di trasformazione 4x4 arbitraria a un'immagine.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- effetto trasformazione 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570074"
---
# <a name="3d-transform-effect"></a><span data-ttu-id="2f373-104">Effetto con trasformazione 3D</span><span class="sxs-lookup"><span data-stu-id="2f373-104">3D transform effect</span></span>

<span data-ttu-id="2f373-105">Usare l'effetto di trasformazione 3D per applicare una matrice di trasformazione 4x4 arbitraria a un'immagine.</span><span class="sxs-lookup"><span data-stu-id="2f373-105">Use the 3D transform effect to apply an arbitrary 4x4 transform matrix to an image.</span></span>

<span data-ttu-id="2f373-106">Questo effetto applica la matrice (M?) fornita ai vertici degli angoli dell'immagine di origine ( \[ x y z 1 \] ) utilizzando il calcolo seguente:</span><span class="sxs-lookup"><span data-stu-id="2f373-106">This effect applies the matrix (M?) you provide to the corner vertices of the source image (\[ x y z 1 \]) using this calculation:</span></span>

<span data-ttu-id="2f373-107">\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?</span><span class="sxs-lookup"><span data-stu-id="2f373-107">\[ x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \]=\[ x y z 1 \]\*M?</span></span>

<span data-ttu-id="2f373-108">Il CLSID per questo effetto è CLSID \_ D2D13DTransform.</span><span class="sxs-lookup"><span data-stu-id="2f373-108">The CLSID for this effect is CLSID\_D2D13DTransform.</span></span>

-   [<span data-ttu-id="2f373-109">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="2f373-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="2f373-110">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="2f373-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="2f373-111">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="2f373-111">Interpolation modes</span></span>](#interpolation-modes)
    -   [<span data-ttu-id="2f373-112">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="2f373-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="2f373-113">Classe della matrice di trasformazione 4x4</span><span class="sxs-lookup"><span data-stu-id="2f373-113">4x4 Transform Matrix Class</span></span>](#4x4-transform-matrix-class)
-   [<span data-ttu-id="2f373-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f373-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2f373-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f373-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="2f373-116">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="2f373-116">Example image</span></span>



| <span data-ttu-id="2f373-117">Prima</span><span class="sxs-lookup"><span data-stu-id="2f373-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![immagine prima della trasformazione.](images/default-before.jpg) |
| <span data-ttu-id="2f373-119">After</span><span class="sxs-lookup"><span data-stu-id="2f373-119">After</span></span>                                                         |
| ![immagine dopo la trasformazione.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="2f373-121">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="2f373-121">Effect properties</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2f373-122">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="2f373-122">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="2f373-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f373-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f373-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="2f373-124">InterpolationMode</span></span><br/> <span data-ttu-id="2f373-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="2f373-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="2f373-126">Modalità di interpolazione utilizzata dall'effetto sull'immagine.</span><span class="sxs-lookup"><span data-stu-id="2f373-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="2f373-127">Sono disponibili 5 modalità di ridimensionamento che variano in qualità e velocità.</span><span class="sxs-lookup"><span data-stu-id="2f373-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="2f373-128">Il tipo è D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="2f373-128">Type is D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="2f373-129">Il valore predefinito è D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="2f373-129">Default value is D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f373-130">BorderMode</span><span class="sxs-lookup"><span data-stu-id="2f373-130">BorderMode</span></span><br/> <span data-ttu-id="2f373-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="2f373-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="2f373-132">Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard.</span><span class="sxs-lookup"><span data-stu-id="2f373-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="2f373-133">Per altre informazioni, vedere <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> .</span><span class="sxs-lookup"><span data-stu-id="2f373-133">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span><br/> <span data-ttu-id="2f373-134">Il tipo è D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="2f373-134">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="2f373-135">Il valore predefinito è D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="2f373-135">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f373-136">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="2f373-136">TransformMatrix</span></span><br/> <span data-ttu-id="2f373-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="2f373-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="2f373-138">Matrice di trasformazione 4x4 applicata al piano di proiezione.</span><span class="sxs-lookup"><span data-stu-id="2f373-138">A 4x4 transform matrix applied to the projection plane.</span></span> <span data-ttu-id="2f373-139">Il calcolo matrice seguente viene usato per eseguire il mapping di punti da un sistema di coordinate 3D al sistema di coordinate 2D trasformato.</span><span class="sxs-lookup"><span data-stu-id="2f373-139">The following matrix calculation is used to map points from one 3D coordinate system to the transformed 2D coordinate system.</span></span> <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" /><span data-ttu-id="2f373-140">Dove:</span><span class="sxs-lookup"><span data-stu-id="2f373-140">Where:</span></span><dl> <span data-ttu-id="2f373-141">X, Y, Z = coordinate del piano di proiezione di input</span><span class="sxs-lookup"><span data-stu-id="2f373-141">X, Y, Z = Input projection plane coordinates</span></span><br />
<span data-ttu-id="2f373-142">M<sub>x, y</sub> = elementi della matrice di trasformazione</span><span class="sxs-lookup"><span data-stu-id="2f373-142">M<sub>x,y</sub> = Transform Matrix elements</span></span><br />
<span data-ttu-id="2f373-143">X, Y, Z = coordinate del piano di proiezione di output</span><span class="sxs-lookup"><span data-stu-id="2f373-143">X , Y , Z  =Output projection plane coordinates</span></span><br />
</dl> <br/> <span data-ttu-id="2f373-144">I singoli elementi della matrice non sono limitati e sono senza unità.</span><span class="sxs-lookup"><span data-stu-id="2f373-144">The individual matrix elements are not bounded and are unitless.</span></span> <br/> <span data-ttu-id="2f373-145">Il tipo è D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="2f373-145">Type is D2D1_MATRIX_4X4_F.</span></span><br/> <span data-ttu-id="2f373-146">Il valore predefinito è Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="2f373-146">Default value is Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a><span data-ttu-id="2f373-147">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="2f373-147">Interpolation modes</span></span>



| <span data-ttu-id="2f373-148">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="2f373-148">Enumeration</span></span>                                                   | <span data-ttu-id="2f373-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f373-149">Description</span></span>                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f373-150">D2D1 \_ 3DTRANSFORM- \_ modalità di interpolazione \_ \_ più vicina \_</span><span class="sxs-lookup"><span data-stu-id="2f373-150">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="2f373-151">Campiona il punto singolo più vicino e lo utilizza.</span><span class="sxs-lookup"><span data-stu-id="2f373-151">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="2f373-152">In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.</span><span class="sxs-lookup"><span data-stu-id="2f373-152">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="2f373-153">D2D1 \_ 3DTRANSFORM- \_ modalità di interpolazione \_ \_ lineare</span><span class="sxs-lookup"><span data-stu-id="2f373-153">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="2f373-154">Usa un esempio a quattro punti e un'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="2f373-154">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="2f373-155">Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="2f373-155">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="2f373-156">D2D1 \_ 3DTRANSFORM- \_ modalità di interpolazione \_ \_ cubica</span><span class="sxs-lookup"><span data-stu-id="2f373-156">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="2f373-157">Usa un kernel cubico di esempio 16 per l'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="2f373-157">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="2f373-158">Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="2f373-158">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="2f373-159">D2D1 \_ 3DTRANSFORM- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_</span><span class="sxs-lookup"><span data-stu-id="2f373-159">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="2f373-160">USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi.</span><span class="sxs-lookup"><span data-stu-id="2f373-160">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="2f373-161">Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.</span><span class="sxs-lookup"><span data-stu-id="2f373-161">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="2f373-162">D2D1 \_ 3DTRANSFORM \_ modalità di interpolazione \_ \_ anisotropico</span><span class="sxs-lookup"><span data-stu-id="2f373-162">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="2f373-163">Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.</span><span class="sxs-lookup"><span data-stu-id="2f373-163">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="2f373-164">Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ 3DTRANSFORM \_ modalità di interpolazione \_ \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="2f373-164">If you don't select a mode, the effect defaults to D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="2f373-165">La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che vengono inseriti in questo effetto, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.</span><span class="sxs-lookup"><span data-stu-id="2f373-165">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

### <a name="border-modes"></a><span data-ttu-id="2f373-166">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="2f373-166">Border modes</span></span>



| <span data-ttu-id="2f373-167">Nome</span><span class="sxs-lookup"><span data-stu-id="2f373-167">Name</span></span>                     | <span data-ttu-id="2f373-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f373-168">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f373-169">\_Modalità bordo \_ d2d1 \_ Soft</span><span class="sxs-lookup"><span data-stu-id="2f373-169">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="2f373-170">L'effetto riempie l'immagine con i pixel neri trasparenti durante l'interpolazione, ottenendo un bordo flessibile.</span><span class="sxs-lookup"><span data-stu-id="2f373-170">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="2f373-171">\_Modalità bordo \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="2f373-171">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="2f373-172">L'effetto fissa l'output alla dimensione dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="2f373-172">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a><span data-ttu-id="2f373-173">Classe della matrice di trasformazione 4x4</span><span class="sxs-lookup"><span data-stu-id="2f373-173">4x4 Transform Matrix Class</span></span>

<span data-ttu-id="2f373-174">Direct2D fornisce una classe della matrice 4x4 per fornire funzioni helper per trasformare l'immagine in 3 dimensioni.</span><span class="sxs-lookup"><span data-stu-id="2f373-174">Direct2D provides a 4x4 matrix class to provide helper functions for transforming the image in 3 dimensions.</span></span> <span data-ttu-id="2f373-175">Vedere l'argomento [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) per altre informazioni e una descrizione di tutti i membri della classe.</span><span class="sxs-lookup"><span data-stu-id="2f373-175">See the [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) topic for more info and a description of all the class members.</span></span>



| <span data-ttu-id="2f373-176">Funzione</span><span class="sxs-lookup"><span data-stu-id="2f373-176">Function</span></span>                                | <span data-ttu-id="2f373-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f373-177">Description</span></span>                                                                                    | <span data-ttu-id="2f373-178">Matrice</span><span class="sxs-lookup"><span data-stu-id="2f373-178">Matrix</span></span>                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="2f373-179">Matrix4x4F:: scale (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="2f373-179">Matrix4x4F::Scale(X, Y, Z)</span></span>              | <span data-ttu-id="2f373-180">Genera una matrice di trasformazione che ridimensiona il piano di proiezione nella direzione X, Y e/o Z.</span><span class="sxs-lookup"><span data-stu-id="2f373-180">Generates a transform matrix that scales the projection plane in the X, Y, and/or Z direction.</span></span> | ![matrice scale3d](images/3d-transform-matrix2.png)     |
| <span data-ttu-id="2f373-182">SkewX (X)</span><span class="sxs-lookup"><span data-stu-id="2f373-182">SkewX(X)</span></span>                                | <span data-ttu-id="2f373-183">Genera una matrice di trasformazione che inclina il piano di proiezione nella direzione X.</span><span class="sxs-lookup"><span data-stu-id="2f373-183">Generates a transform matrix that skews the projection plane in the X direction.</span></span>               | ![Mostra una matrice di inclinazione nella direzione X.](images/matrix4x4-skewx.png)             |
| <span data-ttu-id="2f373-185">Asimmetria (Y)</span><span class="sxs-lookup"><span data-stu-id="2f373-185">SkewY(Y)</span></span>                                | <span data-ttu-id="2f373-186">Genera una matrice di trasformazione che inclina il piano di proiezione nella direzione Y.</span><span class="sxs-lookup"><span data-stu-id="2f373-186">Generates a transform matrix that skews the projection plane in the Y direction.</span></span>               | ![matrice di inclinazione](images/matrix4x4-skewy.png)             |
| <span data-ttu-id="2f373-188">Traduzione (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="2f373-188">Translation(X, Y, Z)</span></span>                    | <span data-ttu-id="2f373-189">Genera una matrice di trasformazione che converte il piano di proiezione nella direzione X, Y o Z.</span><span class="sxs-lookup"><span data-stu-id="2f373-189">Generates a transform matrix that translates the projection plane in the X, Y, or Z direction.</span></span> | ![Trasla matrice](images/3d-transform-matrix4.png)   |
| <span data-ttu-id="2f373-191">RotationX (X)</span><span class="sxs-lookup"><span data-stu-id="2f373-191">RotationX(X)</span></span>                            | <span data-ttu-id="2f373-192">Genera una matrice di trasformazione che ruota il piano di proiezione sull'asse X.</span><span class="sxs-lookup"><span data-stu-id="2f373-192">Generates a transform matrix that rotates the projection plane about the X axis.</span></span>               | ![ruota x matrice](images/3d-transform-matrix5.png)    |
| <span data-ttu-id="2f373-194">Rotazione (Y)</span><span class="sxs-lookup"><span data-stu-id="2f373-194">RotationY(Y)</span></span>                            | <span data-ttu-id="2f373-195">Genera una matrice di trasformazione che ruota il piano di proiezione sull'asse Y.</span><span class="sxs-lookup"><span data-stu-id="2f373-195">Generates a transform matrix that rotates the projection plane about the Y axis.</span></span>               | ![ruota y matrice](images/3d-transform-matrix6.png)    |
| <span data-ttu-id="2f373-197">RotationZ (Z)</span><span class="sxs-lookup"><span data-stu-id="2f373-197">RotationZ(Z)</span></span>                            | <span data-ttu-id="2f373-198">Genera una matrice di trasformazione che ruota il piano di proiezione sull'asse Z.</span><span class="sxs-lookup"><span data-stu-id="2f373-198">Generates a transform matrix that rotates the projection plane about the Z axis.</span></span>               | ![ruota matrice z](images/3d-transform-matrix7.png)    |
| <span data-ttu-id="2f373-200">PerspectiveProjection (D)</span><span class="sxs-lookup"><span data-stu-id="2f373-200">PerspectiveProjection(D)</span></span>                | <span data-ttu-id="2f373-201">Trasformazione prospettiva con un valore di profondità pari a D.</span><span class="sxs-lookup"><span data-stu-id="2f373-201">A perspective transformation with a depth value of D.</span></span>                                          | ![matrice prospettiva](images/3d-transform-matrix8.png) |
| <span data-ttu-id="2f373-203">RotationArbitraryAxis (X, Y, Z, gradi)</span><span class="sxs-lookup"><span data-stu-id="2f373-203">RotationArbitraryAxis(X, Y, Z, degrees)</span></span> | <span data-ttu-id="2f373-204">Ruota il piano di proiezione sull'asse specificato.</span><span class="sxs-lookup"><span data-stu-id="2f373-204">Rotates the projection plane about the axis you specify.</span></span>                                       |                                                        |



 

## <a name="requirements"></a><span data-ttu-id="2f373-205">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f373-205">Requirements</span></span>



| <span data-ttu-id="2f373-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f373-206">Requirement</span></span> | <span data-ttu-id="2f373-207">Valore</span><span class="sxs-lookup"><span data-stu-id="2f373-207">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f373-208">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f373-208">Minimum supported client</span></span> | <span data-ttu-id="2f373-209">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2f373-209">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2f373-210">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f373-210">Minimum supported server</span></span> | <span data-ttu-id="2f373-211">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2f373-211">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2f373-212">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f373-212">Header</span></span>                   | <span data-ttu-id="2f373-213">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="2f373-213">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="2f373-214">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f373-214">Library</span></span>                  | <span data-ttu-id="2f373-215">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="2f373-215">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2f373-216">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f373-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f373-217">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="2f373-217">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

