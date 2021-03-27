---
title: if_comp-PS
description: Avvia un'if bool-PS... else-PS... il blocco endif-PS, con una condizione basata sui valori che possono essere calcolati in uno shader. Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719351"
---
# <a name="if_comp---ps"></a><span data-ttu-id="bbd58-104">Se \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="bbd58-104">if\_comp - ps</span></span>

<span data-ttu-id="bbd58-105">Avvia un' [if bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... il blocco [endif-PS](endif---ps.md) , con una condizione basata sui valori che possono essere calcolati in uno shader.</span><span class="sxs-lookup"><span data-stu-id="bbd58-105">Start an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="bbd58-106">Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.</span><span class="sxs-lookup"><span data-stu-id="bbd58-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd58-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbd58-107">Syntax</span></span>



| <span data-ttu-id="bbd58-108">Se \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="bbd58-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="bbd58-109">Dove:</span><span class="sxs-lookup"><span data-stu-id="bbd58-109">Where:</span></span>

-   <span data-ttu-id="bbd58-110">\_comp è un confronto tra i due registri di origine.</span><span class="sxs-lookup"><span data-stu-id="bbd58-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="bbd58-111">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bbd58-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="bbd58-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbd58-112">Syntax</span></span> | <span data-ttu-id="bbd58-113">Confronto</span><span class="sxs-lookup"><span data-stu-id="bbd58-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="bbd58-114">\_gt</span><span class="sxs-lookup"><span data-stu-id="bbd58-114">\_gt</span></span>   | <span data-ttu-id="bbd58-115">Maggiore di</span><span class="sxs-lookup"><span data-stu-id="bbd58-115">Greater than</span></span>          |
    | <span data-ttu-id="bbd58-116">\_lt</span><span class="sxs-lookup"><span data-stu-id="bbd58-116">\_lt</span></span>   | <span data-ttu-id="bbd58-117">Minore di</span><span class="sxs-lookup"><span data-stu-id="bbd58-117">Less than</span></span>             |
    | <span data-ttu-id="bbd58-118">\_GE</span><span class="sxs-lookup"><span data-stu-id="bbd58-118">\_ge</span></span>   | <span data-ttu-id="bbd58-119">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="bbd58-119">Greater than or equal</span></span> |
    | <span data-ttu-id="bbd58-120">\_le</span><span class="sxs-lookup"><span data-stu-id="bbd58-120">\_le</span></span>   | <span data-ttu-id="bbd58-121">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="bbd58-121">Less than or equal</span></span>    |
    | <span data-ttu-id="bbd58-122">\_EQ</span><span class="sxs-lookup"><span data-stu-id="bbd58-122">\_eq</span></span>   | <span data-ttu-id="bbd58-123">Uguale a</span><span class="sxs-lookup"><span data-stu-id="bbd58-123">Equal to</span></span>              |
    | <span data-ttu-id="bbd58-124">\_ne</span><span class="sxs-lookup"><span data-stu-id="bbd58-124">\_ne</span></span>   | <span data-ttu-id="bbd58-125">Diverso da</span><span class="sxs-lookup"><span data-stu-id="bbd58-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="bbd58-126">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="bbd58-126">src0 is a source register.</span></span> <span data-ttu-id="bbd58-127">Per selezionare un componente, è necessario replicare Swizzle.</span><span class="sxs-lookup"><span data-stu-id="bbd58-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="bbd58-128">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="bbd58-128">src1 is a source register.</span></span> <span data-ttu-id="bbd58-129">Per selezionare un componente, è necessario replicare Swizzle.</span><span class="sxs-lookup"><span data-stu-id="bbd58-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd58-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbd58-130">Remarks</span></span>



| <span data-ttu-id="bbd58-131">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="bbd58-131">Pixel shader versions</span></span> | <span data-ttu-id="bbd58-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="bbd58-132">1\_1</span></span> | <span data-ttu-id="bbd58-133">1\_2</span><span class="sxs-lookup"><span data-stu-id="bbd58-133">1\_2</span></span> | <span data-ttu-id="bbd58-134">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bbd58-134">1\_3</span></span> | <span data-ttu-id="bbd58-135">1\_4</span><span class="sxs-lookup"><span data-stu-id="bbd58-135">1\_4</span></span> | <span data-ttu-id="bbd58-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bbd58-136">2\_0</span></span> | <span data-ttu-id="bbd58-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bbd58-137">2\_x</span></span> | <span data-ttu-id="bbd58-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bbd58-138">2\_sw</span></span> | <span data-ttu-id="bbd58-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bbd58-139">3\_0</span></span> | <span data-ttu-id="bbd58-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bbd58-140">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bbd58-141">Se \_ comp</span><span class="sxs-lookup"><span data-stu-id="bbd58-141">if\_comp</span></span>              |      |      |      |      |      | <span data-ttu-id="bbd58-142">x</span><span class="sxs-lookup"><span data-stu-id="bbd58-142">x</span></span>    | <span data-ttu-id="bbd58-143">x</span><span class="sxs-lookup"><span data-stu-id="bbd58-143">x</span></span>     | <span data-ttu-id="bbd58-144">x</span><span class="sxs-lookup"><span data-stu-id="bbd58-144">x</span></span>    | <span data-ttu-id="bbd58-145">x</span><span class="sxs-lookup"><span data-stu-id="bbd58-145">x</span></span>     |



 

<span data-ttu-id="bbd58-146">Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.</span><span class="sxs-lookup"><span data-stu-id="bbd58-146">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="bbd58-147">Prestare attenzione a usare le modalità di confronto uguale a e non uguale per i numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="bbd58-147">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="bbd58-148">Poiché l'arrotondamento si verifica durante i calcoli a virgola mobile, il confronto può essere eseguito su un valore Epsilon (un numero diverso da zero) per evitare errori.</span><span class="sxs-lookup"><span data-stu-id="bbd58-148">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="bbd58-149">Tali restrizioni includono:</span><span class="sxs-lookup"><span data-stu-id="bbd58-149">Restrictions include:</span></span>

-   <span data-ttu-id="bbd58-150">Se \_ comp... [else-PS](else---ps.md)... i blocchi [endif-PS](endif---ps.md) (insieme ai blocchi [if](if-bool---ps.md) predicati) possono essere annidati fino a 24 livelli di profondità.</span><span class="sxs-lookup"><span data-stu-id="bbd58-150">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks (along with the predicated [if](if-bool---ps.md) blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="bbd58-151">i registri src0 e src1 richiedono una replica Swizzle.</span><span class="sxs-lookup"><span data-stu-id="bbd58-151">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="bbd58-152">Se i \_ blocchi comp devono terminare con un'istruzione [else-vs](else---vs.md) o [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="bbd58-152">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="bbd58-153">Se \_ comp... [else-PS](else---ps.md)... i blocchi [endif-PS](endif---ps.md) non possono risiedere in un blocco di ciclo.</span><span class="sxs-lookup"><span data-stu-id="bbd58-153">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="bbd58-154">Il \_ blocco If comp deve trovarsi completamente all'interno o all'esterno del blocco del ciclo.</span><span class="sxs-lookup"><span data-stu-id="bbd58-154">The if\_comp block must be completely inside or outside the loop block.</span></span>

## <a name="example"></a><span data-ttu-id="bbd58-155">Esempio</span><span class="sxs-lookup"><span data-stu-id="bbd58-155">Example</span></span>

<span data-ttu-id="bbd58-156">Questa istruzione fornisce il controllo di flusso dinamico condizionale.</span><span class="sxs-lookup"><span data-stu-id="bbd58-156">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="bbd58-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbd58-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbd58-158">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="bbd58-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




