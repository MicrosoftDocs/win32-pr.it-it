---
title: dcl_output (SM4-ASM)
description: '\_output di DCL (SM4-ASM)'
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4391a30e172ef28133b8fe09a99bae7f77c971af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976490"
---
# <a name="dcl_output-sm4---asm"></a><span data-ttu-id="daa9e-103">\_output di DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="daa9e-103">dcl\_output (sm4 - asm)</span></span>

<span data-ttu-id="daa9e-104">Dichiara un registro di output shader.</span><span class="sxs-lookup"><span data-stu-id="daa9e-104">Declares a shader-output register.</span></span>



| <span data-ttu-id="daa9e-105">output di DCL \_ o *N \[ . \] mask*</span><span class="sxs-lookup"><span data-stu-id="daa9e-105">dcl\_output o *N\[.mask\]*</span></span> |
|---------------------------|



 



| <span data-ttu-id="daa9e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="daa9e-106">Item</span></span>                                                                           | <span data-ttu-id="daa9e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="daa9e-107">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa9e-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="daa9e-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/> | <span data-ttu-id="daa9e-109">\[in \] un registro dei dati di output; *N* è un numero intero che indica il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="daa9e-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>               |
| <span data-ttu-id="daa9e-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. mask\]*</span><span class="sxs-lookup"><span data-stu-id="daa9e-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>     | <span data-ttu-id="daa9e-111">\[in \] facoltativo.</span><span class="sxs-lookup"><span data-stu-id="daa9e-111">\[in\] Optional.</span></span> <span data-ttu-id="daa9e-112">Maschera di componenti (con estensione xyzw) che specifica quale dei componenti del registro utilizzare.</span><span class="sxs-lookup"><span data-stu-id="daa9e-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/> |



 

<span data-ttu-id="daa9e-113">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="daa9e-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="daa9e-114">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="daa9e-114">Vertex Shader</span></span> | <span data-ttu-id="daa9e-115">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="daa9e-115">Geometry Shader</span></span> | <span data-ttu-id="daa9e-116">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="daa9e-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="daa9e-117">x</span><span class="sxs-lookup"><span data-stu-id="daa9e-117">x</span></span>             | <span data-ttu-id="daa9e-118">x</span><span class="sxs-lookup"><span data-stu-id="daa9e-118">x</span></span>               | <span data-ttu-id="daa9e-119">x</span><span class="sxs-lookup"><span data-stu-id="daa9e-119">x</span></span>            |



 

<span data-ttu-id="daa9e-120">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="daa9e-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="daa9e-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="daa9e-121">Example</span></span>

<span data-ttu-id="daa9e-122">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="daa9e-122">Here are some examples.</span></span>


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
```



## <a name="minimum-shader-model"></a><span data-ttu-id="daa9e-123">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="daa9e-123">Minimum Shader Model</span></span>

<span data-ttu-id="daa9e-124">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="daa9e-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="daa9e-125">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="daa9e-125">Shader Model</span></span>                                              | <span data-ttu-id="daa9e-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="daa9e-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="daa9e-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="daa9e-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="daa9e-128">sì</span><span class="sxs-lookup"><span data-stu-id="daa9e-128">yes</span></span>       |
| [<span data-ttu-id="daa9e-129">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="daa9e-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="daa9e-130">sì</span><span class="sxs-lookup"><span data-stu-id="daa9e-130">yes</span></span>       |
| [<span data-ttu-id="daa9e-131">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="daa9e-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="daa9e-132">sì</span><span class="sxs-lookup"><span data-stu-id="daa9e-132">yes</span></span>       |
| [<span data-ttu-id="daa9e-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="daa9e-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="daa9e-134">no</span><span class="sxs-lookup"><span data-stu-id="daa9e-134">no</span></span>        |
| [<span data-ttu-id="daa9e-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="daa9e-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="daa9e-136">no</span><span class="sxs-lookup"><span data-stu-id="daa9e-136">no</span></span>        |
| [<span data-ttu-id="daa9e-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="daa9e-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="daa9e-138">no</span><span class="sxs-lookup"><span data-stu-id="daa9e-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="daa9e-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="daa9e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daa9e-140">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="daa9e-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





