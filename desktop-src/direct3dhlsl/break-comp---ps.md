---
title: break_comp-PS
description: Suddividere il ciclo corrente nel EndLoop-PS o endrep-PS più vicino in base a un confronto per componente.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117201"
---
# <a name="break_comp---ps"></a><span data-ttu-id="3637d-103">Interrompi \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="3637d-103">break\_comp - ps</span></span>

<span data-ttu-id="3637d-104">Suddividere il ciclo corrente nel [EndLoop-PS](endloop---ps.md) o [endrep-PS](endrep---ps.md)più vicino in base a un confronto per componente.</span><span class="sxs-lookup"><span data-stu-id="3637d-104">Break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md), based on a per-component comparison.</span></span>

## <a name="syntax"></a><span data-ttu-id="3637d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3637d-105">Syntax</span></span>



| <span data-ttu-id="3637d-106">Interrompi \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="3637d-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="3637d-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="3637d-107">Where:</span></span>

-   <span data-ttu-id="3637d-108">\_comp è un confronto scalare (o singolo) tra i due registri di origine.</span><span class="sxs-lookup"><span data-stu-id="3637d-108">\_comp is a scalar (or single) comparison between the two source registers.</span></span> <span data-ttu-id="3637d-109">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3637d-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="3637d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3637d-110">Syntax</span></span> | <span data-ttu-id="3637d-111">Confronto</span><span class="sxs-lookup"><span data-stu-id="3637d-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="3637d-112">\_gt</span><span class="sxs-lookup"><span data-stu-id="3637d-112">\_gt</span></span>   | <span data-ttu-id="3637d-113">Maggiore di</span><span class="sxs-lookup"><span data-stu-id="3637d-113">Greater than</span></span>          |
    | <span data-ttu-id="3637d-114">\_lt</span><span class="sxs-lookup"><span data-stu-id="3637d-114">\_lt</span></span>   | <span data-ttu-id="3637d-115">Minore di</span><span class="sxs-lookup"><span data-stu-id="3637d-115">Less than</span></span>             |
    | <span data-ttu-id="3637d-116">\_GE</span><span class="sxs-lookup"><span data-stu-id="3637d-116">\_ge</span></span>   | <span data-ttu-id="3637d-117">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="3637d-117">Greater than or equal</span></span> |
    | <span data-ttu-id="3637d-118">\_le</span><span class="sxs-lookup"><span data-stu-id="3637d-118">\_le</span></span>   | <span data-ttu-id="3637d-119">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="3637d-119">Less than or equal</span></span>    |
    | <span data-ttu-id="3637d-120">\_EQ</span><span class="sxs-lookup"><span data-stu-id="3637d-120">\_eq</span></span>   | <span data-ttu-id="3637d-121">Uguale a</span><span class="sxs-lookup"><span data-stu-id="3637d-121">Equal to</span></span>              |
    | <span data-ttu-id="3637d-122">\_ne</span><span class="sxs-lookup"><span data-stu-id="3637d-122">\_ne</span></span>   | <span data-ttu-id="3637d-123">Diverso da</span><span class="sxs-lookup"><span data-stu-id="3637d-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="3637d-124">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="3637d-124">src0 is a source register.</span></span> <span data-ttu-id="3637d-125">La replica swizzle è obbligatoria se si seleziona un singolo componente.</span><span class="sxs-lookup"><span data-stu-id="3637d-125">Replicate swizzle is required if selecting a single component.</span></span>
-   <span data-ttu-id="3637d-126">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="3637d-126">src1 is a source register.</span></span> <span data-ttu-id="3637d-127">La replica swizzle è obbligatoria se si seleziona un singolo componente.</span><span class="sxs-lookup"><span data-stu-id="3637d-127">Replicate swizzle is required if selecting a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="3637d-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="3637d-128">Remarks</span></span>

<span data-ttu-id="3637d-129">Questa istruzione è supportata nelle versioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3637d-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="3637d-130">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3637d-130">Pixel shader versions</span></span> | <span data-ttu-id="3637d-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="3637d-131">1\_1</span></span> | <span data-ttu-id="3637d-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="3637d-132">1\_2</span></span> | <span data-ttu-id="3637d-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3637d-133">1\_3</span></span> | <span data-ttu-id="3637d-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="3637d-134">1\_4</span></span> | <span data-ttu-id="3637d-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3637d-135">2\_0</span></span> | <span data-ttu-id="3637d-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3637d-136">2\_x</span></span> | <span data-ttu-id="3637d-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3637d-137">2\_sw</span></span> | <span data-ttu-id="3637d-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3637d-138">3\_0</span></span> | <span data-ttu-id="3637d-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3637d-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3637d-140">Interrompi \_ comp</span><span class="sxs-lookup"><span data-stu-id="3637d-140">break\_comp</span></span>           |      |      |      |      |      | <span data-ttu-id="3637d-141">x</span><span class="sxs-lookup"><span data-stu-id="3637d-141">x</span></span>    | <span data-ttu-id="3637d-142">x</span><span class="sxs-lookup"><span data-stu-id="3637d-142">x</span></span>     | <span data-ttu-id="3637d-143">x</span><span class="sxs-lookup"><span data-stu-id="3637d-143">x</span></span>    | <span data-ttu-id="3637d-144">x</span><span class="sxs-lookup"><span data-stu-id="3637d-144">x</span></span>     |



 

<span data-ttu-id="3637d-145">Quando il confronto è true, viene interrotto dal ciclo corrente, come illustrato.</span><span class="sxs-lookup"><span data-stu-id="3637d-145">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="3637d-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3637d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3637d-147">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3637d-147">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




