---
title: POW-vs
description: Src1 ABS a precisione completa (src0). | POW-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234678"
---
# <a name="pow---vs"></a><span data-ttu-id="8ca54-104">POW-vs</span><span class="sxs-lookup"><span data-stu-id="8ca54-104">pow - vs</span></span>

<span data-ttu-id="8ca54-105"><sup>Src1</sup>ABS a precisione completa (src0).</span><span class="sxs-lookup"><span data-stu-id="8ca54-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca54-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ca54-106">Syntax</span></span>



| <span data-ttu-id="8ca54-107">POW DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="8ca54-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="8ca54-108">dove</span><span class="sxs-lookup"><span data-stu-id="8ca54-108">where</span></span>

-   <span data-ttu-id="8ca54-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ca54-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8ca54-110">src0 è un registro di origine di input.</span><span class="sxs-lookup"><span data-stu-id="8ca54-110">src0 is an input source register.</span></span> <span data-ttu-id="8ca54-111">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="8ca54-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="8ca54-112">src1 è un registro di origine di input.</span><span class="sxs-lookup"><span data-stu-id="8ca54-112">src1 is an input source register.</span></span> <span data-ttu-id="8ca54-113">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="8ca54-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca54-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ca54-114">Remarks</span></span>



| <span data-ttu-id="8ca54-115">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="8ca54-115">Vertex shader versions</span></span> | <span data-ttu-id="8ca54-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="8ca54-116">1\_1</span></span> | <span data-ttu-id="8ca54-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8ca54-117">2\_0</span></span> | <span data-ttu-id="8ca54-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8ca54-118">2\_x</span></span> | <span data-ttu-id="8ca54-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8ca54-119">2\_sw</span></span> | <span data-ttu-id="8ca54-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8ca54-120">3\_0</span></span> | <span data-ttu-id="8ca54-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8ca54-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8ca54-122">pow</span><span class="sxs-lookup"><span data-stu-id="8ca54-122">pow</span></span>                    |      | <span data-ttu-id="8ca54-123">x</span><span class="sxs-lookup"><span data-stu-id="8ca54-123">x</span></span>    | <span data-ttu-id="8ca54-124">x</span><span class="sxs-lookup"><span data-stu-id="8ca54-124">x</span></span>    | <span data-ttu-id="8ca54-125">x</span><span class="sxs-lookup"><span data-stu-id="8ca54-125">x</span></span>     | <span data-ttu-id="8ca54-126">x</span><span class="sxs-lookup"><span data-stu-id="8ca54-126">x</span></span>    | <span data-ttu-id="8ca54-127">x</span><span class="sxs-lookup"><span data-stu-id="8ca54-127">x</span></span>     |



 

<span data-ttu-id="8ca54-128">Questa istruzione funziona come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8ca54-128">This instruction works as shown here.</span></span>


```
dest = pow(abs(src0), src1);
```



<span data-ttu-id="8ca54-129">Si tratta di un'istruzione scalare, pertanto è necessario che i registri di origine dispongano della replica swizzles per indicare i canali utilizzati.</span><span class="sxs-lookup"><span data-stu-id="8ca54-129">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="8ca54-130">Il risultato scalare viene replicato in tutti e quattro i canali di output.</span><span class="sxs-lookup"><span data-stu-id="8ca54-130">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="8ca54-131">Questa istruzione può essere espansa come exp (src1 \* log (src0)).</span><span class="sxs-lookup"><span data-stu-id="8ca54-131">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="8ca54-132">La precisione non è inferiore a 15 bit.</span><span class="sxs-lookup"><span data-stu-id="8ca54-132">Precision is not lower than 15 bits.</span></span>

<span data-ttu-id="8ca54-133">Il registro dest deve essere un registro temporaneo e non deve essere lo stesso registro di src1.</span><span class="sxs-lookup"><span data-stu-id="8ca54-133">The dest register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ca54-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ca54-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ca54-135">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="8ca54-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




