---
title: Grammatica
description: Le istruzioni HLSL vengono costruite usando le regole seguenti per la grammatica.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129849"
---
# <a name="grammar"></a><span data-ttu-id="11ace-103">Grammatica</span><span class="sxs-lookup"><span data-stu-id="11ace-103">Grammar</span></span>

<span data-ttu-id="11ace-104">Le istruzioni HLSL vengono costruite usando le regole seguenti per la grammatica.</span><span class="sxs-lookup"><span data-stu-id="11ace-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="11ace-105">Spazio vuoto</span><span class="sxs-lookup"><span data-stu-id="11ace-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="11ace-106">Numeri a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="11ace-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="11ace-107">Numeri interi</span><span class="sxs-lookup"><span data-stu-id="11ace-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="11ace-108">Caratteri</span><span class="sxs-lookup"><span data-stu-id="11ace-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="11ace-109">Stringhe</span><span class="sxs-lookup"><span data-stu-id="11ace-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="11ace-110">Identificatori</span><span class="sxs-lookup"><span data-stu-id="11ace-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="11ace-111">Operatori</span><span class="sxs-lookup"><span data-stu-id="11ace-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="11ace-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11ace-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="11ace-113">Spazio vuoto</span><span class="sxs-lookup"><span data-stu-id="11ace-113">Whitespace</span></span>

<span data-ttu-id="11ace-114">I caratteri seguenti vengono riconosciuti come spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="11ace-114">The following characters are recognized as white space.</span></span>

- <span data-ttu-id="11ace-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="11ace-115">SPACE</span></span>
- <span data-ttu-id="11ace-116">TAB</span><span class="sxs-lookup"><span data-stu-id="11ace-116">TAB</span></span>
- <span data-ttu-id="11ace-117">Eol</span><span class="sxs-lookup"><span data-stu-id="11ace-117">EOL</span></span>
- <span data-ttu-id="11ace-118">Commenti in stile C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="11ace-118">C style comments (/\* \*/)</span></span>
- <span data-ttu-id="11ace-119">Commenti in stile C++ (//)</span><span class="sxs-lookup"><span data-stu-id="11ace-119">C++ style comments (//)</span></span>

## <a name="floating-point-numbers"></a><span data-ttu-id="11ace-120">Numeri a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="11ace-120">Floating point numbers</span></span>

<span data-ttu-id="11ace-121">I numeri a virgola mobile sono rappresentati in HLSL come segue:</span><span class="sxs-lookup"><span data-stu-id="11ace-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="11ace-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="11ace-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="11ace-123">digit-sequence exponent-part floating-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="11ace-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="11ace-124">fractional-constant :</span><span class="sxs-lookup"><span data-stu-id="11ace-124">fractional-constant :</span></span>

    <span data-ttu-id="11ace-125">digit-sequence(opt) .</span><span class="sxs-lookup"><span data-stu-id="11ace-125">digit-sequence(opt) .</span></span> <span data-ttu-id="11ace-126">digit-sequence</span><span class="sxs-lookup"><span data-stu-id="11ace-126">digit-sequence</span></span>

    <span data-ttu-id="11ace-127">digit-sequence .</span><span class="sxs-lookup"><span data-stu-id="11ace-127">digit-sequence .</span></span>

-   <span data-ttu-id="11ace-128">exponent-part :</span><span class="sxs-lookup"><span data-stu-id="11ace-128">exponent-part :</span></span>

    <span data-ttu-id="11ace-129">e sign(opt) digit-sequence</span><span class="sxs-lookup"><span data-stu-id="11ace-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="11ace-130">E sign(opt) digit-sequence</span><span class="sxs-lookup"><span data-stu-id="11ace-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="11ace-131">sign : uno tra</span><span class="sxs-lookup"><span data-stu-id="11ace-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="11ace-132">digit-sequence :</span><span class="sxs-lookup"><span data-stu-id="11ace-132">digit-sequence :</span></span>

    <span data-ttu-id="11ace-133">digit</span><span class="sxs-lookup"><span data-stu-id="11ace-133">digit</span></span>

    <span data-ttu-id="11ace-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="11ace-134">digit-sequence digit</span></span>

-   <span data-ttu-id="11ace-135">floating-suffix : uno tra</span><span class="sxs-lookup"><span data-stu-id="11ace-135">floating-suffix : one of</span></span>

    <span data-ttu-id="11ace-136">h H f F l L</span><span class="sxs-lookup"><span data-stu-id="11ace-136">h H f F l L</span></span>

    <span data-ttu-id="11ace-137">Usare il suffisso "L" per specificare un valore letterale a virgola mobile e precisione a 64 bit completo.</span><span class="sxs-lookup"><span data-stu-id="11ace-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="11ace-138">Un valore letterale float a 32 bit è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="11ace-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="11ace-139">Ad esempio, il compilatore riconosce il valore letterale seguente come valore letterale a virgola mobile e precisione a 32 bit e ignora i bit inferiori:</span><span class="sxs-lookup"><span data-stu-id="11ace-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="11ace-140">Il compilatore riconosce il valore letterale seguente come valore letterale a virgola mobile e precisione a 64 bit:</span><span class="sxs-lookup"><span data-stu-id="11ace-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="11ace-141">Numeri interi</span><span class="sxs-lookup"><span data-stu-id="11ace-141">Integer numbers</span></span>

<span data-ttu-id="11ace-142">I numeri interi sono rappresentati in HLSL come segue:</span><span class="sxs-lookup"><span data-stu-id="11ace-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="11ace-143">integer-constant integer-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="11ace-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="11ace-144">integer-constant: uno di</span><span class="sxs-lookup"><span data-stu-id="11ace-144">integer-constant: one of</span></span>

    <span data-ttu-id="11ace-145">\# (numero decimale)</span><span class="sxs-lookup"><span data-stu-id="11ace-145">\# (decimal number)</span></span>

    <span data-ttu-id="11ace-146">0 \# (numero ottale)</span><span class="sxs-lookup"><span data-stu-id="11ace-146">0\# (octal number)</span></span>

    <span data-ttu-id="11ace-147">0x \# (numero esadecimale)</span><span class="sxs-lookup"><span data-stu-id="11ace-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="11ace-148">integer-suffix può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="11ace-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="11ace-149">u U l L</span><span class="sxs-lookup"><span data-stu-id="11ace-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="11ace-150">Caratteri</span><span class="sxs-lookup"><span data-stu-id="11ace-150">Characters</span></span>

<span data-ttu-id="11ace-151">I caratteri sono rappresentati in HLSL come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="11ace-151">Characters are represented in HLSL as follows:</span></span>



| <span data-ttu-id="11ace-152">Carattere</span><span class="sxs-lookup"><span data-stu-id="11ace-152">Character</span></span>                                          | <span data-ttu-id="11ace-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11ace-153">Description</span></span>                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="11ace-154">'c'</span><span class="sxs-lookup"><span data-stu-id="11ace-154">'c'</span></span>                                       | <span data-ttu-id="11ace-155">(carattere)</span><span class="sxs-lookup"><span data-stu-id="11ace-155">(character)</span></span>                                                     |
| <span data-ttu-id="11ace-156">\\'a' \\ 'b' \\ 'f' \\ 'b' \\ 'r' \\ 't' \\ 'v'</span><span class="sxs-lookup"><span data-stu-id="11ace-156">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="11ace-157">(caratteri di escape)</span><span class="sxs-lookup"><span data-stu-id="11ace-157">(escapes)</span></span>                                                       |
| <span data-ttu-id="11ace-158">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="11ace-158">'\\\#\#\#'</span></span>                                | <span data-ttu-id="11ace-159">(escape ottale, ognuno \# è una cifra ottale)</span><span class="sxs-lookup"><span data-stu-id="11ace-159">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="11ace-160">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="11ace-160">'\\x\#'</span></span>                                   | <span data-ttu-id="11ace-161">(carattere di escape esadecimale, \# numero esadecimale, qualsiasi numero di cifre)</span><span class="sxs-lookup"><span data-stu-id="11ace-161">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="11ace-162">\\'c'</span><span class="sxs-lookup"><span data-stu-id="11ace-162">'\\c'</span></span>                                     | <span data-ttu-id="11ace-163">(c è un altro carattere, incluse la barra rovesciata e le virgolette)</span><span class="sxs-lookup"><span data-stu-id="11ace-163">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="11ace-164">Gli escape non sono supportati nelle espressioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="11ace-164">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="11ace-165">Stringhe</span><span class="sxs-lookup"><span data-stu-id="11ace-165">Strings</span></span>

<span data-ttu-id="11ace-166">Le stringhe sono rappresentate in HLSL come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="11ace-166">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="11ace-167">"s" (s è qualsiasi stringa con caratteri di escape).</span><span class="sxs-lookup"><span data-stu-id="11ace-167">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="11ace-168">Identificatori</span><span class="sxs-lookup"><span data-stu-id="11ace-168">Identifiers</span></span>

<span data-ttu-id="11ace-169">Gli identificatori sono rappresentati in HLSL come segue:</span><span class="sxs-lookup"><span data-stu-id="11ace-169">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="11ace-170">Operatori</span><span class="sxs-lookup"><span data-stu-id="11ace-170">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="11ace-171">Qualsiasi altro carattere singolo che non corrisponde a un'altra regola.</span><span class="sxs-lookup"><span data-stu-id="11ace-171">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11ace-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11ace-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11ace-173">Appendice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11ace-173">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




