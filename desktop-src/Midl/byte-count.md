---
title: attributo byte_count
description: L'attributo \ byte \_ count \ ACF è un attributo di parametro che associa una dimensione, in byte, all'area di memoria indicata dal puntatore.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- attributo byte_count MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334428"
---
# <a name="byte_count-attribute"></a><span data-ttu-id="4297f-104">byte \_ Count (attributo)</span><span class="sxs-lookup"><span data-stu-id="4297f-104">byte\_count attribute</span></span>

<span data-ttu-id="4297f-105">L'attributo di **\[ \_ numero \] di byte** ACF è un attributo di parametro che associa una dimensione, in byte, all'area di memoria indicata dal puntatore.</span><span class="sxs-lookup"><span data-stu-id="4297f-105">The **\[byte\_count\]** ACF attribute is a parameter attribute that associates a size, in bytes, with the memory area indicated by the pointer.</span></span>

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a><span data-ttu-id="4297f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4297f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4297f-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4297f-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4297f-108">Specifica zero o più attributi della funzione ACF.</span><span class="sxs-lookup"><span data-stu-id="4297f-108">Specifies zero or more ACF function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="4297f-109">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="4297f-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4297f-110">Specifica il nome della funzione definita nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="4297f-110">Specifies the name of the function defined in the IDL file.</span></span> <span data-ttu-id="4297f-111">Il nome della funzione è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4297f-111">The function name is required.</span></span>

</dd> <dt>

<span data-ttu-id="4297f-112">*nome-variabile-lunghezza*</span><span class="sxs-lookup"><span data-stu-id="4297f-112">*length-variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4297f-113">Specifica il nome del parametro [**\[ in \]**](in.md)-only che specifica la dimensione, in byte, dell'area di memoria a cui fa riferimento il *parametro-Name*.</span><span class="sxs-lookup"><span data-stu-id="4297f-113">Specifies the name of the [**\[in\]**](in.md)-only parameter that specifies the size, in bytes, of the memory area referenced by *parameter-name*.</span></span>

</dd> <dt>

<span data-ttu-id="4297f-114">*Nome parametro*</span><span class="sxs-lookup"><span data-stu-id="4297f-114">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4297f-115">Specifica il nome del parametro del puntatore di sola [**\[ uscita \]**](out-idl.md)definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="4297f-115">Specifies the name of the [**\[out\]**](out-idl.md)-only pointer parameter defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4297f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4297f-116">Remarks</span></span>

<span data-ttu-id="4297f-117">Il **\[ \_ numero \] di byte** dell'attributo ACF rappresenta un'estensione Microsoft per DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="4297f-117">The ACF attribute **\[byte\_count\]** represents a Microsoft extension to DCE IDL.</span></span> <span data-ttu-id="4297f-118">Pertanto, questo attributo non è disponibile quando si usa l'opzione del compilatore MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="4297f-118">Therefore, this attribute is not available when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

> [!Note]  
> <span data-ttu-id="4297f-119">L'attributo **\[ Count \] byte** non è più supportato nella sintassi NDR64 a causa della difficoltà di stima delle dimensioni necessarie per tutti i parametri [**\[ out \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="4297f-119">The **\[byte count\]** attribute is no longer supported in NDR64 syntax due to the difficulty in estimating the size required for all [**\[out\]**](out-idl.md) parameters.</span></span>

 

<span data-ttu-id="4297f-120">La memoria a cui fa riferimento il parametro puntatore è contigua e non viene allocata o liberata dagli stub client.</span><span class="sxs-lookup"><span data-stu-id="4297f-120">Memory referenced by the pointer parameter is contiguous and is not allocated or freed by the client stubs.</span></span> <span data-ttu-id="4297f-121">Questa funzionalità dell'attributo **\[ \_ conteggio \] byte** consente di creare un'area buffer permanente nella memoria client che può essere riutilizzata durante più di una chiamata alla procedura remota.</span><span class="sxs-lookup"><span data-stu-id="4297f-121">This feature of the **\[byte\_count\]** attribute lets you create a persistent buffer area in client memory that can be reused during more than one call to the remote procedure.</span></span>

<span data-ttu-id="4297f-122">La possibilità di disattivare l'allocazione di memoria stub client consente di ottimizzare l'applicazione per l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="4297f-122">The ability to turn off the client stub memory allocation lets you tune the application for efficiency.</span></span> <span data-ttu-id="4297f-123">Ad esempio, l'attributo **\[ \_ conteggio \] byte** può essere usato dalle funzioni del provider di servizi che usano Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="4297f-123">For example, the **\[byte\_count\]** attribute can be used by service-provider functions that use Microsoft RPC.</span></span> <span data-ttu-id="4297f-124">Quando un'applicazione utente chiama l'API del provider di servizi e invia un puntatore a un buffer, il provider di servizi può passare il puntatore del buffer alla funzione remota.</span><span class="sxs-lookup"><span data-stu-id="4297f-124">When a user application calls the service-provider API and sends a pointer to a buffer, the service provider can pass the buffer pointer on to the remote function.</span></span> <span data-ttu-id="4297f-125">Il provider di servizi può riutilizzare il buffer durante più chiamate remote senza forzare l'utente a riallocare l'area di memoria.</span><span class="sxs-lookup"><span data-stu-id="4297f-125">The service provider can reuse the buffer during multiple remote calls without forcing the user to reallocate the memory area.</span></span>

<span data-ttu-id="4297f-126">L'area di memoria può contenere strutture di dati complesse costituite da più puntatori.</span><span class="sxs-lookup"><span data-stu-id="4297f-126">The memory area can contain complex data structures that consist of multiple pointers.</span></span> <span data-ttu-id="4297f-127">Poiché l'area di memoria è contigua, l'applicazione non deve effettuare diverse chiamate per liberare singolarmente ogni puntatore e struttura.</span><span class="sxs-lookup"><span data-stu-id="4297f-127">Because the memory area is contiguous, the application does not have to make several calls to individually free each pointer and structure.</span></span> <span data-ttu-id="4297f-128">Al contrario, può allocare o liberare l'area di memoria con una sola chiamata all'allocazione di memoria o alla routine gratuita.</span><span class="sxs-lookup"><span data-stu-id="4297f-128">Instead, it can allocate or free the memory area with one call to the memory allocation or free routine.</span></span>

<span data-ttu-id="4297f-129">Il buffer deve essere un parametro di sola [**\[ uscita \]**](out-idl.md), mentre la lunghezza del buffer in byte deve essere un parametro solo [**\[ in \]**](in.md).</span><span class="sxs-lookup"><span data-stu-id="4297f-129">The buffer must be an [**\[out\]**](out-idl.md)-only parameter, while the buffer length in bytes must be an [**\[in\]**](in.md)-only parameter.</span></span>

<span data-ttu-id="4297f-130">Specificare un buffer sufficientemente grande da contenere tutti i parametri [**\[ out \]**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="4297f-130">Specify a buffer that is large enough to contain all the [**\[out\]**](out-idl.md) parameters.</span></span> <span data-ttu-id="4297f-131">A causa della spaziatura interna nascosta, utilizzare le sovrastime anziché i conteggi esatti.</span><span class="sxs-lookup"><span data-stu-id="4297f-131">Because of hidden padding, use overestimates rather than exact counts.</span></span> <span data-ttu-id="4297f-132">Ad esempio, i puntatori a 4 byte vengono sottoposti a unmarshalling su un limite allineato a 4 byte su piattaforme a 32 bit e puntatori a 8 byte su un limite di 8 byte su piattaforme a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4297f-132">For example, 4-byte pointers are unmarshaled on a 4-byte aligned boundary on 32-bit platforms and 8-byte pointers on an 8-byte boundary on 64-bit platforms.</span></span> <span data-ttu-id="4297f-133">La spaziatura interna dell'allineamento che verrà eseguita dagli Stub deve pertanto essere rappresentata nello spazio per il buffer.</span><span class="sxs-lookup"><span data-stu-id="4297f-133">Therefore, the alignment padding the stubs will perform must be accounted for in the space for the buffer.</span></span> <span data-ttu-id="4297f-134">Inoltre, i livelli di compressione utilizzati durante la compilazione in linguaggio C possono variare.</span><span class="sxs-lookup"><span data-stu-id="4297f-134">In addition, packing levels used during C-language compilation can vary.</span></span> <span data-ttu-id="4297f-135">Usare un valore di conteggio byte che conti per i byte di compressione aggiuntivi aggiunti per il livello di compressione usato durante la compilazione in linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="4297f-135">Use a byte count value that accounts for additional packing bytes added for the packing level used during C-language compilation.</span></span> <span data-ttu-id="4297f-136">Una procedura sicura che copre entrambe le piattaforme a 32 bit e le piattaforme a 64 bit consiste nel presupposto che ogni oggetto che entra nel blocco di memoria grande inizi a un indirizzo che è un multiplo di 8.</span><span class="sxs-lookup"><span data-stu-id="4297f-136">A safe practice that covers both 32 bit platforms and 64 bit platforms is to assume that each object going into the big memory block starts at an address that is a multiple of 8.</span></span>

## <a name="examples"></a><span data-ttu-id="4297f-137">Esempi</span><span class="sxs-lookup"><span data-stu-id="4297f-137">Examples</span></span>

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a><span data-ttu-id="4297f-138">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4297f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4297f-139">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="4297f-139">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="4297f-140">**in**</span><span class="sxs-lookup"><span data-stu-id="4297f-140">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="4297f-141">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="4297f-141">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="4297f-142">**/osf**</span><span class="sxs-lookup"><span data-stu-id="4297f-142">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="4297f-143">**out**</span><span class="sxs-lookup"><span data-stu-id="4297f-143">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="4297f-144">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="4297f-144">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 




