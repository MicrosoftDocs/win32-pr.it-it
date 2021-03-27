---
title: exp-PS
description: Fornisce un 2x esponenziale a precisione completa. | exp-PS
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058508"
---
# <a name="exp---ps"></a><span data-ttu-id="5f769-104">exp-PS</span><span class="sxs-lookup"><span data-stu-id="5f769-104">exp - ps</span></span>

<span data-ttu-id="5f769-105">Fornisce la precisione completa esponenziale 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="5f769-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f769-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f769-106">Syntax</span></span>



| <span data-ttu-id="5f769-107">exp DST, src</span><span class="sxs-lookup"><span data-stu-id="5f769-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="5f769-108">dove</span><span class="sxs-lookup"><span data-stu-id="5f769-108">where</span></span>

-   <span data-ttu-id="5f769-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f769-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5f769-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="5f769-110">src is a source register.</span></span> <span data-ttu-id="5f769-111">Il registro di origine richiede l'uso esplicito di swizzle replicate; ovvero, è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a).</span><span class="sxs-lookup"><span data-stu-id="5f769-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="5f769-112">Vedere il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="5f769-112">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f769-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f769-113">Remarks</span></span>



| <span data-ttu-id="5f769-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="5f769-114">Pixel shader versions</span></span> | <span data-ttu-id="5f769-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="5f769-115">1\_1</span></span> | <span data-ttu-id="5f769-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="5f769-116">1\_2</span></span> | <span data-ttu-id="5f769-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5f769-117">1\_3</span></span> | <span data-ttu-id="5f769-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="5f769-118">1\_4</span></span> | <span data-ttu-id="5f769-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5f769-119">2\_0</span></span> | <span data-ttu-id="5f769-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5f769-120">2\_x</span></span> | <span data-ttu-id="5f769-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5f769-121">2\_sw</span></span> | <span data-ttu-id="5f769-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5f769-122">3\_0</span></span> | <span data-ttu-id="5f769-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5f769-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5f769-124">exp</span><span class="sxs-lookup"><span data-stu-id="5f769-124">exp</span></span>                   |      |      |      |      | <span data-ttu-id="5f769-125">x</span><span class="sxs-lookup"><span data-stu-id="5f769-125">x</span></span>    | <span data-ttu-id="5f769-126">x</span><span class="sxs-lookup"><span data-stu-id="5f769-126">x</span></span>    | <span data-ttu-id="5f769-127">x</span><span class="sxs-lookup"><span data-stu-id="5f769-127">x</span></span>     | <span data-ttu-id="5f769-128">x</span><span class="sxs-lookup"><span data-stu-id="5f769-128">x</span></span>    | <span data-ttu-id="5f769-129">x</span><span class="sxs-lookup"><span data-stu-id="5f769-129">x</span></span>     |



 

<span data-ttu-id="5f769-130">Il frammento di codice seguente mostra le operazioni eseguite:</span><span class="sxs-lookup"><span data-stu-id="5f769-130">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="5f769-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f769-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f769-132">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="5f769-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




