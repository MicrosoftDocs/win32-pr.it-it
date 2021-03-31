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
ms.openlocfilehash: 69fc29f366fa781483edb5fd4653674b387fd156
ms.sourcegitcommit: 37fb32f6150b6ca1db6c52d68a553ec2c8c0879a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2020
ms.locfileid: "104472342"
---
# <a name="operators"></a><span data-ttu-id="1abf2-103">Operatori</span><span class="sxs-lookup"><span data-stu-id="1abf2-103">Operators</span></span>

<span data-ttu-id="1abf2-104">Le espressioni sono sequenze di [variabili](dx-graphics-hlsl-variable-syntax.md) e valori letterali punteggiati da [operatori](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="1abf2-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="1abf2-105">Gli operatori determinano il modo in cui le variabili e i valori letterali vengono combinati, confrontati, selezionati e così via.</span><span class="sxs-lookup"><span data-stu-id="1abf2-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="1abf2-106">Gli operatori includono:</span><span class="sxs-lookup"><span data-stu-id="1abf2-106">The operators include:</span></span>



|                                                                                 |                                                                    |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="1abf2-107">Nome operatore</span><span class="sxs-lookup"><span data-stu-id="1abf2-107">Operator Name</span></span>                                                                   | <span data-ttu-id="1abf2-108">Operatori</span><span class="sxs-lookup"><span data-stu-id="1abf2-108">Operators</span></span>                                                          |
| [<span data-ttu-id="1abf2-109">Operatori additivi e moltiplicatori</span><span class="sxs-lookup"><span data-stu-id="1abf2-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="1abf2-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="1abf2-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="1abf2-111">Operatore array</span><span class="sxs-lookup"><span data-stu-id="1abf2-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="1abf2-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="1abf2-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="1abf2-113">Operatori di assegnazione</span><span class="sxs-lookup"><span data-stu-id="1abf2-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="1abf2-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="1abf2-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="1abf2-115">Cast binari</span><span class="sxs-lookup"><span data-stu-id="1abf2-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="1abf2-116">Regole c per le funzioni float e int, C o HLSL per bool</span><span class="sxs-lookup"><span data-stu-id="1abf2-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="1abf2-117">Operatori bit per bit</span><span class="sxs-lookup"><span data-stu-id="1abf2-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="1abf2-118">~,  <<,  >>, &, \| , ^,  <<=,  >>=, &=, \| =, ^ =</span><span class="sxs-lookup"><span data-stu-id="1abf2-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="1abf2-119">Operatori matematici booleani</span><span class="sxs-lookup"><span data-stu-id="1abf2-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="1abf2-120">& &, \| \| ,?:</span><span class="sxs-lookup"><span data-stu-id="1abf2-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="1abf2-121">Operatore cast</span><span class="sxs-lookup"><span data-stu-id="1abf2-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="1abf2-122">tipo</span><span class="sxs-lookup"><span data-stu-id="1abf2-122">(type)</span></span>                                                             |
| [<span data-ttu-id="1abf2-123">Operatore virgola</span><span class="sxs-lookup"><span data-stu-id="1abf2-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="1abf2-124">,</span><span class="sxs-lookup"><span data-stu-id="1abf2-124">,</span></span>                                                                  |
| [<span data-ttu-id="1abf2-125">Operatori di confronto</span><span class="sxs-lookup"><span data-stu-id="1abf2-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="1abf2-126"><, >, = =,! =, <=, >=</span><span class="sxs-lookup"><span data-stu-id="1abf2-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="1abf2-127">Operatori di prefisso o suffisso</span><span class="sxs-lookup"><span data-stu-id="1abf2-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="1abf2-128">++, --</span><span class="sxs-lookup"><span data-stu-id="1abf2-128">++, --</span></span>                                                             |
| [<span data-ttu-id="1abf2-129">Operatore Structure</span><span class="sxs-lookup"><span data-stu-id="1abf2-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="1abf2-130">.</span><span class="sxs-lookup"><span data-stu-id="1abf2-130">.</span></span>                                                                  |
| [<span data-ttu-id="1abf2-131">Operatori unari</span><span class="sxs-lookup"><span data-stu-id="1abf2-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="1abf2-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="1abf2-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="1abf2-133">Molti operatori sono per componente, il che significa che l'operazione viene eseguita in modo indipendente per ogni componente di ogni variabile.</span><span class="sxs-lookup"><span data-stu-id="1abf2-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="1abf2-134">Ad esempio, per una singola variabile componente è stata eseguita un'operazione.</span><span class="sxs-lookup"><span data-stu-id="1abf2-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="1abf2-135">D'altra parte, una variabile a quattro componenti esegue quattro operazioni, una per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="1abf2-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="1abf2-136">Tutti gli operatori che eseguono un'operazione sul valore, ad esempio + e \* , funzionano per componente.</span><span class="sxs-lookup"><span data-stu-id="1abf2-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="1abf2-137">Gli operatori di confronto richiedono un singolo componente per funzionare a meno che non si usi la funzione [**All**](dx-graphics-hlsl-all.md) o [**any**](dx-graphics-hlsl-any.md) intrinseca con una variabile a più componenti.</span><span class="sxs-lookup"><span data-stu-id="1abf2-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="1abf2-138">L'operazione seguente ha esito negativo perché l'istruzione if richiede un solo bool ma riceve un bool4:</span><span class="sxs-lookup"><span data-stu-id="1abf2-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="1abf2-139">Le operazioni seguenti hanno esito positivo:</span><span class="sxs-lookup"><span data-stu-id="1abf2-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="1abf2-140">Gli operatori di cast binari [**AsFloat**](dx-graphics-hlsl-asfloat.md), [**AsInt**](dx-graphics-hlsl-asint.md)e così via funzionano per componente, ad eccezione di [**AsDouble**](asdouble.md) le cui regole speciali sono documentate.</span><span class="sxs-lookup"><span data-stu-id="1abf2-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="1abf2-141">Gli operatori di selezione come il punto, la virgola e le parentesi di matrice non funzionano per componente.</span><span class="sxs-lookup"><span data-stu-id="1abf2-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="1abf2-142">Gli operatori cast modificano il numero di componenti.</span><span class="sxs-lookup"><span data-stu-id="1abf2-142">Cast operators change the number of components.</span></span> <span data-ttu-id="1abf2-143">Le operazioni cast seguenti mostrano l'equivalenza:</span><span class="sxs-lookup"><span data-stu-id="1abf2-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="1abf2-144">Operatori additivi e moltiplicatori</span><span class="sxs-lookup"><span data-stu-id="1abf2-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="1abf2-145">Gli operatori additivi e moltiplicatori sono: +,-, \* ,/,%</span><span class="sxs-lookup"><span data-stu-id="1abf2-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


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



<span data-ttu-id="1abf2-146">L'operatore modulo restituisce il resto di una divisione.</span><span class="sxs-lookup"><span data-stu-id="1abf2-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="1abf2-147">Questo produce risultati diversi quando si usano numeri interi e numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="1abf2-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="1abf2-148">I rimanenti integer che sono frazionari verranno troncati.</span><span class="sxs-lookup"><span data-stu-id="1abf2-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="1abf2-149">L'operatore modulo tronca un resto frazionario quando si usano numeri interi.</span><span class="sxs-lookup"><span data-stu-id="1abf2-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="1abf2-150">L'operatore% viene definito solo nei casi in cui entrambi i lati sono positivi o entrambi i lati sono negativi.</span><span class="sxs-lookup"><span data-stu-id="1abf2-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="1abf2-151">Diversamente da C, funziona anche sui tipi di dati a virgola mobile, nonché sui numeri interi.</span><span class="sxs-lookup"><span data-stu-id="1abf2-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="1abf2-152">Operatore array</span><span class="sxs-lookup"><span data-stu-id="1abf2-152">Array Operator</span></span>

<span data-ttu-id="1abf2-153">L'operatore di selezione dei membri della matrice " \[ i \] " seleziona uno o più componenti in una matrice.</span><span class="sxs-lookup"><span data-stu-id="1abf2-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="1abf2-154">Si tratta di un set di parentesi quadre che contengono un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="1abf2-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="1abf2-155">L'operatore di matrice può essere usato anche per accedere a un vettore.</span><span class="sxs-lookup"><span data-stu-id="1abf2-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="1abf2-156">Con l'aggiunta di un indice aggiuntivo, l'operatore di matrice può accedere anche a una matrice.</span><span class="sxs-lookup"><span data-stu-id="1abf2-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="1abf2-157">Il primo indice è l'indice di riga in base zero.</span><span class="sxs-lookup"><span data-stu-id="1abf2-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="1abf2-158">Il secondo indice è l'indice di colonna in base zero.</span><span class="sxs-lookup"><span data-stu-id="1abf2-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="1abf2-159">Operatori di assegnazione</span><span class="sxs-lookup"><span data-stu-id="1abf2-159">Assignment Operators</span></span>

<span data-ttu-id="1abf2-160">Gli operatori di assegnazione sono: =, + =,-=, \* =,/=</span><span class="sxs-lookup"><span data-stu-id="1abf2-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="1abf2-161">Alle variabili possono essere assegnati valori letterali:</span><span class="sxs-lookup"><span data-stu-id="1abf2-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="1abf2-162">Alle variabili è inoltre possibile assegnare il risultato di un'operazione matematica:</span><span class="sxs-lookup"><span data-stu-id="1abf2-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="1abf2-163">Una variabile può essere usata su entrambi i lati del segno di uguale:</span><span class="sxs-lookup"><span data-stu-id="1abf2-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="1abf2-164">La divisione per le variabili a virgola mobile è come previsto perché i residui decimali non rappresentano un problema.</span><span class="sxs-lookup"><span data-stu-id="1abf2-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="1abf2-165">Prestare attenzione se si usano numeri interi che possono essere divisi, specialmente quando il troncamento influiscono sul risultato.</span><span class="sxs-lookup"><span data-stu-id="1abf2-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="1abf2-166">Questo esempio è identico all'esempio precedente, ad eccezione del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="1abf2-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="1abf2-167">Il troncamento causa un risultato molto diverso.</span><span class="sxs-lookup"><span data-stu-id="1abf2-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="1abf2-168">Cast binari</span><span class="sxs-lookup"><span data-stu-id="1abf2-168">Binary Casts</span></span>

<span data-ttu-id="1abf2-169">Con l'operazione di cast tra int e float, il valore numerico viene convertito nelle rappresentazioni appropriate che seguono le regole C per il troncamento di un tipo int.</span><span class="sxs-lookup"><span data-stu-id="1abf2-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="1abf2-170">Eseguendo il cast di un valore da un valore float a un int e viceversa a un valore float si otterrà una conversione con perdita di valori in base alla precisione della destinazione.</span><span class="sxs-lookup"><span data-stu-id="1abf2-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="1abf2-171">I cast binari possono essere eseguiti anche usando [**funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), che riinterpretano la rappresentazione di bit di un numero nel tipo di dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1abf2-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="1abf2-172">Operatori bit per bit</span><span class="sxs-lookup"><span data-stu-id="1abf2-172">Bitwise Operators</span></span>

<span data-ttu-id="1abf2-173">HLSL supporta gli operatori bit per bit seguenti, che seguono la stessa precedenza di C rispetto ad altri operatori.</span><span class="sxs-lookup"><span data-stu-id="1abf2-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="1abf2-174">Nella tabella seguente vengono descritti gli operatori di.</span><span class="sxs-lookup"><span data-stu-id="1abf2-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="1abf2-175">Gli operatori bit per bit richiedono il [modello di Shader 4 \_ 0](dx-graphics-hlsl-sm4.md) con Direct3D 10 e hardware superiore.</span><span class="sxs-lookup"><span data-stu-id="1abf2-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



|           |                   |
|-----------|-------------------|
| <span data-ttu-id="1abf2-176">Operatore</span><span class="sxs-lookup"><span data-stu-id="1abf2-176">Operator</span></span>  | <span data-ttu-id="1abf2-177">Funzione</span><span class="sxs-lookup"><span data-stu-id="1abf2-177">Function</span></span>          |
| ~         | <span data-ttu-id="1abf2-178">Not logico</span><span class="sxs-lookup"><span data-stu-id="1abf2-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="1abf2-179">Spostamento a sinistra</span><span class="sxs-lookup"><span data-stu-id="1abf2-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="1abf2-180">Spostamento a destra</span><span class="sxs-lookup"><span data-stu-id="1abf2-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="1abf2-181">And logico</span><span class="sxs-lookup"><span data-stu-id="1abf2-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="1abf2-182">Esegue un'operazione di Or logico.</span><span class="sxs-lookup"><span data-stu-id="1abf2-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="1abf2-183">XOR logico</span><span class="sxs-lookup"><span data-stu-id="1abf2-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="1abf2-184">Spostamento a sinistra uguale</span><span class="sxs-lookup"><span data-stu-id="1abf2-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="1abf2-185">Spostamento a destra uguale</span><span class="sxs-lookup"><span data-stu-id="1abf2-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="1abf2-186">E uguale a</span><span class="sxs-lookup"><span data-stu-id="1abf2-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="1abf2-187">O uguale a</span><span class="sxs-lookup"><span data-stu-id="1abf2-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="1abf2-188">XOR uguale</span><span class="sxs-lookup"><span data-stu-id="1abf2-188">Xor Equal</span></span>         |



 

<span data-ttu-id="1abf2-189">Gli operatori bit per bit vengono definiti per operare solo sui tipi di dati int e uint.</span><span class="sxs-lookup"><span data-stu-id="1abf2-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="1abf2-190">Il tentativo di utilizzare operatori bit per bit sui tipi di dati float o struct provocherà un errore.</span><span class="sxs-lookup"><span data-stu-id="1abf2-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="1abf2-191">Operatori matematici booleani</span><span class="sxs-lookup"><span data-stu-id="1abf2-191">Boolean Math Operators</span></span>

<span data-ttu-id="1abf2-192">Gli operatori matematici booleani sono:  &&, \| \| ,?:</span><span class="sxs-lookup"><span data-stu-id="1abf2-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="1abf2-193">A differenza della valutazione a corto circuito di &&, \| \| e?: in C, le espressioni HLSL non eseguono mai un cortocircuito di valutazione perché si tratta di operazioni vettoriali.</span><span class="sxs-lookup"><span data-stu-id="1abf2-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="1abf2-194">Tutti i lati dell'espressione vengono sempre valutati.</span><span class="sxs-lookup"><span data-stu-id="1abf2-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="1abf2-195">Gli operatori booleani funzionano in base ai singoli componenti.</span><span class="sxs-lookup"><span data-stu-id="1abf2-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="1abf2-196">Ciò significa che se si confrontano due vettori, il risultato è un vettore che contiene il risultato booleano del confronto per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="1abf2-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="1abf2-197">Per le espressioni che usano operatori booleani, le dimensioni e il tipo di componente di ogni variabile vengono promossi come uguali prima che si verifichi l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1abf2-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="1abf2-198">Il tipo innalzato di livello determina la risoluzione in cui viene eseguita l'operazione e il tipo di risultato dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="1abf2-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="1abf2-199">Ad esempio, un'espressione INT3 + float verrà innalzata a float3 + float3 per la valutazione e il risultato sarà di tipo float3.</span><span class="sxs-lookup"><span data-stu-id="1abf2-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="1abf2-200">Operatore cast</span><span class="sxs-lookup"><span data-stu-id="1abf2-200">Cast Operator</span></span>

<span data-ttu-id="1abf2-201">Un'espressione preceduta da un nome di tipo tra parentesi è un cast di tipo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1abf2-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="1abf2-202">Un cast di tipo converte l'espressione originale nel tipo di dati del cast.</span><span class="sxs-lookup"><span data-stu-id="1abf2-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="1abf2-203">In generale, è possibile eseguire il cast dei tipi di dati semplici ai tipi di dati più complessi (con un cast di innalzamento di livello), ma è possibile eseguire il cast solo di alcuni tipi di dati complessi in tipi di dati semplici (con un cast di abbassamento di livello).</span><span class="sxs-lookup"><span data-stu-id="1abf2-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="1abf2-204">Il cast del tipo di lato destro è valido.</span><span class="sxs-lookup"><span data-stu-id="1abf2-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="1abf2-205">Ad esempio, le espressioni come non `(int)myFloat = myInt;` sono valide.</span><span class="sxs-lookup"><span data-stu-id="1abf2-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="1abf2-206">In alternativa, utilizzare `myFloat = (float)myInt;`.</span><span class="sxs-lookup"><span data-stu-id="1abf2-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="1abf2-207">Il compilatore esegue anche il cast implicito del tipo.</span><span class="sxs-lookup"><span data-stu-id="1abf2-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="1abf2-208">Ad esempio, le due espressioni seguenti sono equivalenti:</span><span class="sxs-lookup"><span data-stu-id="1abf2-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="1abf2-209">Operatore virgola</span><span class="sxs-lookup"><span data-stu-id="1abf2-209">Comma Operator</span></span>

<span data-ttu-id="1abf2-210">L'operatore virgola (,) separa una o più espressioni che devono essere valutate in ordine.</span><span class="sxs-lookup"><span data-stu-id="1abf2-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="1abf2-211">Il valore dell'ultima espressione nella sequenza viene utilizzato come valore della sequenza.</span><span class="sxs-lookup"><span data-stu-id="1abf2-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="1abf2-212">Di seguito è riportato un caso che vale la pena richiamare attenzione a.</span><span class="sxs-lookup"><span data-stu-id="1abf2-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="1abf2-213">Se il tipo di costruttore viene accidentalmente lasciato dal lato destro del segno di uguale, il lato destro contiene ora quattro espressioni, separate da tre virgole.</span><span class="sxs-lookup"><span data-stu-id="1abf2-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="1abf2-214">L'operatore virgola valuta un'espressione da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="1abf2-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="1abf2-215">In questo modo si riduce il lato destro per:</span><span class="sxs-lookup"><span data-stu-id="1abf2-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="1abf2-216">In questo caso, HLSL usa la promozione scalare, quindi il risultato è come se fosse stato scritto nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="1abf2-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="1abf2-217">In questo caso, l'uscita dal tipo float4 dal lato destro è probabilmente un errore che il compilatore non è in grado di rilevare perché si tratta di un'istruzione valida.</span><span class="sxs-lookup"><span data-stu-id="1abf2-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="1abf2-218">Operatori di confronto</span><span class="sxs-lookup"><span data-stu-id="1abf2-218">Comparison Operators</span></span>

<span data-ttu-id="1abf2-219">Gli operatori di confronto sono: <, >, = =,! =, <=, >=.</span><span class="sxs-lookup"><span data-stu-id="1abf2-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="1abf2-220">Confrontare i valori che sono maggiori di (o minori di) qualsiasi valore scalare:</span><span class="sxs-lookup"><span data-stu-id="1abf2-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="1abf2-221">In alternativa, confrontare i valori uguali a (o non uguali) con qualsiasi valore scalare:</span><span class="sxs-lookup"><span data-stu-id="1abf2-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="1abf2-222">In alternativa, combinare e confrontare i valori che sono maggiori o uguali o minori o uguali a qualsiasi valore scalare:</span><span class="sxs-lookup"><span data-stu-id="1abf2-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="1abf2-223">Ognuno di questi confronti può essere eseguito con qualsiasi tipo di dati scalari.</span><span class="sxs-lookup"><span data-stu-id="1abf2-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="1abf2-224">Per utilizzare gli operatori di confronto con i tipi Vector e Matrix, utilizzare la funzione [**All**](dx-graphics-hlsl-all.md) o [**any**](dx-graphics-hlsl-any.md) intrinseca.</span><span class="sxs-lookup"><span data-stu-id="1abf2-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="1abf2-225">Questa operazione ha esito negativo perché l'istruzione if richiede un solo bool ma riceve un bool4:</span><span class="sxs-lookup"><span data-stu-id="1abf2-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="1abf2-226">Queste operazioni hanno esito positivo:</span><span class="sxs-lookup"><span data-stu-id="1abf2-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="1abf2-227">Operatori di prefisso o suffisso</span><span class="sxs-lookup"><span data-stu-id="1abf2-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="1abf2-228">Gli operatori prefisso e suffisso sono: + +,--.</span><span class="sxs-lookup"><span data-stu-id="1abf2-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="1abf2-229">Gli operatori di prefisso modificano il contenuto della variabile prima che l'espressione venga valutata.</span><span class="sxs-lookup"><span data-stu-id="1abf2-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="1abf2-230">Gli operatori di suffisso modificano il contenuto della variabile dopo la valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="1abf2-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="1abf2-231">In questo caso, un ciclo utilizza il contenuto di i per tenere traccia del conteggio dei cicli.</span><span class="sxs-lookup"><span data-stu-id="1abf2-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="1abf2-232">Poiché viene usato l'operatore di incremento suffisso (+ +), arrayOfFloats \[ i \] viene moltiplicato per 2 prima di essere incrementato.</span><span class="sxs-lookup"><span data-stu-id="1abf2-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="1abf2-233">Questa operazione potrebbe essere leggermente riordinata in modo da utilizzare l'operatore di incremento prefisso.</span><span class="sxs-lookup"><span data-stu-id="1abf2-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="1abf2-234">Questo è più difficile da leggere, sebbene entrambi gli esempi siano equivalenti.</span><span class="sxs-lookup"><span data-stu-id="1abf2-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="1abf2-235">Poiché viene usato l'operatore di prefisso (+ +), arrayOfFloats \[ i + 1-1 \] viene moltiplicato per 2 dopo l'incremento.</span><span class="sxs-lookup"><span data-stu-id="1abf2-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="1abf2-236">L'operatore di decremento prefisso e di decremento suffisso (--) viene applicato nella stessa sequenza dell'operatore di incremento.</span><span class="sxs-lookup"><span data-stu-id="1abf2-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="1abf2-237">La differenza consiste nel fatto che decrementa sottrae 1 anziché aggiungere 1.</span><span class="sxs-lookup"><span data-stu-id="1abf2-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="1abf2-238">Operatore Structure</span><span class="sxs-lookup"><span data-stu-id="1abf2-238">Structure Operator</span></span>

<span data-ttu-id="1abf2-239">L'operatore di selezione dei membri della struttura (.) è un punto.</span><span class="sxs-lookup"><span data-stu-id="1abf2-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="1abf2-240">Data questa struttura:</span><span class="sxs-lookup"><span data-stu-id="1abf2-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="1abf2-241">Può essere letto come segue:</span><span class="sxs-lookup"><span data-stu-id="1abf2-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="1abf2-242">Ogni membro può essere letto o scritto con l'operatore Structure:</span><span class="sxs-lookup"><span data-stu-id="1abf2-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="1abf2-243">Operatori unari</span><span class="sxs-lookup"><span data-stu-id="1abf2-243">Unary Operators</span></span>

<span data-ttu-id="1abf2-244">Gli operatori unari sono:!,-, +</span><span class="sxs-lookup"><span data-stu-id="1abf2-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="1abf2-245">Gli operatori unari operano su un singolo operando.</span><span class="sxs-lookup"><span data-stu-id="1abf2-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="1abf2-246">Ordine di precedenza degli operatori</span><span class="sxs-lookup"><span data-stu-id="1abf2-246">Operator Precedence</span></span>

<span data-ttu-id="1abf2-247">Quando un'espressione contiene più di un operatore, la precedenza degli operatori determina l'ordine di valutazione.</span><span class="sxs-lookup"><span data-stu-id="1abf2-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="1abf2-248">La precedenza degli operatori per HLSL segue la stessa precedenza di C.</span><span class="sxs-lookup"><span data-stu-id="1abf2-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="1abf2-249">Commenti</span><span class="sxs-lookup"><span data-stu-id="1abf2-249">Remarks</span></span>

<span data-ttu-id="1abf2-250">Le parentesi graffe ( {,} ) iniziano e terminano un blocco di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="1abf2-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="1abf2-251">Quando un blocco di istruzioni usa un'unica istruzione, le parentesi graffe sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="1abf2-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1abf2-252">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1abf2-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1abf2-253">Istruzioni (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1abf2-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




