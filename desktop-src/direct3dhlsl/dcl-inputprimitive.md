---
title: dcl_inputPrimitive (SM4-ASM)
description: '\_inputPrimitive DCL (SM4-ASM)'
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 76c131b7c4225c0b30ad1183e4da1fe6c0561754
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956085"
---
# <a name="dcl_inputprimitive-sm4---asm"></a><span data-ttu-id="ccff2-103">\_inputPrimitive DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ccff2-103">dcl\_inputPrimitive (sm4 - asm)</span></span>

<span data-ttu-id="ccff2-104">Dichiara il tipo primitivo per gli input dello shader di geometria.</span><span class="sxs-lookup"><span data-stu-id="ccff2-104">Declares the primitive type for geometry-shader inputs.</span></span>



| <span data-ttu-id="ccff2-105">\_ *tipo* di inputPrimitive DCL</span><span class="sxs-lookup"><span data-stu-id="ccff2-105">dcl\_inputPrimitive *type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ccff2-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ccff2-106">Item</span></span></th>
<th><span data-ttu-id="ccff2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccff2-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ccff2-108"><span id="type"></span><span id="TYPE"></span><em>tipo</em></span><span class="sxs-lookup"><span data-stu-id="ccff2-108"><span id="type"></span><span id="TYPE"></span><em>type</em></span></span><br/></td>
<td><span data-ttu-id="ccff2-109">in Input: tipo primitivo di dati, che è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccff2-109">[in] Input-data primitive type, which is one of the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="ccff2-110"><em>punto</em> - di Elenco punti</span><span class="sxs-lookup"><span data-stu-id="ccff2-110"><em>point</em> - point list</span></span></li>
<li><span data-ttu-id="ccff2-111"><em>riga</em> - di elenco linee</span><span class="sxs-lookup"><span data-stu-id="ccff2-111"><em>line</em> - line list</span></span></li>
<li><span data-ttu-id="ccff2-112"><em>triangolo</em> - elenco di triangolo</span><span class="sxs-lookup"><span data-stu-id="ccff2-112"><em>triangle</em> - triangle list</span></span></li>
<li><span data-ttu-id="ccff2-113"><em>line_adj</em> - elenco linee con dati adiacenza</span><span class="sxs-lookup"><span data-stu-id="ccff2-113"><em>line_adj</em> - line list with adjacency data</span></span></li>
<li><span data-ttu-id="ccff2-114"><em>triangle_adj</em> - elenco di triangolo con dati adiacenza</span><span class="sxs-lookup"><span data-stu-id="ccff2-114"><em>triangle_adj</em> - triangle list with adjacency data</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ccff2-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccff2-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ccff2-116">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="ccff2-116">Vertex Shader</span></span> | <span data-ttu-id="ccff2-117">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="ccff2-117">Geometry Shader</span></span> | <span data-ttu-id="ccff2-118">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="ccff2-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="ccff2-119">x</span><span class="sxs-lookup"><span data-stu-id="ccff2-119">x</span></span>               |              |



 

<span data-ttu-id="ccff2-120">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="ccff2-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="ccff2-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="ccff2-121">Example</span></span>

<span data-ttu-id="ccff2-122">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="ccff2-122">Here is an example.</span></span>


```
dcl_inputPrimitive triangle
```



## <a name="minimum-shader-model"></a><span data-ttu-id="ccff2-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ccff2-123">Minimum Shader Model</span></span>

<span data-ttu-id="ccff2-124">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="ccff2-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ccff2-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ccff2-125">Shader Model</span></span>                                              | <span data-ttu-id="ccff2-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="ccff2-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ccff2-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="ccff2-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ccff2-128">sì</span><span class="sxs-lookup"><span data-stu-id="ccff2-128">yes</span></span>       |
| [<span data-ttu-id="ccff2-129">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="ccff2-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ccff2-130">sì</span><span class="sxs-lookup"><span data-stu-id="ccff2-130">yes</span></span>       |
| [<span data-ttu-id="ccff2-131">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="ccff2-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ccff2-132">sì</span><span class="sxs-lookup"><span data-stu-id="ccff2-132">yes</span></span>       |
| [<span data-ttu-id="ccff2-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccff2-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ccff2-134">no</span><span class="sxs-lookup"><span data-stu-id="ccff2-134">no</span></span>        |
| [<span data-ttu-id="ccff2-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccff2-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ccff2-136">no</span><span class="sxs-lookup"><span data-stu-id="ccff2-136">no</span></span>        |
| [<span data-ttu-id="ccff2-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccff2-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ccff2-138">no</span><span class="sxs-lookup"><span data-stu-id="ccff2-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ccff2-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ccff2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccff2-140">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccff2-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





