---
title: Modificatori per ps_1_X
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856958"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="5eca8-103">Modificatori per PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="5eca8-103">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="5eca8-104">I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5eca8-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="5eca8-105">Usare, ad esempio, per moltiplicare o dividere il risultato per un fattore di due o per bloccare il risultato tra zero e uno.</span><span class="sxs-lookup"><span data-stu-id="5eca8-105">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="5eca8-106">I modificatori di istruzione vengono applicati dopo l'esecuzione dell'istruzione, ma prima di scrivere il risultato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5eca8-106">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="5eca8-107">Di seguito è riportato un elenco dei modificatori.</span><span class="sxs-lookup"><span data-stu-id="5eca8-107">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="5eca8-108">Modificatore</span><span class="sxs-lookup"><span data-stu-id="5eca8-108">Modifier</span></span> | <span data-ttu-id="5eca8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eca8-109">Description</span></span>                   | <span data-ttu-id="5eca8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5eca8-110">Syntax</span></span>           | <span data-ttu-id="5eca8-111">Versione</span><span class="sxs-lookup"><span data-stu-id="5eca8-111">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="5eca8-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="5eca8-112">1\_1</span></span>    | <span data-ttu-id="5eca8-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="5eca8-113">1\_2</span></span> | <span data-ttu-id="5eca8-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5eca8-114">1\_3</span></span> | <span data-ttu-id="5eca8-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="5eca8-115">1\_4</span></span> |
| <span data-ttu-id="5eca8-116">\_X2</span><span class="sxs-lookup"><span data-stu-id="5eca8-116">\_x2</span></span>     | <span data-ttu-id="5eca8-117">Moltiplica per 2</span><span class="sxs-lookup"><span data-stu-id="5eca8-117">Multiply by 2</span></span>                 | <span data-ttu-id="5eca8-118">istruzione \_ X2</span><span class="sxs-lookup"><span data-stu-id="5eca8-118">instruction\_x2</span></span>  | <span data-ttu-id="5eca8-119">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-119">X</span></span>       | <span data-ttu-id="5eca8-120">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-120">X</span></span>    | <span data-ttu-id="5eca8-121">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-121">X</span></span>    | <span data-ttu-id="5eca8-122">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-122">X</span></span>    |
| <span data-ttu-id="5eca8-123">\_X4</span><span class="sxs-lookup"><span data-stu-id="5eca8-123">\_x4</span></span>     | <span data-ttu-id="5eca8-124">Moltiplica per 4</span><span class="sxs-lookup"><span data-stu-id="5eca8-124">Multiply by 4</span></span>                 | <span data-ttu-id="5eca8-125">istruzioni \_ X4</span><span class="sxs-lookup"><span data-stu-id="5eca8-125">instruction\_x4</span></span>  | <span data-ttu-id="5eca8-126">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-126">X</span></span>       | <span data-ttu-id="5eca8-127">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-127">X</span></span>    | <span data-ttu-id="5eca8-128">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-128">X</span></span>    | <span data-ttu-id="5eca8-129">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-129">X</span></span>    |
| <span data-ttu-id="5eca8-130">\_X8</span><span class="sxs-lookup"><span data-stu-id="5eca8-130">\_x8</span></span>     | <span data-ttu-id="5eca8-131">Moltiplica per 8</span><span class="sxs-lookup"><span data-stu-id="5eca8-131">Multiply by 8</span></span>                 | <span data-ttu-id="5eca8-132">istruzione \_ x8</span><span class="sxs-lookup"><span data-stu-id="5eca8-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="5eca8-133">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-133">X</span></span>    |
| <span data-ttu-id="5eca8-134">\_D2</span><span class="sxs-lookup"><span data-stu-id="5eca8-134">\_d2</span></span>     | <span data-ttu-id="5eca8-135">Divisione per 2</span><span class="sxs-lookup"><span data-stu-id="5eca8-135">Divide by 2</span></span>                   | <span data-ttu-id="5eca8-136">istruzioni \_ D2</span><span class="sxs-lookup"><span data-stu-id="5eca8-136">instruction\_d2</span></span>  | <span data-ttu-id="5eca8-137">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-137">X</span></span>       | <span data-ttu-id="5eca8-138">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-138">X</span></span>    | <span data-ttu-id="5eca8-139">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-139">X</span></span>    | <span data-ttu-id="5eca8-140">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-140">X</span></span>    |
| <span data-ttu-id="5eca8-141">\_D4</span><span class="sxs-lookup"><span data-stu-id="5eca8-141">\_d4</span></span>     | <span data-ttu-id="5eca8-142">Divisione per 4</span><span class="sxs-lookup"><span data-stu-id="5eca8-142">Divide by 4</span></span>                   | <span data-ttu-id="5eca8-143">istruzione \_ D4</span><span class="sxs-lookup"><span data-stu-id="5eca8-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="5eca8-144">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-144">X</span></span>    |
| <span data-ttu-id="5eca8-145">\_D8</span><span class="sxs-lookup"><span data-stu-id="5eca8-145">\_d8</span></span>     | <span data-ttu-id="5eca8-146">Divisione per 8</span><span class="sxs-lookup"><span data-stu-id="5eca8-146">Divide by 8</span></span>                   | <span data-ttu-id="5eca8-147">istruzione \_ D8</span><span class="sxs-lookup"><span data-stu-id="5eca8-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="5eca8-148">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-148">X</span></span>    |
| <span data-ttu-id="5eca8-149">\_Sat</span><span class="sxs-lookup"><span data-stu-id="5eca8-149">\_sat</span></span>    | <span data-ttu-id="5eca8-150">Satura (morsetto da 0 a 1)</span><span class="sxs-lookup"><span data-stu-id="5eca8-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="5eca8-151">istruzioni \_ Sat</span><span class="sxs-lookup"><span data-stu-id="5eca8-151">instruction\_sat</span></span> | <span data-ttu-id="5eca8-152">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-152">X</span></span>       | <span data-ttu-id="5eca8-153">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-153">X</span></span>    | <span data-ttu-id="5eca8-154">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-154">X</span></span>    | <span data-ttu-id="5eca8-155">X</span><span class="sxs-lookup"><span data-stu-id="5eca8-155">X</span></span>    |



 

-   <span data-ttu-id="5eca8-156">Il modificatore Multiply Moltiplica i dati del registro per una potenza di due dopo che è stata letta.</span><span class="sxs-lookup"><span data-stu-id="5eca8-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="5eca8-157">Si tratta dello stesso valore di Shift Left.</span><span class="sxs-lookup"><span data-stu-id="5eca8-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="5eca8-158">Il modificatore divide divide i dati del registro per una potenza di due dopo che è stato letto.</span><span class="sxs-lookup"><span data-stu-id="5eca8-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="5eca8-159">Si tratta della stessa operazione di spostamento a destra.</span><span class="sxs-lookup"><span data-stu-id="5eca8-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="5eca8-160">Il modificatore di saturazione blocca l'intervallo di valori di registro da zero a uno.</span><span class="sxs-lookup"><span data-stu-id="5eca8-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="5eca8-161">I modificatori di istruzione possono essere utilizzati nelle istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="5eca8-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="5eca8-162">Non possono essere usate nelle istruzioni relative all'indirizzo della trama.</span><span class="sxs-lookup"><span data-stu-id="5eca8-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="5eca8-163">Modificatore Multiply</span><span class="sxs-lookup"><span data-stu-id="5eca8-163">Multiply modifier</span></span>

<span data-ttu-id="5eca8-164">In questo esempio viene caricato il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e viene moltiplicato per due il risultato.</span><span class="sxs-lookup"><span data-stu-id="5eca8-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="5eca8-165">In questo esempio vengono combinati due modificatori di istruzione.</span><span class="sxs-lookup"><span data-stu-id="5eca8-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="5eca8-166">In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1).</span><span class="sxs-lookup"><span data-stu-id="5eca8-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="5eca8-167">Il risultato viene quindi moltiplicato per due e fissato tra 0,0 e 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="5eca8-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="5eca8-168">Il risultato viene salvato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5eca8-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="5eca8-169">Modificatore di divisione</span><span class="sxs-lookup"><span data-stu-id="5eca8-169">Divide modifier</span></span>

<span data-ttu-id="5eca8-170">In questo esempio viene caricato il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e il risultato viene diviso per due.</span><span class="sxs-lookup"><span data-stu-id="5eca8-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="5eca8-171">Modificatore saturazione</span><span class="sxs-lookup"><span data-stu-id="5eca8-171">Saturate modifier</span></span>

<span data-ttu-id="5eca8-172">Per istruzioni aritmetiche, il modificatore di saturazione blocca il risultato di questa istruzione nell'intervallo compreso tra 0,0 e 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="5eca8-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="5eca8-173">Nell'esempio seguente viene illustrato come utilizzare questo modificatore di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="5eca8-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="5eca8-174">Questa operazione si verifica dopo qualsiasi modificatore di istruzione Multiply o divide.</span><span class="sxs-lookup"><span data-stu-id="5eca8-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="5eca8-175">\_Sat viene usato più spesso per bloccare i risultati dei prodotti in un punto.</span><span class="sxs-lookup"><span data-stu-id="5eca8-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="5eca8-176">Tuttavia, consente anche un'emulazione coerente di metodi MultiPASS, in cui il buffer dei frame è sempre compreso tra 0 e 1 e la sintassi multitrama di DirectX 6 e 7,0, in cui la saturazione viene definita in ogni fase.</span><span class="sxs-lookup"><span data-stu-id="5eca8-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="5eca8-177">Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e blocca il risultato nell'intervallo compreso tra 0,0 e 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="5eca8-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="5eca8-178">In questo esempio vengono combinati due modificatori di istruzione.</span><span class="sxs-lookup"><span data-stu-id="5eca8-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="5eca8-179">In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1).</span><span class="sxs-lookup"><span data-stu-id="5eca8-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="5eca8-180">Il risultato viene moltiplicato per due e fissato tra 0,0 e 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="5eca8-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="5eca8-181">Il risultato viene salvato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5eca8-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="5eca8-182">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5eca8-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eca8-183">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="5eca8-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




