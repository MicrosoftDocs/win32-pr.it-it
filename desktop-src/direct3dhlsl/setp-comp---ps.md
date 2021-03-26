---
title: setp_comp-PS
description: Impostare il registro del predicato. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234826"
---
# <a name="setp_comp---ps"></a><span data-ttu-id="b946e-104">setp \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="b946e-104">setp\_comp - ps</span></span>

<span data-ttu-id="b946e-105">Impostare il registro del predicato.</span><span class="sxs-lookup"><span data-stu-id="b946e-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="b946e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b946e-106">Syntax</span></span>



| <span data-ttu-id="b946e-107">setp \_ comp DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="b946e-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="b946e-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="b946e-108">Where:</span></span>

-   <span data-ttu-id="b946e-109">\_comp è un confronto per canale tra i due registri di origine.</span><span class="sxs-lookup"><span data-stu-id="b946e-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="b946e-110">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b946e-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="b946e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b946e-111">Syntax</span></span> | <span data-ttu-id="b946e-112">Confronto</span><span class="sxs-lookup"><span data-stu-id="b946e-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="b946e-113">\_gt</span><span class="sxs-lookup"><span data-stu-id="b946e-113">\_gt</span></span>   | <span data-ttu-id="b946e-114">Maggiore di</span><span class="sxs-lookup"><span data-stu-id="b946e-114">Greater than</span></span>          |
    | <span data-ttu-id="b946e-115">\_lt</span><span class="sxs-lookup"><span data-stu-id="b946e-115">\_lt</span></span>   | <span data-ttu-id="b946e-116">Minore di</span><span class="sxs-lookup"><span data-stu-id="b946e-116">Less than</span></span>             |
    | <span data-ttu-id="b946e-117">\_GE</span><span class="sxs-lookup"><span data-stu-id="b946e-117">\_ge</span></span>   | <span data-ttu-id="b946e-118">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="b946e-118">Greater than or equal</span></span> |
    | <span data-ttu-id="b946e-119">\_le</span><span class="sxs-lookup"><span data-stu-id="b946e-119">\_le</span></span>   | <span data-ttu-id="b946e-120">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="b946e-120">Less than or equal</span></span>    |
    | <span data-ttu-id="b946e-121">\_EQ</span><span class="sxs-lookup"><span data-stu-id="b946e-121">\_eq</span></span>   | <span data-ttu-id="b946e-122">Uguale a</span><span class="sxs-lookup"><span data-stu-id="b946e-122">Equal to</span></span>              |
    | <span data-ttu-id="b946e-123">\_ne</span><span class="sxs-lookup"><span data-stu-id="b946e-123">\_ne</span></span>   | <span data-ttu-id="b946e-124">Diverso da</span><span class="sxs-lookup"><span data-stu-id="b946e-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="b946e-125">DST è il registro [Register del predicato](dx9-graphics-reference-asm-ps-registers-predicate.md) , P0.</span><span class="sxs-lookup"><span data-stu-id="b946e-125">dst is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="b946e-126">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="b946e-126">src0 is a source register.</span></span>
-   <span data-ttu-id="b946e-127">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="b946e-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b946e-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="b946e-128">Remarks</span></span>



| <span data-ttu-id="b946e-129">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="b946e-129">Pixel shader versions</span></span> | <span data-ttu-id="b946e-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="b946e-130">1\_1</span></span> | <span data-ttu-id="b946e-131">1\_2</span><span class="sxs-lookup"><span data-stu-id="b946e-131">1\_2</span></span> | <span data-ttu-id="b946e-132">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b946e-132">1\_3</span></span> | <span data-ttu-id="b946e-133">1\_4</span><span class="sxs-lookup"><span data-stu-id="b946e-133">1\_4</span></span> | <span data-ttu-id="b946e-134">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b946e-134">2\_0</span></span> | <span data-ttu-id="b946e-135">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b946e-135">2\_x</span></span> | <span data-ttu-id="b946e-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b946e-136">2\_sw</span></span> | <span data-ttu-id="b946e-137">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b946e-137">3\_0</span></span> | <span data-ttu-id="b946e-138">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b946e-138">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b946e-139">setp \_ comp</span><span class="sxs-lookup"><span data-stu-id="b946e-139">setp\_comp</span></span>            |      |      |      |      |      | <span data-ttu-id="b946e-140">x</span><span class="sxs-lookup"><span data-stu-id="b946e-140">x</span></span>    | <span data-ttu-id="b946e-141">x</span><span class="sxs-lookup"><span data-stu-id="b946e-141">x</span></span>     | <span data-ttu-id="b946e-142">x</span><span class="sxs-lookup"><span data-stu-id="b946e-142">x</span></span>    | <span data-ttu-id="b946e-143">x</span><span class="sxs-lookup"><span data-stu-id="b946e-143">x</span></span>     |



 

<span data-ttu-id="b946e-144">Questa istruzione funziona come segue:</span><span class="sxs-lookup"><span data-stu-id="b946e-144">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="b946e-145">Per ogni canale che può essere scritto in base alla maschera di scrittura di destinazione, salvare il risultato booleano dell'operazione di confronto tra i canali corrispondenti di src0 e src1 (dopo la risoluzione del modificatore di origine swizzles).</span><span class="sxs-lookup"><span data-stu-id="b946e-145">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="b946e-146">I registri di origine consentono di specificare un componente arbitrario swizzles.</span><span class="sxs-lookup"><span data-stu-id="b946e-146">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="b946e-147">Il registro di destinazione consente le maschere di scrittura arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="b946e-147">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="b946e-148">Il registro DST deve essere il registro predicato.</span><span class="sxs-lookup"><span data-stu-id="b946e-148">The dst register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="b946e-149">Applicazione del registro predicato</span><span class="sxs-lookup"><span data-stu-id="b946e-149">Applying the Predicate Register</span></span>

<span data-ttu-id="b946e-150">Quando il registro predicato è stato inizializzato con setp \_ comp, può essere usato per controllare un'istruzione per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="b946e-150">Once the predicate register has been initialized with setp\_comp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="b946e-151">Ecco la sintassi:</span><span class="sxs-lookup"><span data-stu-id="b946e-151">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



<span data-ttu-id="b946e-152">Dove:</span><span class="sxs-lookup"><span data-stu-id="b946e-152">Where:</span></span>

-   <span data-ttu-id="b946e-153">\[!\] è un valore booleano facoltativo NOT</span><span class="sxs-lookup"><span data-stu-id="b946e-153">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="b946e-154">P0 è il registro predicato</span><span class="sxs-lookup"><span data-stu-id="b946e-154">p0 is the predicate register</span></span>
-   <span data-ttu-id="b946e-155">\[. Swizzle \] è un swizzle facoltativo da applicare al contenuto del registro predicato prima di utilizzarlo per mascherare l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="b946e-155">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="b946e-156">I swizzles disponibili sono:. xyzw (impostazione predefinita quando non è specificato alcun parametro) o qualsiasi replica swizzle:. x/. r,. y/. g,. z/. b o. a/. w.</span><span class="sxs-lookup"><span data-stu-id="b946e-156">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="b946e-157">l'istruzione è qualsiasi aritmetic o istruzione di trama.</span><span class="sxs-lookup"><span data-stu-id="b946e-157">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="b946e-158">Non può essere un'istruzione di controllo di flusso statica o dinamica.</span><span class="sxs-lookup"><span data-stu-id="b946e-158">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="b946e-159">dest, src0,... sono i registri richiesti dall'istruzione</span><span class="sxs-lookup"><span data-stu-id="b946e-159">dest, src0, ... are the registers required by the instruction</span></span>

<span data-ttu-id="b946e-160">Supponendo che il registro dei predicati sia stato configurato con i valori dei componenti (true, true, false, false), è possibile applicare questa istruzione:</span><span class="sxs-lookup"><span data-stu-id="b946e-160">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
(p0) add r1, r2, r3
```



<span data-ttu-id="b946e-161">per eseguire un'aggiunta a 2 componenti.</span><span class="sxs-lookup"><span data-stu-id="b946e-161">to perform a 2 component add.</span></span>


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



<span data-ttu-id="b946e-162">I componenti z e w di R1 non verranno scritti poiché il registro predicato contiene false nei componenti z e w.</span><span class="sxs-lookup"><span data-stu-id="b946e-162">The z and w components of r1 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="b946e-163">Se si applica il registro predicato a un'istruzione aritmetica o di trama, il numero di slot di istruzioni aumenta di 1.</span><span class="sxs-lookup"><span data-stu-id="b946e-163">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="b946e-164">Il registro predicato può essere applicato anche a se le istruzioni [prede-PS](if-pred---ps.md), [callnz prede-PS](callnz-pred---ps.md) e [Breakp-PS](break-p---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="b946e-164">The predicate register can also be applied to [if pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) and [breakp - ps](break-p---ps.md) instructions.</span></span> <span data-ttu-id="b946e-165">Queste istruzioni di controllo di flusso non hanno alcun aumento nel numero di slot di istruzioni quando si usa il registro predicato.</span><span class="sxs-lookup"><span data-stu-id="b946e-165">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b946e-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b946e-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b946e-167">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="b946e-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




