---
title: dcl_immediateConstantBuffer (SM4-ASM)
description: '\_immediateConstantBuffer DCL (SM4-ASM)'
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335652"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a><span data-ttu-id="2538f-103">\_immediateConstantBuffer DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2538f-103">dcl\_immediateConstantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="2538f-104">Dichiara un buffer di costante (immediate) dello shader.</span><span class="sxs-lookup"><span data-stu-id="2538f-104">Declares a shader immediate-constant buffer.</span></span>



| <span data-ttu-id="2538f-105">\_ *valori* immediateConstantBuffer di DCL</span><span class="sxs-lookup"><span data-stu-id="2538f-105">dcl\_immediateConstantBuffer *value(s)*</span></span> |
|-----------------------------------------|



 

<dl> <dt>

<span data-ttu-id="2538f-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*valore/i*</span><span class="sxs-lookup"><span data-stu-id="2538f-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*</span></span>
</dt> <dd>

<span data-ttu-id="2538f-107">\[nel \] buffer deve contenere almeno un valore, ma non più di 4096 valori.</span><span class="sxs-lookup"><span data-stu-id="2538f-107">\[in\] The buffer must contain at least one value, but not more than 4096 values.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="2538f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="2538f-108">Remarks</span></span>

<span data-ttu-id="2538f-109">Uno shader è consentito un buffer di costante immediata.</span><span class="sxs-lookup"><span data-stu-id="2538f-109">A shader is allowed one immediate-constant buffer.</span></span> <span data-ttu-id="2538f-110">Viene eseguito l'accesso a un buffer di costanti immediate come un buffer costante con indicizzazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="2538f-110">An immediate-constant buffer is accessed just like a constant buffer with dynamic indexing.</span></span>

<span data-ttu-id="2538f-111">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2538f-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2538f-112">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="2538f-112">Vertex Shader</span></span> | <span data-ttu-id="2538f-113">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="2538f-113">Geometry Shader</span></span> | <span data-ttu-id="2538f-114">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="2538f-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2538f-115">x</span><span class="sxs-lookup"><span data-stu-id="2538f-115">x</span></span>             | <span data-ttu-id="2538f-116">x</span><span class="sxs-lookup"><span data-stu-id="2538f-116">x</span></span>               | <span data-ttu-id="2538f-117">x</span><span class="sxs-lookup"><span data-stu-id="2538f-117">x</span></span>            |



 

<span data-ttu-id="2538f-118">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="2538f-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="2538f-119">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2538f-119">Minimum Shader Model</span></span>

<span data-ttu-id="2538f-120">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2538f-120">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2538f-121">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2538f-121">Shader Model</span></span>                                              | <span data-ttu-id="2538f-122">Supportato</span><span class="sxs-lookup"><span data-stu-id="2538f-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2538f-123">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2538f-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2538f-124">sì</span><span class="sxs-lookup"><span data-stu-id="2538f-124">yes</span></span>       |
| [<span data-ttu-id="2538f-125">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2538f-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2538f-126">sì</span><span class="sxs-lookup"><span data-stu-id="2538f-126">yes</span></span>       |
| [<span data-ttu-id="2538f-127">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2538f-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2538f-128">sì</span><span class="sxs-lookup"><span data-stu-id="2538f-128">yes</span></span>       |
| [<span data-ttu-id="2538f-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2538f-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2538f-130">no</span><span class="sxs-lookup"><span data-stu-id="2538f-130">no</span></span>        |
| [<span data-ttu-id="2538f-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2538f-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2538f-132">no</span><span class="sxs-lookup"><span data-stu-id="2538f-132">no</span></span>        |
| [<span data-ttu-id="2538f-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2538f-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2538f-134">no</span><span class="sxs-lookup"><span data-stu-id="2538f-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2538f-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2538f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2538f-136">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2538f-136">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




