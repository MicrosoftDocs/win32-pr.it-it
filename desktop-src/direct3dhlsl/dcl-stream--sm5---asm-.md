---
title: dcl_stream (SM5-ASM)
description: Dichiarare un flusso di output di Geometry shader.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398297"
---
# <a name="dcl_stream-sm5---asm"></a><span data-ttu-id="2d77b-103">\_flusso DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2d77b-103">dcl\_stream (sm5 - asm)</span></span>

<span data-ttu-id="2d77b-104">Dichiarare un flusso di output di Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="2d77b-104">Declare a geometry shader output stream.</span></span>



| <span data-ttu-id="2d77b-105">\_flusso DCL m\#</span><span class="sxs-lookup"><span data-stu-id="2d77b-105">dcl\_stream m\#</span></span> |
|-----------------|



 



| <span data-ttu-id="2d77b-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2d77b-106">Item</span></span>                                                       | <span data-ttu-id="2d77b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d77b-107">Description</span></span>                             |
|------------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="2d77b-108"><span id="m_"></span><span id="M_"></span>*m\#*</span><span class="sxs-lookup"><span data-stu-id="2d77b-108"><span id="m_"></span><span id="M_"></span>*m\#*</span></span><br/> | <span data-ttu-id="2d77b-109">\[nel \] flusso 0.. 3 (M0.. m3).</span><span class="sxs-lookup"><span data-stu-id="2d77b-109">\[in\] Stream 0..3 (m0..m3).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d77b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d77b-110">Remarks</span></span>

<span data-ttu-id="2d77b-111">Un flusso specificato può essere dichiarato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="2d77b-111">A given stream can only be declared once.</span></span>

<span data-ttu-id="2d77b-112">Se non viene dichiarato alcun flusso, si presuppone che le dichiarazioni di topologia di output e output siano per il flusso 0.</span><span class="sxs-lookup"><span data-stu-id="2d77b-112">If no streams are declared, output and output topology declarations are assumed to be for stream 0.</span></span>

<span data-ttu-id="2d77b-113">Il primo **\_ flusso di DCL** non può comparire dopo le istruzioni di **\_ output** di DCL o di **DCL \_ outputTopology** .</span><span class="sxs-lookup"><span data-stu-id="2d77b-113">The first **dcl\_stream** cannot appear after any **dcl\_output** or **dcl\_outputTopology** statements.</span></span>

<span data-ttu-id="2d77b-114">Tutte le istruzioni di **\_ output** o **DCL \_ outputToplogy** di DCL dopo un'istruzione del **\_ flusso DCL** m \# definiscono gli output per il flusso m \# .</span><span class="sxs-lookup"><span data-stu-id="2d77b-114">Any **dcl\_output** or **dcl\_outputToplogy** statements after any **dcl\_stream** m\# statement define the outputs for stream m\#.</span></span>

<span data-ttu-id="2d77b-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d77b-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2d77b-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="2d77b-116">Vertex</span></span> | <span data-ttu-id="2d77b-117">Hull</span><span class="sxs-lookup"><span data-stu-id="2d77b-117">Hull</span></span> | <span data-ttu-id="2d77b-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="2d77b-118">Domain</span></span> | <span data-ttu-id="2d77b-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="2d77b-119">Geometry</span></span> | <span data-ttu-id="2d77b-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="2d77b-120">Pixel</span></span> | <span data-ttu-id="2d77b-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2d77b-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="2d77b-122">X</span><span class="sxs-lookup"><span data-stu-id="2d77b-122">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2d77b-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2d77b-123">Minimum Shader Model</span></span>

<span data-ttu-id="2d77b-124">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d77b-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2d77b-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2d77b-125">Shader Model</span></span>                                              | <span data-ttu-id="2d77b-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="2d77b-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2d77b-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2d77b-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2d77b-128">sì</span><span class="sxs-lookup"><span data-stu-id="2d77b-128">yes</span></span>       |
| [<span data-ttu-id="2d77b-129">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2d77b-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2d77b-130">no</span><span class="sxs-lookup"><span data-stu-id="2d77b-130">no</span></span>        |
| [<span data-ttu-id="2d77b-131">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2d77b-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2d77b-132">no</span><span class="sxs-lookup"><span data-stu-id="2d77b-132">no</span></span>        |
| [<span data-ttu-id="2d77b-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d77b-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2d77b-134">no</span><span class="sxs-lookup"><span data-stu-id="2d77b-134">no</span></span>        |
| [<span data-ttu-id="2d77b-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d77b-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2d77b-136">no</span><span class="sxs-lookup"><span data-stu-id="2d77b-136">no</span></span>        |
| [<span data-ttu-id="2d77b-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d77b-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2d77b-138">no</span><span class="sxs-lookup"><span data-stu-id="2d77b-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2d77b-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d77b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d77b-140">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d77b-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





