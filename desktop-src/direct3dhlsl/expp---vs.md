---
title: EXPP-vs
description: Fornisce la precisione parziale esponenziale 2x.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719405"
---
# <a name="expp---vs"></a><span data-ttu-id="d5c3b-103">EXPP-vs</span><span class="sxs-lookup"><span data-stu-id="d5c3b-103">expp - vs</span></span>

<span data-ttu-id="d5c3b-104">Fornisce la precisione parziale esponenziale 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="d5c3b-104">Provides partial precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5c3b-105">Syntax</span></span>



| <span data-ttu-id="d5c3b-106">EXPP DST, src. x</span><span class="sxs-lookup"><span data-stu-id="d5c3b-106">expp dst, src.{x\</span></span>|<span data-ttu-id="d5c3b-107">y</span><span class="sxs-lookup"><span data-stu-id="d5c3b-107">y\</span></span>|<span data-ttu-id="d5c3b-108">z</span><span class="sxs-lookup"><span data-stu-id="d5c3b-108">z\</span></span>|<span data-ttu-id="d5c3b-109">w</span><span class="sxs-lookup"><span data-stu-id="d5c3b-109">w}</span></span> |
|----------------------------|



 

<span data-ttu-id="d5c3b-110">Dove:</span><span class="sxs-lookup"><span data-stu-id="d5c3b-110">Where:</span></span>

-   <span data-ttu-id="d5c3b-111">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d5c3b-111">dst is the destination register.</span></span>
-   <span data-ttu-id="d5c3b-112">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="d5c3b-112">src is a source register.</span></span> <span data-ttu-id="d5c3b-113">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="d5c3b-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="d5c3b-114">{x \| y \| z \| w} è la replica obbligatoria swizzle nel registro di origine.</span><span class="sxs-lookup"><span data-stu-id="d5c3b-114">{x\|y\|z\|w} is the required replicate swizzle on source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c3b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5c3b-115">Remarks</span></span>



| <span data-ttu-id="d5c3b-116">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="d5c3b-116">Vertex shader versions</span></span> | <span data-ttu-id="d5c3b-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="d5c3b-117">1\_1</span></span> | <span data-ttu-id="d5c3b-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d5c3b-118">2\_0</span></span> | <span data-ttu-id="d5c3b-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d5c3b-119">2\_x</span></span> | <span data-ttu-id="d5c3b-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d5c3b-120">2\_sw</span></span> | <span data-ttu-id="d5c3b-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d5c3b-121">3\_0</span></span> | <span data-ttu-id="d5c3b-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d5c3b-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d5c3b-123">expp</span><span class="sxs-lookup"><span data-stu-id="d5c3b-123">expp</span></span>                   | <span data-ttu-id="d5c3b-124">x</span><span class="sxs-lookup"><span data-stu-id="d5c3b-124">x</span></span>    | <span data-ttu-id="d5c3b-125">x</span><span class="sxs-lookup"><span data-stu-id="d5c3b-125">x</span></span>    | <span data-ttu-id="d5c3b-126">x</span><span class="sxs-lookup"><span data-stu-id="d5c3b-126">x</span></span>    | <span data-ttu-id="d5c3b-127">x</span><span class="sxs-lookup"><span data-stu-id="d5c3b-127">x</span></span>     | <span data-ttu-id="d5c3b-128">x</span><span class="sxs-lookup"><span data-stu-id="d5c3b-128">x</span></span>    | <span data-ttu-id="d5c3b-129">x</span><span class="sxs-lookup"><span data-stu-id="d5c3b-129">x</span></span>     |



 

### <a name="vs_1_1"></a><span data-ttu-id="d5c3b-130">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d5c3b-130">vs\_1\_1</span></span>

<span data-ttu-id="d5c3b-131">L'istruzione [Exp-vs](exp---vs.md) funziona in modo diverso a seconda delle versioni del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="d5c3b-131">The [exp - vs](exp---vs.md) instruction operates differently depending on vertex shader versions.</span></span>

<span data-ttu-id="d5c3b-132">In Visual Studio \_ 1 \_ , l'istruzione EXPP fornisce i risultati seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5c3b-132">In vs\_1\_1, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



<span data-ttu-id="d5c3b-133">In vs \_ 2 \_ 0 e su, l'istruzione EXPP fornisce i risultati seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5c3b-133">In vs\_2\_0 and up, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a><span data-ttu-id="d5c3b-134">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d5c3b-134">vs\_2\_0</span></span>

<span data-ttu-id="d5c3b-135">In vs \_ 2 \_ 0 e su, l'istruzione funziona come segue:</span><span class="sxs-lookup"><span data-stu-id="d5c3b-135">In vs\_2\_0 and up, the instruction works like this:</span></span>


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



<span data-ttu-id="d5c3b-136">L'istruzione fornisce almeno 10 bit di precisione.</span><span class="sxs-lookup"><span data-stu-id="d5c3b-136">The instruction provides at least 10 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5c3b-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5c3b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5c3b-138">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="d5c3b-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




