---
title: dcl_constantBuffer (SM4-ASM)
description: '\_constantBuffer DCL (SM4-ASM)'
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117209"
---
# <a name="dcl_constantbuffer-sm4---asm"></a><span data-ttu-id="caa60-103">\_constantBuffer DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="caa60-103">dcl\_constantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="caa60-104">Dichiara un buffer costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="caa60-104">Declares a shader constant buffer.</span></span>



| <span data-ttu-id="caa60-105">\_ *\[ dimensioni \] cbN* constantBuffer di DCL, *AccessPattern*</span><span class="sxs-lookup"><span data-stu-id="caa60-105">dcl\_constantBuffer *cbN\[size\]*, *AccessPattern*</span></span> |
|----------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="caa60-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="caa60-106">Item</span></span></th>
<th><span data-ttu-id="caa60-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caa60-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="caa60-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [dimensioni]</em></span><span class="sxs-lookup"><span data-stu-id="caa60-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N[size]</em></span></span><br/></td>
<td><span data-ttu-id="caa60-109">in Buffer costante dello shader dove N è un numero intero che denota il numero di registro constant-buffer e size è un numero intero che indica il numero di elementi nel buffer.</span><span class="sxs-lookup"><span data-stu-id="caa60-109">[in] A shader constant buffer where N is an integer that denotes the constant-buffer-register number and size is an integer that denotes the number of elements in the buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caa60-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span><span class="sxs-lookup"><span data-stu-id="caa60-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span></span><br/></td>
<td><span data-ttu-id="caa60-111">in Il modo in cui il buffer sarà accessibile dal codice dello shader, che è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="caa60-111">[in] The way that the buffer will be accessed by shader code, which is one of the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="caa60-112">Nome</span><span class="sxs-lookup"><span data-stu-id="caa60-112">Name</span></span></th>
<th><span data-ttu-id="caa60-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caa60-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="caa60-114">immediateIndexed</span><span class="sxs-lookup"><span data-stu-id="caa60-114">immediateIndexed</span></span></td>
<td><span data-ttu-id="caa60-115">Indicizzare il buffer con un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="caa60-115">Index the buffer with a literal value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caa60-116">dynamic_indexed</span><span class="sxs-lookup"><span data-stu-id="caa60-116">dynamic_indexed</span></span></td>
<td><span data-ttu-id="caa60-117">Indicizzare il buffer con il risultato di un'espressione valutata.</span><span class="sxs-lookup"><span data-stu-id="caa60-117">Index the buffer with the result of an evaluated expression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="caa60-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="caa60-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="caa60-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="caa60-119">Vertex Shader</span></span> | <span data-ttu-id="caa60-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="caa60-120">Geometry Shader</span></span> | <span data-ttu-id="caa60-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="caa60-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="caa60-122">x</span><span class="sxs-lookup"><span data-stu-id="caa60-122">x</span></span>             | <span data-ttu-id="caa60-123">x</span><span class="sxs-lookup"><span data-stu-id="caa60-123">x</span></span>               | <span data-ttu-id="caa60-124">x</span><span class="sxs-lookup"><span data-stu-id="caa60-124">x</span></span>            |



 

<span data-ttu-id="caa60-125">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="caa60-125">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="caa60-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="caa60-126">Example</span></span>

<span data-ttu-id="caa60-127">Questo esempio dichiara un buffer costante per Register CB0, che include 19 elementi.</span><span class="sxs-lookup"><span data-stu-id="caa60-127">This example declares a constant buffer for register cb0, which has 19 elements.</span></span> <span data-ttu-id="caa60-128">Questi elementi sono accessibili con un indice letterale.</span><span class="sxs-lookup"><span data-stu-id="caa60-128">These elements are accessed with a literal index.</span></span>


```
dcl_constantbuffer  cb0[19], immediateIndexed
```



## <a name="minimum-shader-model"></a><span data-ttu-id="caa60-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="caa60-129">Minimum Shader Model</span></span>

<span data-ttu-id="caa60-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="caa60-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="caa60-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="caa60-131">Shader Model</span></span>                                              | <span data-ttu-id="caa60-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="caa60-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="caa60-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="caa60-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="caa60-134">sì</span><span class="sxs-lookup"><span data-stu-id="caa60-134">yes</span></span>       |
| [<span data-ttu-id="caa60-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="caa60-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="caa60-136">sì</span><span class="sxs-lookup"><span data-stu-id="caa60-136">yes</span></span>       |
| [<span data-ttu-id="caa60-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="caa60-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="caa60-138">sì</span><span class="sxs-lookup"><span data-stu-id="caa60-138">yes</span></span>       |
| [<span data-ttu-id="caa60-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="caa60-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="caa60-140">no</span><span class="sxs-lookup"><span data-stu-id="caa60-140">no</span></span>        |
| [<span data-ttu-id="caa60-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="caa60-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="caa60-142">no</span><span class="sxs-lookup"><span data-stu-id="caa60-142">no</span></span>        |
| [<span data-ttu-id="caa60-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="caa60-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="caa60-144">no</span><span class="sxs-lookup"><span data-stu-id="caa60-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="caa60-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="caa60-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caa60-146">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="caa60-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





