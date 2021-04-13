---
title: dcl_indexableTemp (SM4-ASM)
description: '\_indexableTemp DCL (SM4-ASM)'
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993240"
---
# <a name="dcl_indexabletemp-sm4---asm"></a><span data-ttu-id="428de-103">\_indexableTemp DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="428de-103">dcl\_indexableTemp (sm4 - asm)</span></span>

<span data-ttu-id="428de-104">Dichiara un registro temporaneo indicizzabile.</span><span class="sxs-lookup"><span data-stu-id="428de-104">Declares an indexable, temporary register.</span></span>



| <span data-ttu-id="428de-105">\_dimensioni indexableTemp di DCL x *N \[ \] , ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="428de-105">dcl\_indexableTemp x *N\[size\], ComponentCount*</span></span> |
|-------------------------------------------------|



 



| <span data-ttu-id="428de-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="428de-106">Item</span></span>                                                                                                                           | <span data-ttu-id="428de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="428de-107">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="428de-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="428de-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/>                                                                         | <span data-ttu-id="428de-109">\[in \] un Integer che indica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="428de-109">\[in\] An integer that denotes the register number.</span></span><br/>                              |
| <span data-ttu-id="428de-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[dimensioni\]*</span><span class="sxs-lookup"><span data-stu-id="428de-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[size\]*</span></span><br/>                                                        | <span data-ttu-id="428de-111">\[in \] un valore integer facoltativo.</span><span class="sxs-lookup"><span data-stu-id="428de-111">\[in\] An optional integer value.</span></span> <span data-ttu-id="428de-112">Numero di elementi nella matrice di registro.</span><span class="sxs-lookup"><span data-stu-id="428de-112">The number of elements in the register array.</span></span><br/>  |
| <span data-ttu-id="428de-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="428de-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span></span><br/> | <span data-ttu-id="428de-114">\[in \] un valore integer facoltativo. Numero di componenti nella matrice di registro.</span><span class="sxs-lookup"><span data-stu-id="428de-114">\[in\] An optional integer value.The number of components in the register array.</span></span><br/> |



 

<span data-ttu-id="428de-115">Un registro contiene spazio sufficiente per un valore a quattro componenti a 32 bit. il numero di elementi nella matrice di registri temporanei (indicizzabile e [non indicizzabile](dcl-temps.md)) non può essere maggiore di 4096.</span><span class="sxs-lookup"><span data-stu-id="428de-115">A register contains enough space for a 32-bit four-component value; the number of elements in the array of temporary registers (indexable and [non-indexable](dcl-temps.md)) cannot exceed 4096.</span></span>

<span data-ttu-id="428de-116">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="428de-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="428de-117">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="428de-117">Vertex Shader</span></span> | <span data-ttu-id="428de-118">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="428de-118">Geometry Shader</span></span> | <span data-ttu-id="428de-119">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="428de-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="428de-120">x</span><span class="sxs-lookup"><span data-stu-id="428de-120">x</span></span>             | <span data-ttu-id="428de-121">x</span><span class="sxs-lookup"><span data-stu-id="428de-121">x</span></span>               | <span data-ttu-id="428de-122">x</span><span class="sxs-lookup"><span data-stu-id="428de-122">x</span></span>            |



 

<span data-ttu-id="428de-123">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="428de-123">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="428de-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="428de-124">Example</span></span>

<span data-ttu-id="428de-125">Di seguito sono riportati alcuni esempi del codice generato per i registri indicizzabili.</span><span class="sxs-lookup"><span data-stu-id="428de-125">Here are some examples of the code generated for indexable registers.</span></span>


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a><span data-ttu-id="428de-126">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="428de-126">Minimum Shader Model</span></span>

<span data-ttu-id="428de-127">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="428de-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="428de-128">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="428de-128">Shader Model</span></span>                                              | <span data-ttu-id="428de-129">Supportato</span><span class="sxs-lookup"><span data-stu-id="428de-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="428de-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="428de-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="428de-131">sì</span><span class="sxs-lookup"><span data-stu-id="428de-131">yes</span></span>       |
| [<span data-ttu-id="428de-132">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="428de-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="428de-133">sì</span><span class="sxs-lookup"><span data-stu-id="428de-133">yes</span></span>       |
| [<span data-ttu-id="428de-134">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="428de-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="428de-135">sì</span><span class="sxs-lookup"><span data-stu-id="428de-135">yes</span></span>       |
| [<span data-ttu-id="428de-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="428de-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="428de-137">no</span><span class="sxs-lookup"><span data-stu-id="428de-137">no</span></span>        |
| [<span data-ttu-id="428de-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="428de-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="428de-139">no</span><span class="sxs-lookup"><span data-stu-id="428de-139">no</span></span>        |
| [<span data-ttu-id="428de-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="428de-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="428de-141">no</span><span class="sxs-lookup"><span data-stu-id="428de-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="428de-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="428de-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="428de-143">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="428de-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





