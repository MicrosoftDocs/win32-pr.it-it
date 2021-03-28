---
title: dcl_output oDepth (SM4-ASM)
description: '\_oDepth di output di DCL (SM4-ASM)'
ms.assetid: 7ee3026d-507f-4aa8-8335-d92c5f649f46
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43580a542c1a66961cfa7434c65cd8d271fb0367
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335636"
---
# <a name="dcl_output-odepth-sm4---asm"></a><span data-ttu-id="9ac68-103">\_oDepth di output di DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9ac68-103">dcl\_output oDepth (sm4 - asm)</span></span>

<span data-ttu-id="9ac68-104">Dichiara che un pixel shader utilizzerà il registro di profondità di output.</span><span class="sxs-lookup"><span data-stu-id="9ac68-104">Declares that a pixel shader will use the output-depth register.</span></span>



| <span data-ttu-id="9ac68-105">\_oDepth output DCL</span><span class="sxs-lookup"><span data-stu-id="9ac68-105">dcl\_output oDepth</span></span> |
|--------------------|



 

<span data-ttu-id="9ac68-106">Il valore nel registro di profondità di output viene usato durante un confronto di profondità, se è abilitato il confronto di profondità.</span><span class="sxs-lookup"><span data-stu-id="9ac68-106">The value in the output-depth register is used during a depth comparison (if depth compare is enabled).</span></span>

<span data-ttu-id="9ac68-107">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ac68-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9ac68-108">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="9ac68-108">Vertex Shader</span></span> | <span data-ttu-id="9ac68-109">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="9ac68-109">Geometry Shader</span></span> | <span data-ttu-id="9ac68-110">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="9ac68-110">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="9ac68-111">x</span><span class="sxs-lookup"><span data-stu-id="9ac68-111">x</span></span>            |



 

<span data-ttu-id="9ac68-112">Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="9ac68-112">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="9ac68-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="9ac68-113">Example</span></span>

<span data-ttu-id="9ac68-114">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="9ac68-114">Here are some examples.</span></span>


```
dcl_output oDepth
```



## <a name="minimum-shader-model"></a><span data-ttu-id="9ac68-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9ac68-115">Minimum Shader Model</span></span>

<span data-ttu-id="9ac68-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ac68-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9ac68-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9ac68-117">Shader Model</span></span>                                              | <span data-ttu-id="9ac68-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="9ac68-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9ac68-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9ac68-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9ac68-120">sì</span><span class="sxs-lookup"><span data-stu-id="9ac68-120">yes</span></span>       |
| [<span data-ttu-id="9ac68-121">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="9ac68-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9ac68-122">sì</span><span class="sxs-lookup"><span data-stu-id="9ac68-122">yes</span></span>       |
| [<span data-ttu-id="9ac68-123">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9ac68-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9ac68-124">sì</span><span class="sxs-lookup"><span data-stu-id="9ac68-124">yes</span></span>       |
| [<span data-ttu-id="9ac68-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ac68-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9ac68-126">no</span><span class="sxs-lookup"><span data-stu-id="9ac68-126">no</span></span>        |
| [<span data-ttu-id="9ac68-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ac68-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9ac68-128">no</span><span class="sxs-lookup"><span data-stu-id="9ac68-128">no</span></span>        |
| [<span data-ttu-id="9ac68-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ac68-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9ac68-130">no</span><span class="sxs-lookup"><span data-stu-id="9ac68-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9ac68-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ac68-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ac68-132">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ac68-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




