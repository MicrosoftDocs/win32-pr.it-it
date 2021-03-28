---
title: dcl_input vOutputControlPointID (SM5-ASM)
description: Dichiarare l'ID del punto di controllo dell'output in una fase del punto di controllo Hull shader.
ms.assetid: 376ECA4F-DD71-4466-8A9D-E92A536832BC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cee49a8a825f25b0fbbccff027d5ad1b9ade514
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046126"
---
# <a name="dcl_input-voutputcontrolpointid-sm5---asm"></a><span data-ttu-id="62037-103">\_vOutputControlPointID di input DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="62037-103">dcl\_input vOutputControlPointID (sm5 - asm)</span></span>

<span data-ttu-id="62037-104">Dichiarare l'ID del punto di controllo dell'output in una fase del punto di controllo Hull shader.</span><span class="sxs-lookup"><span data-stu-id="62037-104">Declare the output control point ID in a hull shader control point phase.</span></span>



| <span data-ttu-id="62037-105">\_vOutputControlPointID di input DCL</span><span class="sxs-lookup"><span data-stu-id="62037-105">dcl\_input vOutputControlPointID</span></span> |
|----------------------------------|



 



| <span data-ttu-id="62037-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="62037-106">Item</span></span>                                                                                                                                                       | <span data-ttu-id="62037-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62037-107">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="62037-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span><span class="sxs-lookup"><span data-stu-id="62037-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span></span><br/> | <span data-ttu-id="62037-109">\[nell' \] ID del punto di controllo dell'output.</span><span class="sxs-lookup"><span data-stu-id="62037-109">\[in\] The output control point ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62037-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="62037-110">Remarks</span></span>

<span data-ttu-id="62037-111">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="62037-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="62037-112">Vertice</span><span class="sxs-lookup"><span data-stu-id="62037-112">Vertex</span></span> | <span data-ttu-id="62037-113">Hull</span><span class="sxs-lookup"><span data-stu-id="62037-113">Hull</span></span> | <span data-ttu-id="62037-114">Dominio</span><span class="sxs-lookup"><span data-stu-id="62037-114">Domain</span></span> | <span data-ttu-id="62037-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="62037-115">Geometry</span></span> | <span data-ttu-id="62037-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="62037-116">Pixel</span></span> | <span data-ttu-id="62037-117">Calcolo</span><span class="sxs-lookup"><span data-stu-id="62037-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="62037-118">X</span><span class="sxs-lookup"><span data-stu-id="62037-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="62037-119">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="62037-119">Minimum Shader Model</span></span>

<span data-ttu-id="62037-120">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="62037-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="62037-121">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="62037-121">Shader Model</span></span>                                              | <span data-ttu-id="62037-122">Supportato</span><span class="sxs-lookup"><span data-stu-id="62037-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="62037-123">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="62037-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="62037-124">sì</span><span class="sxs-lookup"><span data-stu-id="62037-124">yes</span></span>       |
| [<span data-ttu-id="62037-125">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="62037-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="62037-126">no</span><span class="sxs-lookup"><span data-stu-id="62037-126">no</span></span>        |
| [<span data-ttu-id="62037-127">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="62037-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="62037-128">no</span><span class="sxs-lookup"><span data-stu-id="62037-128">no</span></span>        |
| [<span data-ttu-id="62037-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62037-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="62037-130">no</span><span class="sxs-lookup"><span data-stu-id="62037-130">no</span></span>        |
| [<span data-ttu-id="62037-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62037-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="62037-132">no</span><span class="sxs-lookup"><span data-stu-id="62037-132">no</span></span>        |
| [<span data-ttu-id="62037-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62037-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="62037-134">no</span><span class="sxs-lookup"><span data-stu-id="62037-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="62037-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62037-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62037-136">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62037-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





