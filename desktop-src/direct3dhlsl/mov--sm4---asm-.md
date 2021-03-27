---
title: MOV (SM4-ASM)
description: Spostamento a livello di componente. | MOV (SM4-ASM)
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f029cd8a31a9348e729681878773c225b87b9fbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234641"
---
# <a name="mov-sm4---asm"></a><span data-ttu-id="22cee-104">MOV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="22cee-104">mov (sm4 - asm)</span></span>

<span data-ttu-id="22cee-105">Spostamento a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="22cee-105">Component-wise move.</span></span>



| <span data-ttu-id="22cee-106">Istruzione: MOV \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="22cee-106">Instruction: mov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="22cee-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="22cee-107">Item</span></span>                                                            | <span data-ttu-id="22cee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22cee-108">Description</span></span>                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22cee-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="22cee-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="22cee-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="22cee-110">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="22cee-111">*dest*  =  *src0*</span><span class="sxs-lookup"><span data-stu-id="22cee-111">*dest* = *src0*</span></span><br/> |
| <span data-ttu-id="22cee-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="22cee-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="22cee-113">\[nei \] componenti da spostare.</span><span class="sxs-lookup"><span data-stu-id="22cee-113">\[in\] The components to move.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="22cee-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="22cee-114">Remarks</span></span>

<span data-ttu-id="22cee-115">I modificatori, diversi da Swizzle, presuppongono che i dati siano a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="22cee-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="22cee-116">L'assenza di modificatori sposta solo i dati senza alterare i bit.</span><span class="sxs-lookup"><span data-stu-id="22cee-116">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="22cee-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="22cee-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="22cee-118">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="22cee-118">Vertex Shader</span></span> | <span data-ttu-id="22cee-119">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="22cee-119">Geometry Shader</span></span> | <span data-ttu-id="22cee-120">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="22cee-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="22cee-121">x</span><span class="sxs-lookup"><span data-stu-id="22cee-121">x</span></span>             | <span data-ttu-id="22cee-122">x</span><span class="sxs-lookup"><span data-stu-id="22cee-122">x</span></span>               | <span data-ttu-id="22cee-123">x</span><span class="sxs-lookup"><span data-stu-id="22cee-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="22cee-124">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="22cee-124">Minimum Shader Model</span></span>

<span data-ttu-id="22cee-125">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="22cee-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="22cee-126">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="22cee-126">Shader Model</span></span>                                              | <span data-ttu-id="22cee-127">Supportato</span><span class="sxs-lookup"><span data-stu-id="22cee-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="22cee-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="22cee-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="22cee-129">sì</span><span class="sxs-lookup"><span data-stu-id="22cee-129">yes</span></span>       |
| [<span data-ttu-id="22cee-130">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="22cee-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="22cee-131">sì</span><span class="sxs-lookup"><span data-stu-id="22cee-131">yes</span></span>       |
| [<span data-ttu-id="22cee-132">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="22cee-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="22cee-133">sì</span><span class="sxs-lookup"><span data-stu-id="22cee-133">yes</span></span>       |
| [<span data-ttu-id="22cee-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22cee-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="22cee-135">no</span><span class="sxs-lookup"><span data-stu-id="22cee-135">no</span></span>        |
| [<span data-ttu-id="22cee-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22cee-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="22cee-137">no</span><span class="sxs-lookup"><span data-stu-id="22cee-137">no</span></span>        |
| [<span data-ttu-id="22cee-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22cee-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="22cee-139">no</span><span class="sxs-lookup"><span data-stu-id="22cee-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="22cee-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22cee-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22cee-141">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22cee-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





