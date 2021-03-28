---
title: dcl_input vThread (SM5-ASM)
description: Dichiarare gli ID di input compute shader.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719483"
---
# <a name="dcl_input-vthread-sm5---asm"></a><span data-ttu-id="1b55a-103">\_vThread di input DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1b55a-103">dcl\_input vThread (sm5 - asm)</span></span>

<span data-ttu-id="1b55a-104">Dichiarare gli ID di input compute shader.</span><span class="sxs-lookup"><span data-stu-id="1b55a-104">Declare compute shader input IDs.</span></span>



| <span data-ttu-id="1b55a-105">\_input DCL {vThreadID.XYZ </span><span class="sxs-lookup"><span data-stu-id="1b55a-105">dcl\_input {vThreadID.xyz</span></span>\|<span data-ttu-id="1b55a-106">vThreadGroupID.xyz </span><span class="sxs-lookup"><span data-stu-id="1b55a-106">vThreadGroupID.xyz</span></span>\| <span data-ttu-id="1b55a-107">vThreadIDInGroup.xyz </span><span class="sxs-lookup"><span data-stu-id="1b55a-107">vThreadIDInGroup.xyz</span></span>\|<span data-ttu-id="1b55a-108">vThreadIDInGroupFlattened}</span><span class="sxs-lookup"><span data-stu-id="1b55a-108">vThreadIDInGroupFlattened}</span></span> |
|--------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1b55a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b55a-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="1b55a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b55a-110">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1b55a-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span><span class="sxs-lookup"><span data-stu-id="1b55a-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span></span><br/> | <span data-ttu-id="1b55a-112">\[nel \] valore ID integer a 32 bit senza segno a 3 componenti.</span><span class="sxs-lookup"><span data-stu-id="1b55a-112">\[in\] The 3-component unsigned 32-bit integer ID value.</span></span><br/> |



 

<span data-ttu-id="1b55a-113">**l' \_ input di DCL** è una dichiarazione esistente in altre fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="1b55a-113">**dcl\_input** is an existing declaration in other shader stages.</span></span> <span data-ttu-id="1b55a-114">Viene usato in compute shader per dichiarare i vari valori ID integer a 32 bit senza segno a 3 componenti univoci per compute shader.</span><span class="sxs-lookup"><span data-stu-id="1b55a-114">It is used in the compute shader to declare the various 3-component unsigned 32-bit integer ID values unique to the compute shader.</span></span> <span data-ttu-id="1b55a-115">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="1b55a-115">They are:</span></span>

-   <span data-ttu-id="1b55a-116">vThreadID.xyz</span><span class="sxs-lookup"><span data-stu-id="1b55a-116">vThreadID.xyz</span></span>
-   <span data-ttu-id="1b55a-117">vGroupID.xyz</span><span class="sxs-lookup"><span data-stu-id="1b55a-117">vGroupID.xyz</span></span>
-   <span data-ttu-id="1b55a-118">vThreadIDInGroup.xyz</span><span class="sxs-lookup"><span data-stu-id="1b55a-118">vThreadIDInGroup.xyz</span></span>
-   <span data-ttu-id="1b55a-119">vThreadIDInGroupFlattened (componente singolo)</span><span class="sxs-lookup"><span data-stu-id="1b55a-119">vThreadIDInGroupFlattened (single component)</span></span>

<span data-ttu-id="1b55a-120">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b55a-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1b55a-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="1b55a-121">Vertex</span></span> | <span data-ttu-id="1b55a-122">Hull</span><span class="sxs-lookup"><span data-stu-id="1b55a-122">Hull</span></span> | <span data-ttu-id="1b55a-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="1b55a-123">Domain</span></span> | <span data-ttu-id="1b55a-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="1b55a-124">Geometry</span></span> | <span data-ttu-id="1b55a-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="1b55a-125">Pixel</span></span> | <span data-ttu-id="1b55a-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="1b55a-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="1b55a-127">X</span><span class="sxs-lookup"><span data-stu-id="1b55a-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1b55a-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="1b55a-128">Minimum Shader Model</span></span>

<span data-ttu-id="1b55a-129">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b55a-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1b55a-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="1b55a-130">Shader Model</span></span>                                              | <span data-ttu-id="1b55a-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="1b55a-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1b55a-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="1b55a-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1b55a-133">sì</span><span class="sxs-lookup"><span data-stu-id="1b55a-133">yes</span></span>       |
| [<span data-ttu-id="1b55a-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="1b55a-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1b55a-135">no</span><span class="sxs-lookup"><span data-stu-id="1b55a-135">no</span></span>        |
| [<span data-ttu-id="1b55a-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="1b55a-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1b55a-137">no</span><span class="sxs-lookup"><span data-stu-id="1b55a-137">no</span></span>        |
| [<span data-ttu-id="1b55a-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b55a-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1b55a-139">no</span><span class="sxs-lookup"><span data-stu-id="1b55a-139">no</span></span>        |
| [<span data-ttu-id="1b55a-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b55a-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1b55a-141">no</span><span class="sxs-lookup"><span data-stu-id="1b55a-141">no</span></span>        |
| [<span data-ttu-id="1b55a-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b55a-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1b55a-143">no</span><span class="sxs-lookup"><span data-stu-id="1b55a-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1b55a-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b55a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b55a-145">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b55a-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





