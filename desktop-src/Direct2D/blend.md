---
title: Effetto sfumatura
description: Usare l'effetto Blend per combinare 2 immagini. Questo effetto presenta 26 modalità di Blend.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- effetto Blend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874470"
---
# <a name="blend-effect"></a><span data-ttu-id="22c9a-105">Effetto sfumatura</span><span class="sxs-lookup"><span data-stu-id="22c9a-105">Blend effect</span></span>

<span data-ttu-id="22c9a-106">Usare l'effetto Blend per combinare 2 immagini.</span><span class="sxs-lookup"><span data-stu-id="22c9a-106">Use the blend effect to combine 2 images.</span></span> <span data-ttu-id="22c9a-107">Questo effetto presenta 26 modalità di Blend.</span><span class="sxs-lookup"><span data-stu-id="22c9a-107">This effect has 26 blend modes.</span></span>

<span data-ttu-id="22c9a-108">Il CLSID per questo effetto è CLSID \_ D2D1Blend.</span><span class="sxs-lookup"><span data-stu-id="22c9a-108">The CLSID for this effect is CLSID\_D2D1Blend.</span></span>

-   [<span data-ttu-id="22c9a-109">Esempi di fusione</span><span class="sxs-lookup"><span data-stu-id="22c9a-109">Blending examples</span></span>](#blending-examples)
-   [<span data-ttu-id="22c9a-110">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="22c9a-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="22c9a-111">Modalità di Blend</span><span class="sxs-lookup"><span data-stu-id="22c9a-111">Blend modes</span></span>](#blend-modes)
-   [<span data-ttu-id="22c9a-112">Conversioni dello spazio dei colori HSL</span><span class="sxs-lookup"><span data-stu-id="22c9a-112">HSL color space conversions</span></span>](#hsl-color-space-conversions)
    -   [<span data-ttu-id="22c9a-113">Conversione da RGB a HSL</span><span class="sxs-lookup"><span data-stu-id="22c9a-113">Converting from RGB to HSL</span></span>](#converting-from-rgb-to-hsl)
    -   [<span data-ttu-id="22c9a-114">Conversione da HSL a RGB</span><span class="sxs-lookup"><span data-stu-id="22c9a-114">Converting from HSL to RGB</span></span>](#converting-from-hsl-to-rgb)
-   [<span data-ttu-id="22c9a-115">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="22c9a-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="22c9a-116">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="22c9a-116">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="22c9a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22c9a-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="22c9a-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22c9a-118">Related topics</span></span>](#related-topics)

## <a name="blending-examples"></a><span data-ttu-id="22c9a-119">Esempi di fusione</span><span class="sxs-lookup"><span data-stu-id="22c9a-119">Blending examples</span></span>

<span data-ttu-id="22c9a-120">Ecco un'immagine di esempio di ogni modalità di Blend dell'effetto Blend.</span><span class="sxs-lookup"><span data-stu-id="22c9a-120">Here is an example image of every blend mode of the blend effect.</span></span> <span data-ttu-id="22c9a-121">Un elenco completo delle modalità di Blend e delle proprietà della modalità corrispondenti si trova nella sezione successiva</span><span class="sxs-lookup"><span data-stu-id="22c9a-121">A full list of the blend modes and the corresponding mode properties are in the next section</span></span>

![schermata di esempio effetto di tutte le modalità di Blend disponibili.](images/blend-modes.png)

<span data-ttu-id="22c9a-123">Di seguito è riportato un altro esempio che usa la modalità di esclusione.</span><span class="sxs-lookup"><span data-stu-id="22c9a-123">Here is another example using the exclusion mode.</span></span>



| <span data-ttu-id="22c9a-124">Prima dell'immagine 1</span><span class="sxs-lookup"><span data-stu-id="22c9a-124">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![prima immagine di origine prima dell'effetto.](images/default-before.jpg)    |
| <span data-ttu-id="22c9a-126">Prima dell'immagine 2</span><span class="sxs-lookup"><span data-stu-id="22c9a-126">Before image 2</span></span>                                                             |
| ![seconda immagine prima dell'effetto.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="22c9a-128">After</span><span class="sxs-lookup"><span data-stu-id="22c9a-128">After</span></span>                                                                      |
| ![immagine dopo la trasformazione.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="22c9a-130">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="22c9a-130">Effect properties</span></span>



| <span data-ttu-id="22c9a-131">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="22c9a-131">Display name and index enumeration</span></span>                 | <span data-ttu-id="22c9a-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22c9a-132">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c9a-133">Mode</span><span class="sxs-lookup"><span data-stu-id="22c9a-133">Mode</span></span><br/> <span data-ttu-id="22c9a-134">\_ \_ Modalità prop di Blend d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="22c9a-134">D2D1\_BLEND\_PROP\_MODE</span></span><br/> | <span data-ttu-id="22c9a-135">Modalità di Blend utilizzata per l'effetto.</span><span class="sxs-lookup"><span data-stu-id="22c9a-135">The blend mode used for the effect.</span></span> <span data-ttu-id="22c9a-136">Per altre informazioni, vedere [modalità di Blend](#blend-modes) .</span><span class="sxs-lookup"><span data-stu-id="22c9a-136">See [Blend modes](#blend-modes) for more info.</span></span> <span data-ttu-id="22c9a-137">Il tipo è D2D1 \_ Blend \_ mode.</span><span class="sxs-lookup"><span data-stu-id="22c9a-137">The type is D2D1\_BLEND\_MODE.</span></span><br/> <span data-ttu-id="22c9a-138">Il valore predefinito è D2D1 \_ Blend \_ mode \_ Multiply.</span><span class="sxs-lookup"><span data-stu-id="22c9a-138">The default value is D2D1\_BLEND\_MODE\_MULTIPLY.</span></span><br/> |



 

## <a name="blend-modes"></a><span data-ttu-id="22c9a-139">Modalità di Blend</span><span class="sxs-lookup"><span data-stu-id="22c9a-139">Blend modes</span></span>

<span data-ttu-id="22c9a-140">La tabella seguente mostra tutte le modalità di combinazione di questo effetto.</span><span class="sxs-lookup"><span data-stu-id="22c9a-140">The table here shows all the blend modes of this effect.</span></span> <span data-ttu-id="22c9a-141">Le funzioni di supporto necessarie per calcolare l'output dell'effetto sono disponibili nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="22c9a-141">The helper functions necessary to compute the output of the effect are in the next section.</span></span>

<span data-ttu-id="22c9a-142">Colore: O <sub>PRGB</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + b <sub>RGB</sub> \* b <sub>a</sub> \* (1-f <sub>a</sub>)</span><span class="sxs-lookup"><span data-stu-id="22c9a-142">Color: O <sub>PRGB</sub> = *f*(F<sub>RGB</sub>, B<sub>RGB</sub>) \* F<sub>A</sub> \* B<sub>A</sub> + F<sub>RGB</sub> \* F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>RGB</sub> \* B<sub>A</sub> \* (1 - F<sub>A</sub>)</span></span>

<span data-ttu-id="22c9a-143">Alfa: O<sub>a</sub> = F<sub>a</sub> \* (1-b<sub>a</sub>) + B<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="22c9a-143">Alpha: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub></span></span>

<span data-ttu-id="22c9a-144">Dove:</span><span class="sxs-lookup"><span data-stu-id="22c9a-144">Where:</span></span>

-   <span data-ttu-id="22c9a-145">O<sub>PRGB</sub> è il colore di output pre-moltiplicato</span><span class="sxs-lookup"><span data-stu-id="22c9a-145">O<sub>PRGB</sub> is the pre-multiplied output color</span></span>
-   <span data-ttu-id="22c9a-146">O<sub>A è l'</sub> output alfa</span><span class="sxs-lookup"><span data-stu-id="22c9a-146">O<sub>A</sub> is Output Alpha</span></span>
-   <span data-ttu-id="22c9a-147">B<sub>RGB</sub> è il colore di destinazione non pre-moltiplicato</span><span class="sxs-lookup"><span data-stu-id="22c9a-147">B<sub>RGB</sub> is the un-pre-multiplied destination color</span></span>
-   <span data-ttu-id="22c9a-148">B<sub>A</sub> è Alpha di destinazione</span><span class="sxs-lookup"><span data-stu-id="22c9a-148">B<sub>A</sub> is destination alpha</span></span>
-   <span data-ttu-id="22c9a-149">F<sub>RGB</sub> è il colore di origine non pre-moltiplicato</span><span class="sxs-lookup"><span data-stu-id="22c9a-149">F<sub>RGB</sub> is the un-pre-multiplied source color</span></span>
-   <span data-ttu-id="22c9a-150">F<sub>A è un Alpha di</sub> origine</span><span class="sxs-lookup"><span data-stu-id="22c9a-150">F<sub>A</sub> is source alpha</span></span>
-   <span data-ttu-id="22c9a-151">*f*(S <sub>RGB</sub>, D <sub>RGB</sub>) è una funzione Blend che varia in base alla modalità per Blend</span><span class="sxs-lookup"><span data-stu-id="22c9a-151">*f*(S<sub>RGB</sub>, D<sub>RGB</sub>) is a blend function that varies per-blend-mode</span></span>

<span data-ttu-id="22c9a-152">Per alcune delle modalità di Blend è necessario eseguire la conversione da e verso lo spazio dei colori Hue, Saturation, luminosità (HSL) in RGB.</span><span class="sxs-lookup"><span data-stu-id="22c9a-152">Some of the blend modes require conversion to and from the hue, saturation, luminosity (HSL) color space to RGB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22c9a-153">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="22c9a-153">Enumeration</span></span></th>
<th><span data-ttu-id="22c9a-154">Equazione</span><span class="sxs-lookup"><span data-stu-id="22c9a-154">Equation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22c9a-155">D2D1_BLEND_MODE_DARKEN</span><span class="sxs-lookup"><span data-stu-id="22c9a-155">D2D1_BLEND_MODE_DARKEN</span></span></td>
<td><span data-ttu-id="22c9a-156">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-156">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-157">D2D1_BLEND_MODE_MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="22c9a-157">D2D1_BLEND_MODE_MULTIPLY</span></span></td>
<td><span data-ttu-id="22c9a-158">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-158">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-159">D2D1_BLEND_MODE_COLOR_BURN</span><span class="sxs-lookup"><span data-stu-id="22c9a-159">D2D1_BLEND_MODE_COLOR_BURN</span></span></td>
<td><span data-ttu-id="22c9a-160">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-160">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-161">D2D1_BLEND_MODE_LINEAR_BURN</span><span class="sxs-lookup"><span data-stu-id="22c9a-161">D2D1_BLEND_MODE_LINEAR_BURN</span></span></td>
<td><span data-ttu-id="22c9a-162">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-162">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-163">D2D1_BLEND_MODE_DARKER_COLOR</span><span class="sxs-lookup"><span data-stu-id="22c9a-163">D2D1_BLEND_MODE_DARKER_COLOR</span></span></td>
<td><span data-ttu-id="22c9a-164">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-164">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-165">D2D1_BLEND_MODE_LIGHTEN</span><span class="sxs-lookup"><span data-stu-id="22c9a-165">D2D1_BLEND_MODE_LIGHTEN</span></span></td>
<td><span data-ttu-id="22c9a-166">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-166">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-167">D2D1_BLEND_MODE_SCREEN</span><span class="sxs-lookup"><span data-stu-id="22c9a-167">D2D1_BLEND_MODE_SCREEN</span></span></td>
<td><span data-ttu-id="22c9a-168">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-168">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-169">D2D1_BLEND_MODE_COLOR_DODGE</span><span class="sxs-lookup"><span data-stu-id="22c9a-169">D2D1_BLEND_MODE_COLOR_DODGE</span></span></td>
<td><span data-ttu-id="22c9a-170">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-170">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-171">D2D1_BLEND_MODE_LINEAR_DODGE</span><span class="sxs-lookup"><span data-stu-id="22c9a-171">D2D1_BLEND_MODE_LINEAR_DODGE</span></span></td>
<td><span data-ttu-id="22c9a-172">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-172">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span><span class="sxs-lookup"><span data-stu-id="22c9a-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span></span></td>
<td><span data-ttu-id="22c9a-174">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-174">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-175">D2D1_BLEND_MODE_OVERLAY</span><span class="sxs-lookup"><span data-stu-id="22c9a-175">D2D1_BLEND_MODE_OVERLAY</span></span></td>
<td><span data-ttu-id="22c9a-176">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-176">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-177">D2D1_BLEND_MODE_SOFT_LIGHT</span><span class="sxs-lookup"><span data-stu-id="22c9a-177">D2D1_BLEND_MODE_SOFT_LIGHT</span></span></td>
<td><span data-ttu-id="22c9a-178">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-178">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-179">D2D1_BLEND_MODE_HARD_LIGHT</span><span class="sxs-lookup"><span data-stu-id="22c9a-179">D2D1_BLEND_MODE_HARD_LIGHT</span></span></td>
<td><span data-ttu-id="22c9a-180">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-180">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-181">D2D1_BLEND_MODE_VIVID_LIGHT</span><span class="sxs-lookup"><span data-stu-id="22c9a-181">D2D1_BLEND_MODE_VIVID_LIGHT</span></span></td>
<td><span data-ttu-id="22c9a-182">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-182">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span><span class="sxs-lookup"><span data-stu-id="22c9a-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span></span></td>
<td><span data-ttu-id="22c9a-184">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-184">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-185">D2D1_BLEND_MODE_PIN_LIGHT</span><span class="sxs-lookup"><span data-stu-id="22c9a-185">D2D1_BLEND_MODE_PIN_LIGHT</span></span></td>
<td><span data-ttu-id="22c9a-186">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-186">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-187">D2D1_BLEND_MODE_HARD_MIX</span><span class="sxs-lookup"><span data-stu-id="22c9a-187">D2D1_BLEND_MODE_HARD_MIX</span></span></td>
<td><span data-ttu-id="22c9a-188">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="22c9a-188">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-189">D2D1_BLEND_MODE_DIFFERENCE</span><span class="sxs-lookup"><span data-stu-id="22c9a-189">D2D1_BLEND_MODE_DIFFERENCE</span></span></td>
<td><span data-ttu-id="22c9a-190">Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RGB</sub> - B<sub>RGB</sub>)</span><span class="sxs-lookup"><span data-stu-id="22c9a-190">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-191">D2D1_BLEND_MODE_EXCLUSION</span><span class="sxs-lookup"><span data-stu-id="22c9a-191">D2D1_BLEND_MODE_EXCLUSION</span></span></td>
<td><span data-ttu-id="22c9a-192">Formule di base di Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + b<sub>RGB</sub> 2 \* f<sub>RGB</sub> \* b<sub></sub> RGB</span><span class="sxs-lookup"><span data-stu-id="22c9a-192">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 \* F<sub>RGB</sub> \* B<sub>RGB</sub></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-193">D2D1_BLEND_MODE_HUE</span><span class="sxs-lookup"><span data-stu-id="22c9a-193">D2D1_BLEND_MODE_HUE</span></span></td>
<td><span data-ttu-id="22c9a-194">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-194">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-195">D2D1_BLEND_MODE_SATURATION</span><span class="sxs-lookup"><span data-stu-id="22c9a-195">D2D1_BLEND_MODE_SATURATION</span></span></td>
<td><span data-ttu-id="22c9a-196">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-196">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-197">D2D1_BLEND_MODE_COLOR</span><span class="sxs-lookup"><span data-stu-id="22c9a-197">D2D1_BLEND_MODE_COLOR</span></span></td>
<td><span data-ttu-id="22c9a-198">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-198">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-199">D2D1_BLEND_MODE_LUMINOSITY</span><span class="sxs-lookup"><span data-stu-id="22c9a-199">D2D1_BLEND_MODE_LUMINOSITY</span></span></td>
<td><span data-ttu-id="22c9a-200">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-200">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-201">D2D1_BLEND_MODE_DISSOLVE</span><span class="sxs-lookup"><span data-stu-id="22c9a-201">D2D1_BLEND_MODE_DISSOLVE</span></span></td>
<td><span data-ttu-id="22c9a-202">Si consideri quanto segue:</span><span class="sxs-lookup"><span data-stu-id="22c9a-202">Given:</span></span>
<ul>
<li><span data-ttu-id="22c9a-203">Coordinata XY del pixel corrente</span><span class="sxs-lookup"><span data-stu-id="22c9a-203">A scene coordinate XY for the current pixel</span></span></li>
<li><span data-ttu-id="22c9a-204">Un generatore di numeri pseudo-casuali deterministico (XY) basato su una coordinata XY con una distribuzione non distorta dei valori da [0,1]</span><span class="sxs-lookup"><span data-stu-id="22c9a-204">A deterministic pseudo-random number generator rand(XY) based on seed coordinate XY, with unbiased distribution of values from [0, 1]</span></span></li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c9a-205">D2D1_BLEND_MODE_SUBTRACT</span><span class="sxs-lookup"><span data-stu-id="22c9a-205">D2D1_BLEND_MODE_SUBTRACT</span></span></td>
<td><span data-ttu-id="22c9a-206">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-206">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c9a-207">D2D1_BLEND_MODE_DIVISION</span><span class="sxs-lookup"><span data-stu-id="22c9a-207">D2D1_BLEND_MODE_DIVISION</span></span></td>
<td><span data-ttu-id="22c9a-208">Formula di Blend di base solo per Alpha.</span><span class="sxs-lookup"><span data-stu-id="22c9a-208">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="22c9a-209">Per tutte le modalità di Blend, il valore di output è premoltiplicato e viene premuto per l'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="22c9a-209">For all Blend modes, the output value is premultiplied and clamped to the range \[0, 1\].</span></span>

 

## <a name="hsl-color-space-conversions"></a><span data-ttu-id="22c9a-210">Conversioni dello spazio dei colori HSL</span><span class="sxs-lookup"><span data-stu-id="22c9a-210">HSL color space conversions</span></span>

<span data-ttu-id="22c9a-211">Il componente luminosità viene calcolato usando i pesi RGB qui:</span><span class="sxs-lookup"><span data-stu-id="22c9a-211">The luminosity component is computed using the RGB weights here:</span></span>

-   <span data-ttu-id="22c9a-212">*k*<sub>R</sub> = 0,30</span><span class="sxs-lookup"><span data-stu-id="22c9a-212">*k*<sub>R</sub> = 0.30</span></span>
-   <span data-ttu-id="22c9a-213">*k*<sub>G</sub> = 0,59</span><span class="sxs-lookup"><span data-stu-id="22c9a-213">*k*<sub>G</sub> = 0.59</span></span>
-   <span data-ttu-id="22c9a-214">*k*<sub>B</sub> = 0,11</span><span class="sxs-lookup"><span data-stu-id="22c9a-214">*k*<sub>B</sub> = 0.11</span></span>

### <a name="converting-from-rgb-to-hsl"></a><span data-ttu-id="22c9a-215">Conversione da RGB a HSL</span><span class="sxs-lookup"><span data-stu-id="22c9a-215">Converting from RGB to HSL</span></span>

![formula matematica che descrive la trasformazione dal colore RGB al colore HSL.](images/blend-rgb-to-hsl-1.png)

<span data-ttu-id="22c9a-217">Questo inserisce *S* e *L* nell'intervallo \[ 0,0, 1,0 \] e *H* nell'intervallo \[ 1,0, 5,0 \] .</span><span class="sxs-lookup"><span data-stu-id="22c9a-217">This places *S* and *L* in the range \[0.0, 1.0\] and *H* in the range \[-1.0, 5.0\].</span></span>

### <a name="converting-from-hsl-to-rgb"></a><span data-ttu-id="22c9a-218">Conversione da HSL a RGB</span><span class="sxs-lookup"><span data-stu-id="22c9a-218">Converting from HSL to RGB</span></span>

<span data-ttu-id="22c9a-219">Per convertire l'altro modo si usa l'inverso dei calcoli precedenti.</span><span class="sxs-lookup"><span data-stu-id="22c9a-219">To convert the other way we use the inverse of the previous calculations.</span></span>

<span data-ttu-id="22c9a-220">Se *S* = 0, *R*  =  *G*  =  *B*  =  *L*</span><span class="sxs-lookup"><span data-stu-id="22c9a-220">If *S* = 0 then *R* = *G* = *B* = *L*</span></span>

<span data-ttu-id="22c9a-221">In caso contrario, sono presenti sei casi di Hue:</span><span class="sxs-lookup"><span data-stu-id="22c9a-221">Otherwise there are six hue-dependant cases:</span></span>

<span data-ttu-id="22c9a-222">Se *H* è maggiore di 0, i valori si trovano nel settore rosso/magenta dove *R*  >  *B*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="22c9a-222">If *H* is greater than 0, the values are in the red/magenta sector where *R* > *B* > *G*.</span></span>

![equaiton matematico passaggio uno di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1rm.png)

<span data-ttu-id="22c9a-224">Se *H* è maggiore o uguale a 0 e minore di 1, i valori sono nel settore rosso/giallo dove *R*  >  *G*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="22c9a-224">If *H* is greater than or equal to 0 and less than 1, the values are in the red/yellow sector where *R* > *G* > *B*.</span></span>

![equaiton matematico-passaggio due di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1ry.png)

<span data-ttu-id="22c9a-226">Se *H* è maggiore o uguale a 1 e minore di 2, i valori sono nel settore giallo/verde dove *G*  >  *R*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="22c9a-226">If *H* is greater than or equal to 1 and less than 2, the values are in the yellow/green sector where *G* > *R* > *B*.</span></span>

![equaiton matematico 3 di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1yg.png)

<span data-ttu-id="22c9a-228">Se *H* è maggiore o uguale a 2 e minore di 3, i valori sono nel settore verde/ciano dove *G*  >  *B*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="22c9a-228">If *H* is greater than or equal to 2 and less than 3, the values are in the green/cyan sector where *G* > *B* > *R*.</span></span>

![equaiton matematico-passaggio quattro di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1gc.png)

<span data-ttu-id="22c9a-230">Se *H* è maggiore o uguale a 3 e minore di 4, i valori si trovano nel settore cyan/blue dove *B*  >  *G*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="22c9a-230">If *H* is greater than or equal to 3 and less than 4, the values are in the cyan/blue sector where *B* > *G* > *R*.</span></span>

![equaiton matematico-passaggio cinque di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1cb.png)

<span data-ttu-id="22c9a-232">Se *H* è maggiore o uguale a 4, i valori si trovano nel settore blu/Magenta dove *B*  >  *R*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="22c9a-232">If *H* is greater than or equal to 4, the values are in the blue/magenta sector where *B* > *R* > *G*.</span></span>

![equaiton matematico 6 di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1bm.png)

<span data-ttu-id="22c9a-234">Poiché le modalità di fusione consentono di combinare arbitrariamente i componenti HSL da due colori diversi, il valore RGB convertito non è compreso nell'intervallo, ovvero uno o più componenti del canale potrebbero non essere compresi nell'intervallo valido \[ 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="22c9a-234">Because the blending modes make arbitrary combinations of HSL components from two different colors, it is common for the converted RGB value to be out-of-gamut, that is, one or more channel components may be outside the legal range of \[0.0, 1.0\].</span></span> <span data-ttu-id="22c9a-235">Questi colori vengono restituiti in gamut riducendo al minimo la saturazione, mantenendo al tempo stesso tonalità e luminosità:</span><span class="sxs-lookup"><span data-stu-id="22c9a-235">These colors are brought back into gamut by minimally reducing the saturation, while preserving both hue and luminosity:</span></span>

![formula matematica che descrive le correzioni necessarie per le istanze out-of-gamut.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a><span data-ttu-id="22c9a-237">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="22c9a-237">Output bitmap</span></span>

<span data-ttu-id="22c9a-238">La bitmap di output per questo effetto è sempre la dimensione dell'Unione delle due immagini di input.</span><span class="sxs-lookup"><span data-stu-id="22c9a-238">The output bitmap for this effect is always the size of the union of the two input images.</span></span>

## <a name="sample-code"></a><span data-ttu-id="22c9a-239">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="22c9a-239">Sample code</span></span>

<span data-ttu-id="22c9a-240">Per un esempio di questo effetto, scaricare l' [esempio Direct2D composite Effect modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="22c9a-240">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="22c9a-241">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22c9a-241">Requirements</span></span>



| <span data-ttu-id="22c9a-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c9a-242">Requirement</span></span> | <span data-ttu-id="22c9a-243">Valore</span><span class="sxs-lookup"><span data-stu-id="22c9a-243">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22c9a-244">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22c9a-244">Minimum supported client</span></span> | <span data-ttu-id="22c9a-245">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="22c9a-245">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="22c9a-246">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22c9a-246">Minimum supported server</span></span> | <span data-ttu-id="22c9a-247">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="22c9a-247">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="22c9a-248">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22c9a-248">Header</span></span>                   | <span data-ttu-id="22c9a-249">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="22c9a-249">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="22c9a-250">Libreria</span><span class="sxs-lookup"><span data-stu-id="22c9a-250">Library</span></span>                  | <span data-ttu-id="22c9a-251">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="22c9a-251">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="22c9a-252">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22c9a-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c9a-253">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="22c9a-253">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

