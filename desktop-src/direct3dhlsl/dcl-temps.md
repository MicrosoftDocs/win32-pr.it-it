---
title: dcl_temps (SM4-ASM)
description: '\_temps DCL (SM4-ASM)'
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc3a468575b30836d4574edb13c4fc77a3505fc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993200"
---
# <a name="dcl_temps-sm4---asm"></a><span data-ttu-id="3ea78-103">\_temps DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3ea78-103">dcl\_temps (sm4 - asm)</span></span>

<span data-ttu-id="3ea78-104">Dichiara registri temporanei.</span><span class="sxs-lookup"><span data-stu-id="3ea78-104">Declares temporary registers.</span></span>



| <span data-ttu-id="3ea78-105">\_temps DCL N</span><span class="sxs-lookup"><span data-stu-id="3ea78-105">dcl\_temps N</span></span> |
|--------------|



 



| <span data-ttu-id="3ea78-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="3ea78-106">Item</span></span>                                                   | <span data-ttu-id="3ea78-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ea78-107">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ea78-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="3ea78-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="3ea78-109">\[nel \] numero di registri temporanei.</span><span class="sxs-lookup"><span data-stu-id="3ea78-109">\[in\] The number of temporary registers.</span></span><br/> |



 

<span data-ttu-id="3ea78-110">Ogni registro ha spazio per un valore a quattro componenti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3ea78-110">Each register has space for a 32-bit four-component value.</span></span> <span data-ttu-id="3ea78-111">Il numero totale di registri temporanei e [indicizzabili](dcl-indexabletemp.md) temporanei deve essere minore o uguale a 4096.</span><span class="sxs-lookup"><span data-stu-id="3ea78-111">The total number of temporary and [indexable-temporary](dcl-indexabletemp.md) registers must be less than or equal to 4096.</span></span>

<span data-ttu-id="3ea78-112">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ea78-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3ea78-113">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="3ea78-113">Vertex Shader</span></span> | <span data-ttu-id="3ea78-114">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="3ea78-114">Geometry Shader</span></span> | <span data-ttu-id="3ea78-115">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="3ea78-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3ea78-116">x</span><span class="sxs-lookup"><span data-stu-id="3ea78-116">x</span></span>             | <span data-ttu-id="3ea78-117">x</span><span class="sxs-lookup"><span data-stu-id="3ea78-117">x</span></span>               | <span data-ttu-id="3ea78-118">x</span><span class="sxs-lookup"><span data-stu-id="3ea78-118">x</span></span>            |



 

<span data-ttu-id="3ea78-119">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="3ea78-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="3ea78-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="3ea78-120">Example</span></span>

<span data-ttu-id="3ea78-121">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="3ea78-121">Here is an example.</span></span>


```
dcl_temps 10; // Declare r0-r9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="3ea78-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3ea78-122">Minimum Shader Model</span></span>

<span data-ttu-id="3ea78-123">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="3ea78-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3ea78-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3ea78-124">Shader Model</span></span>                                              | <span data-ttu-id="3ea78-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="3ea78-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3ea78-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3ea78-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3ea78-127">sì</span><span class="sxs-lookup"><span data-stu-id="3ea78-127">yes</span></span>       |
| [<span data-ttu-id="3ea78-128">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="3ea78-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3ea78-129">sì</span><span class="sxs-lookup"><span data-stu-id="3ea78-129">yes</span></span>       |
| [<span data-ttu-id="3ea78-130">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="3ea78-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3ea78-131">sì</span><span class="sxs-lookup"><span data-stu-id="3ea78-131">yes</span></span>       |
| [<span data-ttu-id="3ea78-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3ea78-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3ea78-133">no</span><span class="sxs-lookup"><span data-stu-id="3ea78-133">no</span></span>        |
| [<span data-ttu-id="3ea78-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3ea78-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3ea78-135">no</span><span class="sxs-lookup"><span data-stu-id="3ea78-135">no</span></span>        |
| [<span data-ttu-id="3ea78-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3ea78-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3ea78-137">no</span><span class="sxs-lookup"><span data-stu-id="3ea78-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3ea78-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ea78-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ea78-139">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3ea78-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





