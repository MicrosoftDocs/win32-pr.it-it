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
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129678"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="27f81-103">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="27f81-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="27f81-104">Usare i modificatori del registro di origine per modificare il valore letto da un registro prima dell'esecuzione di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="27f81-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="27f81-105">Il contenuto di un registro di origine rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="27f81-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="27f81-106">I modificatori sono utili per modificare l'intervallo di dati del registro in preparazione dell'istruzione .</span><span class="sxs-lookup"><span data-stu-id="27f81-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="27f81-107">Un set di modificatori denominati selettori copia o replica i dati da un singolo canale (r,g,b,a) negli altri canali.</span><span class="sxs-lookup"><span data-stu-id="27f81-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="27f81-108">ps \_ 1 \_ 1 - ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="27f81-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="27f81-109">Questa tabella identifica le versioni che supportano ogni modificatore:</span><span class="sxs-lookup"><span data-stu-id="27f81-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="27f81-110">Modificatori del registro di origine</span><span class="sxs-lookup"><span data-stu-id="27f81-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="27f81-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27f81-111">Syntax</span></span>         | <span data-ttu-id="27f81-112">Versione 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="27f81-112">Version 1\_1</span></span> | <span data-ttu-id="27f81-113">Versione 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="27f81-113">Version 1\_2</span></span>     | <span data-ttu-id="27f81-114">Versione 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="27f81-114">Version 1\_3</span></span>     | <span data-ttu-id="27f81-115">Versione 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="27f81-115">Version 1\_4</span></span>     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [<span data-ttu-id="27f81-116">Pregiudizi</span><span class="sxs-lookup"><span data-stu-id="27f81-116">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="27f81-117">registrare \_ la distorsione</span><span class="sxs-lookup"><span data-stu-id="27f81-117">register\_bias</span></span> | <span data-ttu-id="27f81-118">X</span><span class="sxs-lookup"><span data-stu-id="27f81-118">X</span></span>       | <span data-ttu-id="27f81-119">X</span><span class="sxs-lookup"><span data-stu-id="27f81-119">X</span></span>    | <span data-ttu-id="27f81-120">X</span><span class="sxs-lookup"><span data-stu-id="27f81-120">X</span></span>    | <span data-ttu-id="27f81-121">X</span><span class="sxs-lookup"><span data-stu-id="27f81-121">X</span></span>    |
| [<span data-ttu-id="27f81-122">Invertire</span><span class="sxs-lookup"><span data-stu-id="27f81-122">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="27f81-123">1 - Registrazione</span><span class="sxs-lookup"><span data-stu-id="27f81-123">1 - register</span></span>   | <span data-ttu-id="27f81-124">X</span><span class="sxs-lookup"><span data-stu-id="27f81-124">X</span></span>       | <span data-ttu-id="27f81-125">X</span><span class="sxs-lookup"><span data-stu-id="27f81-125">X</span></span>    | <span data-ttu-id="27f81-126">X</span><span class="sxs-lookup"><span data-stu-id="27f81-126">X</span></span>    | <span data-ttu-id="27f81-127">X</span><span class="sxs-lookup"><span data-stu-id="27f81-127">X</span></span>    |
| [<span data-ttu-id="27f81-128">negate</span><span class="sxs-lookup"><span data-stu-id="27f81-128">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="27f81-129">\- Registro</span><span class="sxs-lookup"><span data-stu-id="27f81-129">\- register</span></span>    | <span data-ttu-id="27f81-130">X</span><span class="sxs-lookup"><span data-stu-id="27f81-130">X</span></span>       | <span data-ttu-id="27f81-131">X</span><span class="sxs-lookup"><span data-stu-id="27f81-131">X</span></span>    | <span data-ttu-id="27f81-132">X</span><span class="sxs-lookup"><span data-stu-id="27f81-132">X</span></span>    | <span data-ttu-id="27f81-133">X</span><span class="sxs-lookup"><span data-stu-id="27f81-133">X</span></span>    |
| [<span data-ttu-id="27f81-134">ridimensionare per 2</span><span class="sxs-lookup"><span data-stu-id="27f81-134">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="27f81-135">registrare \_ x2</span><span class="sxs-lookup"><span data-stu-id="27f81-135">register\_x2</span></span>   |         |      |      | <span data-ttu-id="27f81-136">X</span><span class="sxs-lookup"><span data-stu-id="27f81-136">X</span></span>    |
| [<span data-ttu-id="27f81-137">ridimensionamento con segno</span><span class="sxs-lookup"><span data-stu-id="27f81-137">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="27f81-138">registrare \_ bx2</span><span class="sxs-lookup"><span data-stu-id="27f81-138">register\_bx2</span></span>  | <span data-ttu-id="27f81-139">X</span><span class="sxs-lookup"><span data-stu-id="27f81-139">X</span></span>       | <span data-ttu-id="27f81-140">X</span><span class="sxs-lookup"><span data-stu-id="27f81-140">X</span></span>    | <span data-ttu-id="27f81-141">X</span><span class="sxs-lookup"><span data-stu-id="27f81-141">X</span></span>    | <span data-ttu-id="27f81-142">X</span><span class="sxs-lookup"><span data-stu-id="27f81-142">X</span></span>    |
| [<span data-ttu-id="27f81-143">Modificatori texld e texcrd</span><span class="sxs-lookup"><span data-stu-id="27f81-143">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="27f81-144">register \_ d\*</span><span class="sxs-lookup"><span data-stu-id="27f81-144">register\_d\*</span></span>  | <span data-ttu-id="27f81-145">X</span><span class="sxs-lookup"><span data-stu-id="27f81-145">X</span></span>       | <span data-ttu-id="27f81-146">X</span><span class="sxs-lookup"><span data-stu-id="27f81-146">X</span></span>    | <span data-ttu-id="27f81-147">X</span><span class="sxs-lookup"><span data-stu-id="27f81-147">X</span></span>    | <span data-ttu-id="27f81-148">X</span><span class="sxs-lookup"><span data-stu-id="27f81-148">X</span></span>    |
| [<span data-ttu-id="27f81-149">swizzling del registro di origine</span><span class="sxs-lookup"><span data-stu-id="27f81-149">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="27f81-150">register.xyzw</span><span class="sxs-lookup"><span data-stu-id="27f81-150">register.xyzw</span></span>  | <span data-ttu-id="27f81-151">X</span><span class="sxs-lookup"><span data-stu-id="27f81-151">X</span></span>       | <span data-ttu-id="27f81-152">X</span><span class="sxs-lookup"><span data-stu-id="27f81-152">X</span></span>    | <span data-ttu-id="27f81-153">X</span><span class="sxs-lookup"><span data-stu-id="27f81-153">X</span></span>    | <span data-ttu-id="27f81-154">X</span><span class="sxs-lookup"><span data-stu-id="27f81-154">X</span></span>    |



 

<span data-ttu-id="27f81-155">I modificatori del registro di origine possono essere usati solo nelle istruzioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="27f81-155">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="27f81-156">Non possono essere usati nelle istruzioni relative all'indirizzo della trama.</span><span class="sxs-lookup"><span data-stu-id="27f81-156">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="27f81-157">L'eccezione è il [modificatore scale by 2.](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)</span><span class="sxs-lookup"><span data-stu-id="27f81-157">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="27f81-158">Per la versione 1 1, è possibile usare la scalabilità con segno \_ nell'argomento di origine di qualsiasi istruzione texm. \*</span><span class="sxs-lookup"><span data-stu-id="27f81-158">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="27f81-159">Per la versione 1 \_ 2 o 1 3, è possibile usare la scalabilità con segno nell'argomento di origine \_ di qualsiasi istruzione di indirizzo di trama.</span><span class="sxs-lookup"><span data-stu-id="27f81-159">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="27f81-160">Alcune restrizioni specifiche del modificatore:</span><span class="sxs-lookup"><span data-stu-id="27f81-160">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="27f81-161">Negate può essere combinato con il modificatore bias, signed scaling o scalex2.</span><span class="sxs-lookup"><span data-stu-id="27f81-161">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="27f81-162">Se combinato, negate viene eseguito per ultimo.</span><span class="sxs-lookup"><span data-stu-id="27f81-162">When combined, negate is run last.</span></span>
-   <span data-ttu-id="27f81-163">Invert non può essere combinato con altri modificatori.</span><span class="sxs-lookup"><span data-stu-id="27f81-163">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="27f81-164">Invert, negate, bias, signed scaling e scalex2 possono essere combinati con qualsiasi selettore.</span><span class="sxs-lookup"><span data-stu-id="27f81-164">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="27f81-165">I modificatori del registro di origine non devono essere usati nei registri costanti perché causeranno risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="27f81-165">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="27f81-166">Per la versione \_ 1 4, i modificatori sulle costanti non sono consentiti e la convalida avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="27f81-166">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="27f81-167">ps \_ 2 \_ 0 e successive</span><span class="sxs-lookup"><span data-stu-id="27f81-167">ps\_2\_0 and Above</span></span>

<span data-ttu-id="27f81-168">Per la versione ps \_ 2 \_ 0 e successiva, il numero di modificatori è stato semplificato.</span><span class="sxs-lookup"><span data-stu-id="27f81-168">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="27f81-169">Negate</span><span class="sxs-lookup"><span data-stu-id="27f81-169">Negate</span></span>

<span data-ttu-id="27f81-170">Negare il contenuto del registro di origine.</span><span class="sxs-lookup"><span data-stu-id="27f81-170">Negate the contents of the source register.</span></span>



| <span data-ttu-id="27f81-171">Modificatore di componente</span><span class="sxs-lookup"><span data-stu-id="27f81-171">Component modifier</span></span> | <span data-ttu-id="27f81-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27f81-172">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="27f81-173">\- R</span><span class="sxs-lookup"><span data-stu-id="27f81-173">\- r</span></span>               | <span data-ttu-id="27f81-174">Negazione dell'origine</span><span class="sxs-lookup"><span data-stu-id="27f81-174">Source negation</span></span> |



 

<span data-ttu-id="27f81-175">Il modificatore negate non può essere usato nel secondo registro di origine di queste istruzioni: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md)e [m4x4 - ps](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="27f81-175">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="27f81-176">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="27f81-176">Pixel shader versions</span></span> | <span data-ttu-id="27f81-177">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27f81-177">2\_0</span></span> | <span data-ttu-id="27f81-178">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="27f81-178">2\_x</span></span> | <span data-ttu-id="27f81-179">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="27f81-179">2\_sw</span></span> | <span data-ttu-id="27f81-180">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27f81-180">3\_0</span></span> | <span data-ttu-id="27f81-181">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="27f81-181">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="27f81-182">x</span><span class="sxs-lookup"><span data-stu-id="27f81-182">x</span></span>    | <span data-ttu-id="27f81-183">x</span><span class="sxs-lookup"><span data-stu-id="27f81-183">x</span></span>    | <span data-ttu-id="27f81-184">x</span><span class="sxs-lookup"><span data-stu-id="27f81-184">x</span></span>     | <span data-ttu-id="27f81-185">x</span><span class="sxs-lookup"><span data-stu-id="27f81-185">x</span></span>    | <span data-ttu-id="27f81-186">x</span><span class="sxs-lookup"><span data-stu-id="27f81-186">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="27f81-187">Valore assoluto</span><span class="sxs-lookup"><span data-stu-id="27f81-187">Absolute Value</span></span>

<span data-ttu-id="27f81-188">Prendere il valore assoluto del registro.</span><span class="sxs-lookup"><span data-stu-id="27f81-188">Take the absolute value of the register.</span></span>



| <span data-ttu-id="27f81-189">Versioni dei pixel shader</span><span class="sxs-lookup"><span data-stu-id="27f81-189">Pixel shader versions</span></span> | <span data-ttu-id="27f81-190">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27f81-190">2\_0</span></span> | <span data-ttu-id="27f81-191">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="27f81-191">2\_x</span></span> | <span data-ttu-id="27f81-192">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="27f81-192">2\_sw</span></span> | <span data-ttu-id="27f81-193">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27f81-193">3\_0</span></span> | <span data-ttu-id="27f81-194">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="27f81-194">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="27f81-195">abs</span><span class="sxs-lookup"><span data-stu-id="27f81-195">abs</span></span>                   |      |      |       | <span data-ttu-id="27f81-196">x</span><span class="sxs-lookup"><span data-stu-id="27f81-196">x</span></span>    | <span data-ttu-id="27f81-197">x</span><span class="sxs-lookup"><span data-stu-id="27f81-197">x</span></span>     |



 

<span data-ttu-id="27f81-198">Se uno shader versione 3 legge da uno o più registri float costanti (c), uno dei \# seguenti deve essere true.</span><span class="sxs-lookup"><span data-stu-id="27f81-198">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="27f81-199">Tutti i registri a virgola mobile costanti devono usare il modificatore abs.</span><span class="sxs-lookup"><span data-stu-id="27f81-199">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="27f81-200">Nessuno dei registri a virgola mobile costanti può usare il modificatore abs.</span><span class="sxs-lookup"><span data-stu-id="27f81-200">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27f81-201">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27f81-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27f81-202">Modificatori di registro pixel shader</span><span class="sxs-lookup"><span data-stu-id="27f81-202">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




