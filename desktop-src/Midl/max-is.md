---
title: max_is (attributo)
description: L'attributo \ Max \_ is \ indica il valore massimo per un indice di matrice valido.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- attributo max_is MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337046"
---
# <a name="max_is-attribute"></a><span data-ttu-id="49269-104">\_attributo max is</span><span class="sxs-lookup"><span data-stu-id="49269-104">max\_is attribute</span></span>

<span data-ttu-id="49269-105">L'attributo **\[ Max \_ is \]** indica il valore massimo per un indice di matrice valido.</span><span class="sxs-lookup"><span data-stu-id="49269-105">The **\[max\_is\]** attribute designates the maximum value for a valid array index.</span></span>

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="49269-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49269-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49269-107">*elenco di espressioni limitate*</span><span class="sxs-lookup"><span data-stu-id="49269-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="49269-108">Specifica una o più espressioni del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="49269-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="49269-109">Ogni espressione restituisce un intero che rappresenta l'indice di matrice valido più alto.</span><span class="sxs-lookup"><span data-stu-id="49269-109">Each expression evaluates to an integer that represents the highest valid array index.</span></span> <span data-ttu-id="49269-110">Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="49269-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="49269-111">MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.</span><span class="sxs-lookup"><span data-stu-id="49269-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="49269-112">Separare più espressioni con virgole.</span><span class="sxs-lookup"><span data-stu-id="49269-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49269-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="49269-113">Remarks</span></span>

<span data-ttu-id="49269-114">L'attributo **\[ Max \_ is \]** non corrisponde necessariamente al numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="49269-114">The **\[max\_is\]** attribute does not necessarily correspond to the number of elements in the array.</span></span> <span data-ttu-id="49269-115">Per una matrice di dimensioni *n* in C, dove il primo elemento della matrice è il numero di elemento zero, il valore massimo per un indice di matrice valido è *n*-1.</span><span class="sxs-lookup"><span data-stu-id="49269-115">For an array of size *n* in C, where the first array element is element number zero, the maximum value for a valid array index is *n*–1.</span></span>

<span data-ttu-id="49269-116">L'attributo **\[ Max \_ is \]** non può essere utilizzato come attributo di campo allo stesso tempo della **\[** [**dimensione \_**](size-is.md) **\]** Attribute.</span><span class="sxs-lookup"><span data-stu-id="49269-116">The **\[max\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**size\_is**](size-is.md)**\]** attribute.</span></span>

<span data-ttu-id="49269-117">Sebbene sia possibile utilizzare l'attributo **\[ Max \_ is \]** con un'espressione costante, questa operazione non è efficiente e non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="49269-117">While it is legal to use the **\[max\_is\]** attribute with a constant expression, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="49269-118">Ad esempio, usare una matrice a dimensione fissa:</span><span class="sxs-lookup"><span data-stu-id="49269-118">For example, use a fixed size array:</span></span>

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

<span data-ttu-id="49269-119">invece di:</span><span class="sxs-lookup"><span data-stu-id="49269-119">instead of:</span></span>

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a><span data-ttu-id="49269-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="49269-120">Examples</span></span>

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a><span data-ttu-id="49269-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="49269-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49269-122">Attributi di campo</span><span class="sxs-lookup"><span data-stu-id="49269-122">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="49269-123">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="49269-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="49269-124">**min \_ è**</span><span class="sxs-lookup"><span data-stu-id="49269-124">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="49269-125">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="49269-125">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 