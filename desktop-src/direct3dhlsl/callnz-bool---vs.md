---
title: callnz bool-vs
description: Chiamare se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995762"
---
# <a name="callnz-bool---vs"></a><span data-ttu-id="fc1e3-105">callnz bool-vs</span><span class="sxs-lookup"><span data-stu-id="fc1e3-105">callnz bool - vs</span></span>

<span data-ttu-id="fc1e3-106">Chiamare se diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fc1e3-106">Call if not zero.</span></span> <span data-ttu-id="fc1e3-107">Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="fc1e3-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1e3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc1e3-108">Syntax</span></span>



| <span data-ttu-id="fc1e3-109">callnz l \# , \[ ! \] b\#</span><span class="sxs-lookup"><span data-stu-id="fc1e3-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="fc1e3-110">dove:</span><span class="sxs-lookup"><span data-stu-id="fc1e3-110">where:</span></span>

-   <span data-ttu-id="fc1e3-111">dove l \# è un' [etichetta-vs](label---vs.md) che contrassegna l'inizio della subroutine da chiamare.</span><span class="sxs-lookup"><span data-stu-id="fc1e3-111">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="fc1e3-112">\[!\] è il modificatore booleano NOT facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc1e3-112">\[!\] is the optional boolean NOT modifier.</span></span>
-   <span data-ttu-id="fc1e3-113">b \# identifica un [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="fc1e3-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1e3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc1e3-114">Remarks</span></span>



| <span data-ttu-id="fc1e3-115">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="fc1e3-115">Vertex shader versions</span></span> | <span data-ttu-id="fc1e3-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="fc1e3-116">1\_1</span></span> | <span data-ttu-id="fc1e3-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc1e3-117">2\_0</span></span> | <span data-ttu-id="fc1e3-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fc1e3-118">2\_x</span></span> | <span data-ttu-id="fc1e3-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fc1e3-119">2\_sw</span></span> | <span data-ttu-id="fc1e3-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc1e3-120">3\_0</span></span> | <span data-ttu-id="fc1e3-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fc1e3-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="fc1e3-122">bool callnz</span><span class="sxs-lookup"><span data-stu-id="fc1e3-122">callnz bool</span></span>            |      | <span data-ttu-id="fc1e3-123">x</span><span class="sxs-lookup"><span data-stu-id="fc1e3-123">x</span></span>    | <span data-ttu-id="fc1e3-124">x</span><span class="sxs-lookup"><span data-stu-id="fc1e3-124">x</span></span>    | <span data-ttu-id="fc1e3-125">x</span><span class="sxs-lookup"><span data-stu-id="fc1e3-125">x</span></span>     | <span data-ttu-id="fc1e3-126">x</span><span class="sxs-lookup"><span data-stu-id="fc1e3-126">x</span></span>    | <span data-ttu-id="fc1e3-127">x</span><span class="sxs-lookup"><span data-stu-id="fc1e3-127">x</span></span>     |



 

<span data-ttu-id="fc1e3-128">Questa istruzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc1e3-128">This instruction does the following:</span></span>


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="fc1e3-129">Questa istruzione usa uno slot di istruzioni vertex shader.</span><span class="sxs-lookup"><span data-stu-id="fc1e3-129">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc1e3-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc1e3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc1e3-131">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="fc1e3-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




