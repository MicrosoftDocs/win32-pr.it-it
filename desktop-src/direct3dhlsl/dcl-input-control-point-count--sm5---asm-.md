---
title: dcl_input_control_point_count (SM5-ASM)
description: Dichiarare il numero di punti di controllo di input di Hull shader nella sezione relativa alla dichiarazione di Hull shader.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398306"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a><span data-ttu-id="0eef7-103">\_ \_ \_ conteggio punti di controllo input DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0eef7-103">dcl\_input\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="0eef7-104">Dichiarare il numero di punti di controllo di input di Hull shader nella sezione relativa alla dichiarazione di Hull shader.</span><span class="sxs-lookup"><span data-stu-id="0eef7-104">Declare the hull shader input control point count in the hull shader declaration section.</span></span>



| <span data-ttu-id="0eef7-105">\_ \_ conteggio punti di controllo input DCL \_ \_ {1.32}</span><span class="sxs-lookup"><span data-stu-id="0eef7-105">dcl\_input\_control\_point\_count {1..32}</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="0eef7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0eef7-106">Item</span></span>                                                   | <span data-ttu-id="0eef7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eef7-107">Description</span></span>                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="0eef7-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="0eef7-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="0eef7-109">\[nel \] conteggio dei punti di controllo di input.</span><span class="sxs-lookup"><span data-stu-id="0eef7-109">\[in\] The input control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0eef7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0eef7-110">Remarks</span></span>

<span data-ttu-id="0eef7-111">È necessario almeno un punto di controllo di input. Se non è necessario, può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="0eef7-111">At least 1 input control point is required; it can be empty if it is not needed.</span></span>

<span data-ttu-id="0eef7-112">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0eef7-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0eef7-113">Vertice</span><span class="sxs-lookup"><span data-stu-id="0eef7-113">Vertex</span></span> | <span data-ttu-id="0eef7-114">Hull</span><span class="sxs-lookup"><span data-stu-id="0eef7-114">Hull</span></span> | <span data-ttu-id="0eef7-115">Dominio</span><span class="sxs-lookup"><span data-stu-id="0eef7-115">Domain</span></span> | <span data-ttu-id="0eef7-116">Geometria</span><span class="sxs-lookup"><span data-stu-id="0eef7-116">Geometry</span></span> | <span data-ttu-id="0eef7-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="0eef7-117">Pixel</span></span> | <span data-ttu-id="0eef7-118">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0eef7-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="0eef7-119">X</span><span class="sxs-lookup"><span data-stu-id="0eef7-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0eef7-120">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0eef7-120">Minimum Shader Model</span></span>

<span data-ttu-id="0eef7-121">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0eef7-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0eef7-122">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0eef7-122">Shader Model</span></span>                                              | <span data-ttu-id="0eef7-123">Supportato</span><span class="sxs-lookup"><span data-stu-id="0eef7-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0eef7-124">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="0eef7-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0eef7-125">sì</span><span class="sxs-lookup"><span data-stu-id="0eef7-125">yes</span></span>       |
| [<span data-ttu-id="0eef7-126">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="0eef7-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0eef7-127">no</span><span class="sxs-lookup"><span data-stu-id="0eef7-127">no</span></span>        |
| [<span data-ttu-id="0eef7-128">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="0eef7-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0eef7-129">no</span><span class="sxs-lookup"><span data-stu-id="0eef7-129">no</span></span>        |
| [<span data-ttu-id="0eef7-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0eef7-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0eef7-131">no</span><span class="sxs-lookup"><span data-stu-id="0eef7-131">no</span></span>        |
| [<span data-ttu-id="0eef7-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0eef7-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0eef7-133">no</span><span class="sxs-lookup"><span data-stu-id="0eef7-133">no</span></span>        |
| [<span data-ttu-id="0eef7-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0eef7-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0eef7-135">no</span><span class="sxs-lookup"><span data-stu-id="0eef7-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0eef7-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0eef7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eef7-137">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0eef7-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





