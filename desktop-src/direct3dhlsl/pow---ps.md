---
title: POW-PS
description: Src1 ABS a precisione completa (src0). | POW-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981271"
---
# <a name="pow---ps"></a><span data-ttu-id="ce04a-104">POW-PS</span><span class="sxs-lookup"><span data-stu-id="ce04a-104">pow - ps</span></span>

<span data-ttu-id="ce04a-105"><sup>Src1</sup>ABS a precisione completa (src0).</span><span class="sxs-lookup"><span data-stu-id="ce04a-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce04a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce04a-106">Syntax</span></span>



| <span data-ttu-id="ce04a-107">POW DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="ce04a-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="ce04a-108">dove</span><span class="sxs-lookup"><span data-stu-id="ce04a-108">where</span></span>

-   <span data-ttu-id="ce04a-109">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ce04a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ce04a-110">src0 è un registro di origine di input.</span><span class="sxs-lookup"><span data-stu-id="ce04a-110">src0 is an input source register.</span></span> <span data-ttu-id="ce04a-111">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="ce04a-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="ce04a-112">src1 è un registro di origine di input.</span><span class="sxs-lookup"><span data-stu-id="ce04a-112">src1 is an input source register.</span></span> <span data-ttu-id="ce04a-113">Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="ce04a-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce04a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce04a-114">Remarks</span></span>



| <span data-ttu-id="ce04a-115">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="ce04a-115">Pixel shader versions</span></span> | <span data-ttu-id="ce04a-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="ce04a-116">1\_1</span></span> | <span data-ttu-id="ce04a-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="ce04a-117">1\_2</span></span> | <span data-ttu-id="ce04a-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ce04a-118">1\_3</span></span> | <span data-ttu-id="ce04a-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="ce04a-119">1\_4</span></span> | <span data-ttu-id="ce04a-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce04a-120">2\_0</span></span> | <span data-ttu-id="ce04a-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ce04a-121">2\_x</span></span> | <span data-ttu-id="ce04a-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ce04a-122">2\_sw</span></span> | <span data-ttu-id="ce04a-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce04a-123">3\_0</span></span> | <span data-ttu-id="ce04a-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ce04a-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ce04a-125">pow</span><span class="sxs-lookup"><span data-stu-id="ce04a-125">pow</span></span>                   |      |      |      |      | <span data-ttu-id="ce04a-126">x</span><span class="sxs-lookup"><span data-stu-id="ce04a-126">x</span></span>    | <span data-ttu-id="ce04a-127">x</span><span class="sxs-lookup"><span data-stu-id="ce04a-127">x</span></span>    | <span data-ttu-id="ce04a-128">x</span><span class="sxs-lookup"><span data-stu-id="ce04a-128">x</span></span>     | <span data-ttu-id="ce04a-129">x</span><span class="sxs-lookup"><span data-stu-id="ce04a-129">x</span></span>    | <span data-ttu-id="ce04a-130">x</span><span class="sxs-lookup"><span data-stu-id="ce04a-130">x</span></span>     |



 

<span data-ttu-id="ce04a-131">Questa istruzione funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ce04a-131">This instruction works as follows:</span></span>

<span data-ttu-id="ce04a-132">dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>src1</sup>;</span><span class="sxs-lookup"><span data-stu-id="ce04a-132">dest.x = dest.y = dest.z = dest.w = \[abs(src0)\]<sup>src1</sup>;</span></span>

<span data-ttu-id="ce04a-133">Si tratta di un'istruzione scalare, pertanto è necessario che i registri di origine dispongano della replica swizzles per indicare i canali utilizzati.</span><span class="sxs-lookup"><span data-stu-id="ce04a-133">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="ce04a-134">La potenza di input (src1) deve essere scalare.</span><span class="sxs-lookup"><span data-stu-id="ce04a-134">The input power (src1) must be a scalar.</span></span>

<span data-ttu-id="ce04a-135">Il risultato scalare viene replicato in tutti e quattro i canali di output.</span><span class="sxs-lookup"><span data-stu-id="ce04a-135">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="ce04a-136">Questa istruzione può essere espansa come exp (src1 \* log (src0)).</span><span class="sxs-lookup"><span data-stu-id="ce04a-136">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="ce04a-137">Il registro DST deve essere un registro temporaneo e non deve essere lo stesso registro di src1.</span><span class="sxs-lookup"><span data-stu-id="ce04a-137">The dst register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce04a-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce04a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce04a-139">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="ce04a-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




