---
title: last_is (attributo)
description: Il campo attributo \ Last \_ is \ specifica l'indice dell'ultimo elemento della matrice da trasmettere. Quando l'indice specificato è zero o negativo, non viene trasmesso alcun elemento della matrice.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- attributo last_is MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516774"
---
# <a name="last_is-attribute"></a><span data-ttu-id="e32d7-105">\_attributo Last is</span><span class="sxs-lookup"><span data-stu-id="e32d7-105">last\_is attribute</span></span>

<span data-ttu-id="e32d7-106">L'attributo Field **\[ Last \_ viene \]** specificato l'indice dell'ultimo elemento della matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="e32d7-106">The field attribute **\[last\_is\]** specifies the index of the last array element to be transmitted.</span></span> <span data-ttu-id="e32d7-107">Quando l'indice specificato è zero o negativo, non viene trasmesso alcun elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="e32d7-107">When the specified index is zero or negative, no array elements are transmitted.</span></span>

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="e32d7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e32d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e32d7-109">*elenco di espressioni limitate*</span><span class="sxs-lookup"><span data-stu-id="e32d7-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e32d7-110">Specifica una o più espressioni del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="e32d7-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="e32d7-111">Ogni espressione restituisce un intero che rappresenta l'indice della matrice dell'ultimo elemento della matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="e32d7-111">Each expression evaluates to an integer that represents the array index of the last array element to be transmitted.</span></span> <span data-ttu-id="e32d7-112">Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="e32d7-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="e32d7-113">MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.</span><span class="sxs-lookup"><span data-stu-id="e32d7-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="e32d7-114">Separare più espressioni con virgole.</span><span class="sxs-lookup"><span data-stu-id="e32d7-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e32d7-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e32d7-115">Remarks</span></span>

<span data-ttu-id="e32d7-116">L'attributo **\[ Last \_ is \]** determina che il valore dell'indice della matrice corrispondente alla **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** lunghezza è Attribute quando length non è specificato.</span><span class="sxs-lookup"><span data-stu-id="e32d7-116">The **\[last\_is\]** attribute determines the value of the array index corresponding to the **\[**[**length\_is**](length-is.md)**\]** attribute when **\[length\_is\]** is not specified.</span></span> <span data-ttu-id="e32d7-117">La relazione tra questi indici di matrice è la seguente: length = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="e32d7-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="e32d7-118">Se il valore dell'indice della matrice specificato da **\[** [**First \_**](first-is.md) è **\]** maggiore del valore specificato da **\[ Last \_ \] è**, verranno trasmessi zero elementi.</span><span class="sxs-lookup"><span data-stu-id="e32d7-118">If the value of the array index specified by **\[**[**first\_is**](first-is.md)**\]** is larger than the value specified by **\[last\_is\]**, zero elements are transmitted.</span></span>

<span data-ttu-id="e32d7-119">L'attributo **\[ Last \_ is \]** non può essere utilizzato come attributo di campo nello stesso momento in cui la **\[** [**lunghezza \_ è**](length-is.md) **\]** Attribute o l' **\[** attributo [**String**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e32d7-119">The **\[last\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**length\_is**](length-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="e32d7-120">L'utilizzo di un'espressione costante con l'attributo **\[ Last \_ è \]** un utilizzo non appropriato dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="e32d7-120">Using a constant expression with the **\[last\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="e32d7-121">È valido, ma inefficiente, e comporterà il codice di marshalling più lento.</span><span class="sxs-lookup"><span data-stu-id="e32d7-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="e32d7-122">Se il valore specificato da **\[** [**Max \_ è**](max-is.md) **\]** uguale a o maggiore di zero, deve essere true la relazione seguente: 0 <= Last \_ è <= Max \_ è.</span><span class="sxs-lookup"><span data-stu-id="e32d7-122">When the value specified by **\[**[**max\_is**](max-is.md)**\]** is equal to or greater than zero, the following relationship must be true: 0 <= last\_is <= max\_is.</span></span>

## <a name="examples"></a><span data-ttu-id="e32d7-123">Esempi</span><span class="sxs-lookup"><span data-stu-id="e32d7-123">Examples</span></span>

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a><span data-ttu-id="e32d7-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e32d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e32d7-125">Attributi di campo</span><span class="sxs-lookup"><span data-stu-id="e32d7-125">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="e32d7-126">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="e32d7-126">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="e32d7-127">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="e32d7-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e32d7-128">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="e32d7-128">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="e32d7-129">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="e32d7-129">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="e32d7-130">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="e32d7-130">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 