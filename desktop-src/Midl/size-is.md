---
title: size_is (attributo)
description: Usare l'attributo \ size \_ is \ per specificare le dimensioni della memoria, negli elementi, allocati per i puntatori dimensionati, i puntatori dimensionati ai puntatori dimensionati e le matrici mono o multidimensionali.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- attributo size_is MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724946"
---
# <a name="size_is-attribute"></a><span data-ttu-id="48a18-104">size \_ è un attributo</span><span class="sxs-lookup"><span data-stu-id="48a18-104">size\_is attribute</span></span>

<span data-ttu-id="48a18-105">Usare l' \[ attributo **size \_ è** \] per specificare la dimensione della memoria, in elementi, allocata per i puntatori dimensionati, i puntatori dimensionati ai puntatori di dimensione e le matrici mono o multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="48a18-105">Use the \[**size\_is**\] attribute to specify the size of memory, in elements, allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.</span></span>

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a><span data-ttu-id="48a18-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="48a18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a18-107">*elenco di espressioni limitate*</span><span class="sxs-lookup"><span data-stu-id="48a18-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="48a18-108">Specifica una o più espressioni del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="48a18-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="48a18-109">Ogni espressione restituisce un numero intero non negativo che rappresenta la quantità di memoria allocata a un puntatore di dimensioni o una matrice.</span><span class="sxs-lookup"><span data-stu-id="48a18-109">Each expression evaluates to a non-negative integer that represents the amount of memory allocated to a sized pointer or an array.</span></span> <span data-ttu-id="48a18-110">Nel caso di una matrice, specifica una singola espressione che rappresenta la dimensione di allocazione, in elementi, della prima dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="48a18-110">In the case of an array, specifies a single expression that represents the allocation size, in elements, of the first dimension of that array.</span></span> <span data-ttu-id="48a18-111">Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="48a18-111">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="48a18-112">MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.</span><span class="sxs-lookup"><span data-stu-id="48a18-112">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="48a18-113">Utilizzare le virgole come segnaposto per i parametri impliciti o per separare più espressioni.</span><span class="sxs-lookup"><span data-stu-id="48a18-113">Use commas as placeholders for implicit parameters, or to separate multiple expressions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48a18-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="48a18-114">Remarks</span></span>

<span data-ttu-id="48a18-115">Se si utilizza la \[ **dimensione \_ è** \] attributo per allocare memoria per una matrice multidimensionale e si utilizza la \[ \] notazione di matrice, tenere presente che solo la prima dimensione di una matrice multidimensionale può essere determinata in modo dinamico in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="48a18-115">If you are using the \[**size\_is**\] attribute to allocate memory for a multidimensional array and you are using array \[ \] notation, keep in mind that only the first dimension of a multidimensional array can be dynamically determined at run time.</span></span> <span data-ttu-id="48a18-116">Le altre dimensioni devono essere specificate in modo statico.</span><span class="sxs-lookup"><span data-stu-id="48a18-116">The other dimensions must be statically specified.</span></span> <span data-ttu-id="48a18-117">Per ulteriori informazioni sull'utilizzo delle \[ **dimensioni \_ è** \] attributo con più livelli di puntatori per consentire a un server di restituire una matrice di dati di dimensioni dinamiche a un client, come illustrato nell'esempio Proc7, vedere [più livelli di puntatori](/windows/desktop/Rpc/multiple-levels-of-pointers).</span><span class="sxs-lookup"><span data-stu-id="48a18-117">For more information on using the \[**size\_is**\] attribute with multiple levels of pointers to enable a server to return a dynamically-sized array of data to a client, as shown in the example Proc7, see [Multiple Levels of Pointers](/windows/desktop/Rpc/multiple-levels-of-pointers).</span></span>

<span data-ttu-id="48a18-118">È possibile utilizzare le \[ **dimensioni \_** \] oppure il valore [**Max \_ è**](max-is.md) (ma non entrambi nello stesso elenco di attributi) per specificare le dimensioni di una matrice i cui limiti superiori vengono determinati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="48a18-118">You can use either \[**size\_is**\] or [**max\_is**](max-is.md) (but not both in the same attribute list) to specify the size of an array whose upper bounds are determined at run time.</span></span> <span data-ttu-id="48a18-119">Si noti, tuttavia, che la \[ **dimensione \_ è** \] attributo non può essere utilizzata sulle dimensioni della matrice fisse.</span><span class="sxs-lookup"><span data-stu-id="48a18-119">Note, however, that the \[**size\_is**\] attribute cannot be used on array dimensions that are fixed.</span></span> <span data-ttu-id="48a18-120">L' \[ attributo **Max \_ is** \] specifica l'indice di matrice valido massimo.</span><span class="sxs-lookup"><span data-stu-id="48a18-120">The \[**max\_is**\] attribute specifies the maximum valid array index.</span></span> <span data-ttu-id="48a18-121">Di conseguenza, se si specifica \[ size \_ è (n) \] equivale a specificare \[ Max \_ è (n-1) \] .</span><span class="sxs-lookup"><span data-stu-id="48a18-121">As a result, specifying \[size\_is(n)\] is equivalent to specifying \[max\_is(n-1)\].</span></span>

<span data-ttu-id="48a18-122">Un oggetto \[ [**in**](in.md) \] o \[ in, [**out**](out-idl.md) \] conforme-il parametro della matrice con l' \[ attributo [**stringa**](string.md) \] non deve avere la \[ **dimensione \_ è** \] o \[ [**Max \_ è**](max-is.md) \] Attribute.</span><span class="sxs-lookup"><span data-stu-id="48a18-122">An \[ [**in**](in.md)\] or \[in, [**out**](out-idl.md)\] conformant-array parameter with the \[ [**string**](string.md)\] attribute need not have the \[**size\_is**\] or \[[**max\_is**](max-is.md)\] attribute.</span></span> <span data-ttu-id="48a18-123">In questo caso, la dimensione dell'allocazione è determinata dal carattere di terminazione NULL della stringa di input.</span><span class="sxs-lookup"><span data-stu-id="48a18-123">In this case, the size of the allocation is determined from the NULL terminator of the input string.</span></span> <span data-ttu-id="48a18-124">Tutte le altre matrici conformi con l' \[ \] attributo stringa devono avere una \[ **dimensione \_** oppure il valore \] \[ **massimo \_ è** \] attributo.</span><span class="sxs-lookup"><span data-stu-id="48a18-124">All other conformant arrays with the \[string\] attribute must have a \[**size\_is**\] or \[**max\_is**\] attribute.</span></span>

<span data-ttu-id="48a18-125">Sebbene sia possibile utilizzare la \[ **dimensione \_ è** l' \] attributo con una costante, questa operazione non è efficiente e non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="48a18-125">While it is legal to use the \[**size\_is**\] attribute with a constant, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="48a18-126">Ad esempio, usare una matrice a dimensione fissa:</span><span class="sxs-lookup"><span data-stu-id="48a18-126">For example, use a fixed size array:</span></span>

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

<span data-ttu-id="48a18-127">invece di:</span><span class="sxs-lookup"><span data-stu-id="48a18-127">instead of:</span></span>

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

<span data-ttu-id="48a18-128">È possibile utilizzare la \[ **dimensione \_** \] e la \[ [**lunghezza \_ sono**](length-is.md) \] gli attributi insieme.</span><span class="sxs-lookup"><span data-stu-id="48a18-128">You can use the \[**size\_is**\] and \[[**length\_is**](length-is.md)\] attributes together.</span></span> <span data-ttu-id="48a18-129">Quando si esegue questa operazione, la \[ **dimensione \_ è** \] attributo che controlla la quantità di memoria allocata per i dati.</span><span class="sxs-lookup"><span data-stu-id="48a18-129">When you do, the \[**size\_is**\] attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="48a18-130">L' \[ **attributo \_ length** \] indica il numero di elementi trasmessi.</span><span class="sxs-lookup"><span data-stu-id="48a18-130">The \[**length\_is**\] attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="48a18-131">La quantità di memoria specificata dalla \[ **dimensione \_ è** \] e la \[ **lunghezza \_ è** che \] gli attributi non devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="48a18-131">The amount of memory specified by the \[**size\_is**\] and \[**length\_is**\] attributes need not be the same.</span></span> <span data-ttu-id="48a18-132">Ad esempio, il client può passare un \[ parametro in, out \] a un server e specificare un'allocazione di memoria di grandi dimensioni \[ **\_** \] , anche se specifica un numero ridotto di elementi di dati da passare con \[ **length \_** \] .</span><span class="sxs-lookup"><span data-stu-id="48a18-132">For instance, your client may pass an \[in,out\] parameter to a server and specify a large memory allocation with \[**size\_is**\], even though it specifies a small number of data elements to be passed with \[**length\_is**\].</span></span> <span data-ttu-id="48a18-133">Ciò consente al server di riempire la matrice con un numero di dati superiore a quello ricevuto, che può quindi inviare di nuovo al client.</span><span class="sxs-lookup"><span data-stu-id="48a18-133">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="48a18-134">In generale, non è utile specificare le \[ **\_ dimensioni** \] e la \[ [**lunghezza \_ è**](length-is.md) nei \] \[ parametri in \] o \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="48a18-134">In general, it isn't useful to specify both \[**size\_is**\] and \[[**length\_is**](length-is.md)\] on \[in\] or \[out\] parameters.</span></span> <span data-ttu-id="48a18-135">In entrambi i casi, \[ **size \_** \] Controlla l'allocazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="48a18-135">In both cases, \[**size\_is**\] controls memory allocation.</span></span> <span data-ttu-id="48a18-136">È possibile che l'applicazione utilizzi \[ **dimensioni \_** \] per allocare più elementi di matrice rispetto a quanto trasmesso (come specificato dalla \[ **lunghezza \_** \] ).</span><span class="sxs-lookup"><span data-stu-id="48a18-136">Your application could use \[**size\_is**\] to allocate more array elements than it transmits (as specified by \[**length\_is**\]).</span></span> <span data-ttu-id="48a18-137">Tuttavia, questo sarebbe inefficiente.</span><span class="sxs-lookup"><span data-stu-id="48a18-137">However, this would be inefficient.</span></span> <span data-ttu-id="48a18-138">Sarebbe anche inefficiente specificare valori identici per \[ le **dimensioni e \_** la \] \[ **lunghezza \_ è** \] .</span><span class="sxs-lookup"><span data-stu-id="48a18-138">It would also be inefficient to specify identical values for \[**size\_is**\] and \[**length\_is**\].</span></span> <span data-ttu-id="48a18-139">Creerebbe un sovraccarico aggiuntivo durante il marshalling del parametro.</span><span class="sxs-lookup"><span data-stu-id="48a18-139">It would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="48a18-140">Se i valori di \[ **size \_** \] e \[ **length \_** \] sono sempre uguali, omettere la \[ **lunghezza \_ è** \] Attribute.</span><span class="sxs-lookup"><span data-stu-id="48a18-140">If the values of \[**size\_is**\] and \[**length\_is**\] are always the same, omit the \[**length\_is**\] attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="48a18-141">Esempi</span><span class="sxs-lookup"><span data-stu-id="48a18-141">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a><span data-ttu-id="48a18-142">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="48a18-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a18-143">**matrici**</span><span class="sxs-lookup"><span data-stu-id="48a18-143">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="48a18-144">Attributi di campo</span><span class="sxs-lookup"><span data-stu-id="48a18-144">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="48a18-145">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="48a18-145">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="48a18-146">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="48a18-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="48a18-147">**in**</span><span class="sxs-lookup"><span data-stu-id="48a18-147">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="48a18-148">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="48a18-148">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="48a18-149">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="48a18-149">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="48a18-150">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="48a18-150">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="48a18-151">**min \_ è**</span><span class="sxs-lookup"><span data-stu-id="48a18-151">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="48a18-152">**out**</span><span class="sxs-lookup"><span data-stu-id="48a18-152">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="48a18-153">**string**</span><span class="sxs-lookup"><span data-stu-id="48a18-153">**string**</span></span>](string.md)
</dt> </dl>

 

 