---
title: Modificatori del registro di origine pixel shader
description: Usare i modificatori del registro di origine per modificare il valore letto da un registro prima dell'esecuzione di un'istruzione.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332615"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="18b83-103">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="18b83-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="18b83-104">Usare i modificatori del registro di origine per modificare il valore letto da un registro prima dell'esecuzione di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="18b83-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="18b83-105">Il contenuto di un registro di origine viene lasciato invariato.</span><span class="sxs-lookup"><span data-stu-id="18b83-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="18b83-106">I modificatori sono utili per modificare l'intervallo dei dati del registro in preparazione all'istruzione.</span><span class="sxs-lookup"><span data-stu-id="18b83-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="18b83-107">Un set di modificatori chiamati selettori copia o replica i dati da un singolo canale (r, g, b, a) negli altri canali.</span><span class="sxs-lookup"><span data-stu-id="18b83-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="18b83-108">PS \_ 1 \_ 1-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="18b83-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="18b83-109">Questa tabella identifica le versioni che supportano ogni modificatore:</span><span class="sxs-lookup"><span data-stu-id="18b83-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="18b83-110">Modificatori del registro di origine</span><span class="sxs-lookup"><span data-stu-id="18b83-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="18b83-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18b83-111">Syntax</span></span>         | <span data-ttu-id="18b83-112">Versione</span><span class="sxs-lookup"><span data-stu-id="18b83-112">Version</span></span> |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | <span data-ttu-id="18b83-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="18b83-113">1\_1</span></span>    | <span data-ttu-id="18b83-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="18b83-114">1\_2</span></span> | <span data-ttu-id="18b83-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="18b83-115">1\_3</span></span> | <span data-ttu-id="18b83-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="18b83-116">1\_4</span></span> |     |     |
| [<span data-ttu-id="18b83-117">distorsione</span><span class="sxs-lookup"><span data-stu-id="18b83-117">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="18b83-118">\_distorsione registro</span><span class="sxs-lookup"><span data-stu-id="18b83-118">register\_bias</span></span> | <span data-ttu-id="18b83-119">X</span><span class="sxs-lookup"><span data-stu-id="18b83-119">X</span></span>       | <span data-ttu-id="18b83-120">X</span><span class="sxs-lookup"><span data-stu-id="18b83-120">X</span></span>    | <span data-ttu-id="18b83-121">X</span><span class="sxs-lookup"><span data-stu-id="18b83-121">X</span></span>    | <span data-ttu-id="18b83-122">X</span><span class="sxs-lookup"><span data-stu-id="18b83-122">X</span></span>    |     |     |
| [<span data-ttu-id="18b83-123">inversione</span><span class="sxs-lookup"><span data-stu-id="18b83-123">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="18b83-124">1-registrazione</span><span class="sxs-lookup"><span data-stu-id="18b83-124">1 - register</span></span>   | <span data-ttu-id="18b83-125">X</span><span class="sxs-lookup"><span data-stu-id="18b83-125">X</span></span>       | <span data-ttu-id="18b83-126">X</span><span class="sxs-lookup"><span data-stu-id="18b83-126">X</span></span>    | <span data-ttu-id="18b83-127">X</span><span class="sxs-lookup"><span data-stu-id="18b83-127">X</span></span>    | <span data-ttu-id="18b83-128">X</span><span class="sxs-lookup"><span data-stu-id="18b83-128">X</span></span>    |     |     |
| [<span data-ttu-id="18b83-129">negate</span><span class="sxs-lookup"><span data-stu-id="18b83-129">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="18b83-130">\- Registro</span><span class="sxs-lookup"><span data-stu-id="18b83-130">\- register</span></span>    | <span data-ttu-id="18b83-131">X</span><span class="sxs-lookup"><span data-stu-id="18b83-131">X</span></span>       | <span data-ttu-id="18b83-132">X</span><span class="sxs-lookup"><span data-stu-id="18b83-132">X</span></span>    | <span data-ttu-id="18b83-133">X</span><span class="sxs-lookup"><span data-stu-id="18b83-133">X</span></span>    | <span data-ttu-id="18b83-134">X</span><span class="sxs-lookup"><span data-stu-id="18b83-134">X</span></span>    |     |     |
| [<span data-ttu-id="18b83-135">Ridimensiona per 2</span><span class="sxs-lookup"><span data-stu-id="18b83-135">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="18b83-136">Registra \_ X2</span><span class="sxs-lookup"><span data-stu-id="18b83-136">register\_x2</span></span>   |         |      |      | <span data-ttu-id="18b83-137">X</span><span class="sxs-lookup"><span data-stu-id="18b83-137">X</span></span>    |     |     |
| [<span data-ttu-id="18b83-138">scalabilità con segno</span><span class="sxs-lookup"><span data-stu-id="18b83-138">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="18b83-139">Registra \_ BX2</span><span class="sxs-lookup"><span data-stu-id="18b83-139">register\_bx2</span></span>  | <span data-ttu-id="18b83-140">X</span><span class="sxs-lookup"><span data-stu-id="18b83-140">X</span></span>       | <span data-ttu-id="18b83-141">X</span><span class="sxs-lookup"><span data-stu-id="18b83-141">X</span></span>    | <span data-ttu-id="18b83-142">X</span><span class="sxs-lookup"><span data-stu-id="18b83-142">X</span></span>    | <span data-ttu-id="18b83-143">X</span><span class="sxs-lookup"><span data-stu-id="18b83-143">X</span></span>    |     |     |
| [<span data-ttu-id="18b83-144">modificatori texld e texcrd</span><span class="sxs-lookup"><span data-stu-id="18b83-144">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="18b83-145">Registra \_ d\*</span><span class="sxs-lookup"><span data-stu-id="18b83-145">register\_d\*</span></span>  | <span data-ttu-id="18b83-146">X</span><span class="sxs-lookup"><span data-stu-id="18b83-146">X</span></span>       | <span data-ttu-id="18b83-147">X</span><span class="sxs-lookup"><span data-stu-id="18b83-147">X</span></span>    | <span data-ttu-id="18b83-148">X</span><span class="sxs-lookup"><span data-stu-id="18b83-148">X</span></span>    | <span data-ttu-id="18b83-149">X</span><span class="sxs-lookup"><span data-stu-id="18b83-149">X</span></span>    |     |     |
| [<span data-ttu-id="18b83-150">swizzling del registro di origine</span><span class="sxs-lookup"><span data-stu-id="18b83-150">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="18b83-151">Register. xyzw</span><span class="sxs-lookup"><span data-stu-id="18b83-151">register.xyzw</span></span>  | <span data-ttu-id="18b83-152">X</span><span class="sxs-lookup"><span data-stu-id="18b83-152">X</span></span>       | <span data-ttu-id="18b83-153">X</span><span class="sxs-lookup"><span data-stu-id="18b83-153">X</span></span>    | <span data-ttu-id="18b83-154">X</span><span class="sxs-lookup"><span data-stu-id="18b83-154">X</span></span>    | <span data-ttu-id="18b83-155">X</span><span class="sxs-lookup"><span data-stu-id="18b83-155">X</span></span>    |     |     |



 

<span data-ttu-id="18b83-156">I modificatori del registro di origine possono essere utilizzati solo nelle istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="18b83-156">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="18b83-157">Non possono essere usati nelle istruzioni relative all'indirizzo di trama.</span><span class="sxs-lookup"><span data-stu-id="18b83-157">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="18b83-158">L'eccezione è rappresentata dal modificatore [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) .</span><span class="sxs-lookup"><span data-stu-id="18b83-158">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="18b83-159">Per la versione 1 \_ , è possibile usare la scala con segno nell'argomento di origine di qualsiasi \* istruzione texm.</span><span class="sxs-lookup"><span data-stu-id="18b83-159">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="18b83-160">Per la versione 1 \_ 2 o 1 \_ 3, la scala con segno può essere usata nell'argomento di origine di qualsiasi istruzione di indirizzo di trama.</span><span class="sxs-lookup"><span data-stu-id="18b83-160">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="18b83-161">Alcune restrizioni specifiche del modificatore:</span><span class="sxs-lookup"><span data-stu-id="18b83-161">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="18b83-162">È possibile combinare negate con il modificatore di distorsione, di ridimensionamento con firma o di scalex2.</span><span class="sxs-lookup"><span data-stu-id="18b83-162">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="18b83-163">In combinazione, viene eseguita l'ultima negazione.</span><span class="sxs-lookup"><span data-stu-id="18b83-163">When combined, negate is run last.</span></span>
-   <span data-ttu-id="18b83-164">Non è possibile combinare l'inversione con altri modificatori.</span><span class="sxs-lookup"><span data-stu-id="18b83-164">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="18b83-165">Invertire, negare, bias, la scalabilità con segno e scalex2 possono essere combinati con uno qualsiasi dei selettori.</span><span class="sxs-lookup"><span data-stu-id="18b83-165">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="18b83-166">I modificatori del registro di origine non devono essere usati nei registri costanti perché determineranno risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="18b83-166">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="18b83-167">Per la versione 1 \_ 4, i modificatori sulle costanti non sono consentiti e la convalida avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="18b83-167">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="18b83-168">PS \_ 2 \_ 0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="18b83-168">ps\_2\_0 and Above</span></span>

<span data-ttu-id="18b83-169">Per la versione PS \_ 2 \_ 0 e su, il numero di modificatori è stato semplificato.</span><span class="sxs-lookup"><span data-stu-id="18b83-169">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="18b83-170">Negate</span><span class="sxs-lookup"><span data-stu-id="18b83-170">Negate</span></span>

<span data-ttu-id="18b83-171">Negare il contenuto del registro di origine.</span><span class="sxs-lookup"><span data-stu-id="18b83-171">Negate the contents of the source register.</span></span>



| <span data-ttu-id="18b83-172">Modificatore Component</span><span class="sxs-lookup"><span data-stu-id="18b83-172">Component modifier</span></span> | <span data-ttu-id="18b83-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18b83-173">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="18b83-174">\- r</span><span class="sxs-lookup"><span data-stu-id="18b83-174">\- r</span></span>               | <span data-ttu-id="18b83-175">Negazione origine</span><span class="sxs-lookup"><span data-stu-id="18b83-175">Source negation</span></span> |



 

<span data-ttu-id="18b83-176">Non è possibile usare il modificatore negazioni nel secondo registro di origine di queste istruzioni: [M3X2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)e [M4x4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="18b83-176">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="18b83-177">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="18b83-177">Pixel shader versions</span></span> | <span data-ttu-id="18b83-178">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="18b83-178">2\_0</span></span> | <span data-ttu-id="18b83-179">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="18b83-179">2\_x</span></span> | <span data-ttu-id="18b83-180">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="18b83-180">2\_sw</span></span> | <span data-ttu-id="18b83-181">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="18b83-181">3\_0</span></span> | <span data-ttu-id="18b83-182">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="18b83-182">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="18b83-183">x</span><span class="sxs-lookup"><span data-stu-id="18b83-183">x</span></span>    | <span data-ttu-id="18b83-184">x</span><span class="sxs-lookup"><span data-stu-id="18b83-184">x</span></span>    | <span data-ttu-id="18b83-185">x</span><span class="sxs-lookup"><span data-stu-id="18b83-185">x</span></span>     | <span data-ttu-id="18b83-186">x</span><span class="sxs-lookup"><span data-stu-id="18b83-186">x</span></span>    | <span data-ttu-id="18b83-187">x</span><span class="sxs-lookup"><span data-stu-id="18b83-187">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="18b83-188">Valore assoluto</span><span class="sxs-lookup"><span data-stu-id="18b83-188">Absolute Value</span></span>

<span data-ttu-id="18b83-189">Assumere il valore assoluto del registro.</span><span class="sxs-lookup"><span data-stu-id="18b83-189">Take the absolute value of the register.</span></span>



| <span data-ttu-id="18b83-190">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="18b83-190">Pixel shader versions</span></span> | <span data-ttu-id="18b83-191">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="18b83-191">2\_0</span></span> | <span data-ttu-id="18b83-192">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="18b83-192">2\_x</span></span> | <span data-ttu-id="18b83-193">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="18b83-193">2\_sw</span></span> | <span data-ttu-id="18b83-194">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="18b83-194">3\_0</span></span> | <span data-ttu-id="18b83-195">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="18b83-195">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="18b83-196">abs</span><span class="sxs-lookup"><span data-stu-id="18b83-196">abs</span></span>                   |      |      |       | <span data-ttu-id="18b83-197">x</span><span class="sxs-lookup"><span data-stu-id="18b83-197">x</span></span>    | <span data-ttu-id="18b83-198">x</span><span class="sxs-lookup"><span data-stu-id="18b83-198">x</span></span>     |



 

<span data-ttu-id="18b83-199">Se una versione 3 dello shader legge da uno o più registri float costanti (c \# ), uno dei seguenti deve essere true.</span><span class="sxs-lookup"><span data-stu-id="18b83-199">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="18b83-200">Tutti i registri a virgola mobile costanti devono usare il modificatore ABS.</span><span class="sxs-lookup"><span data-stu-id="18b83-200">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="18b83-201">Nessun registro a virgola mobile costante può utilizzare il modificatore ABS.</span><span class="sxs-lookup"><span data-stu-id="18b83-201">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18b83-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18b83-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18b83-203">Modificatori del registro pixel shader</span><span class="sxs-lookup"><span data-stu-id="18b83-203">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




