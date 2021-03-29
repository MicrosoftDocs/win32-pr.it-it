---
title: if_comp-vs
description: Avviare un if bool-vs... else-vs... il blocco endif-vs, con una condizione basata sui valori che possono essere calcolati in uno shader. Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992960"
---
# <a name="if_comp---vs"></a><span data-ttu-id="6b49c-104">Se \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="6b49c-104">if\_comp - vs</span></span>

<span data-ttu-id="6b49c-105">Avviare un [if bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... il blocco [endif-vs](endif---vs.md) , con una condizione basata sui valori che possono essere calcolati in uno shader.</span><span class="sxs-lookup"><span data-stu-id="6b49c-105">Start an [if bool - vs](if-bool---vs.md)...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="6b49c-106">Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.</span><span class="sxs-lookup"><span data-stu-id="6b49c-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b49c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b49c-107">Syntax</span></span>



| <span data-ttu-id="6b49c-108">Se \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="6b49c-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="6b49c-109">Dove:</span><span class="sxs-lookup"><span data-stu-id="6b49c-109">Where:</span></span>

-   <span data-ttu-id="6b49c-110">\_comp è un confronto tra i due registri di origine.</span><span class="sxs-lookup"><span data-stu-id="6b49c-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="6b49c-111">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b49c-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="6b49c-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b49c-112">Syntax</span></span> | <span data-ttu-id="6b49c-113">Confronto</span><span class="sxs-lookup"><span data-stu-id="6b49c-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="6b49c-114">\_gt</span><span class="sxs-lookup"><span data-stu-id="6b49c-114">\_gt</span></span>   | <span data-ttu-id="6b49c-115">Maggiore di</span><span class="sxs-lookup"><span data-stu-id="6b49c-115">Greater than</span></span>          |
    | <span data-ttu-id="6b49c-116">\_lt</span><span class="sxs-lookup"><span data-stu-id="6b49c-116">\_lt</span></span>   | <span data-ttu-id="6b49c-117">Minore di</span><span class="sxs-lookup"><span data-stu-id="6b49c-117">Less than</span></span>             |
    | <span data-ttu-id="6b49c-118">\_GE</span><span class="sxs-lookup"><span data-stu-id="6b49c-118">\_ge</span></span>   | <span data-ttu-id="6b49c-119">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="6b49c-119">Greater than or equal</span></span> |
    | <span data-ttu-id="6b49c-120">\_le</span><span class="sxs-lookup"><span data-stu-id="6b49c-120">\_le</span></span>   | <span data-ttu-id="6b49c-121">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="6b49c-121">Less than or equal</span></span>    |
    | <span data-ttu-id="6b49c-122">\_EQ</span><span class="sxs-lookup"><span data-stu-id="6b49c-122">\_eq</span></span>   | <span data-ttu-id="6b49c-123">Uguale a</span><span class="sxs-lookup"><span data-stu-id="6b49c-123">Equal to</span></span>              |
    | <span data-ttu-id="6b49c-124">\_ne</span><span class="sxs-lookup"><span data-stu-id="6b49c-124">\_ne</span></span>   | <span data-ttu-id="6b49c-125">Diverso da</span><span class="sxs-lookup"><span data-stu-id="6b49c-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="6b49c-126">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6b49c-126">src0 is a source register.</span></span> <span data-ttu-id="6b49c-127">Per selezionare un componente, è necessario replicare Swizzle.</span><span class="sxs-lookup"><span data-stu-id="6b49c-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="6b49c-128">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6b49c-128">src1 is a source register.</span></span> <span data-ttu-id="6b49c-129">Per selezionare un componente, è necessario replicare Swizzle.</span><span class="sxs-lookup"><span data-stu-id="6b49c-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b49c-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b49c-130">Remarks</span></span>



| <span data-ttu-id="6b49c-131">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="6b49c-131">Vertex shader versions</span></span> | <span data-ttu-id="6b49c-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="6b49c-132">1\_1</span></span> | <span data-ttu-id="6b49c-133">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6b49c-133">2\_0</span></span> | <span data-ttu-id="6b49c-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6b49c-134">2\_x</span></span> | <span data-ttu-id="6b49c-135">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6b49c-135">2\_sw</span></span> | <span data-ttu-id="6b49c-136">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6b49c-136">3\_0</span></span> | <span data-ttu-id="6b49c-137">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6b49c-137">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="6b49c-138">Se \_ comp</span><span class="sxs-lookup"><span data-stu-id="6b49c-138">if\_comp</span></span>               |      |      | <span data-ttu-id="6b49c-139">x</span><span class="sxs-lookup"><span data-stu-id="6b49c-139">x</span></span>    | <span data-ttu-id="6b49c-140">x</span><span class="sxs-lookup"><span data-stu-id="6b49c-140">x</span></span>     | <span data-ttu-id="6b49c-141">x</span><span class="sxs-lookup"><span data-stu-id="6b49c-141">x</span></span>    | <span data-ttu-id="6b49c-142">x</span><span class="sxs-lookup"><span data-stu-id="6b49c-142">x</span></span>     |



 

<span data-ttu-id="6b49c-143">Questa istruzione viene usata per ignorare un blocco di codice, in base a una condizione.</span><span class="sxs-lookup"><span data-stu-id="6b49c-143">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="6b49c-144">Prestare attenzione a usare le modalità di confronto uguale a e non uguale per i numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="6b49c-144">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="6b49c-145">Poiché l'arrotondamento si verifica durante i calcoli a virgola mobile, il confronto può essere eseguito su un valore Epsilon (un numero diverso da zero) per evitare errori.</span><span class="sxs-lookup"><span data-stu-id="6b49c-145">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="6b49c-146">Tali restrizioni includono:</span><span class="sxs-lookup"><span data-stu-id="6b49c-146">Restrictions include:</span></span>

-   <span data-ttu-id="6b49c-147">Se \_ comp... [else-vs](else---vs.md)... i blocchi [endif-vs](endif---vs.md) (insieme ai blocchi if predicati) possono essere annidati fino a 24 livelli di profondità.</span><span class="sxs-lookup"><span data-stu-id="6b49c-147">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks (along with the predicated if blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="6b49c-148">i registri src0 e src1 richiedono una replica Swizzle.</span><span class="sxs-lookup"><span data-stu-id="6b49c-148">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="6b49c-149">Se i \_ blocchi comp devono terminare con un'istruzione [else-vs](else---vs.md) o [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="6b49c-149">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="6b49c-150">Se \_ comp... [else-vs](else---vs.md)... i blocchi [endif-vs](endif---vs.md) non possono risiedere in un blocco di ciclo.</span><span class="sxs-lookup"><span data-stu-id="6b49c-150">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="6b49c-151">Il \_ blocco If comp deve essere completamente interno o all'esterno del blocco [loop-vs](loop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="6b49c-151">The if\_comp block must be completely inside, or outside the [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="6b49c-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="6b49c-152">Example</span></span>

<span data-ttu-id="6b49c-153">Questa istruzione fornisce il controllo di flusso dinamico condizionale.</span><span class="sxs-lookup"><span data-stu-id="6b49c-153">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="6b49c-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b49c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b49c-155">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="6b49c-155">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




