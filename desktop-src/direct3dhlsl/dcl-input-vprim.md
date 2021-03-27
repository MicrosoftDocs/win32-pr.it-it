---
title: dcl_input vPrim (SM4-ASM)
description: '\_vPrim di input DCL (SM4-ASM)'
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9742c6066d66d7aa4121c1d1d1df98a37cb0147e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398304"
---
# <a name="dcl_input-vprim-sm4---asm"></a><span data-ttu-id="2c500-103">\_vPrim di input DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2c500-103">dcl\_input vPrim (sm4 - asm)</span></span>

<span data-ttu-id="2c500-104">Dichiara che un geometry shader usa il vPrim di registrazione scalare di input.</span><span class="sxs-lookup"><span data-stu-id="2c500-104">Declares that a geometry shader uses its scalar input-register vPrim.</span></span>



| <span data-ttu-id="2c500-105">\_ *vPrim* di input DCL</span><span class="sxs-lookup"><span data-stu-id="2c500-105">dcl\_input *vPrim*</span></span> |
|--------------------|



 



| <span data-ttu-id="2c500-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c500-106">Item</span></span>                                                                                       | <span data-ttu-id="2c500-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c500-107">Description</span></span>                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c500-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span><span class="sxs-lookup"><span data-stu-id="2c500-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span></span><br/> | <span data-ttu-id="2c500-109">\[in \] uno scalare a 32 bit, che può essere applicato a ogni primitiva interna in un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="2c500-109">\[in\] A 32-bit scalar, which can be applied to each interior primitive in a geometry shader.</span></span><br/> |



 

<span data-ttu-id="2c500-110">Il valore scalare non può essere applicato a eventuali primitive adiacenti.</span><span class="sxs-lookup"><span data-stu-id="2c500-110">The scalar cannot be applied to any adjacent primitives.</span></span>

<span data-ttu-id="2c500-111">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c500-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c500-112">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="2c500-112">Vertex Shader</span></span> | <span data-ttu-id="2c500-113">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="2c500-113">Geometry Shader</span></span> | <span data-ttu-id="2c500-114">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="2c500-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="2c500-115">x</span><span class="sxs-lookup"><span data-stu-id="2c500-115">x</span></span>               |              |



 

<span data-ttu-id="2c500-116">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="2c500-116">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="2c500-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2c500-117">Minimum Shader Model</span></span>

<span data-ttu-id="2c500-118">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c500-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2c500-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2c500-119">Shader Model</span></span>                                              | <span data-ttu-id="2c500-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="2c500-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c500-121">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2c500-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c500-122">sì</span><span class="sxs-lookup"><span data-stu-id="2c500-122">yes</span></span>       |
| [<span data-ttu-id="2c500-123">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2c500-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c500-124">sì</span><span class="sxs-lookup"><span data-stu-id="2c500-124">yes</span></span>       |
| [<span data-ttu-id="2c500-125">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2c500-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c500-126">sì</span><span class="sxs-lookup"><span data-stu-id="2c500-126">yes</span></span>       |
| [<span data-ttu-id="2c500-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c500-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c500-128">no</span><span class="sxs-lookup"><span data-stu-id="2c500-128">no</span></span>        |
| [<span data-ttu-id="2c500-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c500-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c500-130">no</span><span class="sxs-lookup"><span data-stu-id="2c500-130">no</span></span>        |
| [<span data-ttu-id="2c500-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c500-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c500-132">no</span><span class="sxs-lookup"><span data-stu-id="2c500-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2c500-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c500-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c500-134">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c500-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





