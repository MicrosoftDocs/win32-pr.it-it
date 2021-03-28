---
title: hs_control_point_phase (SM5-ASM)
description: Avviare la fase del punto di controllo in uno scafo dello shader.
ms.assetid: 9CF26691-C04F-4728-8418-40F313ABBE4A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba3f591fcd656e64609513dca7b9126496a86d6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046108"
---
# <a name="hs_control_point_phase-sm5---asm"></a><span data-ttu-id="b0ea8-103">\_fase del \_ punto di controllo HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b0ea8-103">hs\_control\_point\_phase (sm5 - asm)</span></span>

<span data-ttu-id="b0ea8-104">Avviare la fase del punto di controllo in uno scafo dello shader.</span><span class="sxs-lookup"><span data-stu-id="b0ea8-104">Start the control point phase in a hull shader.</span></span>



| <span data-ttu-id="b0ea8-105">\_ \_ fase punto di controllo HS \_</span><span class="sxs-lookup"><span data-stu-id="b0ea8-105">hs\_control\_point\_phase</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="b0ea8-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0ea8-106">Remarks</span></span>

<span data-ttu-id="b0ea8-107">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0ea8-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b0ea8-108">Vertice</span><span class="sxs-lookup"><span data-stu-id="b0ea8-108">Vertex</span></span> | <span data-ttu-id="b0ea8-109">Hull</span><span class="sxs-lookup"><span data-stu-id="b0ea8-109">Hull</span></span> | <span data-ttu-id="b0ea8-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="b0ea8-110">Domain</span></span> | <span data-ttu-id="b0ea8-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="b0ea8-111">Geometry</span></span> | <span data-ttu-id="b0ea8-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="b0ea8-112">Pixel</span></span> | <span data-ttu-id="b0ea8-113">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b0ea8-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="b0ea8-114">X</span><span class="sxs-lookup"><span data-stu-id="b0ea8-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b0ea8-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b0ea8-115">Minimum Shader Model</span></span>

<span data-ttu-id="b0ea8-116">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0ea8-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b0ea8-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b0ea8-117">Shader Model</span></span>                                              | <span data-ttu-id="b0ea8-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="b0ea8-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b0ea8-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b0ea8-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b0ea8-120">sì</span><span class="sxs-lookup"><span data-stu-id="b0ea8-120">yes</span></span>       |
| [<span data-ttu-id="b0ea8-121">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b0ea8-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b0ea8-122">no</span><span class="sxs-lookup"><span data-stu-id="b0ea8-122">no</span></span>        |
| [<span data-ttu-id="b0ea8-123">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b0ea8-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b0ea8-124">no</span><span class="sxs-lookup"><span data-stu-id="b0ea8-124">no</span></span>        |
| [<span data-ttu-id="b0ea8-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0ea8-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b0ea8-126">no</span><span class="sxs-lookup"><span data-stu-id="b0ea8-126">no</span></span>        |
| [<span data-ttu-id="b0ea8-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0ea8-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b0ea8-128">no</span><span class="sxs-lookup"><span data-stu-id="b0ea8-128">no</span></span>        |
| [<span data-ttu-id="b0ea8-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0ea8-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b0ea8-130">no</span><span class="sxs-lookup"><span data-stu-id="b0ea8-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b0ea8-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0ea8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0ea8-132">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0ea8-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




