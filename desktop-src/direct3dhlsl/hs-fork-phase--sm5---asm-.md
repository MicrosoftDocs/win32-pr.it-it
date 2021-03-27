---
title: hs_fork_phase (SM5-ASM)
description: Avviare la fase di fork in uno scafo dello shader.
ms.assetid: 13D6A06C-F001-45BE-8AB4-D7ACA73BF535
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9316cc92c1bf5683afa620927b3c6f38432c3c4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398280"
---
# <a name="hs_fork_phase-sm5---asm"></a><span data-ttu-id="e5b1d-103">\_fase fork HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e5b1d-103">hs\_fork\_phase (sm5 - asm)</span></span>

<span data-ttu-id="e5b1d-104">Avviare la fase di fork in uno scafo dello shader.</span><span class="sxs-lookup"><span data-stu-id="e5b1d-104">Start the fork phase in a hull shader.</span></span>



| <span data-ttu-id="e5b1d-105">\_fase fork \_ HS</span><span class="sxs-lookup"><span data-stu-id="e5b1d-105">hs\_fork\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="e5b1d-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5b1d-106">Remarks</span></span>

<span data-ttu-id="e5b1d-107">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5b1d-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e5b1d-108">Vertice</span><span class="sxs-lookup"><span data-stu-id="e5b1d-108">Vertex</span></span> | <span data-ttu-id="e5b1d-109">Hull</span><span class="sxs-lookup"><span data-stu-id="e5b1d-109">Hull</span></span> | <span data-ttu-id="e5b1d-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="e5b1d-110">Domain</span></span> | <span data-ttu-id="e5b1d-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="e5b1d-111">Geometry</span></span> | <span data-ttu-id="e5b1d-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="e5b1d-112">Pixel</span></span> | <span data-ttu-id="e5b1d-113">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e5b1d-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="e5b1d-114">X</span><span class="sxs-lookup"><span data-stu-id="e5b1d-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e5b1d-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e5b1d-115">Minimum Shader Model</span></span>

<span data-ttu-id="e5b1d-116">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5b1d-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e5b1d-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e5b1d-117">Shader Model</span></span>                                              | <span data-ttu-id="e5b1d-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="e5b1d-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e5b1d-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e5b1d-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e5b1d-120">sì</span><span class="sxs-lookup"><span data-stu-id="e5b1d-120">yes</span></span>       |
| [<span data-ttu-id="e5b1d-121">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="e5b1d-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e5b1d-122">no</span><span class="sxs-lookup"><span data-stu-id="e5b1d-122">no</span></span>        |
| [<span data-ttu-id="e5b1d-123">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="e5b1d-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e5b1d-124">no</span><span class="sxs-lookup"><span data-stu-id="e5b1d-124">no</span></span>        |
| [<span data-ttu-id="e5b1d-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b1d-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e5b1d-126">no</span><span class="sxs-lookup"><span data-stu-id="e5b1d-126">no</span></span>        |
| [<span data-ttu-id="e5b1d-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b1d-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e5b1d-128">no</span><span class="sxs-lookup"><span data-stu-id="e5b1d-128">no</span></span>        |
| [<span data-ttu-id="e5b1d-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b1d-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e5b1d-130">no</span><span class="sxs-lookup"><span data-stu-id="e5b1d-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e5b1d-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5b1d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5b1d-132">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b1d-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




