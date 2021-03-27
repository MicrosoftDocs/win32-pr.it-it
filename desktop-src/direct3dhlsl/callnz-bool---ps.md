---
title: callnz bool-PS
description: Chiamare se diverso da zero. Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995765"
---
# <a name="callnz-bool---ps"></a><span data-ttu-id="837d4-105">callnz bool-PS</span><span class="sxs-lookup"><span data-stu-id="837d4-105">callnz bool - ps</span></span>

<span data-ttu-id="837d4-106">Chiamare se diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="837d4-106">Call if not zero.</span></span> <span data-ttu-id="837d4-107">Esegue una chiamata condizionale all'istruzione contrassegnata dall'indice dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="837d4-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="837d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="837d4-108">Syntax</span></span>



| <span data-ttu-id="837d4-109">callnz l \# , \[ ! \] b\#</span><span class="sxs-lookup"><span data-stu-id="837d4-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="837d4-110">Dove:</span><span class="sxs-lookup"><span data-stu-id="837d4-110">Where:</span></span>

-   <span data-ttu-id="837d4-111">l \# è un' [etichetta-PS](label---ps.md) che contrassegna l'inizio della subroutine da chiamare.</span><span class="sxs-lookup"><span data-stu-id="837d4-111">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="837d4-112">\[!\] modificatore negazioni facoltativo.</span><span class="sxs-lookup"><span data-stu-id="837d4-112">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="837d4-113">b \# identifica un [Registro booleano costante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="837d4-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="837d4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="837d4-114">Remarks</span></span>



| <span data-ttu-id="837d4-115">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="837d4-115">Pixel shader versions</span></span> | <span data-ttu-id="837d4-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="837d4-116">1\_1</span></span> | <span data-ttu-id="837d4-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="837d4-117">1\_2</span></span> | <span data-ttu-id="837d4-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="837d4-118">1\_3</span></span> | <span data-ttu-id="837d4-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="837d4-119">1\_4</span></span> | <span data-ttu-id="837d4-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="837d4-120">2\_0</span></span> | <span data-ttu-id="837d4-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="837d4-121">2\_x</span></span> | <span data-ttu-id="837d4-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="837d4-122">2\_sw</span></span> | <span data-ttu-id="837d4-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="837d4-123">3\_0</span></span> | <span data-ttu-id="837d4-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="837d4-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="837d4-125">bool callnz</span><span class="sxs-lookup"><span data-stu-id="837d4-125">callnz bool</span></span>           |      |      |      |      |      | <span data-ttu-id="837d4-126">x</span><span class="sxs-lookup"><span data-stu-id="837d4-126">x</span></span>    | <span data-ttu-id="837d4-127">x</span><span class="sxs-lookup"><span data-stu-id="837d4-127">x</span></span>     | <span data-ttu-id="837d4-128">x</span><span class="sxs-lookup"><span data-stu-id="837d4-128">x</span></span>    | <span data-ttu-id="837d4-129">x</span><span class="sxs-lookup"><span data-stu-id="837d4-129">x</span></span>     |



 

<span data-ttu-id="837d4-130">Questa istruzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="837d4-130">This instruction does the following:</span></span>


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="837d4-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="837d4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="837d4-132">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="837d4-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




