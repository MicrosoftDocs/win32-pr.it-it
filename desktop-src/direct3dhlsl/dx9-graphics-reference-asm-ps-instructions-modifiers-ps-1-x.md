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
ms.openlocfilehash: 6c97196040a8f5f9888cb2fb354dcc18ca3743c7
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988726"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="c51a5-104">Modificatori per ps \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="c51a5-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="c51a5-105">I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c51a5-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="c51a5-106">Ad esempio, usarli per moltiplicare o dividere il risultato per un fattore di due o per stringere il risultato tra zero e uno.</span><span class="sxs-lookup"><span data-stu-id="c51a5-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="c51a5-107">I modificatori di istruzione vengono applicati dopo l'esecuzione dell'istruzione, ma prima della scrittura del risultato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c51a5-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="c51a5-108">Di seguito è riportato un elenco dei modificatori.</span><span class="sxs-lookup"><span data-stu-id="c51a5-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="c51a5-109">Modificatore</span><span class="sxs-lookup"><span data-stu-id="c51a5-109">Modifier</span></span> | <span data-ttu-id="c51a5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c51a5-110">Description</span></span>                   | <span data-ttu-id="c51a5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c51a5-111">Syntax</span></span>           | <span data-ttu-id="c51a5-112">Versione</span><span class="sxs-lookup"><span data-stu-id="c51a5-112">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="c51a5-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="c51a5-113">1\_1</span></span>    | <span data-ttu-id="c51a5-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="c51a5-114">1\_2</span></span> | <span data-ttu-id="c51a5-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c51a5-115">1\_3</span></span> | <span data-ttu-id="c51a5-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="c51a5-116">1\_4</span></span> |
| <span data-ttu-id="c51a5-117">\_x2</span><span class="sxs-lookup"><span data-stu-id="c51a5-117">\_x2</span></span>     | <span data-ttu-id="c51a5-118">Moltiplica per 2</span><span class="sxs-lookup"><span data-stu-id="c51a5-118">Multiply by 2</span></span>                 | <span data-ttu-id="c51a5-119">istruzione \_ x2</span><span class="sxs-lookup"><span data-stu-id="c51a5-119">instruction\_x2</span></span>  | <span data-ttu-id="c51a5-120">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-120">X</span></span>       | <span data-ttu-id="c51a5-121">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-121">X</span></span>    | <span data-ttu-id="c51a5-122">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-122">X</span></span>    | <span data-ttu-id="c51a5-123">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-123">X</span></span>    |
| <span data-ttu-id="c51a5-124">\_x4</span><span class="sxs-lookup"><span data-stu-id="c51a5-124">\_x4</span></span>     | <span data-ttu-id="c51a5-125">Moltiplica per 4</span><span class="sxs-lookup"><span data-stu-id="c51a5-125">Multiply by 4</span></span>                 | <span data-ttu-id="c51a5-126">istruzione \_ x4</span><span class="sxs-lookup"><span data-stu-id="c51a5-126">instruction\_x4</span></span>  | <span data-ttu-id="c51a5-127">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-127">X</span></span>       | <span data-ttu-id="c51a5-128">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-128">X</span></span>    | <span data-ttu-id="c51a5-129">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-129">X</span></span>    | <span data-ttu-id="c51a5-130">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-130">X</span></span>    |
| <span data-ttu-id="c51a5-131">\_x8</span><span class="sxs-lookup"><span data-stu-id="c51a5-131">\_x8</span></span>     | <span data-ttu-id="c51a5-132">Moltiplica per 8</span><span class="sxs-lookup"><span data-stu-id="c51a5-132">Multiply by 8</span></span>                 | <span data-ttu-id="c51a5-133">istruzione \_ x8</span><span class="sxs-lookup"><span data-stu-id="c51a5-133">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="c51a5-134">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-134">X</span></span>    |
| <span data-ttu-id="c51a5-135">\_d2</span><span class="sxs-lookup"><span data-stu-id="c51a5-135">\_d2</span></span>     | <span data-ttu-id="c51a5-136">Divisione per 2</span><span class="sxs-lookup"><span data-stu-id="c51a5-136">Divide by 2</span></span>                   | <span data-ttu-id="c51a5-137">istruzione \_ d2</span><span class="sxs-lookup"><span data-stu-id="c51a5-137">instruction\_d2</span></span>  | <span data-ttu-id="c51a5-138">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-138">X</span></span>       | <span data-ttu-id="c51a5-139">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-139">X</span></span>    | <span data-ttu-id="c51a5-140">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-140">X</span></span>    | <span data-ttu-id="c51a5-141">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-141">X</span></span>    |
| <span data-ttu-id="c51a5-142">\_d4</span><span class="sxs-lookup"><span data-stu-id="c51a5-142">\_d4</span></span>     | <span data-ttu-id="c51a5-143">Divisione per 4</span><span class="sxs-lookup"><span data-stu-id="c51a5-143">Divide by 4</span></span>                   | <span data-ttu-id="c51a5-144">istruzione \_ d4</span><span class="sxs-lookup"><span data-stu-id="c51a5-144">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="c51a5-145">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-145">X</span></span>    |
| <span data-ttu-id="c51a5-146">\_d8</span><span class="sxs-lookup"><span data-stu-id="c51a5-146">\_d8</span></span>     | <span data-ttu-id="c51a5-147">Divisione per 8</span><span class="sxs-lookup"><span data-stu-id="c51a5-147">Divide by 8</span></span>                   | <span data-ttu-id="c51a5-148">istruzione \_ d8</span><span class="sxs-lookup"><span data-stu-id="c51a5-148">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="c51a5-149">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-149">X</span></span>    |
| <span data-ttu-id="c51a5-150">\_Sab</span><span class="sxs-lookup"><span data-stu-id="c51a5-150">\_sat</span></span>    | <span data-ttu-id="c51a5-151">Saturazione (0 e 1)</span><span class="sxs-lookup"><span data-stu-id="c51a5-151">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="c51a5-152">istruzione \_ sat</span><span class="sxs-lookup"><span data-stu-id="c51a5-152">instruction\_sat</span></span> | <span data-ttu-id="c51a5-153">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-153">X</span></span>       | <span data-ttu-id="c51a5-154">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-154">X</span></span>    | <span data-ttu-id="c51a5-155">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-155">X</span></span>    | <span data-ttu-id="c51a5-156">X</span><span class="sxs-lookup"><span data-stu-id="c51a5-156">X</span></span>    |



 

-   <span data-ttu-id="c51a5-157">Il modificatore multiply moltiplica i dati del registro per una potenza di due dopo la lettura.</span><span class="sxs-lookup"><span data-stu-id="c51a5-157">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="c51a5-158">Corrisponde a uno spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="c51a5-158">This is the same as a shift left.</span></span>
-   <span data-ttu-id="c51a5-159">Il modificatore divide divide i dati del registro per una potenza di due dopo la lettura.</span><span class="sxs-lookup"><span data-stu-id="c51a5-159">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="c51a5-160">Corrisponde a uno spostamento a destra.</span><span class="sxs-lookup"><span data-stu-id="c51a5-160">This is the same as a shift right.</span></span>
-   <span data-ttu-id="c51a5-161">Il modificatore saturate stringe l'intervallo di valori di registro da zero a uno.</span><span class="sxs-lookup"><span data-stu-id="c51a5-161">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="c51a5-162">I modificatori di istruzione possono essere usati nelle istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="c51a5-162">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="c51a5-163">Non possono essere usati nelle istruzioni relative all'indirizzo della trama.</span><span class="sxs-lookup"><span data-stu-id="c51a5-163">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="c51a5-164">Modificatore di moltiplicazione</span><span class="sxs-lookup"><span data-stu-id="c51a5-164">Multiply modifier</span></span>

<span data-ttu-id="c51a5-165">Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e moltiplica il risultato per due.</span><span class="sxs-lookup"><span data-stu-id="c51a5-165">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="c51a5-166">In questo esempio vengono combinati due modificatori di istruzione.</span><span class="sxs-lookup"><span data-stu-id="c51a5-166">This example combines two instruction modifiers.</span></span> <span data-ttu-id="c51a5-167">In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1).</span><span class="sxs-lookup"><span data-stu-id="c51a5-167">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="c51a5-168">Il risultato viene quindi moltiplicato per due e con un numero di elementi compreso tra 0,0 e 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="c51a5-168">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="c51a5-169">Il risultato viene salvato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c51a5-169">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="c51a5-170">Modificatore divide</span><span class="sxs-lookup"><span data-stu-id="c51a5-170">Divide modifier</span></span>

<span data-ttu-id="c51a5-171">Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e divide il risultato per due.</span><span class="sxs-lookup"><span data-stu-id="c51a5-171">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="c51a5-172">Modificatore Saturate</span><span class="sxs-lookup"><span data-stu-id="c51a5-172">Saturate modifier</span></span>

<span data-ttu-id="c51a5-173">Per le istruzioni aritmetiche, il modificatore di saturazione stringe il risultato di questa istruzione nell'intervallo da 0.0 a 1.0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="c51a5-173">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="c51a5-174">Nell'esempio seguente viene illustrato come usare questo modificatore di istruzione.</span><span class="sxs-lookup"><span data-stu-id="c51a5-174">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="c51a5-175">Questa operazione si verifica dopo qualsiasi modificatore di istruzione di moltiplicazione o divisione.</span><span class="sxs-lookup"><span data-stu-id="c51a5-175">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="c51a5-176">\_sat viene usato più spesso per stringere i risultati del prodotto punto.</span><span class="sxs-lookup"><span data-stu-id="c51a5-176">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="c51a5-177">Tuttavia, consente anche l'emulazione coerente dei metodi multi-passaggio in cui il buffer dei frame è sempre compreso nell'intervallo da 0 a 1 e della sintassi multitesto DirectX 6 e 7.0, in cui la saturazione è definita in ogni fase.</span><span class="sxs-lookup"><span data-stu-id="c51a5-177">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="c51a5-178">Questo esempio carica il registro di destinazione (dest) con la somma dei due colori negli operandi di origine (src0 e src1) e stringe il risultato nell'intervallo da 0,0 a 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="c51a5-178">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="c51a5-179">In questo esempio vengono combinati due modificatori di istruzione.</span><span class="sxs-lookup"><span data-stu-id="c51a5-179">This example combines two instruction modifiers.</span></span> <span data-ttu-id="c51a5-180">In primo luogo, vengono aggiunti due colori negli operandi di origine (src0 e src1).</span><span class="sxs-lookup"><span data-stu-id="c51a5-180">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="c51a5-181">Il risultato viene moltiplicato per due e con un numero di elementi compreso tra 0,0 e 1,0 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="c51a5-181">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="c51a5-182">Il risultato viene salvato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c51a5-182">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="c51a5-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c51a5-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c51a5-184">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="c51a5-184">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




