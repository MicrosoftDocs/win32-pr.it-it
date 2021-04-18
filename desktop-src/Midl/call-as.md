---
title: call_as (attributo)
description: L'attributo \ Call \_ As \ consente di eseguire il mapping di una funzione che non può essere chiamata in modalità remota a una funzione remota.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- attributo call_as MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299211"
---
# <a name="call_as-attribute"></a><span data-ttu-id="e5e2d-104">chiama \_ come attributo</span><span class="sxs-lookup"><span data-stu-id="e5e2d-104">call\_as attribute</span></span>

<span data-ttu-id="e5e2d-105">L'attributo **\[ Call \_ As \]** consente di eseguire il mapping di una funzione che non può essere chiamata in modalità remota a una funzione remota.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-105">The **\[call\_as\]** attribute enables you to map a function that cannot be called remotely to a remote function.</span></span>

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a><span data-ttu-id="e5e2d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5e2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e2d-107">*local-proc*</span><span class="sxs-lookup"><span data-stu-id="e5e2d-107">*local-proc*</span></span> 
</dt> <dd>

<span data-ttu-id="e5e2d-108">Specifica una routine definita dall'operazione.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-108">Specifies an operation-defined routine.</span></span>

</dd> <dt>

<span data-ttu-id="e5e2d-109">*operazione-attributo-List*</span><span class="sxs-lookup"><span data-stu-id="e5e2d-109">*operation-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e5e2d-110">Specifica uno o più attributi che si applicano all'operazione.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-110">Specifies one or more attributes that apply to the operation.</span></span> <span data-ttu-id="e5e2d-111">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e5e2d-112">*nome operazione*</span><span class="sxs-lookup"><span data-stu-id="e5e2d-112">*operation-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e5e2d-113">Specifica l'operazione denominata presentata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-113">Specifies the named operation presented to the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5e2d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5e2d-114">Remarks</span></span>

<span data-ttu-id="e5e2d-115">La possibilità di eseguire il mapping di una funzione che non può essere chiamata in modalità remota a una funzione remota è particolarmente utile nelle interfacce con numerosi tipi di parametro che non possono essere trasmessi attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-115">The ability to map a function that cannot be called remotely to a remote function is particularly helpful in interfaces that have numerous parameter types that cannot be transmitted across the network.</span></span> <span data-ttu-id="e5e2d-116">Anziché utilizzare molti tipi di **\[** [**rappresentazione \_**](represent-as.md) **\]** e **\[** [**trasmissione \_ come**](transmit-as.md) **\]** tipi, è possibile combinare tutte le conversioni utilizzando la **\[ chiamata \_ come \]** routine.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-116">Rather than using many **\[**[**represent\_as**](represent-as.md)**\]** and **\[**[**transmit\_as**](transmit-as.md)**\]** types, you can combine all the conversions using **\[call\_as\]** routines.</span></span> <span data-ttu-id="e5e2d-117">Si forniscono le due chiamate **\[ \_ come \]** routine (lato client e lato server) per associare la routine tra le chiamate dell'applicazione e le chiamate remote.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-117">You supply the two **\[call\_as\]** routines (client side and server side) to bind the routine between the application calls and the remote calls.</span></span>

<span data-ttu-id="e5e2d-118">La **\[ chiamata \_ come \]** attributo può essere usata per le interfacce oggetto.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-118">The **\[call\_as\]** attribute can be used for object interfaces.</span></span> <span data-ttu-id="e5e2d-119">In questo caso, la definizione dell'interfaccia può essere usata per le chiamate locali e per le chiamate remote perché **\[ Call \_ As \]** consente a un'interfaccia a cui non è possibile accedere in modalità remota di essere mappata in modo trasparente a un'interfaccia remota.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-119">In this case, the interface definition can be used for local calls as well as remote calls because **\[call\_as\]** allows an interface that can't be accessed remotely to be transparently mapped to a remote interface.</span></span> <span data-ttu-id="e5e2d-120">Impossibile utilizzare la **\[ chiamata \_ come \]** attributo con la modalità [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="e5e2d-120">The **\[call\_as\]** attribute cannot be used with [**/osf**](-osf.md) mode.</span></span>

<span data-ttu-id="e5e2d-121">Si supponga, ad esempio, che la routine **F1** nell'interfaccia oggetto **IFace** richieda numerose conversioni tra le chiamate utente e ciò che viene effettivamente trasmesso.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-121">For example, assume that the routine **f1** in object interface **IFace** requires numerous conversions between the user calls and what is actually transmitted.</span></span> <span data-ttu-id="e5e2d-122">Gli esempi seguenti descrivono i file IDL e ACF per l'interfaccia **IFace**:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-122">The following examples describe the IDL and ACF files for interface **IFace**:</span></span>

<span data-ttu-id="e5e2d-123">Nel file IDL per l'interfaccia **IFace**:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-123">In the IDL file for interface **IFace**:</span></span>

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

<span data-ttu-id="e5e2d-124">In ACF per l'interfaccia **IFace**:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-124">In the ACF for interface **IFace**:</span></span>

``` syntax
[call_as( f1 )] Remf1();
```

<span data-ttu-id="e5e2d-125">In questo modo il file di intestazione generato definisce l'interfaccia utilizzando la definizione **F1**, ma fornisce anche stub per **Remf1**.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-125">This causes the generated header file to define the interface using the definition of **f1**, yet it also provides stubs for **Remf1**.</span></span>

<span data-ttu-id="e5e2d-126">Il compilatore MIDL genererà il seguente vtable nel file di intestazione per l'interfaccia **IFace**:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-126">The MIDL compiler will generate the following Vtable in the header file for interface **IFace**:</span></span>

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

<span data-ttu-id="e5e2d-127">Il proxy sul lato client avrà quindi un tipico proxy generato da MIDL per **Remf1**, mentre lo stub del lato server per **Remf1** sarà lo stesso dello stub tipico generato da MIDL:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-127">The client-side proxy would then have a typical MIDL-generated proxy for **Remf1**, while the server side stub for **Remf1** would be the same as the typical MIDL-generated stub:</span></span>

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

<span data-ttu-id="e5e2d-128">Quindi, le due **\[ chiamate \_ come \] routine di** vincolo (lato client e lato server) devono essere codificate manualmente:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-128">Then, the two **\[call\_as\]** bond routines (client side and server side) must be manually coded:</span></span>

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

<span data-ttu-id="e5e2d-129">Per le interfacce oggetto, si tratta dei prototipi per le routine di vincolo.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-129">For object interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="e5e2d-130">Per lato client:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-130">For client side:</span></span>

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

<span data-ttu-id="e5e2d-131">Per lato server:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-131">For server side:</span></span>

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

<span data-ttu-id="e5e2d-132">Per le interfacce non oggetto, si tratta dei prototipi per le routine di vincolo.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-132">For nonobject interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="e5e2d-133">Per lato client:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-133">For client side:</span></span>

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

<span data-ttu-id="e5e2d-134">Per lato server:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-134">For server side:</span></span>

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a><span data-ttu-id="e5e2d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5e2d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e2d-136">**/osf**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-136">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="e5e2d-137">**rappresenta \_ come**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-137">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="e5e2d-138">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-138">**transmit\_as**</span></span>](transmit-as.md)
</dt> </dl>

 

 




