---
title: callnz prede-PS
description: Chiamare con un predicato, se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predicazione usa un valore booleano per determinare se non eseguire l'istruzione.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956071"
---
# <a name="callnz-pred---ps"></a><span data-ttu-id="6f9d5-105">callnz prede-PS</span><span class="sxs-lookup"><span data-stu-id="6f9d5-105">callnz pred - ps</span></span>

<span data-ttu-id="6f9d5-106">Chiamare con un predicato, se diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="6f9d5-106">Call with a predicate, if not zero.</span></span> <span data-ttu-id="6f9d5-107">Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="6f9d5-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="6f9d5-108">Predicazione usa un valore booleano per determinare se non eseguire l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="6f9d5-108">Predication uses a Boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f9d5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f9d5-109">Syntax</span></span>



| <span data-ttu-id="6f9d5-110">callnz l \# , \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="6f9d5-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="6f9d5-111">y</span><span class="sxs-lookup"><span data-stu-id="6f9d5-111">y\</span></span>|<span data-ttu-id="6f9d5-112">z</span><span class="sxs-lookup"><span data-stu-id="6f9d5-112">z\</span></span>|<span data-ttu-id="6f9d5-113">w</span><span class="sxs-lookup"><span data-stu-id="6f9d5-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="6f9d5-114">Dove:</span><span class="sxs-lookup"><span data-stu-id="6f9d5-114">Where:</span></span>

-   <span data-ttu-id="6f9d5-115">dove l \# è un' [etichetta-PS](label---ps.md) che contrassegna l'inizio della subroutine da chiamare.</span><span class="sxs-lookup"><span data-stu-id="6f9d5-115">where l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="6f9d5-116">\[!\] modificatore negazioni facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6f9d5-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="6f9d5-117">P0 è il registro predicato.</span><span class="sxs-lookup"><span data-stu-id="6f9d5-117">p0 is the predicate register.</span></span> <span data-ttu-id="6f9d5-118">Vedere [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="6f9d5-118">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="6f9d5-119">{x \| y \| z \| w} è la replica obbligatoria swizzle su P0.</span><span class="sxs-lookup"><span data-stu-id="6f9d5-119">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9d5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f9d5-120">Remarks</span></span>



| <span data-ttu-id="6f9d5-121">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="6f9d5-121">Pixel shader versions</span></span> | <span data-ttu-id="6f9d5-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="6f9d5-122">1\_1</span></span> | <span data-ttu-id="6f9d5-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="6f9d5-123">1\_2</span></span> | <span data-ttu-id="6f9d5-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6f9d5-124">1\_3</span></span> | <span data-ttu-id="6f9d5-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="6f9d5-125">1\_4</span></span> | <span data-ttu-id="6f9d5-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6f9d5-126">2\_0</span></span> | <span data-ttu-id="6f9d5-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6f9d5-127">2\_x</span></span> | <span data-ttu-id="6f9d5-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6f9d5-128">2\_sw</span></span> | <span data-ttu-id="6f9d5-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6f9d5-129">3\_0</span></span> | <span data-ttu-id="6f9d5-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6f9d5-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6f9d5-131">predazione callnz</span><span class="sxs-lookup"><span data-stu-id="6f9d5-131">callnz pred</span></span>           |      |      |      |      |      | <span data-ttu-id="6f9d5-132">x</span><span class="sxs-lookup"><span data-stu-id="6f9d5-132">x</span></span>    | <span data-ttu-id="6f9d5-133">x</span><span class="sxs-lookup"><span data-stu-id="6f9d5-133">x</span></span>     | <span data-ttu-id="6f9d5-134">x</span><span class="sxs-lookup"><span data-stu-id="6f9d5-134">x</span></span>    | <span data-ttu-id="6f9d5-135">x</span><span class="sxs-lookup"><span data-stu-id="6f9d5-135">x</span></span>     |



 

<span data-ttu-id="6f9d5-136">Questa istruzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f9d5-136">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="6f9d5-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f9d5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f9d5-138">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="6f9d5-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




