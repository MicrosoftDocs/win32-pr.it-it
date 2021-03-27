---
title: dcl_input_sv (SM4-ASM)
description: '\_input DCL \_ SV (SM4-ASM)'
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719486"
---
# <a name="dcl_input_sv-sm4---asm"></a><span data-ttu-id="2f374-103">\_input DCL \_ SV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2f374-103">dcl\_input\_sv (sm4 - asm)</span></span>

<span data-ttu-id="2f374-104">Dichiara un registro di input shader che prevede che un valore di [sistema](dx-graphics-hlsl-semantics.md) venga fornito da una fase precedente.</span><span class="sxs-lookup"><span data-stu-id="2f374-104">Declares a shader-input register that expects a [system-value](dx-graphics-hlsl-semantics.md) to be provided from a preceding stage.</span></span>



| <span data-ttu-id="2f374-105">\_input DCL \_ SV v *N \[ . mask \]*, *systemValueName \[ , interpolationMode \]*</span><span class="sxs-lookup"><span data-stu-id="2f374-105">dcl\_input\_sv v *N\[.mask\]*, *systemValueName\[, interpolationMode\]*</span></span> |
|------------------------------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f374-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2f374-106">Item</span></span></th>
<th><span data-ttu-id="2f374-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f374-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f374-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. mask]</em></span><span class="sxs-lookup"><span data-stu-id="2f374-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="2f374-109">in Registro dei dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2f374-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="2f374-110"><em>N</em> è un intero che identifica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="2f374-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="2f374-111"><em>[. mask]</em> è una maschera di componenti facoltativa (con estensione xyzw) che specifica quale dei componenti del registro utilizzare.</span><span class="sxs-lookup"><span data-stu-id="2f374-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f374-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span><span class="sxs-lookup"><span data-stu-id="2f374-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span></span><br/></td>
<td><span data-ttu-id="2f374-113">in Nome del valore di sistema che è una stringa (vedere <a href="dx-graphics-hlsl-semantics.md">semantica del valore di sistema</a>) senza &quot; il &quot; prefisso SV_.</span><span class="sxs-lookup"><span data-stu-id="2f374-113">[in] The system-value name which is a string (see <a href="dx-graphics-hlsl-semantics.md">system-value semantics</a>) without the &quot;SV_&quot; prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f374-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="2f374-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="2f374-115">[in] Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2f374-115">[in] Optional.</span></span> <span data-ttu-id="2f374-116">La modalità di interpolazione che influiscono sulle modalità di calcolo dei valori durante la rasterizzazione; la modalità viene utilizzata solo da un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="2f374-116">The interpolation mode which affects how values are calculated during rasterization; the mode is only used by a pixel shader.</span></span> <span data-ttu-id="2f374-117">Può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f374-117">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="2f374-118">Constant: non esegue l'interpolazione tra valori di registro.</span><span class="sxs-lookup"><span data-stu-id="2f374-118">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="2f374-119">lineare: esegue l'interpolazione lineare tra i valori di registro.</span><span class="sxs-lookup"><span data-stu-id="2f374-119">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="2f374-120">linearCentroid: uguale a lineare, ma al centro quando viene premuto il multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="2f374-120">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="2f374-121">linearNoperspective: uguale a lineare, ma senza correzione della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="2f374-121">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="2f374-122">linearNoperspectiveCentroid: uguale a lineare, ma senza correzione della prospettiva e centro per il multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="2f374-122">linearNoperspectiveCentroid - same as linear but with no perspective correction and centroid clamped when multisampling.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2f374-123">Una maschera di componente per una dichiarazione di valore di sistema può essere qualsiasi subset appropriato di \[ xyzw \] ; le dichiarazioni non possono sovrapporsi (ogni dichiarazione deve seguire la sequenza xyzw).</span><span class="sxs-lookup"><span data-stu-id="2f374-123">A component mask for a system-value declaration can be any appropriate subset of \[xyzw\]; declarations may not overlap (each declaration must follow the sequence xyzw).</span></span> <span data-ttu-id="2f374-124">Quando si dichiarano valori di sistema scalari (ad esempio distanza di ritaglio e distanza di abbattimento), è possibile dichiarare più valori di sistema in un unico registro.</span><span class="sxs-lookup"><span data-stu-id="2f374-124">When declaring scalar system values (clip distance and cull distance for example), you can declare multiple system values in a single register.</span></span> <span data-ttu-id="2f374-125">In tal caso, assicurarsi che altri modificatori come le modalità di interpolazione corrispondano.</span><span class="sxs-lookup"><span data-stu-id="2f374-125">If you do so, make sure other modifiers like the interpolation modes match.</span></span>

<span data-ttu-id="2f374-126">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f374-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2f374-127">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="2f374-127">Vertex Shader</span></span> | <span data-ttu-id="2f374-128">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="2f374-128">Geometry Shader</span></span> | <span data-ttu-id="2f374-129">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="2f374-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2f374-130">x</span><span class="sxs-lookup"><span data-stu-id="2f374-130">x</span></span>             | <span data-ttu-id="2f374-131">x</span><span class="sxs-lookup"><span data-stu-id="2f374-131">x</span></span>               | <span data-ttu-id="2f374-132">x</span><span class="sxs-lookup"><span data-stu-id="2f374-132">x</span></span>            |



 

<span data-ttu-id="2f374-133">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="2f374-133">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="2f374-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="2f374-134">Example</span></span>

<span data-ttu-id="2f374-135">Ecco alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="2f374-135">Here are some examples:</span></span>


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a><span data-ttu-id="2f374-136">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2f374-136">Minimum Shader Model</span></span>

<span data-ttu-id="2f374-137">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f374-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2f374-138">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2f374-138">Shader Model</span></span>                                              | <span data-ttu-id="2f374-139">Supportato</span><span class="sxs-lookup"><span data-stu-id="2f374-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2f374-140">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2f374-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2f374-141">sì</span><span class="sxs-lookup"><span data-stu-id="2f374-141">yes</span></span>       |
| [<span data-ttu-id="2f374-142">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2f374-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2f374-143">sì</span><span class="sxs-lookup"><span data-stu-id="2f374-143">yes</span></span>       |
| [<span data-ttu-id="2f374-144">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2f374-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2f374-145">sì</span><span class="sxs-lookup"><span data-stu-id="2f374-145">yes</span></span>       |
| [<span data-ttu-id="2f374-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f374-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2f374-147">no</span><span class="sxs-lookup"><span data-stu-id="2f374-147">no</span></span>        |
| [<span data-ttu-id="2f374-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f374-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2f374-149">no</span><span class="sxs-lookup"><span data-stu-id="2f374-149">no</span></span>        |
| [<span data-ttu-id="2f374-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f374-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2f374-151">no</span><span class="sxs-lookup"><span data-stu-id="2f374-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2f374-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f374-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f374-153">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f374-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





