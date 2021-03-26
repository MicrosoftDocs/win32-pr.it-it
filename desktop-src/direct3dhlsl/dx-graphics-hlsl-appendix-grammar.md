---
title: Grammatica
description: Le istruzioni HLSL vengono create usando le regole seguenti per la grammatica.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516519"
---
# <a name="grammar"></a><span data-ttu-id="c53ea-103">Grammatica</span><span class="sxs-lookup"><span data-stu-id="c53ea-103">Grammar</span></span>

<span data-ttu-id="c53ea-104">Le istruzioni HLSL vengono create usando le regole seguenti per la grammatica.</span><span class="sxs-lookup"><span data-stu-id="c53ea-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="c53ea-105">Whitespace</span><span class="sxs-lookup"><span data-stu-id="c53ea-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="c53ea-106">Numeri a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="c53ea-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="c53ea-107">Numeri interi</span><span class="sxs-lookup"><span data-stu-id="c53ea-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="c53ea-108">Caratteri</span><span class="sxs-lookup"><span data-stu-id="c53ea-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="c53ea-109">Stringhe</span><span class="sxs-lookup"><span data-stu-id="c53ea-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="c53ea-110">Identificatori</span><span class="sxs-lookup"><span data-stu-id="c53ea-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="c53ea-111">Operatori</span><span class="sxs-lookup"><span data-stu-id="c53ea-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="c53ea-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c53ea-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="c53ea-113">Spazi vuoti</span><span class="sxs-lookup"><span data-stu-id="c53ea-113">Whitespace</span></span>

<span data-ttu-id="c53ea-114">I caratteri seguenti sono riconosciuti come spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="c53ea-114">The following characters are recognized as white space.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="c53ea-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="c53ea-115">SPACE</span></span>                      |
| <span data-ttu-id="c53ea-116">TAB</span><span class="sxs-lookup"><span data-stu-id="c53ea-116">TAB</span></span>                        |
| <span data-ttu-id="c53ea-117">FINE riga</span><span class="sxs-lookup"><span data-stu-id="c53ea-117">EOL</span></span>                        |
| <span data-ttu-id="c53ea-118">Commenti in stile C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="c53ea-118">C style comments (/\* \*/)</span></span> |
| <span data-ttu-id="c53ea-119">Commenti in stile C++ (//)</span><span class="sxs-lookup"><span data-stu-id="c53ea-119">C++ style comments (//)</span></span>    |



 

## <a name="floating-point-numbers"></a><span data-ttu-id="c53ea-120">Numeri a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="c53ea-120">Floating point numbers</span></span>

<span data-ttu-id="c53ea-121">I numeri a virgola mobile sono rappresentati in HLSL, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c53ea-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="c53ea-122">frazionario: suffisso a virgola mobile (opt) a virgola mobile (opt)</span><span class="sxs-lookup"><span data-stu-id="c53ea-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="c53ea-123">cifre-sequenza esponente-parte a virgola mobile (opt)</span><span class="sxs-lookup"><span data-stu-id="c53ea-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="c53ea-124">costante frazionaria:</span><span class="sxs-lookup"><span data-stu-id="c53ea-124">fractional-constant :</span></span>

    <span data-ttu-id="c53ea-125">digit-Sequence (opt).</span><span class="sxs-lookup"><span data-stu-id="c53ea-125">digit-sequence(opt) .</span></span> <span data-ttu-id="c53ea-126">digit-sequence</span><span class="sxs-lookup"><span data-stu-id="c53ea-126">digit-sequence</span></span>

    <span data-ttu-id="c53ea-127">sequenza numerica.</span><span class="sxs-lookup"><span data-stu-id="c53ea-127">digit-sequence .</span></span>

-   <span data-ttu-id="c53ea-128">parte esponente:</span><span class="sxs-lookup"><span data-stu-id="c53ea-128">exponent-part :</span></span>

    <span data-ttu-id="c53ea-129">segno e (opt) digit-Sequence</span><span class="sxs-lookup"><span data-stu-id="c53ea-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="c53ea-130">Segno E (opt) digit-Sequence</span><span class="sxs-lookup"><span data-stu-id="c53ea-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="c53ea-131">sign : uno tra</span><span class="sxs-lookup"><span data-stu-id="c53ea-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="c53ea-132">sequenza numerica:</span><span class="sxs-lookup"><span data-stu-id="c53ea-132">digit-sequence :</span></span>

    <span data-ttu-id="c53ea-133">digit</span><span class="sxs-lookup"><span data-stu-id="c53ea-133">digit</span></span>

    <span data-ttu-id="c53ea-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="c53ea-134">digit-sequence digit</span></span>

-   <span data-ttu-id="c53ea-135">floating-suffix : uno tra</span><span class="sxs-lookup"><span data-stu-id="c53ea-135">floating-suffix : one of</span></span>

    <span data-ttu-id="c53ea-136">h H f l L</span><span class="sxs-lookup"><span data-stu-id="c53ea-136">h H f F l L</span></span>

    <span data-ttu-id="c53ea-137">Usare il suffisso "L" per specificare un valore letterale a virgola mobile con precisione a 64 bit completo.</span><span class="sxs-lookup"><span data-stu-id="c53ea-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="c53ea-138">Il valore predefinito è un valore letterale float a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c53ea-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="c53ea-139">Il compilatore, ad esempio, riconosce il valore letterale seguente come valore letterale a virgola mobile con precisione a 32 bit e ignora i bit inferiori:</span><span class="sxs-lookup"><span data-stu-id="c53ea-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="c53ea-140">Il compilatore riconosce il valore letterale seguente come valore letterale a virgola mobile con precisione a 64 bit:</span><span class="sxs-lookup"><span data-stu-id="c53ea-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="c53ea-141">Numeri interi</span><span class="sxs-lookup"><span data-stu-id="c53ea-141">Integer numbers</span></span>

<span data-ttu-id="c53ea-142">I numeri interi sono rappresentati in HLSL, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c53ea-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="c53ea-143">Integer-Constant Integer-suffisso (opt)</span><span class="sxs-lookup"><span data-stu-id="c53ea-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="c53ea-144">costante Integer: uno tra</span><span class="sxs-lookup"><span data-stu-id="c53ea-144">integer-constant: one of</span></span>

    <span data-ttu-id="c53ea-145">\# (numero decimale)</span><span class="sxs-lookup"><span data-stu-id="c53ea-145">\# (decimal number)</span></span>

    <span data-ttu-id="c53ea-146">0 \# (numero ottale)</span><span class="sxs-lookup"><span data-stu-id="c53ea-146">0\# (octal number)</span></span>

    <span data-ttu-id="c53ea-147">0x \# (numero esadecimale)</span><span class="sxs-lookup"><span data-stu-id="c53ea-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="c53ea-148">il suffisso Integer può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="c53ea-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="c53ea-149">u U l</span><span class="sxs-lookup"><span data-stu-id="c53ea-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="c53ea-150">Caratteri</span><span class="sxs-lookup"><span data-stu-id="c53ea-150">Characters</span></span>

<span data-ttu-id="c53ea-151">I caratteri sono rappresentati in HLSL, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c53ea-151">Characters are represented in HLSL as follows:</span></span>



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="c53ea-152">c</span><span class="sxs-lookup"><span data-stu-id="c53ea-152">'c'</span></span>                                       | <span data-ttu-id="c53ea-153">carattere</span><span class="sxs-lookup"><span data-stu-id="c53ea-153">(character)</span></span>                                                     |
| <span data-ttu-id="c53ea-154">' \\ a' \\ b '' \\ f '' \\ b '' \\ r '' T'' \\ \\ v'</span><span class="sxs-lookup"><span data-stu-id="c53ea-154">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="c53ea-155">Escape</span><span class="sxs-lookup"><span data-stu-id="c53ea-155">(escapes)</span></span>                                                       |
| <span data-ttu-id="c53ea-156">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="c53ea-156">'\\\#\#\#'</span></span>                                | <span data-ttu-id="c53ea-157">(escape ottale, ognuno \# è una cifra ottale)</span><span class="sxs-lookup"><span data-stu-id="c53ea-157">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="c53ea-158">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="c53ea-158">'\\x\#'</span></span>                                   | <span data-ttu-id="c53ea-159">(escape esadecimale, \# è un numero esadecimale, un numero qualsiasi di cifre)</span><span class="sxs-lookup"><span data-stu-id="c53ea-159">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="c53ea-160">' \\ c'</span><span class="sxs-lookup"><span data-stu-id="c53ea-160">'\\c'</span></span>                                     | <span data-ttu-id="c53ea-161">(c è un altro carattere, incluse la barra rovesciata e le virgolette)</span><span class="sxs-lookup"><span data-stu-id="c53ea-161">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="c53ea-162">Le espressioni di escape non sono supportate nelle espressioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="c53ea-162">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="c53ea-163">Stringhe</span><span class="sxs-lookup"><span data-stu-id="c53ea-163">Strings</span></span>

<span data-ttu-id="c53ea-164">Le stringhe sono rappresentate in HLSL, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c53ea-164">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="c53ea-165">"s" (s è qualsiasi stringa con caratteri di escape).</span><span class="sxs-lookup"><span data-stu-id="c53ea-165">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="c53ea-166">Identificatori</span><span class="sxs-lookup"><span data-stu-id="c53ea-166">Identifiers</span></span>

<span data-ttu-id="c53ea-167">Gli identificatori sono rappresentati in HLSL, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c53ea-167">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="c53ea-168">Operatori</span><span class="sxs-lookup"><span data-stu-id="c53ea-168">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="c53ea-169">Anche qualsiasi altro carattere singolo che non corrisponde a un'altra regola.</span><span class="sxs-lookup"><span data-stu-id="c53ea-169">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c53ea-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c53ea-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c53ea-171">Appendice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c53ea-171">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




