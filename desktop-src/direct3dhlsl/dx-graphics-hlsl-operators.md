---
title: Operatori
description: Le espressioni sono sequenze di variabili e valori letterali punteggiati da operatori.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7a44fe02983038658247fedaec7122f09306548
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119606"
---
# <a name="operators"></a><span data-ttu-id="fe037-103">Operatori</span><span class="sxs-lookup"><span data-stu-id="fe037-103">Operators</span></span>

<span data-ttu-id="fe037-104">Le espressioni sono sequenze di [variabili](dx-graphics-hlsl-variable-syntax.md) e valori letterali punteggiati dagli [operatori](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="fe037-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="fe037-105">Gli operatori determinano il modo in cui le variabili e i valori letterali vengono combinati, confrontati, selezionati e così via.</span><span class="sxs-lookup"><span data-stu-id="fe037-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="fe037-106">Gli operatori includono:</span><span class="sxs-lookup"><span data-stu-id="fe037-106">The operators include:</span></span>



| <span data-ttu-id="fe037-107">Nome operatore</span><span class="sxs-lookup"><span data-stu-id="fe037-107">Operator name</span></span>                                                                                | <span data-ttu-id="fe037-108">Operatori</span><span class="sxs-lookup"><span data-stu-id="fe037-108">Operators</span></span>                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="fe037-109">Operatori additivi e moltiplicativi</span><span class="sxs-lookup"><span data-stu-id="fe037-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="fe037-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="fe037-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="fe037-111">Operatore Array</span><span class="sxs-lookup"><span data-stu-id="fe037-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="fe037-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="fe037-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="fe037-113">Operatori di assegnazione</span><span class="sxs-lookup"><span data-stu-id="fe037-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="fe037-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="fe037-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="fe037-115">Cast binari</span><span class="sxs-lookup"><span data-stu-id="fe037-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="fe037-116">Regole C per float e int, regole C o intrinseci HLSL per bool</span><span class="sxs-lookup"><span data-stu-id="fe037-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="fe037-117">Operatori bit per bit</span><span class="sxs-lookup"><span data-stu-id="fe037-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="fe037-118">~, <<, >>, &, \| , ^, <<=, >>=, &=, \| =, ^=</span><span class="sxs-lookup"><span data-stu-id="fe037-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="fe037-119">Operatori matematici booleani</span><span class="sxs-lookup"><span data-stu-id="fe037-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="fe037-120">& &, , \| \| ?:</span><span class="sxs-lookup"><span data-stu-id="fe037-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="fe037-121">Operatore Cast</span><span class="sxs-lookup"><span data-stu-id="fe037-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="fe037-122">(tipo)</span><span class="sxs-lookup"><span data-stu-id="fe037-122">(type)</span></span>                                                             |
| [<span data-ttu-id="fe037-123">Operatore virgola</span><span class="sxs-lookup"><span data-stu-id="fe037-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="fe037-124">,</span><span class="sxs-lookup"><span data-stu-id="fe037-124">,</span></span>                                                                  |
| [<span data-ttu-id="fe037-125">Operatori di confronto</span><span class="sxs-lookup"><span data-stu-id="fe037-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="fe037-126"><, >, ==, !=, <=, >=</span><span class="sxs-lookup"><span data-stu-id="fe037-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="fe037-127">Operatori di prefisso o suffisso</span><span class="sxs-lookup"><span data-stu-id="fe037-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="fe037-128">++, --</span><span class="sxs-lookup"><span data-stu-id="fe037-128">++, --</span></span>                                                             |
| [<span data-ttu-id="fe037-129">Operatore Structure</span><span class="sxs-lookup"><span data-stu-id="fe037-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="fe037-130">.</span><span class="sxs-lookup"><span data-stu-id="fe037-130">.</span></span>                                                                  |
| [<span data-ttu-id="fe037-131">Operatori unari</span><span class="sxs-lookup"><span data-stu-id="fe037-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="fe037-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="fe037-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="fe037-133">Molti operatori sono per componente, pertanto l'operazione viene eseguita in modo indipendente per ogni componente di ogni variabile.</span><span class="sxs-lookup"><span data-stu-id="fe037-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="fe037-134">Ad esempio, una singola variabile componente ha un'operazione eseguita.</span><span class="sxs-lookup"><span data-stu-id="fe037-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="fe037-135">D'altra parte, una variabile a quattro componenti ha quattro operazioni eseguite, una per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="fe037-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="fe037-136">Tutti gli operatori che e fanno qualcosa per il valore, ad esempio + e \* , funzionano per componente.</span><span class="sxs-lookup"><span data-stu-id="fe037-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="fe037-137">Gli operatori di confronto richiedono il funzionamento di un singolo componente, a meno che non si usi [**la**](dx-graphics-hlsl-all.md) funzione all o [**qualsiasi**](dx-graphics-hlsl-any.md) funzione intrinseca con una variabile a più componenti.</span><span class="sxs-lookup"><span data-stu-id="fe037-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="fe037-138">L'operazione seguente non riesce perché l'istruzione if richiede un singolo bool ma riceve un bool4:</span><span class="sxs-lookup"><span data-stu-id="fe037-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="fe037-139">Le operazioni seguenti hanno esito positivo:</span><span class="sxs-lookup"><span data-stu-id="fe037-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="fe037-140">Gli operatori di cast binari [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md)e così via funzionano per componente, ad eccezione di [**asdouble**](asdouble.md) le cui regole speciali sono documentate.</span><span class="sxs-lookup"><span data-stu-id="fe037-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="fe037-141">Gli operatori di selezione, ad esempio punto, virgola e parentesi di matrice, non funzionano per componente.</span><span class="sxs-lookup"><span data-stu-id="fe037-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="fe037-142">Gli operatori cast modificano il numero di componenti.</span><span class="sxs-lookup"><span data-stu-id="fe037-142">Cast operators change the number of components.</span></span> <span data-ttu-id="fe037-143">Le operazioni cast seguenti mostrano l'equivalenza:</span><span class="sxs-lookup"><span data-stu-id="fe037-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="fe037-144">Operatori additivi e moltiplicativi</span><span class="sxs-lookup"><span data-stu-id="fe037-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="fe037-145">Gli operatori additivi e moltiplicativi sono: +, -, \* , /, %</span><span class="sxs-lookup"><span data-stu-id="fe037-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



<span data-ttu-id="fe037-146">L'operatore modulo restituisce il resto di una divisione.</span><span class="sxs-lookup"><span data-stu-id="fe037-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="fe037-147">Ciò produce risultati diversi quando si usano numeri interi e numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="fe037-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="fe037-148">I resti interi frazionari verranno troncati.</span><span class="sxs-lookup"><span data-stu-id="fe037-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="fe037-149">L'operatore modulo tronca un resto frazionario quando si usano numeri interi.</span><span class="sxs-lookup"><span data-stu-id="fe037-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="fe037-150">L'operatore % viene definito solo nei casi in cui entrambi i lati sono positivi o entrambi i lati sono negativi.</span><span class="sxs-lookup"><span data-stu-id="fe037-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="fe037-151">A differenza di C, funziona anche su tipi di dati a virgola mobile, nonché su numeri interi.</span><span class="sxs-lookup"><span data-stu-id="fe037-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="fe037-152">Operatore Array</span><span class="sxs-lookup"><span data-stu-id="fe037-152">Array Operator</span></span>

<span data-ttu-id="fe037-153">L'operatore di selezione dei membri della matrice " \[ i " seleziona uno o più componenti in una \] matrice.</span><span class="sxs-lookup"><span data-stu-id="fe037-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="fe037-154">È un set di parentesi quadre che contengono un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="fe037-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="fe037-155">L'operatore array può essere usato anche per accedere a un vettore.</span><span class="sxs-lookup"><span data-stu-id="fe037-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="fe037-156">Aggiungendo un indice aggiuntivo, l'operatore array può anche accedere a una matrice.</span><span class="sxs-lookup"><span data-stu-id="fe037-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="fe037-157">Il primo indice è l'indice di riga in base zero.</span><span class="sxs-lookup"><span data-stu-id="fe037-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="fe037-158">Il secondo indice è l'indice di colonna in base zero.</span><span class="sxs-lookup"><span data-stu-id="fe037-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="fe037-159">Operatori di assegnazione</span><span class="sxs-lookup"><span data-stu-id="fe037-159">Assignment Operators</span></span>

<span data-ttu-id="fe037-160">Gli operatori di assegnazione sono: =, +=, -=, \* =, /=</span><span class="sxs-lookup"><span data-stu-id="fe037-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="fe037-161">Alle variabili possono essere assegnati valori letterali:</span><span class="sxs-lookup"><span data-stu-id="fe037-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="fe037-162">È anche possibile assegnare alle variabili il risultato di un'operazione matematica:</span><span class="sxs-lookup"><span data-stu-id="fe037-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="fe037-163">Una variabile può essere usata su entrambi i lati del segno di uguale:</span><span class="sxs-lookup"><span data-stu-id="fe037-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="fe037-164">La divisione per le variabili a virgola mobile è come previsto perché i resti decimali non sono un problema.</span><span class="sxs-lookup"><span data-stu-id="fe037-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="fe037-165">Prestare attenzione se si usano numeri interi che possono essere divisi, soprattutto quando il troncamento influisce sul risultato.</span><span class="sxs-lookup"><span data-stu-id="fe037-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="fe037-166">Questo esempio è identico all'esempio precedente, ad eccezione del tipo di dati .</span><span class="sxs-lookup"><span data-stu-id="fe037-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="fe037-167">Il troncamento causa un risultato molto diverso.</span><span class="sxs-lookup"><span data-stu-id="fe037-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="fe037-168">Cast binari</span><span class="sxs-lookup"><span data-stu-id="fe037-168">Binary Casts</span></span>

<span data-ttu-id="fe037-169">L'operazione di cast tra int e float converte il valore numerico nelle rappresentazioni appropriate in base alle regole C per il troncamento di un tipo int.</span><span class="sxs-lookup"><span data-stu-id="fe037-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="fe037-170">Il cast di un valore da float a int e di nuovo a un tipo float comporta una conversione in perdita in base alla precisione della destinazione.</span><span class="sxs-lookup"><span data-stu-id="fe037-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="fe037-171">I cast binari possono essere eseguiti anche usando [**funzioni intrinseche (DirectX HLSL),**](dx-graphics-hlsl-intrinsic-functions.md)che reinterpretano la rappresentazione in bit di un numero nel tipo di dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fe037-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="fe037-172">Operatori bit per bit</span><span class="sxs-lookup"><span data-stu-id="fe037-172">Bitwise Operators</span></span>

<span data-ttu-id="fe037-173">HLSL supporta gli operatori bit per bit seguenti, che seguono la stessa precedenza di C rispetto ad altri operatori.</span><span class="sxs-lookup"><span data-stu-id="fe037-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="fe037-174">Nella tabella seguente vengono descritti gli operatori .</span><span class="sxs-lookup"><span data-stu-id="fe037-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="fe037-175">Gli operatori bit per bit [richiedono Shader Model \_ 4 0](dx-graphics-hlsl-sm4.md) con Direct3D 10 e hardware superiore.</span><span class="sxs-lookup"><span data-stu-id="fe037-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



| <span data-ttu-id="fe037-176">Operatore</span><span class="sxs-lookup"><span data-stu-id="fe037-176">Operator</span></span>          |  <span data-ttu-id="fe037-177">Funzione</span><span class="sxs-lookup"><span data-stu-id="fe037-177">Function</span></span>                 |
|-----------|-------------------|
| ~         | <span data-ttu-id="fe037-178">Not logico</span><span class="sxs-lookup"><span data-stu-id="fe037-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="fe037-179">Maiusc di sinistra</span><span class="sxs-lookup"><span data-stu-id="fe037-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="fe037-180">Maiusc di destra</span><span class="sxs-lookup"><span data-stu-id="fe037-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="fe037-181">And logico</span><span class="sxs-lookup"><span data-stu-id="fe037-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="fe037-182">Esegue un'operazione di Or logico.</span><span class="sxs-lookup"><span data-stu-id="fe037-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="fe037-183">Xor logico</span><span class="sxs-lookup"><span data-stu-id="fe037-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="fe037-184">Maiusc di sinistra uguale</span><span class="sxs-lookup"><span data-stu-id="fe037-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="fe037-185">Maiusc destro uguale</span><span class="sxs-lookup"><span data-stu-id="fe037-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="fe037-186">E uguale</span><span class="sxs-lookup"><span data-stu-id="fe037-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="fe037-187">O uguale a</span><span class="sxs-lookup"><span data-stu-id="fe037-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="fe037-188">Xor Uguale</span><span class="sxs-lookup"><span data-stu-id="fe037-188">Xor Equal</span></span>         |



 

<span data-ttu-id="fe037-189">Gli operatori bit per bit vengono definiti per operare solo sui tipi di dati int e uint.</span><span class="sxs-lookup"><span data-stu-id="fe037-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="fe037-190">Il tentativo di usare operatori bit per bit su tipi di dati float o struct restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="fe037-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="fe037-191">Operatori matematici booleani</span><span class="sxs-lookup"><span data-stu-id="fe037-191">Boolean Math Operators</span></span>

<span data-ttu-id="fe037-192">Gli operatori matematici booleani sono:  &&, \| \| , ?:</span><span class="sxs-lookup"><span data-stu-id="fe037-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="fe037-193">A differenza della valutazione di corto circuito di &&, e ?: in C, le espressioni HLSL non esereranno mai un corto circuito per una valutazione perché \| \| sono operazioni vettoriali.</span><span class="sxs-lookup"><span data-stu-id="fe037-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="fe037-194">Tutti i lati dell'espressione vengono sempre valutati.</span><span class="sxs-lookup"><span data-stu-id="fe037-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="fe037-195">Gli operatori booleani funzionano in base al componente.</span><span class="sxs-lookup"><span data-stu-id="fe037-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="fe037-196">Ciò significa che se si confrontano due vettori, il risultato è un vettore contenente il risultato booleano del confronto per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="fe037-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="fe037-197">Per le espressioni che usano operatori booleani, le dimensioni e il tipo di componente di ogni variabile vengono promossi in modo che siano uguali prima che venga eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe037-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="fe037-198">Il tipo alzato di livello determina la risoluzione in corrispondenza della quale viene eseguita l'operazione, nonché il tipo di risultato dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="fe037-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="fe037-199">Ad esempio, un'espressione int3 + float viene promossa a float3 + float3 per la valutazione e il risultato sarà di tipo float3.</span><span class="sxs-lookup"><span data-stu-id="fe037-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="fe037-200">Operatore cast</span><span class="sxs-lookup"><span data-stu-id="fe037-200">Cast Operator</span></span>

<span data-ttu-id="fe037-201">Un'espressione preceduta da un nome di tipo tra parentesi è un cast di tipo esplicito.</span><span class="sxs-lookup"><span data-stu-id="fe037-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="fe037-202">Un cast di tipo converte l'espressione originale nel tipo di dati del cast.</span><span class="sxs-lookup"><span data-stu-id="fe037-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="fe037-203">In generale, è possibile eseguire il cast dei tipi di dati semplici ai tipi di dati più complessi (con un cast di promozione), ma è possibile eseguire il cast solo di alcuni tipi di dati complessi in tipi di dati semplici (con un cast di abbassamento di livello).</span><span class="sxs-lookup"><span data-stu-id="fe037-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="fe037-204">È valido solo il cast del tipo sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="fe037-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="fe037-205">Ad esempio, espressioni come non `(int)myFloat = myInt;` sono valide.</span><span class="sxs-lookup"><span data-stu-id="fe037-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="fe037-206">In alternativa, utilizzare `myFloat = (float)myInt;`.</span><span class="sxs-lookup"><span data-stu-id="fe037-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="fe037-207">Il compilatore esegue anche il cast di tipo implicito.</span><span class="sxs-lookup"><span data-stu-id="fe037-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="fe037-208">Ad esempio, le due espressioni seguenti sono equivalenti:</span><span class="sxs-lookup"><span data-stu-id="fe037-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="fe037-209">Operatore virgola</span><span class="sxs-lookup"><span data-stu-id="fe037-209">Comma Operator</span></span>

<span data-ttu-id="fe037-210">L'operatore virgola (,) separa una o più espressioni che devono essere valutate in ordine.</span><span class="sxs-lookup"><span data-stu-id="fe037-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="fe037-211">Il valore dell'ultima espressione nella sequenza viene usato come valore della sequenza.</span><span class="sxs-lookup"><span data-stu-id="fe037-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="fe037-212">Ecco un caso a cui vale la pena richiamare l'attenzione.</span><span class="sxs-lookup"><span data-stu-id="fe037-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="fe037-213">Se il tipo di costruttore viene accidentalmente lasciato fuori dal lato destro del segno di uguale, il lato destro contiene ora quattro espressioni, separate da tre virgole.</span><span class="sxs-lookup"><span data-stu-id="fe037-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="fe037-214">L'operatore virgola valuta un'espressione da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="fe037-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="fe037-215">In questo modo si riduce il lato destro per:</span><span class="sxs-lookup"><span data-stu-id="fe037-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="fe037-216">HLSL usa la promozione scalare in questo caso, quindi il risultato è come se fosse scritto come segue:</span><span class="sxs-lookup"><span data-stu-id="fe037-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="fe037-217">In questo caso, lasciare il tipo float4 dal lato destro è probabilmente un errore che il compilatore non è in grado di rilevare perché si tratta di un'istruzione valida.</span><span class="sxs-lookup"><span data-stu-id="fe037-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="fe037-218">Operatori di confronto</span><span class="sxs-lookup"><span data-stu-id="fe037-218">Comparison Operators</span></span>

<span data-ttu-id="fe037-219">Gli operatori di confronto sono: <, >, ==, !=, <=, >=.</span><span class="sxs-lookup"><span data-stu-id="fe037-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="fe037-220">Confrontare i valori maggiori o minori di qualsiasi valore scalare:</span><span class="sxs-lookup"><span data-stu-id="fe037-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="fe037-221">In caso contrario, confrontare i valori uguali (o non uguali) a qualsiasi valore scalare:</span><span class="sxs-lookup"><span data-stu-id="fe037-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="fe037-222">Oppure combinare e confrontare valori maggiori o uguali a (o minori o uguali a) qualsiasi valore scalare:</span><span class="sxs-lookup"><span data-stu-id="fe037-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="fe037-223">Ognuno di questi confronti può essere eseguito con qualsiasi tipo di dati scalare.</span><span class="sxs-lookup"><span data-stu-id="fe037-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="fe037-224">Per usare gli operatori di confronto con i tipi di vettore e matrice, usare la [**funzione intrinseca all**](dx-graphics-hlsl-all.md) [**o**](dx-graphics-hlsl-any.md) any.</span><span class="sxs-lookup"><span data-stu-id="fe037-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="fe037-225">Questa operazione ha esito negativo perché l'istruzione if richiede un solo bool ma riceve un valore bool4:</span><span class="sxs-lookup"><span data-stu-id="fe037-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="fe037-226">Queste operazioni hanno esito positivo:</span><span class="sxs-lookup"><span data-stu-id="fe037-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="fe037-227">Operatori prefisso o suffisso</span><span class="sxs-lookup"><span data-stu-id="fe037-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="fe037-228">Gli operatori prefisso e suffisso sono: ++, --.</span><span class="sxs-lookup"><span data-stu-id="fe037-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="fe037-229">Gli operatori di prefisso modificano il contenuto della variabile prima che l'espressione venga valutata.</span><span class="sxs-lookup"><span data-stu-id="fe037-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="fe037-230">Gli operatori suffissi modificano il contenuto della variabile dopo la valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="fe037-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="fe037-231">In questo caso, un ciclo usa il contenuto di i per tenere traccia del conteggio dei cicli.</span><span class="sxs-lookup"><span data-stu-id="fe037-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="fe037-232">Poiché viene usato l'operatore di incremento suffisso (++), arrayOfFloats i viene moltiplicato per \[ \] 2 prima che i venga incrementato.</span><span class="sxs-lookup"><span data-stu-id="fe037-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="fe037-233">Questa operazione potrebbe essere leggermente ridisposta in modo da usare l'operatore di incremento prefisso.</span><span class="sxs-lookup"><span data-stu-id="fe037-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="fe037-234">Questo è più difficile da leggere, anche se entrambi gli esempi sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="fe037-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="fe037-235">Poiché viene usato l'operatore prefisso (++), arrayOfFloats \[ i+1 - 1 viene moltiplicato per 2 dopo l'incremento \] di i.</span><span class="sxs-lookup"><span data-stu-id="fe037-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="fe037-236">L'operatore di decremento prefisso e decremento suffisso (--) viene applicato nella stessa sequenza dell'operatore di incremento.</span><span class="sxs-lookup"><span data-stu-id="fe037-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="fe037-237">La differenza è che il decremento sottrae 1 anziché aggiungere 1.</span><span class="sxs-lookup"><span data-stu-id="fe037-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="fe037-238">Operatore Structure</span><span class="sxs-lookup"><span data-stu-id="fe037-238">Structure Operator</span></span>

<span data-ttu-id="fe037-239">L'operatore di selezione dei membri della struttura (.) è un punto.</span><span class="sxs-lookup"><span data-stu-id="fe037-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="fe037-240">Data questa struttura:</span><span class="sxs-lookup"><span data-stu-id="fe037-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="fe037-241">Può essere letto nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="fe037-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="fe037-242">Ogni membro può essere letto o scritto con l'operatore structure:</span><span class="sxs-lookup"><span data-stu-id="fe037-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="fe037-243">Operatori unari</span><span class="sxs-lookup"><span data-stu-id="fe037-243">Unary Operators</span></span>

<span data-ttu-id="fe037-244">Gli operatori unari sono: !, -, +</span><span class="sxs-lookup"><span data-stu-id="fe037-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="fe037-245">Gli operatori unari operano su un singolo operando.</span><span class="sxs-lookup"><span data-stu-id="fe037-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="fe037-246">Ordine di precedenza degli operatori</span><span class="sxs-lookup"><span data-stu-id="fe037-246">Operator Precedence</span></span>

<span data-ttu-id="fe037-247">Quando un'espressione contiene più di un operatore, la precedenza degli operatori determina l'ordine di valutazione.</span><span class="sxs-lookup"><span data-stu-id="fe037-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="fe037-248">La precedenza degli operatori per HLSL segue la stessa precedenza di C.</span><span class="sxs-lookup"><span data-stu-id="fe037-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe037-249">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe037-249">Remarks</span></span>

<span data-ttu-id="fe037-250">Le parentesi graffe ( {,} ) avviano e terminano un blocco di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="fe037-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="fe037-251">Quando un blocco di istruzioni usa una singola istruzione, le parentesi graffe sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="fe037-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe037-252">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe037-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe037-253">Istruzioni (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe037-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




