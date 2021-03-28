---
title: dcl_input (SM4-ASM)
description: '\_input DCL (SM4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993229"
---
# <a name="dcl_input-sm4---asm"></a><span data-ttu-id="7dd06-103">\_input DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7dd06-103">dcl\_input (sm4 - asm)</span></span>

<span data-ttu-id="7dd06-104">Dichiara un registro di input shader.</span><span class="sxs-lookup"><span data-stu-id="7dd06-104">Declares a shader-input register.</span></span>



| <span data-ttu-id="7dd06-105">\_input DCL v *N \[ . mask \] \[ , interpolationMode \]*</span><span class="sxs-lookup"><span data-stu-id="7dd06-105">dcl\_input v *N\[.mask\]\[, interpolationMode\]*</span></span> |
|-------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7dd06-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7dd06-106">Item</span></span></th>
<th><span data-ttu-id="7dd06-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dd06-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7dd06-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. mask]</em></span><span class="sxs-lookup"><span data-stu-id="7dd06-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="7dd06-109">in Registro dei dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="7dd06-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="7dd06-110"><em>N</em> è un intero che identifica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="7dd06-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="7dd06-111"><em>[. mask]</em> è una maschera di componenti facoltativa (con estensione xyzw) che specifica quale dei componenti del registro utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7dd06-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7dd06-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="7dd06-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="7dd06-113">[in] Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7dd06-113">[in] Optional.</span></span> <span data-ttu-id="7dd06-114">La modalità di interpolazione, che viene rispettata solo nei registri di input pixel shader.</span><span class="sxs-lookup"><span data-stu-id="7dd06-114">The interpolation mode, which is only honored on pixel shader input registers.</span></span> <span data-ttu-id="7dd06-115">Può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7dd06-115">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="7dd06-116">Constant: non esegue l'interpolazione tra valori di registro.</span><span class="sxs-lookup"><span data-stu-id="7dd06-116">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="7dd06-117">lineare: esegue l'interpolazione lineare tra i valori di registro.</span><span class="sxs-lookup"><span data-stu-id="7dd06-117">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="7dd06-118">linearCentroid: uguale a lineare, ma al centro quando viene premuto il multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="7dd06-118">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="7dd06-119">linearNoperspective: uguale a lineare, ma senza correzione della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="7dd06-119">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="7dd06-120">linearNoperspectiveCentroid: uguale a lineare, al centro quando si verifica il multicampionamento, senza correzione della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="7dd06-120">linearNoperspectiveCentroid - same as linear, centroid clamped when multisampling, no perspective correction.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a><span data-ttu-id="7dd06-121">Note di interpolazione</span><span class="sxs-lookup"><span data-stu-id="7dd06-121">Interpolation Notes</span></span>

<span data-ttu-id="7dd06-122">Per impostazione predefinita, gli attributi dei vertici vengono interpolati da un pixel Center quando si esegue l'anti-aliasing multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="7dd06-122">By default, vertex attributes are interpolated from a pixel center when performing multisample antialiasing.</span></span> <span data-ttu-id="7dd06-123">Se non viene analizzato un pixel Center, un attributo viene estrapolato in un centro pixel prima dell'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="7dd06-123">If a pixel center is not covered, an attribute is extrapolated to a pixel center before interpolation.</span></span>

<span data-ttu-id="7dd06-124">Per un pixel non completamente coperto o un attributo che non copre un pixel Center, è possibile specificare il campionamento del baricentro che forza il campionamento in un punto qualsiasi all'interno dell'area coperta del pixel.</span><span class="sxs-lookup"><span data-stu-id="7dd06-124">For a pixel that is not fully covered or an attribute that does not cover a pixel center, you can specify centroid sampling which forces sampling to occur somewhere within the covered area of the pixel.</span></span> <span data-ttu-id="7dd06-125">Poiché una maschera di esempio (se utilizzata) viene applicata prima che il baricentro venga calcolato, qualsiasi percorso di esempio mascherato dalla maschera di esempio non può essere scelto come posizione del centro.</span><span class="sxs-lookup"><span data-stu-id="7dd06-125">Because a sample mask (if used) is applied before the centroid is computed, any sample location masked out by the sample mask cannot be chosen as a centroid location.</span></span>

<span data-ttu-id="7dd06-126">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7dd06-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7dd06-127">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="7dd06-127">Vertex Shader</span></span> | <span data-ttu-id="7dd06-128">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="7dd06-128">Geometry Shader</span></span> | <span data-ttu-id="7dd06-129">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="7dd06-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7dd06-130">x</span><span class="sxs-lookup"><span data-stu-id="7dd06-130">x</span></span>             | <span data-ttu-id="7dd06-131">x</span><span class="sxs-lookup"><span data-stu-id="7dd06-131">x</span></span>               | <span data-ttu-id="7dd06-132">x</span><span class="sxs-lookup"><span data-stu-id="7dd06-132">x</span></span>            |



 

<span data-ttu-id="7dd06-133">Per identificare l'input come valore di sistema, usare [l' \_ input DCL \_ SV (SM4-ASM)](dcl-input-sv.md).</span><span class="sxs-lookup"><span data-stu-id="7dd06-133">To identify the input as a system value, use [dcl\_input\_sv (sm4 - asm)](dcl-input-sv.md).</span></span>

<span data-ttu-id="7dd06-134">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="7dd06-134">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="7dd06-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="7dd06-135">Example</span></span>

<span data-ttu-id="7dd06-136">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="7dd06-136">Here are some examples.</span></span>


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a><span data-ttu-id="7dd06-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="7dd06-137">Minimum Shader Model</span></span>

<span data-ttu-id="7dd06-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="7dd06-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7dd06-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7dd06-139">Shader Model</span></span>                                              | <span data-ttu-id="7dd06-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="7dd06-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7dd06-141">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7dd06-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7dd06-142">sì</span><span class="sxs-lookup"><span data-stu-id="7dd06-142">yes</span></span>       |
| [<span data-ttu-id="7dd06-143">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="7dd06-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7dd06-144">sì</span><span class="sxs-lookup"><span data-stu-id="7dd06-144">yes</span></span>       |
| [<span data-ttu-id="7dd06-145">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="7dd06-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7dd06-146">sì</span><span class="sxs-lookup"><span data-stu-id="7dd06-146">yes</span></span>       |
| [<span data-ttu-id="7dd06-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7dd06-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7dd06-148">no</span><span class="sxs-lookup"><span data-stu-id="7dd06-148">no</span></span>        |
| [<span data-ttu-id="7dd06-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7dd06-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7dd06-150">no</span><span class="sxs-lookup"><span data-stu-id="7dd06-150">no</span></span>        |
| [<span data-ttu-id="7dd06-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7dd06-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7dd06-152">no</span><span class="sxs-lookup"><span data-stu-id="7dd06-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7dd06-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7dd06-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dd06-154">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7dd06-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





