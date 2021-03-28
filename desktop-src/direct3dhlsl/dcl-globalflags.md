---
title: dcl_globalFlags (SM4-ASM)
description: '\_globalFlags DCL (SM4-ASM)'
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e15fce958056f91a41954b987850ad4c5a43e521
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398308"
---
# <a name="dcl_globalflags-sm4---asm"></a><span data-ttu-id="4aa9a-103">\_globalFlags DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4aa9a-103">dcl\_globalFlags (sm4 - asm)</span></span>

<span data-ttu-id="4aa9a-104">Dichiara i flag globali dello shader.</span><span class="sxs-lookup"><span data-stu-id="4aa9a-104">Declares shader global flags.</span></span>



| <span data-ttu-id="4aa9a-105">\_ *flag* globalFlags DCL</span><span class="sxs-lookup"><span data-stu-id="4aa9a-105">dcl\_globalFlags *flags*</span></span> |
|--------------------------|



 

<dl> <dt>

<span data-ttu-id="4aa9a-106"><span id="flags"></span><span id="FLAGS"></span>*Bandiere*</span><span class="sxs-lookup"><span data-stu-id="4aa9a-106"><span id="flags"></span><span id="FLAGS"></span>*flags*</span></span>
</dt> <dd>

<span data-ttu-id="4aa9a-107">\[in \] un flag shader globale.</span><span class="sxs-lookup"><span data-stu-id="4aa9a-107">\[in\] A global shader flag.</span></span> <span data-ttu-id="4aa9a-108">Attualmente è definito un flag.</span><span class="sxs-lookup"><span data-stu-id="4aa9a-108">There is currently one flag defined.</span></span>

-   <span data-ttu-id="4aa9a-109">Refactoring \_ consentito: consente al driver di riordinare le operazioni aritmetiche per l'ottimizzazione, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4aa9a-109">REFACTORING\_ALLOWED - Permits the driver to reorder arithmetic operations for optimization, as shown here.</span></span>

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> <span data-ttu-id="4aa9a-110">Il riordino delle operazioni aritmetiche può generare risultati diversi.</span><span class="sxs-lookup"><span data-stu-id="4aa9a-110">Reordering arithmetic operations may generate different results.</span></span>

 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="4aa9a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4aa9a-111">Remarks</span></span>

<span data-ttu-id="4aa9a-112">Questa istruzione facoltativa si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4aa9a-112">This optional instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4aa9a-113">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="4aa9a-113">Vertex Shader</span></span> | <span data-ttu-id="4aa9a-114">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="4aa9a-114">Geometry Shader</span></span> | <span data-ttu-id="4aa9a-115">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="4aa9a-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4aa9a-116">x</span><span class="sxs-lookup"><span data-stu-id="4aa9a-116">x</span></span>             | <span data-ttu-id="4aa9a-117">x</span><span class="sxs-lookup"><span data-stu-id="4aa9a-117">x</span></span>               | <span data-ttu-id="4aa9a-118">x</span><span class="sxs-lookup"><span data-stu-id="4aa9a-118">x</span></span>            |



 

<span data-ttu-id="4aa9a-119">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="4aa9a-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4aa9a-120">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="4aa9a-120">Minimum Shader Model</span></span>

<span data-ttu-id="4aa9a-121">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4aa9a-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4aa9a-122">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4aa9a-122">Shader Model</span></span>                                              | <span data-ttu-id="4aa9a-123">Supportato</span><span class="sxs-lookup"><span data-stu-id="4aa9a-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4aa9a-124">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4aa9a-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4aa9a-125">sì</span><span class="sxs-lookup"><span data-stu-id="4aa9a-125">yes</span></span>       |
| [<span data-ttu-id="4aa9a-126">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="4aa9a-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4aa9a-127">sì</span><span class="sxs-lookup"><span data-stu-id="4aa9a-127">yes</span></span>       |
| [<span data-ttu-id="4aa9a-128">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="4aa9a-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4aa9a-129">sì</span><span class="sxs-lookup"><span data-stu-id="4aa9a-129">yes</span></span>       |
| [<span data-ttu-id="4aa9a-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4aa9a-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4aa9a-131">no</span><span class="sxs-lookup"><span data-stu-id="4aa9a-131">no</span></span>        |
| [<span data-ttu-id="4aa9a-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4aa9a-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4aa9a-133">no</span><span class="sxs-lookup"><span data-stu-id="4aa9a-133">no</span></span>        |
| [<span data-ttu-id="4aa9a-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4aa9a-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4aa9a-135">no</span><span class="sxs-lookup"><span data-stu-id="4aa9a-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4aa9a-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4aa9a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aa9a-137">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4aa9a-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




