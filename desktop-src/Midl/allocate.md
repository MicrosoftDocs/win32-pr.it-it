---
title: alloca attributo
description: L'attributo \ allocate \ ACF consente di personalizzare l'allocazione e la deallocazione della memoria per un tipo definito nel file IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- alloca attributo MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857270"
---
# <a name="allocate-attribute"></a><span data-ttu-id="ef902-104">alloca attributo</span><span class="sxs-lookup"><span data-stu-id="ef902-104">allocate attribute</span></span>

<span data-ttu-id="ef902-105">L'attributo **\[ allocate \]** ACF consente di personalizzare l'allocazione e la deallocazione della memoria per un tipo definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="ef902-105">The **\[allocate\]** ACF attribute lets you customize memory allocation and deallocation for a type defined in the IDL file.</span></span>

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="ef902-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef902-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef902-107">*allocate-Option-List*</span><span class="sxs-lookup"><span data-stu-id="ef902-107">*allocate-option-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ef902-108">Specifica una o più opzioni di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="ef902-108">Specifies one or more memory-allocation options.</span></span> <span data-ttu-id="ef902-109">Selezionare uno dei nodi **a \_ nodo singolo** o a **tutti i \_ nodi** oppure una delle due coppie **disponibili** o **non \_ disponibili**.</span><span class="sxs-lookup"><span data-stu-id="ef902-109">Select one of either **single\_node** or **all\_nodes**, or one of either **free** or **dont\_free**, or one from each pair.</span></span> <span data-ttu-id="ef902-110">Quando si specifica più di un'opzione, separare le opzioni con virgole.</span><span class="sxs-lookup"><span data-stu-id="ef902-110">When you specify more than one option, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ef902-111">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ef902-111">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ef902-112">Specifica altri attributi di tipo ACF facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ef902-112">Specifies other optional ACF-type attributes.</span></span> <span data-ttu-id="ef902-113">Quando si specifica più di un attributo di tipo, separare le opzioni con virgole.</span><span class="sxs-lookup"><span data-stu-id="ef902-113">When you specify more than one type attribute, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ef902-114">*Nome-tipo*</span><span class="sxs-lookup"><span data-stu-id="ef902-114">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ef902-115">Specifica un tipo definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="ef902-115">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef902-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef902-116">Remarks</span></span>

<span data-ttu-id="ef902-117">L'attributo **\[ allocate \]** presenta le seguenti opzioni valide.</span><span class="sxs-lookup"><span data-stu-id="ef902-117">The **\[allocate\]** attribute has the following valid options.</span></span>



| <span data-ttu-id="ef902-118">Opzione</span><span class="sxs-lookup"><span data-stu-id="ef902-118">Option</span></span>           | <span data-ttu-id="ef902-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef902-119">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ef902-120">**tutti i \_ nodi**</span><span class="sxs-lookup"><span data-stu-id="ef902-120">**all\_nodes**</span></span>   | <span data-ttu-id="ef902-121">Effettua una chiamata per allocare e liberare memoria per tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="ef902-121">Makes one call to allocate and free memory for all nodes.</span></span>             |
| <span data-ttu-id="ef902-122">**\_nodo singolo**</span><span class="sxs-lookup"><span data-stu-id="ef902-122">**single\_node**</span></span> | <span data-ttu-id="ef902-123">Esegue molte chiamate singole per allocare e liberare ogni nodo di memoria.</span><span class="sxs-lookup"><span data-stu-id="ef902-123">Makes many individual calls to allocate and free each node of memory.</span></span> |
| <span data-ttu-id="ef902-124">**free**</span><span class="sxs-lookup"><span data-stu-id="ef902-124">**free**</span></span>         | <span data-ttu-id="ef902-125">Libera la memoria al ritorno dallo stub del server.</span><span class="sxs-lookup"><span data-stu-id="ef902-125">Frees memory on return from the server stub.</span></span>                          |
| <span data-ttu-id="ef902-126">**non \_ liberare**</span><span class="sxs-lookup"><span data-stu-id="ef902-126">**dont\_free**</span></span>   | <span data-ttu-id="ef902-127">Non libera la memoria al ritorno dallo stub del server.</span><span class="sxs-lookup"><span data-stu-id="ef902-127">Does not free memory on return from the server stub.</span></span>                  |



 

<span data-ttu-id="ef902-128">Per impostazione predefinita, gli stub possono allocare spazio di archiviazione per i dati a cui fa riferimento un puntatore univoco o completo chiamando l' [**\_ utente MIDL \_ allocate**](midl-user-allocate-1.md) e l' [**\_ utente MIDL \_ gratuitamente**](midl-user-free-1.md) singolarmente per ogni puntatore.</span><span class="sxs-lookup"><span data-stu-id="ef902-128">By default, the stubs may allocate storage for data referenced by a unique or full pointer by calling [**midl\_user\_allocate**](midl-user-allocate-1.md) and [**midl\_user\_free**](midl-user-free-1.md) individually for each pointer.</span></span>

<span data-ttu-id="ef902-129">È possibile ottimizzare la velocità dell'applicazione specificando l'opzione **tutti i \_ nodi**.</span><span class="sxs-lookup"><span data-stu-id="ef902-129">You can optimize the speed of your application by specifying the option **all\_nodes**.</span></span> <span data-ttu-id="ef902-130">Questa opzione indica allo stub di calcolare la dimensione di tutta la memoria a cui viene fatto riferimento tramite il puntatore del tipo specificato e di eseguire una singola chiamata [**all' \_ utente MIDL \_ allocate**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="ef902-130">This option directs the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span> <span data-ttu-id="ef902-131">Lo stub rilascia la memoria rendendo disponibile una sola chiamata [**a \_ MIDL \_ User**](midl-user-free-1.md).</span><span class="sxs-lookup"><span data-stu-id="ef902-131">The stub releases the memory by making one call to [**midl\_user\_free**](midl-user-free-1.md).</span></span>

<span data-ttu-id="ef902-132">L'opzione Not **\_ Free** indica al compilatore MIDL di generare uno stub del server che non chiama [**\_ \_ Free User MIDL**](midl-user-free-1.md) per il tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="ef902-132">The **dont\_free** option directs the MIDL compiler to generate a server stub that does not call [**midl\_user\_free**](midl-user-free-1.md) for the specified type.</span></span> <span data-ttu-id="ef902-133">L'opzione Not **\_ Free** consente alle strutture del puntatore di rimanere accessibili all'applicazione server dopo che la chiamata RPC è stata completata e restituita al client.</span><span class="sxs-lookup"><span data-stu-id="ef902-133">The **dont\_free** option allows the pointer structures to remain accessible to the server application after the remote procedure call has completed and returned to the client.</span></span>

<span data-ttu-id="ef902-134">L'attributo **\[ allocate \]** provocherà qualsiasi parametro **\[ in \] , out** che è un puntatore a un tipo qualificato con l'opzione **All \_ Nodes** per riallocare la memoria quando viene eseguito l'unmarshalling dei dati.</span><span class="sxs-lookup"><span data-stu-id="ef902-134">The **\[allocate\]** attribute will cause any **\[in, out\]** parameter that is a pointer to a type qualified with the **all\_nodes** option to reallocate memory when the data is unmarshaled.</span></span> <span data-ttu-id="ef902-135">È responsabilità dell'applicazione liberare la memoria allocata in precedenza per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ef902-135">It is the responsibility of the application to free the memory allocated previously for this parameter.</span></span> <span data-ttu-id="ef902-136">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="ef902-136">For example:</span></span>

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

<span data-ttu-id="ef902-137">Il tipo di dati PTHISTYPE verrà riallocato nella direzione di [**\[ uscita \]**](out-idl.md) dallo stub prima dell'unmarshalling.</span><span class="sxs-lookup"><span data-stu-id="ef902-137">The data type PTHISTYPE will be reallocated in the [**\[out\]**](out-idl.md) direction by the stub before unmarshaling.</span></span> <span data-ttu-id="ef902-138">Pertanto, l'applicazione deve liberare la memoria allocata in precedenza per i dati di questo parametro o si verificherà una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="ef902-138">Therefore, the application must free the memory it previously allocated for this parameter's data, or a memory leak will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="ef902-139">Esempi</span><span class="sxs-lookup"><span data-stu-id="ef902-139">Examples</span></span>

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a><span data-ttu-id="ef902-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ef902-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef902-141">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="ef902-141">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="ef902-142">**in**</span><span class="sxs-lookup"><span data-stu-id="ef902-142">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="ef902-143">**\_alloca utente \_ MIDL**</span><span class="sxs-lookup"><span data-stu-id="ef902-143">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="ef902-144">**\_utente MIDL \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="ef902-144">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="ef902-145">**out**</span><span class="sxs-lookup"><span data-stu-id="ef902-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="ef902-146">**typedef**</span><span class="sxs-lookup"><span data-stu-id="ef902-146">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




