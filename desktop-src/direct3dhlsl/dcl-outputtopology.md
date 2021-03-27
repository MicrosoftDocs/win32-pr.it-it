---
title: dcl_outputTopology (SM4-ASM)
description: '\_outputTopology DCL (SM4-ASM)'
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3b305d195ca09a1ef95c99624b47a50058021ca
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719474"
---
# <a name="dcl_outputtopology-sm4---asm"></a><span data-ttu-id="f01c1-103">\_outputTopology DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f01c1-103">dcl\_outputTopology (sm4 - asm)</span></span>

<span data-ttu-id="f01c1-104">Dichiara i dati di output del tipo primitivo geometry-shader.</span><span class="sxs-lookup"><span data-stu-id="f01c1-104">Declares the primitive type geometry-shader output data.</span></span>



| <span data-ttu-id="f01c1-105">\_ *tipo* di outputTopology DCL</span><span class="sxs-lookup"><span data-stu-id="f01c1-105">dcl\_outputTopology *Type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f01c1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f01c1-106">Item</span></span></th>
<th><span data-ttu-id="f01c1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f01c1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f01c1-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Tipo</em></span><span class="sxs-lookup"><span data-stu-id="f01c1-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span><br/></td>
<td><span data-ttu-id="f01c1-109">in Una topologia primitiva di output, che è uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f01c1-109">[in] An output primitive topology, which is one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="f01c1-110"><em>pointList</em></span><span class="sxs-lookup"><span data-stu-id="f01c1-110"><em>pointlist</em></span></span></li>
<li><span data-ttu-id="f01c1-111"><em>linestrip</em></span><span class="sxs-lookup"><span data-stu-id="f01c1-111"><em>linestrip</em></span></span></li>
<li><span data-ttu-id="f01c1-112"><em>trianglestrip</em></span><span class="sxs-lookup"><span data-stu-id="f01c1-112"><em>trianglestrip</em></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f01c1-113">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f01c1-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f01c1-114">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="f01c1-114">Vertex Shader</span></span> | <span data-ttu-id="f01c1-115">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="f01c1-115">Geometry Shader</span></span> | <span data-ttu-id="f01c1-116">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="f01c1-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="f01c1-117">x</span><span class="sxs-lookup"><span data-stu-id="f01c1-117">x</span></span>               |              |



 

<span data-ttu-id="f01c1-118">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="f01c1-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="f01c1-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="f01c1-119">Example</span></span>

<span data-ttu-id="f01c1-120">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="f01c1-120">Here is an example.</span></span>


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a><span data-ttu-id="f01c1-121">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f01c1-121">Minimum Shader Model</span></span>

<span data-ttu-id="f01c1-122">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f01c1-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f01c1-123">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f01c1-123">Shader Model</span></span>                                              | <span data-ttu-id="f01c1-124">Supportato</span><span class="sxs-lookup"><span data-stu-id="f01c1-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f01c1-125">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f01c1-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f01c1-126">sì</span><span class="sxs-lookup"><span data-stu-id="f01c1-126">yes</span></span>       |
| [<span data-ttu-id="f01c1-127">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="f01c1-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f01c1-128">sì</span><span class="sxs-lookup"><span data-stu-id="f01c1-128">yes</span></span>       |
| [<span data-ttu-id="f01c1-129">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="f01c1-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f01c1-130">sì</span><span class="sxs-lookup"><span data-stu-id="f01c1-130">yes</span></span>       |
| [<span data-ttu-id="f01c1-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f01c1-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f01c1-132">no</span><span class="sxs-lookup"><span data-stu-id="f01c1-132">no</span></span>        |
| [<span data-ttu-id="f01c1-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f01c1-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f01c1-134">no</span><span class="sxs-lookup"><span data-stu-id="f01c1-134">no</span></span>        |
| [<span data-ttu-id="f01c1-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f01c1-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f01c1-136">no</span><span class="sxs-lookup"><span data-stu-id="f01c1-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f01c1-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f01c1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f01c1-138">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f01c1-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





