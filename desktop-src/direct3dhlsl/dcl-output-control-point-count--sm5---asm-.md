---
title: dcl_output_control_point_count (SM5-ASM)
description: Dichiara il conteggio dei punti di controllo dell'output di Hull shader.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046124"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a><span data-ttu-id="3fae8-103">\_ \_ \_ conteggio punti di controllo output DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3fae8-103">dcl\_output\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="3fae8-104">Dichiara il conteggio dei punti di controllo dell'output di Hull shader.</span><span class="sxs-lookup"><span data-stu-id="3fae8-104">Declares the hull shader output control point count.</span></span>



| <span data-ttu-id="3fae8-105">\_ \_ conteggio punti di controllo output DCL \_ \_ N</span><span class="sxs-lookup"><span data-stu-id="3fae8-105">dcl\_output\_control\_point\_count N</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="3fae8-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fae8-106">Item</span></span>                                                   | <span data-ttu-id="3fae8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fae8-107">Description</span></span>                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fae8-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="3fae8-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="3fae8-109">\[in \] un valore intero compreso tra 0 e 32 che specifica il conteggio dei punti di controllo di output.</span><span class="sxs-lookup"><span data-stu-id="3fae8-109">\[in\] An integer value from 0 to 32 that specifies the output control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3fae8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fae8-110">Remarks</span></span>

<span data-ttu-id="3fae8-111">Se non sono necessari, Hull shader può restituire 0 punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="3fae8-111">The hull shader can output 0 control points if they are not needed.</span></span>

<span data-ttu-id="3fae8-112">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fae8-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3fae8-113">Vertice</span><span class="sxs-lookup"><span data-stu-id="3fae8-113">Vertex</span></span> | <span data-ttu-id="3fae8-114">Hull</span><span class="sxs-lookup"><span data-stu-id="3fae8-114">Hull</span></span>                 | <span data-ttu-id="3fae8-115">Dominio</span><span class="sxs-lookup"><span data-stu-id="3fae8-115">Domain</span></span> | <span data-ttu-id="3fae8-116">Geometria</span><span class="sxs-lookup"><span data-stu-id="3fae8-116">Geometry</span></span> | <span data-ttu-id="3fae8-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="3fae8-117">Pixel</span></span> | <span data-ttu-id="3fae8-118">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3fae8-118">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="3fae8-119">Sezione delle dichiarazioni</span><span class="sxs-lookup"><span data-stu-id="3fae8-119">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3fae8-120">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3fae8-120">Minimum Shader Model</span></span>

<span data-ttu-id="3fae8-121">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fae8-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3fae8-122">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3fae8-122">Shader Model</span></span>                                              | <span data-ttu-id="3fae8-123">Supportato</span><span class="sxs-lookup"><span data-stu-id="3fae8-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3fae8-124">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3fae8-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3fae8-125">sì</span><span class="sxs-lookup"><span data-stu-id="3fae8-125">yes</span></span>       |
| [<span data-ttu-id="3fae8-126">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="3fae8-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3fae8-127">no</span><span class="sxs-lookup"><span data-stu-id="3fae8-127">no</span></span>        |
| [<span data-ttu-id="3fae8-128">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="3fae8-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3fae8-129">no</span><span class="sxs-lookup"><span data-stu-id="3fae8-129">no</span></span>        |
| [<span data-ttu-id="3fae8-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fae8-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3fae8-131">no</span><span class="sxs-lookup"><span data-stu-id="3fae8-131">no</span></span>        |
| [<span data-ttu-id="3fae8-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fae8-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3fae8-133">no</span><span class="sxs-lookup"><span data-stu-id="3fae8-133">no</span></span>        |
| [<span data-ttu-id="3fae8-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fae8-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3fae8-135">no</span><span class="sxs-lookup"><span data-stu-id="3fae8-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3fae8-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fae8-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fae8-137">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fae8-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





