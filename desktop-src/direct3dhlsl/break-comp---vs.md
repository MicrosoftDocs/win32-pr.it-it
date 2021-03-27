---
title: break_comp-vs
description: Suddividere in modo condizionale il ciclo corrente nel EndLoop-vs o endrep-vs più vicino.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857778"
---
# <a name="break_comp---vs"></a><span data-ttu-id="4b819-103">Interrompi \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="4b819-103">break\_comp - vs</span></span>

<span data-ttu-id="4b819-104">Suddividere in modo condizionale il ciclo corrente nel [EndLoop-vs](endloop---vs.md) o [endrep-vs](endrep---vs.md)più vicino.</span><span class="sxs-lookup"><span data-stu-id="4b819-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b819-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b819-105">Syntax</span></span>



| <span data-ttu-id="4b819-106">Interrompi \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="4b819-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="4b819-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="4b819-107">Where:</span></span>

-   <span data-ttu-id="4b819-108">\_comp è un confronto tra i due registri di origine.</span><span class="sxs-lookup"><span data-stu-id="4b819-108">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="4b819-109">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b819-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="4b819-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b819-110">Syntax</span></span> | <span data-ttu-id="4b819-111">Confronto</span><span class="sxs-lookup"><span data-stu-id="4b819-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="4b819-112">\_gt</span><span class="sxs-lookup"><span data-stu-id="4b819-112">\_gt</span></span>   | <span data-ttu-id="4b819-113">Maggiore di</span><span class="sxs-lookup"><span data-stu-id="4b819-113">Greater than</span></span>          |
    | <span data-ttu-id="4b819-114">\_lt</span><span class="sxs-lookup"><span data-stu-id="4b819-114">\_lt</span></span>   | <span data-ttu-id="4b819-115">Minore di</span><span class="sxs-lookup"><span data-stu-id="4b819-115">Less than</span></span>             |
    | <span data-ttu-id="4b819-116">\_GE</span><span class="sxs-lookup"><span data-stu-id="4b819-116">\_ge</span></span>   | <span data-ttu-id="4b819-117">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="4b819-117">Greater than or equal</span></span> |
    | <span data-ttu-id="4b819-118">\_le</span><span class="sxs-lookup"><span data-stu-id="4b819-118">\_le</span></span>   | <span data-ttu-id="4b819-119">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="4b819-119">Less than or equal</span></span>    |
    | <span data-ttu-id="4b819-120">\_EQ</span><span class="sxs-lookup"><span data-stu-id="4b819-120">\_eq</span></span>   | <span data-ttu-id="4b819-121">Uguale a</span><span class="sxs-lookup"><span data-stu-id="4b819-121">Equal to</span></span>              |
    | <span data-ttu-id="4b819-122">\_ne</span><span class="sxs-lookup"><span data-stu-id="4b819-122">\_ne</span></span>   | <span data-ttu-id="4b819-123">Diverso da</span><span class="sxs-lookup"><span data-stu-id="4b819-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="4b819-124">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="4b819-124">src0 is a source register.</span></span> <span data-ttu-id="4b819-125">Per selezionare un singolo componente è necessario replicare Swizzle.</span><span class="sxs-lookup"><span data-stu-id="4b819-125">Replicate swizzle is required to select a single component.</span></span>
-   <span data-ttu-id="4b819-126">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="4b819-126">src1 is a source register.</span></span> <span data-ttu-id="4b819-127">Per selezionare un singolo componente è necessario replicare Swizzle.</span><span class="sxs-lookup"><span data-stu-id="4b819-127">Replicate swizzle is required to select a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b819-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b819-128">Remarks</span></span>

<span data-ttu-id="4b819-129">Questa istruzione è supportata nelle versioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="4b819-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="4b819-130">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="4b819-130">Vertex shader versions</span></span> | <span data-ttu-id="4b819-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="4b819-131">1\_1</span></span> | <span data-ttu-id="4b819-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b819-132">2\_0</span></span> | <span data-ttu-id="4b819-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4b819-133">2\_x</span></span> | <span data-ttu-id="4b819-134">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4b819-134">2\_sw</span></span> | <span data-ttu-id="4b819-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b819-135">3\_0</span></span> | <span data-ttu-id="4b819-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4b819-136">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4b819-137">Interrompi \_ comp</span><span class="sxs-lookup"><span data-stu-id="4b819-137">break\_comp</span></span>            |      |      | <span data-ttu-id="4b819-138">x</span><span class="sxs-lookup"><span data-stu-id="4b819-138">x</span></span>    | <span data-ttu-id="4b819-139">x</span><span class="sxs-lookup"><span data-stu-id="4b819-139">x</span></span>     | <span data-ttu-id="4b819-140">x</span><span class="sxs-lookup"><span data-stu-id="4b819-140">x</span></span>    | <span data-ttu-id="4b819-141">x</span><span class="sxs-lookup"><span data-stu-id="4b819-141">x</span></span>     |



 

<span data-ttu-id="4b819-142">Quando il confronto è true, viene interrotto dal ciclo corrente, come illustrato.</span><span class="sxs-lookup"><span data-stu-id="4b819-142">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="4b819-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b819-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b819-144">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="4b819-144">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




