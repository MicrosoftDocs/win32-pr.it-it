---
title: exp-vs
description: Fornisce un 2x esponenziale a precisione completa. | exp-vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995708"
---
# <a name="exp---vs"></a><span data-ttu-id="4a7b8-104">exp-vs</span><span class="sxs-lookup"><span data-stu-id="4a7b8-104">exp - vs</span></span>

<span data-ttu-id="4a7b8-105">Fornisce la precisione completa esponenziale 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="4a7b8-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a7b8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a7b8-106">Syntax</span></span>



| <span data-ttu-id="4a7b8-107">exp DST, src</span><span class="sxs-lookup"><span data-stu-id="4a7b8-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="4a7b8-108">dove</span><span class="sxs-lookup"><span data-stu-id="4a7b8-108">where</span></span>

-   <span data-ttu-id="4a7b8-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a7b8-109">dst is the destination register.</span></span>
-   <span data-ttu-id="4a7b8-110">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="4a7b8-110">src is a source register.</span></span> <span data-ttu-id="4a7b8-111">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="4a7b8-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="4a7b8-112">Vedere il [Registro di origine swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="4a7b8-112">See [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a7b8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a7b8-113">Remarks</span></span>



| <span data-ttu-id="4a7b8-114">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="4a7b8-114">Vertex shader versions</span></span> | <span data-ttu-id="4a7b8-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="4a7b8-115">1\_1</span></span> | <span data-ttu-id="4a7b8-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a7b8-116">2\_0</span></span> | <span data-ttu-id="4a7b8-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4a7b8-117">2\_x</span></span> | <span data-ttu-id="4a7b8-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4a7b8-118">2\_sw</span></span> | <span data-ttu-id="4a7b8-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a7b8-119">3\_0</span></span> | <span data-ttu-id="4a7b8-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4a7b8-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4a7b8-121">exp</span><span class="sxs-lookup"><span data-stu-id="4a7b8-121">exp</span></span>                    | <span data-ttu-id="4a7b8-122">x</span><span class="sxs-lookup"><span data-stu-id="4a7b8-122">x</span></span>    | <span data-ttu-id="4a7b8-123">x</span><span class="sxs-lookup"><span data-stu-id="4a7b8-123">x</span></span>    | <span data-ttu-id="4a7b8-124">x</span><span class="sxs-lookup"><span data-stu-id="4a7b8-124">x</span></span>    | <span data-ttu-id="4a7b8-125">x</span><span class="sxs-lookup"><span data-stu-id="4a7b8-125">x</span></span>     | <span data-ttu-id="4a7b8-126">x</span><span class="sxs-lookup"><span data-stu-id="4a7b8-126">x</span></span>    | <span data-ttu-id="4a7b8-127">x</span><span class="sxs-lookup"><span data-stu-id="4a7b8-127">x</span></span>     |



 

<span data-ttu-id="4a7b8-128">Questa istruzione fornisce almeno 21 bit di precisione.</span><span class="sxs-lookup"><span data-stu-id="4a7b8-128">This instruction provides at least 21 bits of precision.</span></span>

<span data-ttu-id="4a7b8-129">Il frammento di codice seguente mostra le operazioni eseguite:</span><span class="sxs-lookup"><span data-stu-id="4a7b8-129">The following code fragment shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="4a7b8-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a7b8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a7b8-131">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="4a7b8-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




