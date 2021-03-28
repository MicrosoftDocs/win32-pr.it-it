---
title: dcl_input vForkInstanceID (SM5-ASM)
description: Dichiarare l'ID istanza in una fase fork dello shader Hull.
ms.assetid: AA73E8B6-C6D7-4483-B46E-C733341F552C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ce5fcf111a59abb0c9a6ccb36de63d94dcb11e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046127"
---
# <a name="dcl_input-vforkinstanceid-sm5---asm"></a><span data-ttu-id="7654c-103">\_vForkInstanceID di input DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7654c-103">dcl\_input vForkInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="7654c-104">Dichiarare l'ID istanza in una fase fork dello shader Hull.</span><span class="sxs-lookup"><span data-stu-id="7654c-104">Declare the instance ID in a hull shader fork phase.</span></span>



| <span data-ttu-id="7654c-105">\_vForkInstanceID di input DCL</span><span class="sxs-lookup"><span data-stu-id="7654c-105">dcl\_input vForkInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="7654c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7654c-106">Item</span></span>                                                                                                                               | <span data-ttu-id="7654c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7654c-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="7654c-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span><span class="sxs-lookup"><span data-stu-id="7654c-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span></span><br/> | <span data-ttu-id="7654c-109">\[nell' \] ID istanza.</span><span class="sxs-lookup"><span data-stu-id="7654c-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7654c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7654c-110">Remarks</span></span>

<span data-ttu-id="7654c-111">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7654c-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7654c-112">Vertice</span><span class="sxs-lookup"><span data-stu-id="7654c-112">Vertex</span></span> | <span data-ttu-id="7654c-113">Hull</span><span class="sxs-lookup"><span data-stu-id="7654c-113">Hull</span></span> | <span data-ttu-id="7654c-114">Dominio</span><span class="sxs-lookup"><span data-stu-id="7654c-114">Domain</span></span> | <span data-ttu-id="7654c-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="7654c-115">Geometry</span></span> | <span data-ttu-id="7654c-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="7654c-116">Pixel</span></span> | <span data-ttu-id="7654c-117">Calcolo</span><span class="sxs-lookup"><span data-stu-id="7654c-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7654c-118">X</span><span class="sxs-lookup"><span data-stu-id="7654c-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7654c-119">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="7654c-119">Minimum Shader Model</span></span>

<span data-ttu-id="7654c-120">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7654c-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7654c-121">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7654c-121">Shader Model</span></span>                                              | <span data-ttu-id="7654c-122">Supportato</span><span class="sxs-lookup"><span data-stu-id="7654c-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7654c-123">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7654c-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7654c-124">sì</span><span class="sxs-lookup"><span data-stu-id="7654c-124">yes</span></span>       |
| [<span data-ttu-id="7654c-125">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="7654c-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7654c-126">no</span><span class="sxs-lookup"><span data-stu-id="7654c-126">no</span></span>        |
| [<span data-ttu-id="7654c-127">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="7654c-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7654c-128">no</span><span class="sxs-lookup"><span data-stu-id="7654c-128">no</span></span>        |
| [<span data-ttu-id="7654c-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7654c-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7654c-130">no</span><span class="sxs-lookup"><span data-stu-id="7654c-130">no</span></span>        |
| [<span data-ttu-id="7654c-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7654c-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7654c-132">no</span><span class="sxs-lookup"><span data-stu-id="7654c-132">no</span></span>        |
| [<span data-ttu-id="7654c-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7654c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7654c-134">no</span><span class="sxs-lookup"><span data-stu-id="7654c-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7654c-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7654c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7654c-136">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7654c-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





