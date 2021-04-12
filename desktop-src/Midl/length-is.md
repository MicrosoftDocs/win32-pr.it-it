---
title: length_is (attributo)
description: L'attributo \ length \_ è \ specifica il numero di elementi della matrice da trasmettere. È necessario specificare un valore non negativo.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- attributo length_is MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473043"
---
# <a name="length_is-attribute"></a><span data-ttu-id="aba78-105">lunghezza \_ attributo</span><span class="sxs-lookup"><span data-stu-id="aba78-105">length\_is attribute</span></span>

<span data-ttu-id="aba78-106">L'attributo **\[ length \_ \]** indica il numero di elementi della matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="aba78-106">The **\[length\_is\]** attribute specifies the number of array elements to be transmitted.</span></span> <span data-ttu-id="aba78-107">È necessario specificare un valore non negativo.</span><span class="sxs-lookup"><span data-stu-id="aba78-107">You must specify a non-negative value.</span></span>

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="aba78-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aba78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aba78-109">*elenco di espressioni limitate*</span><span class="sxs-lookup"><span data-stu-id="aba78-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="aba78-110">Specifica una o più espressioni del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="aba78-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="aba78-111">Ogni espressione restituisce un valore integer che rappresenta il numero di elementi della matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="aba78-111">Each expression evaluates to an integer that represents the number of array elements to be transmitted.</span></span> <span data-ttu-id="aba78-112">Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="aba78-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="aba78-113">MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.</span><span class="sxs-lookup"><span data-stu-id="aba78-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="aba78-114">Separare più espressioni con virgole.</span><span class="sxs-lookup"><span data-stu-id="aba78-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aba78-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="aba78-115">Remarks</span></span>

<span data-ttu-id="aba78-116">L'attributo **\[ length \_ è \]** determinato dal valore degli indici della matrice corrispondenti all' **\[** [**\_**](last-is.md) **\]** **\[ \_ \]** ultimo attributo is quando non è specificato Last.</span><span class="sxs-lookup"><span data-stu-id="aba78-116">The **\[length\_is\]** attribute determines the value of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** attribute when **\[last\_is\]** is not specified.</span></span> <span data-ttu-id="aba78-117">La relazione tra questi indici di matrice è la seguente: length = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="aba78-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="aba78-118">La **\[ \_ lunghezza \]** dell'attributo non può essere utilizzata contemporaneamente all'attributo **\[** [**Last \_**](last-is.md) **\]** o **\[** [**String**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="aba78-118">The **\[length\_is\]** attribute cannot be used at the same time as the **\[**[**last\_is**](last-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="aba78-119">Per definire una stringa calcolata con un valore **\[ length \_ \]** o **\[** [**Last \_ è**](last-is.md) un **\]** attributo, utilizzare una matrice di caratteri o un puntatore senza l' **\[** attributo [**String**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="aba78-119">To define a counted string with a **\[length\_is\]** or **\[**[**last\_is**](last-is.md)**\]** attribute, use a character array or pointer without the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="aba78-120">L'utilizzo di un'espressione costante con la **\[ lunghezza \_ è \]** l'attributo non appropriato dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="aba78-120">Using a constant expression with the **\[length\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="aba78-121">È valido, ma inefficiente, e comporterà il codice di marshalling più lento.</span><span class="sxs-lookup"><span data-stu-id="aba78-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="aba78-122">È possibile utilizzare la **\[** [**dimensione \_**](size-is.md) **\]** e la **\[ lunghezza \_ sono \]** gli attributi insieme.</span><span class="sxs-lookup"><span data-stu-id="aba78-122">You can use the **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** attributes together.</span></span> <span data-ttu-id="aba78-123">Quando si esegue questa operazione, la **\[ dimensione \_ è \]** attributo che controlla la quantità di memoria allocata per i dati.</span><span class="sxs-lookup"><span data-stu-id="aba78-123">When you do, the **\[size\_is\]** attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="aba78-124">L'attributo **\[ length \_ \]** indica il numero di elementi trasmessi.</span><span class="sxs-lookup"><span data-stu-id="aba78-124">The **\[length\_is\]** attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="aba78-125">La quantità di memoria specificata dalla **\[ dimensione \_ è \]** e la **\[ lunghezza \_ è \]** che gli attributi non devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="aba78-125">The amount of memory specified by the **\[size\_is\]** and **\[length\_is\]** attributes need not be the same.</span></span> <span data-ttu-id="aba78-126">Ad esempio, il client può passare un parametro **\[ in**, **out \]** a un server e specificare un'allocazione di **\[ \_ \] memoria di grandi dimensioni, anche** se specifica un **\[ \_ \]** numero ridotto di elementi di dati da passare con length.</span><span class="sxs-lookup"><span data-stu-id="aba78-126">For instance, your client may pass an **\[in**, **out\]** parameter to a server and specify a large memory allocation with **\[size\_is\]**, even though it specifies a small number of data elements to be passed with **\[length\_is\]**.</span></span> <span data-ttu-id="aba78-127">Ciò consente al server di riempire la matrice con un numero di dati superiore a quello ricevuto, che può quindi inviare di nuovo al client.</span><span class="sxs-lookup"><span data-stu-id="aba78-127">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="aba78-128">In generale, non è utile specificare le **\[** [**dimensioni \_**](size-is.md) **\]** e la **\[ lunghezza \_ è \]** nei **\[** parametri [**in**](in.md) **\]** o **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="aba78-128">In general, it isn't useful to specify both **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** on **\[**[**in**](in.md)**\]** or **\[**[**out**](out-idl.md)**\]** parameters.</span></span> <span data-ttu-id="aba78-129">In entrambi i casi, **\[ size \_ \]** controlla l'allocazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="aba78-129">In both cases, **\[size\_is\]** controls memory allocation.</span></span> <span data-ttu-id="aba78-130">**\[ \_ È \]** possibile che l'applicazione utilizzi dimensioni per allocare più elementi di matrice rispetto a quanto trasmesso ( **\[ \_ \]** come specificato dalla lunghezza).</span><span class="sxs-lookup"><span data-stu-id="aba78-130">Your application could use **\[size\_is\]** to allocate more array elements than it transmits (as specified by **\[length\_is\]**).</span></span> <span data-ttu-id="aba78-131">Tuttavia, questo sarebbe inefficiente.</span><span class="sxs-lookup"><span data-stu-id="aba78-131">However, this would be inefficient.</span></span> <span data-ttu-id="aba78-132">Sarebbe anche inefficiente specificare valori identici per le **\[ dimensioni \_ \]** e la **\[ lunghezza \_ è \]**.</span><span class="sxs-lookup"><span data-stu-id="aba78-132">It would also be inefficient to specify identical values for **\[size\_is\]** and **\[length\_is\]**.</span></span> <span data-ttu-id="aba78-133">Poiché creerebbe un sovraccarico aggiuntivo durante il marshalling del parametro.</span><span class="sxs-lookup"><span data-stu-id="aba78-133">Because it would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="aba78-134">Quando i valori di **\[ size \_ \]** e **\[ \_ \] length** sono sempre gli stessi, omettere la **\[ lunghezza \_ è \]** Attribute.</span><span class="sxs-lookup"><span data-stu-id="aba78-134">When the values of **\[size\_is\]** and **\[length\_is\]** are always the same, omit the **\[length\_is\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="aba78-135">Esempi</span><span class="sxs-lookup"><span data-stu-id="aba78-135">Examples</span></span>

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a><span data-ttu-id="aba78-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aba78-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba78-137">Attributi di campo</span><span class="sxs-lookup"><span data-stu-id="aba78-137">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="aba78-138">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="aba78-138">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="aba78-139">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="aba78-139">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="aba78-140">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="aba78-140">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="aba78-141">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="aba78-141">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="aba78-142">**min \_ è**</span><span class="sxs-lookup"><span data-stu-id="aba78-142">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="aba78-143">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="aba78-143">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="aba78-144">**string**</span><span class="sxs-lookup"><span data-stu-id="aba78-144">**string**</span></span>](string.md)
</dt> </dl>

 

 