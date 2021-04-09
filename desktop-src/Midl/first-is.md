---
title: first_is (attributo)
description: L'attributo \ First \_ is \ specifica l'indice del primo elemento della matrice da trasmettere.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- attributo first_is MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872518"
---
# <a name="first_is-attribute"></a><span data-ttu-id="0e95e-104">primo \_ attributo</span><span class="sxs-lookup"><span data-stu-id="0e95e-104">first\_is attribute</span></span>

<span data-ttu-id="0e95e-105">Il \[ **primo attributo \_ è** \] che specifica l'indice del primo elemento di matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="0e95e-105">The \[**first\_is**\] attribute specifies the index of the first array element to be transmitted.</span></span>

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a><span data-ttu-id="0e95e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e95e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e95e-107">*elenco di espressioni limitate*</span><span class="sxs-lookup"><span data-stu-id="0e95e-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0e95e-108">Specifica una o più espressioni del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="0e95e-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="0e95e-109">Ogni espressione restituisce un intero che rappresenta l'indice della matrice del primo elemento di matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="0e95e-109">Each expression evaluates to an integer that represents the array index of the first array element to be transmitted.</span></span> <span data-ttu-id="0e95e-110">Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="0e95e-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="0e95e-111">MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.</span><span class="sxs-lookup"><span data-stu-id="0e95e-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="0e95e-112">Separare più espressioni con virgole.</span><span class="sxs-lookup"><span data-stu-id="0e95e-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e95e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e95e-113">Remarks</span></span>

<span data-ttu-id="0e95e-114">Se il **\[ primo \_ \]** attributo non è presente o se l'indice specificato è un numero negativo, l'elemento della matrice zero è il primo elemento trasmesso.</span><span class="sxs-lookup"><span data-stu-id="0e95e-114">If the **\[first\_is\]** attribute is not present, or if the specified index is a negative number, array element zero is the first element transmitted.</span></span>

<span data-ttu-id="0e95e-115">Il **\[ primo \_ attributo \] è** anche in grado di determinare i valori degli indici della matrice corrispondenti all' **\[** [**ultimo \_**](last-is.md) oggetto **\]** o la **\[** [**lunghezza \_ è**](length-is.md) **\]** attributo quando questi attributi non sono specificati.</span><span class="sxs-lookup"><span data-stu-id="0e95e-115">The **\[first\_is\]** attribute can also help determine the values of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** or **\[**[**length\_is**](length-is.md)**\]** attribute when these attributes are not specified.</span></span> <span data-ttu-id="0e95e-116">La relazione tra gli indici di matrice è la seguente:</span><span class="sxs-lookup"><span data-stu-id="0e95e-116">The relationship between these array indexes is:</span></span>

``` syntax
length = last - first + 1
```

<span data-ttu-id="0e95e-117">È inoltre necessario che la relazione seguente contenga:</span><span class="sxs-lookup"><span data-stu-id="0e95e-117">The following relationship must also hold:</span></span>

``` syntax
0 <= first_is <= max_is
```

<span data-ttu-id="0e95e-118">È necessario che la relazione seguente venga mantenuta quando **\[** [**Max \_ è**](max-is.md) **\] <= 0:**</span><span class="sxs-lookup"><span data-stu-id="0e95e-118">The following relationship must hold when **\[**[**max\_is**](max-is.md)**\] <= 0:**</span></span>

``` syntax
first_is == 0
```

<span data-ttu-id="0e95e-119">Il **\[ primo \_ attributo \] is** non può essere utilizzato contemporaneamente all' **\[** attributo [**String**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0e95e-119">The **\[first\_is\]** attribute cannot be used at the same time as the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="0e95e-120">L'utilizzo di un'espressione costante con il **\[ primo attributo \_ è \]** un utilizzo non appropriato dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="0e95e-120">Using a constant expression with the **\[first\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="0e95e-121">È valido, ma inefficiente, e comporterà il codice di marshalling più lento.</span><span class="sxs-lookup"><span data-stu-id="0e95e-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

## <a name="examples"></a><span data-ttu-id="0e95e-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="0e95e-122">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a><span data-ttu-id="0e95e-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0e95e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e95e-124">attributi di campo \_</span><span class="sxs-lookup"><span data-stu-id="0e95e-124">field\_attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="0e95e-125">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="0e95e-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0e95e-126">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="0e95e-126">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="0e95e-127">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="0e95e-127">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="0e95e-128">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="0e95e-128">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="0e95e-129">**min \_ è**</span><span class="sxs-lookup"><span data-stu-id="0e95e-129">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="0e95e-130">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="0e95e-130">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="0e95e-131">**string**</span><span class="sxs-lookup"><span data-stu-id="0e95e-131">**string**</span></span>](string.md)
</dt> </dl>

 

 