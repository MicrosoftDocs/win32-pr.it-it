---
title: Modificatori per ps_1_X
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione. Informazioni sui modificatori per ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9291d818252c95bc11fae72bd3311ec733a45fa
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129940"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="be352-104">Modificatori per ps \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="be352-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="be352-105">I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be352-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="be352-106">Ad esempio, usarli per moltiplicare o dividere il risultato per un fattore di due o per stringere il risultato tra zero e uno.</span><span class="sxs-lookup"><span data-stu-id="be352-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="be352-107">I modificatori di istruzione vengono applicati dopo l'esecuzione dell'istruzione, ma prima di scrivere il risultato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be352-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="be352-108">Di seguito è riportato un elenco dei modificatori.</span><span class="sxs-lookup"><span data-stu-id="be352-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="be352-109">Modificatore</span><span class="sxs-lookup"><span data-stu-id="be352-109">Modifier</span></span> | <span data-ttu-id="be352-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be352-110">Description</span></span>                   | <span data-ttu-id="be352-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be352-111">Syntax</span></span>           | <span data-ttu-id="be352-112">Versione 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="be352-112">Version 1\_1</span></span> | <span data-ttu-id="be352-113">Versione 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="be352-113">Version 1\_2</span></span>     |<span data-ttu-id="be352-114">Versione 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="be352-114">Version  1\_3</span></span>    | <span data-ttu-id="be352-115">Versione 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="be352-115">Version 1\_4</span></span>    |
|----------|-------------------------------|------------------|---------|------|------|------|
| <span data-ttu-id="be352-116">\_x2</span><span class="sxs-lookup"><span data-stu-id="be352-116">\_x2</span></span>     | <span data-ttu-id="be352-117">Moltiplicare per 2</span><span class="sxs-lookup"><span data-stu-id="be352-117">Multiply by 2</span></span>                 | <span data-ttu-id="be352-118">istruzione \_ x2</span><span class="sxs-lookup"><span data-stu-id="be352-118">instruction\_x2</span></span>  | <span data-ttu-id="be352-119">X</span><span class="sxs-lookup"><span data-stu-id="be352-119">X</span></span>       | <span data-ttu-id="be352-120">X</span><span class="sxs-lookup"><span data-stu-id="be352-120">X</span></span>    | <span data-ttu-id="be352-121">X</span><span class="sxs-lookup"><span data-stu-id="be352-121">X</span></span>    | <span data-ttu-id="be352-122">X</span><span class="sxs-lookup"><span data-stu-id="be352-122">X</span></span>    |
| <span data-ttu-id="be352-123">\_x4</span><span class="sxs-lookup"><span data-stu-id="be352-123">\_x4</span></span>     | <span data-ttu-id="be352-124">Moltiplicare per 4</span><span class="sxs-lookup"><span data-stu-id="be352-124">Multiply by 4</span></span>                 | <span data-ttu-id="be352-125">istruzione \_ x4</span><span class="sxs-lookup"><span data-stu-id="be352-125">instruction\_x4</span></span>  | <span data-ttu-id="be352-126">X</span><span class="sxs-lookup"><span data-stu-id="be352-126">X</span></span>       | <span data-ttu-id="be352-127">X</span><span class="sxs-lookup"><span data-stu-id="be352-127">X</span></span>    | <span data-ttu-id="be352-128">X</span><span class="sxs-lookup"><span data-stu-id="be352-128">X</span></span>    | <span data-ttu-id="be352-129">X</span><span class="sxs-lookup"><span data-stu-id="be352-129">X</span></span>    |
| <span data-ttu-id="be352-130">\_x8</span><span class="sxs-lookup"><span data-stu-id="be352-130">\_x8</span></span>     | <span data-ttu-id="be352-131">Moltiplicare per 8</span><span class="sxs-lookup"><span data-stu-id="be352-131">Multiply by 8</span></span>                 | <span data-ttu-id="be352-132">istruzione \_ x8</span><span class="sxs-lookup"><span data-stu-id="be352-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="be352-133">X</span><span class="sxs-lookup"><span data-stu-id="be352-133">X</span></span>    |
| <span data-ttu-id="be352-134">\_d2</span><span class="sxs-lookup"><span data-stu-id="be352-134">\_d2</span></span>     | <span data-ttu-id="be352-135">Dividere per 2</span><span class="sxs-lookup"><span data-stu-id="be352-135">Divide by 2</span></span>                   | <span data-ttu-id="be352-136">istruzione \_ d2</span><span class="sxs-lookup"><span data-stu-id="be352-136">instruction\_d2</span></span>  | <span data-ttu-id="be352-137">X</span><span class="sxs-lookup"><span data-stu-id="be352-137">X</span></span>       | <span data-ttu-id="be352-138">X</span><span class="sxs-lookup"><span data-stu-id="be352-138">X</span></span>    | <span data-ttu-id="be352-139">X</span><span class="sxs-lookup"><span data-stu-id="be352-139">X</span></span>    | <span data-ttu-id="be352-140">X</span><span class="sxs-lookup"><span data-stu-id="be352-140">X</span></span>    |
| <span data-ttu-id="be352-141">\_d4</span><span class="sxs-lookup"><span data-stu-id="be352-141">\_d4</span></span>     | <span data-ttu-id="be352-142">Dividere per 4</span><span class="sxs-lookup"><span data-stu-id="be352-142">Divide by 4</span></span>                   | <span data-ttu-id="be352-143">istruzione \_ d4</span><span class="sxs-lookup"><span data-stu-id="be352-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="be352-144">X</span><span class="sxs-lookup"><span data-stu-id="be352-144">X</span></span>    |
| <span data-ttu-id="be352-145">\_d8</span><span class="sxs-lookup"><span data-stu-id="be352-145">\_d8</span></span>     | <span data-ttu-id="be352-146">Dividere per 8</span><span class="sxs-lookup"><span data-stu-id="be352-146">Divide by 8</span></span>                   | <span data-ttu-id="be352-147">istruzione \_ d8</span><span class="sxs-lookup"><span data-stu-id="be352-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="be352-148">X</span><span class="sxs-lookup"><span data-stu-id="be352-148">X</span></span>    |
| <span data-ttu-id="be352-149">\_Sab</span><span class="sxs-lookup"><span data-stu-id="be352-149">\_sat</span></span>    | <span data-ttu-id="be352-150">Saturazione (chiusura da 0 e 1)</span><span class="sxs-lookup"><span data-stu-id="be352-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="be352-151">istruzione \_ sab</span><span class="sxs-lookup"><span data-stu-id="be352-151">instruction\_sat</span></span> | <span data-ttu-id="be352-152">X</span><span class="sxs-lookup"><span data-stu-id="be352-152">X</span></span>       | <span data-ttu-id="be352-153">X</span><span class="sxs-lookup"><span data-stu-id="be352-153">X</span></span>    | <span data-ttu-id="be352-154">X</span><span class="sxs-lookup"><span data-stu-id="be352-154">X</span></span>    | <span data-ttu-id="be352-155">X</span><span class="sxs-lookup"><span data-stu-id="be352-155">X</span></span>    |



 

-   <span data-ttu-id="be352-156">Il modificatore multiply moltiplica i dati del registro per una potenza di due dopo la lettura.</span><span class="sxs-lookup"><span data-stu-id="be352-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="be352-157">Questo è lo stesso di uno spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="be352-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="be352-158">Il modificatore divide divide i dati del registro per una potenza di due dopo la lettura.</span><span class="sxs-lookup"><span data-stu-id="be352-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="be352-159">Questo è lo stesso di uno spostamento a destra.</span><span class="sxs-lookup"><span data-stu-id="be352-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="be352-160">Il modificatore saturate stringe l'intervallo di valori di registro da zero a uno.</span><span class="sxs-lookup"><span data-stu-id="be352-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="be352-161">I modificatori di istruzione possono essere usati nelle istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="be352-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="be352-162">Non possono essere usati nelle istruzioni relative all'indirizzo della trama.</span><span class="sxs-lookup"><span data-stu-id="be352-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="be352-163">Modificatore Multiply</span><span class="sxs-lookup"><span data-stu-id="be352-163">Multiply modifier</span></span>

<span data-ttu-id="be352-164">Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e moltiplica il risultato per due.</span><span class="sxs-lookup"><span data-stu-id="be352-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="be352-165">In questo esempio vengono combinati due modificatori di istruzione.</span><span class="sxs-lookup"><span data-stu-id="be352-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="be352-166">In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1).</span><span class="sxs-lookup"><span data-stu-id="be352-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="be352-167">Il risultato viene quindi moltiplicato per due e con un intervallo compreso tra 0,0 e 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="be352-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="be352-168">Il risultato viene salvato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be352-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="be352-169">Modificatore divide</span><span class="sxs-lookup"><span data-stu-id="be352-169">Divide modifier</span></span>

<span data-ttu-id="be352-170">Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e divide il risultato per due.</span><span class="sxs-lookup"><span data-stu-id="be352-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="be352-171">Modificatore Saturate</span><span class="sxs-lookup"><span data-stu-id="be352-171">Saturate modifier</span></span>

<span data-ttu-id="be352-172">Per le istruzioni aritmetiche, il modificatore di saturazione consente di impostare il risultato di questa istruzione nell'intervallo da 0.0 a 1.0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="be352-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="be352-173">Nell'esempio seguente viene illustrato come usare questo modificatore di istruzione.</span><span class="sxs-lookup"><span data-stu-id="be352-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="be352-174">Questa operazione si verifica dopo qualsiasi modificatore di istruzione di moltiplicazione o divisione.</span><span class="sxs-lookup"><span data-stu-id="be352-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="be352-175">\_sat viene usato più spesso per stringere i risultati del prodotto del punto.</span><span class="sxs-lookup"><span data-stu-id="be352-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="be352-176">Tuttavia, consente anche l'emulazione coerente dei metodi multipass in cui il buffer dei frame è sempre compreso nell'intervallo da 0 a 1 e della sintassi multitesto DirectX 6 e 7.0, in cui la saturazione è definita per verificarsi in ogni fase.</span><span class="sxs-lookup"><span data-stu-id="be352-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="be352-177">In questo esempio viene caricato il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e il risultato viene inserito nell'intervallo da 0,0 a 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="be352-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="be352-178">In questo esempio vengono combinati due modificatori di istruzione.</span><span class="sxs-lookup"><span data-stu-id="be352-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="be352-179">In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1).</span><span class="sxs-lookup"><span data-stu-id="be352-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="be352-180">Il risultato viene moltiplicato per due e con un intervallo compreso tra 0,0 e 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="be352-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="be352-181">Il risultato viene salvato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="be352-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="be352-182">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be352-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be352-183">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="be352-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




