---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Dichiarare il partizionamento mosaico in una sezione di dichiarazione Hull shader.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398294"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a><span data-ttu-id="82e8a-103">\_ \_ partizionamento mosaico DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="82e8a-103">dcl\_tessellator\_partitioning (sm5 - asm)</span></span>

<span data-ttu-id="82e8a-104">Dichiarare il partizionamento mosaico in una sezione di dichiarazione Hull shader.</span><span class="sxs-lookup"><span data-stu-id="82e8a-104">Declare the tessellator partitioning in a hull shader declaration section.</span></span>



| <span data-ttu-id="82e8a-105">\_partizionamento di mosaico di DCL \_ {Integer di partizionamento \_ </span><span class="sxs-lookup"><span data-stu-id="82e8a-105">dcl\_tessellator\_partitioning {partitioning\_integer</span></span>\| <span data-ttu-id="82e8a-106">partizionamento \_ pow2 </span><span class="sxs-lookup"><span data-stu-id="82e8a-106">partitioning\_pow2</span></span>\|<span data-ttu-id="82e8a-107">suddivisione \_ frazionaria \_ dispari </span><span class="sxs-lookup"><span data-stu-id="82e8a-107">partitioning\_fractional\_odd</span></span>\| <span data-ttu-id="82e8a-108">partizionamento \_ frazionario \_ pari}</span><span class="sxs-lookup"><span data-stu-id="82e8a-108">partitioning\_fractional\_even}</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="82e8a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="82e8a-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="82e8a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82e8a-110">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="82e8a-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partizionamento di partizionamento Integer partizionamento del partizionamento del partizionamento \_ \| \_ pow2 \| \_ \_ \| \_ frazionario pari \_*</span><span class="sxs-lookup"><span data-stu-id="82e8a-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitioning\_integer\| partitioning\_pow2\|partitioning\_fractional\_odd\| partitioning\_fractional\_even*</span></span><br/> | <span data-ttu-id="82e8a-112">\[nel \] partizionamento mosaico.</span><span class="sxs-lookup"><span data-stu-id="82e8a-112">\[in\] The tessellator partitioning.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="82e8a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="82e8a-113">Remarks</span></span>

<span data-ttu-id="82e8a-114">Dal punto di vista dell'hardware, \_ pow2 si comporta esattamente come \_ Integer.</span><span class="sxs-lookup"><span data-stu-id="82e8a-114">From the hardware point of view, \_pow2 behaves just like \_integer.</span></span> <span data-ttu-id="82e8a-115">Spetta all'autore dello shader HLSL e/o compilercode a arrotondare TessFactors a potenze di 2.</span><span class="sxs-lookup"><span data-stu-id="82e8a-115">It is up to the HLSL shader author and/or compilercode to round TessFactors to powers of 2.</span></span>

<span data-ttu-id="82e8a-116">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="82e8a-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="82e8a-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="82e8a-117">Vertex</span></span> | <span data-ttu-id="82e8a-118">Hull</span><span class="sxs-lookup"><span data-stu-id="82e8a-118">Hull</span></span>                 | <span data-ttu-id="82e8a-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="82e8a-119">Domain</span></span> | <span data-ttu-id="82e8a-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="82e8a-120">Geometry</span></span> | <span data-ttu-id="82e8a-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="82e8a-121">Pixel</span></span> | <span data-ttu-id="82e8a-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="82e8a-122">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="82e8a-123">Sezione delle dichiarazioni</span><span class="sxs-lookup"><span data-stu-id="82e8a-123">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="82e8a-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="82e8a-124">Minimum Shader Model</span></span>

<span data-ttu-id="82e8a-125">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="82e8a-125">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="82e8a-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="82e8a-126">Shader Model</span></span>                                              | <span data-ttu-id="82e8a-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="82e8a-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="82e8a-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="82e8a-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="82e8a-129">sì</span><span class="sxs-lookup"><span data-stu-id="82e8a-129">yes</span></span>       |
| [<span data-ttu-id="82e8a-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="82e8a-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="82e8a-131">no</span><span class="sxs-lookup"><span data-stu-id="82e8a-131">no</span></span>        |
| [<span data-ttu-id="82e8a-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="82e8a-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="82e8a-133">no</span><span class="sxs-lookup"><span data-stu-id="82e8a-133">no</span></span>        |
| [<span data-ttu-id="82e8a-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82e8a-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="82e8a-135">no</span><span class="sxs-lookup"><span data-stu-id="82e8a-135">no</span></span>        |
| [<span data-ttu-id="82e8a-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82e8a-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="82e8a-137">no</span><span class="sxs-lookup"><span data-stu-id="82e8a-137">no</span></span>        |
| [<span data-ttu-id="82e8a-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82e8a-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="82e8a-139">no</span><span class="sxs-lookup"><span data-stu-id="82e8a-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="82e8a-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82e8a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e8a-141">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82e8a-141">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





