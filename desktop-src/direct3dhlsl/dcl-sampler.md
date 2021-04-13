---
title: dcl_sampler (SM4-ASM)
description: '\_campionatore DCL (SM4-ASM)'
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104399823"
---
# <a name="dcl_sampler-sm4---asm"></a><span data-ttu-id="a14b6-103">\_campionatore DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a14b6-103">dcl\_sampler (sm4 - asm)</span></span>

<span data-ttu-id="a14b6-104">Dichiara un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="a14b6-104">Declares a sampler register.</span></span>



| <span data-ttu-id="a14b6-105">\_sn campionatore DCL, modalità</span><span class="sxs-lookup"><span data-stu-id="a14b6-105">dcl\_sampler sN, mode</span></span> |
|-----------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a14b6-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a14b6-106">Item</span></span></th>
<th><span data-ttu-id="a14b6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a14b6-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a14b6-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span><span class="sxs-lookup"><span data-stu-id="a14b6-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span></span><br/></td>
<td><span data-ttu-id="a14b6-109">in Un registro campionatore, dove <em>N</em> è un numero intero che indica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="a14b6-109">[in] A sampler register, where <em>N</em> is an integer that denotes the register number.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14b6-110"><span id="mode"></span><span id="MODE"></span><em>modalità</em></span><span class="sxs-lookup"><span data-stu-id="a14b6-110"><span id="mode"></span><span id="MODE"></span><em>mode</em></span></span><br/></td>
<td><span data-ttu-id="a14b6-111">in Modalità campionatore, che vincola gli Stati del campionatore (elencati nei membri di <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) rispettati.</span><span class="sxs-lookup"><span data-stu-id="a14b6-111">[in] A sampler mode, which constrains which sampler states (listed in the members of <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) are honored.</span></span> <span data-ttu-id="a14b6-112">Le modalità e gli Stati sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a14b6-112">The modes and states are listed in the following table.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a14b6-113">Modalità</span><span class="sxs-lookup"><span data-stu-id="a14b6-113">Mode</span></span></th>
<th><span data-ttu-id="a14b6-114">Stati campionatore rispettati</span><span class="sxs-lookup"><span data-stu-id="a14b6-114">Sampler States Honored</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a14b6-115">default</span><span class="sxs-lookup"><span data-stu-id="a14b6-115">default</span></span></td>
<td><span data-ttu-id="a14b6-116"><em>Filter</em> (non può usare i valori _COMPARISON o _TEXT), <em>Addresse/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="a14b6-116"><em>Filter</em> (may not use the _COMPARISON or _TEXT values), <em>AddressU/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14b6-117">confronto</span><span class="sxs-lookup"><span data-stu-id="a14b6-117">comparison</span></span></td>
<td><span data-ttu-id="a14b6-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressList/V/W</em>, <em>MinLOD, MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="a14b6-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD,MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a14b6-119">mono</span><span class="sxs-lookup"><span data-stu-id="a14b6-119">mono</span></span></td>
<td><span data-ttu-id="a14b6-120"><em>Filter</em> (deve essere uno dei valori _TEXT), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (questi due Stati sono lo stato globale del dispositivo), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span><span class="sxs-lookup"><span data-stu-id="a14b6-120"><em>Filter</em> (must be one of the _TEXT values), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (these two states are global device state), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a14b6-121">La modalità limita le istruzioni di esempio che è possibile utilizzare. Questa tabella elenca i metodi dell'oggetto texture supportati per ogni modalità.</span><span class="sxs-lookup"><span data-stu-id="a14b6-121">The mode restricts the sample instructions that can be used; this table lists the texture-object methods that are supported for each mode.</span></span>



| <span data-ttu-id="a14b6-122">Campionatore che opera in questa modalità</span><span class="sxs-lookup"><span data-stu-id="a14b6-122">A Sampler Operating in this Mode</span></span> | <span data-ttu-id="a14b6-123">Può usare questi metodi di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a14b6-123">Can Use these Texture-Object Methods</span></span>                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14b6-124">default</span><span class="sxs-lookup"><span data-stu-id="a14b6-124">default</span></span>                          | <span data-ttu-id="a14b6-125">[Esempio](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span><span class="sxs-lookup"><span data-stu-id="a14b6-125">[Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span></span> |
| <span data-ttu-id="a14b6-126">confronto</span><span class="sxs-lookup"><span data-stu-id="a14b6-126">comparison</span></span>                       | <span data-ttu-id="a14b6-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span><span class="sxs-lookup"><span data-stu-id="a14b6-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span></span>                               |
| <span data-ttu-id="a14b6-128">mono</span><span class="sxs-lookup"><span data-stu-id="a14b6-128">mono</span></span>                             | [<span data-ttu-id="a14b6-129">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="a14b6-129">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

<span data-ttu-id="a14b6-130">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a14b6-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a14b6-131">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="a14b6-131">Vertex Shader</span></span> | <span data-ttu-id="a14b6-132">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="a14b6-132">Geometry Shader</span></span> | <span data-ttu-id="a14b6-133">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="a14b6-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a14b6-134">x</span><span class="sxs-lookup"><span data-stu-id="a14b6-134">x</span></span>             | <span data-ttu-id="a14b6-135">x</span><span class="sxs-lookup"><span data-stu-id="a14b6-135">x</span></span>               | <span data-ttu-id="a14b6-136">x\*</span><span class="sxs-lookup"><span data-stu-id="a14b6-136">x\*</span></span>          |



 

<span data-ttu-id="a14b6-137">\* -L'uso di un campionatore in modalità mono è supportato solo in un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="a14b6-137">\* - Using a sampler in mono mode is supported only in a pixel shader.</span></span>

<span data-ttu-id="a14b6-138">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="a14b6-138">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="a14b6-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="a14b6-139">Example</span></span>

<span data-ttu-id="a14b6-140">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="a14b6-140">Here is an example.</span></span>


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a><span data-ttu-id="a14b6-141">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a14b6-141">Minimum Shader Model</span></span>

<span data-ttu-id="a14b6-142">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a14b6-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a14b6-143">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a14b6-143">Shader Model</span></span>                                              | <span data-ttu-id="a14b6-144">Supportato</span><span class="sxs-lookup"><span data-stu-id="a14b6-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a14b6-145">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a14b6-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a14b6-146">sì</span><span class="sxs-lookup"><span data-stu-id="a14b6-146">yes</span></span>       |
| [<span data-ttu-id="a14b6-147">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="a14b6-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a14b6-148">sì</span><span class="sxs-lookup"><span data-stu-id="a14b6-148">yes</span></span>       |
| [<span data-ttu-id="a14b6-149">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a14b6-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a14b6-150">sì</span><span class="sxs-lookup"><span data-stu-id="a14b6-150">yes</span></span>       |
| [<span data-ttu-id="a14b6-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a14b6-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a14b6-152">no</span><span class="sxs-lookup"><span data-stu-id="a14b6-152">no</span></span>        |
| [<span data-ttu-id="a14b6-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a14b6-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a14b6-154">no</span><span class="sxs-lookup"><span data-stu-id="a14b6-154">no</span></span>        |
| [<span data-ttu-id="a14b6-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a14b6-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a14b6-156">no</span><span class="sxs-lookup"><span data-stu-id="a14b6-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a14b6-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a14b6-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a14b6-158">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a14b6-158">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

