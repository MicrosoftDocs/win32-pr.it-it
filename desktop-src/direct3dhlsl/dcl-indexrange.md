---
title: dcl_indexRange (SM4-ASM)
description: '\_indexRange DCL (SM4-ASM)'
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976498"
---
# <a name="dcl_indexrange-sm4---asm"></a><span data-ttu-id="dd444-103">\_indexRange DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="dd444-103">dcl\_indexRange (sm4 - asm)</span></span>

<span data-ttu-id="dd444-104">Dichiara un intervallo di registri a cui sarà possibile accedere dall'indice (un Integer calcolato nello shader).</span><span class="sxs-lookup"><span data-stu-id="dd444-104">Declares a range of registers that will be accessed by index (an integer computed in the shader).</span></span>



| <span data-ttu-id="dd444-105">DCL \_ IndexRange *minRegisterM*, *maxRegisterN*</span><span class="sxs-lookup"><span data-stu-id="dd444-105">dcl\_indexRange *minRegisterM*, *maxRegisterN*</span></span> |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd444-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="dd444-106">Item</span></span></th>
<th><span data-ttu-id="dd444-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd444-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd444-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span><span class="sxs-lookup"><span data-stu-id="dd444-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span></span><br/></td>
<td><span data-ttu-id="dd444-109">in Primo registro a cui accedere in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="dd444-109">[in] The first register to access by index.</span></span> <br/>
<ul>
<li><span data-ttu-id="dd444-110"><em>minRegister</em> è <strong>v</strong> per un vertice o pixel shader registro di input oppure <strong>o</strong> per un registro di output del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="dd444-110"><em>minRegister</em> is either <strong>v</strong> for a vertex or pixel shader input register, or <strong>o</strong> for a vertex shader output register.</span></span></li>
<li><span data-ttu-id="dd444-111"><em>M</em> è un numero intero che indica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="dd444-111"><em>M</em> is an integer that denotes the register number.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd444-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span><span class="sxs-lookup"><span data-stu-id="dd444-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span></span><br/></td>
<td><span data-ttu-id="dd444-113">in Ultimo registro a cui accedere in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="dd444-113">[in] The last register to access by index.</span></span> <span data-ttu-id="dd444-114">Lo stesso formato di <em>minRegister</em> ad eccezione di <em>N</em> è il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="dd444-114">Same form as <em>minRegister</em> except <em>N</em> is the register number.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="dd444-115">A tutti i registri si applicano le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd444-115">The following restrictions apply to all registers:</span></span>

-   <span data-ttu-id="dd444-116">I registri min e Max devono essere dello stesso tipo e avere le stesse maschere dei componenti (se le maschere sono dichiarate).</span><span class="sxs-lookup"><span data-stu-id="dd444-116">The min and max registers must be the same type and have the same component masks (if masks are declared).</span></span>
-   <span data-ttu-id="dd444-117">Un registro può avere più intervalli di indice, purché non si sovrappongano.</span><span class="sxs-lookup"><span data-stu-id="dd444-117">A register may have multiple index ranges, as long as they do no not overlap.</span></span>
-   <span data-ttu-id="dd444-118">Il numero di registro minimo deve essere minore del numero massimo di registro.</span><span class="sxs-lookup"><span data-stu-id="dd444-118">The min register number must be less than the max register number.</span></span>
-   <span data-ttu-id="dd444-119">Un registro di indice non può contenere un [valore di sistema](dx-graphics-hlsl-semantics.md).</span><span class="sxs-lookup"><span data-stu-id="dd444-119">An index register cannot contain a [system-value](dx-graphics-hlsl-semantics.md).</span></span>
-   <span data-ttu-id="dd444-120">L'indicizzazione di un registro al di fuori della dichiarazione di indice max produce risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="dd444-120">Indexing a register outside of the max index declaration produces undefined results.</span></span>

<span data-ttu-id="dd444-121">I registri di input dei pixel shader devono usare la stessa modalità di interpolazione; i registri di output pixel shader non sono indicizzabili.</span><span class="sxs-lookup"><span data-stu-id="dd444-121">Pixel shader input registers must use the same interpolation mode; pixel shader output registers are not indexable.</span></span>

<span data-ttu-id="dd444-122">Un registro di input geometry shader è costituito da due dimensioni (asse del vertice, asse degli attributi); l'intervallo di indici si applica solo all'asse degli attributi perché l'asse dei vertici è sempre completamente indicizzabile.</span><span class="sxs-lookup"><span data-stu-id="dd444-122">A geometry shader input register has two dimensions (vertex axis, attribute axis); the index range applies only to the attribute axis because the vertex axis is always fully indexable.</span></span>

<span data-ttu-id="dd444-123">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd444-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dd444-124">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="dd444-124">Vertex Shader</span></span> | <span data-ttu-id="dd444-125">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="dd444-125">Geometry Shader</span></span> | <span data-ttu-id="dd444-126">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="dd444-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dd444-127">x</span><span class="sxs-lookup"><span data-stu-id="dd444-127">x</span></span>             | <span data-ttu-id="dd444-128">x</span><span class="sxs-lookup"><span data-stu-id="dd444-128">x</span></span>               | <span data-ttu-id="dd444-129">x</span><span class="sxs-lookup"><span data-stu-id="dd444-129">x</span></span>            |



 

<span data-ttu-id="dd444-130">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="dd444-130">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="dd444-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="dd444-131">Example</span></span>

<span data-ttu-id="dd444-132">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="dd444-132">Here is an example.</span></span>


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="dd444-133">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="dd444-133">Minimum Shader Model</span></span>

<span data-ttu-id="dd444-134">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="dd444-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dd444-135">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="dd444-135">Shader Model</span></span>                                              | <span data-ttu-id="dd444-136">Supportato</span><span class="sxs-lookup"><span data-stu-id="dd444-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dd444-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="dd444-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dd444-138">sì</span><span class="sxs-lookup"><span data-stu-id="dd444-138">yes</span></span>       |
| [<span data-ttu-id="dd444-139">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="dd444-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dd444-140">sì</span><span class="sxs-lookup"><span data-stu-id="dd444-140">yes</span></span>       |
| [<span data-ttu-id="dd444-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="dd444-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dd444-142">sì</span><span class="sxs-lookup"><span data-stu-id="dd444-142">yes</span></span>       |
| [<span data-ttu-id="dd444-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd444-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dd444-144">no</span><span class="sxs-lookup"><span data-stu-id="dd444-144">no</span></span>        |
| [<span data-ttu-id="dd444-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd444-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dd444-146">no</span><span class="sxs-lookup"><span data-stu-id="dd444-146">no</span></span>        |
| [<span data-ttu-id="dd444-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd444-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dd444-148">no</span><span class="sxs-lookup"><span data-stu-id="dd444-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dd444-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd444-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd444-150">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd444-150">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





