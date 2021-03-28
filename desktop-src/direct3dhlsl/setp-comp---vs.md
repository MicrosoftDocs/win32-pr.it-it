---
title: setp_comp-vs
description: Impostare il registro del predicato. | setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401888"
---
# <a name="setp_comp---vs"></a><span data-ttu-id="f41a6-104">setp \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="f41a6-104">setp\_comp - vs</span></span>

<span data-ttu-id="f41a6-105">Impostare il registro del predicato.</span><span class="sxs-lookup"><span data-stu-id="f41a6-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="f41a6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f41a6-106">Syntax</span></span>



| <span data-ttu-id="f41a6-107">setp \_ comp DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="f41a6-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="f41a6-108">Dove:</span><span class="sxs-lookup"><span data-stu-id="f41a6-108">Where:</span></span>

-   <span data-ttu-id="f41a6-109">\_comp è un confronto per canale tra i due registri di origine.</span><span class="sxs-lookup"><span data-stu-id="f41a6-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="f41a6-110">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f41a6-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="f41a6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f41a6-111">Syntax</span></span> | <span data-ttu-id="f41a6-112">Confronto</span><span class="sxs-lookup"><span data-stu-id="f41a6-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="f41a6-113">\_gt</span><span class="sxs-lookup"><span data-stu-id="f41a6-113">\_gt</span></span>   | <span data-ttu-id="f41a6-114">Maggiore di</span><span class="sxs-lookup"><span data-stu-id="f41a6-114">Greater than</span></span>          |
    | <span data-ttu-id="f41a6-115">\_lt</span><span class="sxs-lookup"><span data-stu-id="f41a6-115">\_lt</span></span>   | <span data-ttu-id="f41a6-116">Minore di</span><span class="sxs-lookup"><span data-stu-id="f41a6-116">Less than</span></span>             |
    | <span data-ttu-id="f41a6-117">\_GE</span><span class="sxs-lookup"><span data-stu-id="f41a6-117">\_ge</span></span>   | <span data-ttu-id="f41a6-118">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="f41a6-118">Greater than or equal</span></span> |
    | <span data-ttu-id="f41a6-119">\_le</span><span class="sxs-lookup"><span data-stu-id="f41a6-119">\_le</span></span>   | <span data-ttu-id="f41a6-120">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="f41a6-120">Less than or equal</span></span>    |
    | <span data-ttu-id="f41a6-121">\_EQ</span><span class="sxs-lookup"><span data-stu-id="f41a6-121">\_eq</span></span>   | <span data-ttu-id="f41a6-122">Uguale a</span><span class="sxs-lookup"><span data-stu-id="f41a6-122">Equal to</span></span>              |
    | <span data-ttu-id="f41a6-123">\_ne</span><span class="sxs-lookup"><span data-stu-id="f41a6-123">\_ne</span></span>   | <span data-ttu-id="f41a6-124">Diverso da</span><span class="sxs-lookup"><span data-stu-id="f41a6-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="f41a6-125">DST è il registro [Register del predicato](dx9-graphics-reference-asm-vs-registers-predicate.md) , P0.</span><span class="sxs-lookup"><span data-stu-id="f41a6-125">dst is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="f41a6-126">src0 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="f41a6-126">src0 is a source register.</span></span>
-   <span data-ttu-id="f41a6-127">src1 è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="f41a6-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f41a6-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="f41a6-128">Remarks</span></span>



| <span data-ttu-id="f41a6-129">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="f41a6-129">Vertex shader versions</span></span> | <span data-ttu-id="f41a6-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="f41a6-130">1\_1</span></span> | <span data-ttu-id="f41a6-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f41a6-131">2\_0</span></span> | <span data-ttu-id="f41a6-132">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f41a6-132">2\_x</span></span> | <span data-ttu-id="f41a6-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f41a6-133">2\_sw</span></span> | <span data-ttu-id="f41a6-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f41a6-134">3\_0</span></span> | <span data-ttu-id="f41a6-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f41a6-135">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f41a6-136">setp \_ comp</span><span class="sxs-lookup"><span data-stu-id="f41a6-136">setp\_comp</span></span>             |      |      | <span data-ttu-id="f41a6-137">x</span><span class="sxs-lookup"><span data-stu-id="f41a6-137">x</span></span>    | <span data-ttu-id="f41a6-138">x</span><span class="sxs-lookup"><span data-stu-id="f41a6-138">x</span></span>     | <span data-ttu-id="f41a6-139">x</span><span class="sxs-lookup"><span data-stu-id="f41a6-139">x</span></span>    | <span data-ttu-id="f41a6-140">x</span><span class="sxs-lookup"><span data-stu-id="f41a6-140">x</span></span>     |



 

<span data-ttu-id="f41a6-141">Questa istruzione funziona come segue:</span><span class="sxs-lookup"><span data-stu-id="f41a6-141">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="f41a6-142">Per ogni canale che può essere scritto in base alla maschera di scrittura di destinazione, salvare il risultato booleano dell'operazione di confronto tra i canali corrispondenti di src0 e src1 (dopo la risoluzione del modificatore di origine swizzles).</span><span class="sxs-lookup"><span data-stu-id="f41a6-142">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="f41a6-143">I registri di origine consentono di specificare un componente arbitrario swizzles.</span><span class="sxs-lookup"><span data-stu-id="f41a6-143">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="f41a6-144">Il registro di destinazione consente le maschere di scrittura arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="f41a6-144">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="f41a6-145">Il registro dest deve essere il registro predicato.</span><span class="sxs-lookup"><span data-stu-id="f41a6-145">The dest register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="f41a6-146">Applicazione del registro predicato</span><span class="sxs-lookup"><span data-stu-id="f41a6-146">Applying the Predicate Register</span></span>

<span data-ttu-id="f41a6-147">Una volta inizializzato il registro predicato con setp, è possibile usarlo per controllare un'istruzione per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="f41a6-147">Once the predicate register has been initialized with setp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="f41a6-148">Ecco la sintassi:</span><span class="sxs-lookup"><span data-stu-id="f41a6-148">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



<span data-ttu-id="f41a6-149">Dove:</span><span class="sxs-lookup"><span data-stu-id="f41a6-149">Where:</span></span>

-   <span data-ttu-id="f41a6-150">\[!\] è un valore booleano facoltativo NOT</span><span class="sxs-lookup"><span data-stu-id="f41a6-150">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="f41a6-151">P0 è il registro predicato</span><span class="sxs-lookup"><span data-stu-id="f41a6-151">p0 is the predicate register</span></span>
-   <span data-ttu-id="f41a6-152">\[. Swizzle \] è un swizzle facoltativo da applicare al contenuto del registro predicato prima di utilizzarlo per mascherare l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="f41a6-152">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="f41a6-153">I swizzles disponibili sono:. xyzw (impostazione predefinita quando non è specificato alcun parametro) o qualsiasi replica swizzle:. x/. r,. y/. g,. z/. b o. a/. w.</span><span class="sxs-lookup"><span data-stu-id="f41a6-153">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="f41a6-154">l'istruzione è qualsiasi aritmetic o istruzione di trama.</span><span class="sxs-lookup"><span data-stu-id="f41a6-154">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="f41a6-155">Non può essere un'istruzione di controllo di flusso statica o dinamica.</span><span class="sxs-lookup"><span data-stu-id="f41a6-155">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="f41a6-156">dest, srcReg,... sono i registri richiesti dall'istruzione</span><span class="sxs-lookup"><span data-stu-id="f41a6-156">dest, srcReg, ... are the registers required by the instruction</span></span>

<span data-ttu-id="f41a6-157">Supponendo che il registro dei predicati sia stato configurato con i valori dei componenti (true, true, false, false), è possibile applicare questa istruzione:</span><span class="sxs-lookup"><span data-stu-id="f41a6-157">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



<span data-ttu-id="f41a6-158">per eseguire un'aggiunta a 2 componenti.</span><span class="sxs-lookup"><span data-stu-id="f41a6-158">to perform a 2 component add.</span></span>


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



<span data-ttu-id="f41a6-159">I componenti x e y di R2 non verranno scritti poiché il registro predicato contiene false nei componenti z e w.</span><span class="sxs-lookup"><span data-stu-id="f41a6-159">The x and y components of r2 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="f41a6-160">Se si applica il registro predicato a un'istruzione aritmetica o di trama, il numero di slot di istruzioni aumenta di 1.</span><span class="sxs-lookup"><span data-stu-id="f41a6-160">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="f41a6-161">Il registro predicato può essere applicato anche a se le istruzioni [prede-vs](if-pred---vs.md), [callnz prede-vs](callnz-pred---vs.md) e [Breakp-vs](breakp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="f41a6-161">The predicate register can also be applied to [if pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) and [breakp - vs](breakp---vs.md) instructions.</span></span> <span data-ttu-id="f41a6-162">Queste istruzioni di controllo di flusso non hanno alcun aumento nel numero di slot di istruzioni quando si usa il registro predicato.</span><span class="sxs-lookup"><span data-stu-id="f41a6-162">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f41a6-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f41a6-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f41a6-164">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="f41a6-164">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




