---
title: callnz Predator-vs
description: Chiamare se non zero, con un predicato. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. Predicazione usa un valore booleano per determinare se non eseguire l'istruzione.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046084"
---
# <a name="callnz-pred---vs"></a><span data-ttu-id="99ffd-105">callnz Predator-vs</span><span class="sxs-lookup"><span data-stu-id="99ffd-105">callnz pred - vs</span></span>

<span data-ttu-id="99ffd-106">Chiamare se non zero, con un predicato.</span><span class="sxs-lookup"><span data-stu-id="99ffd-106">Call if not zero, with a predicate.</span></span> <span data-ttu-id="99ffd-107">Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="99ffd-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="99ffd-108">Predicazione usa un valore booleano per determinare se non eseguire l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="99ffd-108">Predication uses a boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ffd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99ffd-109">Syntax</span></span>



| <span data-ttu-id="99ffd-110">callnz l \# , \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="99ffd-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="99ffd-111">y</span><span class="sxs-lookup"><span data-stu-id="99ffd-111">y\</span></span>|<span data-ttu-id="99ffd-112">z</span><span class="sxs-lookup"><span data-stu-id="99ffd-112">z\</span></span>|<span data-ttu-id="99ffd-113">w</span><span class="sxs-lookup"><span data-stu-id="99ffd-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="99ffd-114">dove:</span><span class="sxs-lookup"><span data-stu-id="99ffd-114">where:</span></span>

-   <span data-ttu-id="99ffd-115">l \# è un' [etichetta-vs](label---vs.md) che contrassegna l'inizio della subroutine da chiamare.</span><span class="sxs-lookup"><span data-stu-id="99ffd-115">l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="99ffd-116">\[!\] modificatore negazioni facoltativo.</span><span class="sxs-lookup"><span data-stu-id="99ffd-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="99ffd-117">P0 è il [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="99ffd-117">p0 is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="99ffd-118">{x \| y \| z \| w} è la replica obbligatoria swizzle su P0.</span><span class="sxs-lookup"><span data-stu-id="99ffd-118">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="99ffd-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="99ffd-119">Remarks</span></span>



| <span data-ttu-id="99ffd-120">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="99ffd-120">Vertex shader versions</span></span> | <span data-ttu-id="99ffd-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="99ffd-121">1\_1</span></span> | <span data-ttu-id="99ffd-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="99ffd-122">2\_0</span></span> | <span data-ttu-id="99ffd-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="99ffd-123">2\_x</span></span> | <span data-ttu-id="99ffd-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="99ffd-124">2\_sw</span></span> | <span data-ttu-id="99ffd-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="99ffd-125">3\_0</span></span> | <span data-ttu-id="99ffd-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="99ffd-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="99ffd-127">predazione callnz</span><span class="sxs-lookup"><span data-stu-id="99ffd-127">callnz pred</span></span>            |      |      | <span data-ttu-id="99ffd-128">x</span><span class="sxs-lookup"><span data-stu-id="99ffd-128">x</span></span>    | <span data-ttu-id="99ffd-129">x</span><span class="sxs-lookup"><span data-stu-id="99ffd-129">x</span></span>     | <span data-ttu-id="99ffd-130">x</span><span class="sxs-lookup"><span data-stu-id="99ffd-130">x</span></span>    | <span data-ttu-id="99ffd-131">x</span><span class="sxs-lookup"><span data-stu-id="99ffd-131">x</span></span>     |



 

<span data-ttu-id="99ffd-132">Questa istruzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="99ffd-132">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="99ffd-133">Questa istruzione usa uno slot di istruzioni vertex shader.</span><span class="sxs-lookup"><span data-stu-id="99ffd-133">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99ffd-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99ffd-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99ffd-135">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="99ffd-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




