---
title: Attributo wire_marshal
description: L'attributo \ Wire \_ Marshal \ è un attributo di tipo IDL simile alla sintassi di \ trasmette \_ come \, ma fornisce un modo più efficiente per effettuare il marshalling dei dati in una rete.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- RPC, attributi, wire_marshal di procedura remota
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399420"
---
# <a name="the-wire_marshal-attribute"></a><span data-ttu-id="76d87-105">Attributo Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="76d87-105">The wire\_marshal Attribute</span></span>

<span data-ttu-id="76d87-106">L' \[ attributo [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] è un attributo di tipo IDL simile alla sintassi per la \[ [trasmissione \_ come](/windows/desktop/Midl/transmit-as) \] , ma fornisce un modo più efficiente per eseguire il marshalling dei dati in una rete.</span><span class="sxs-lookup"><span data-stu-id="76d87-106">The \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] attribute is an IDL-type attribute similar in syntax to \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\], but providing a more efficient way to marshal data across a network.</span></span>

<span data-ttu-id="76d87-107">L' \[ attributo **Wire \_ Marshal** viene utilizzato \] per specificare un tipo di dati che verrà trasmesso al posto del tipo di dati specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76d87-107">You use the \[**wire\_marshal**\] attribute to specify a data type that will be transmitted in place of the application-specific data type.</span></span> <span data-ttu-id="76d87-108">Ogni tipo specifico dell'applicazione ha un tipo transmittable corrispondente che definisce la rappresentazione in transito (la rappresentazione utilizzata sulla rete). Il tipo specifico dell'applicazione non deve essere transmittable, ma deve essere un tipo riconosciuto da MIDL.</span><span class="sxs-lookup"><span data-stu-id="76d87-108">Each application-specific type has a corresponding transmittable type that defines the wire representation (the representation used on the network).The application-specific type need not be transmittable, but it must be a type that MIDL recognizes.</span></span> <span data-ttu-id="76d87-109">Per effettuare il marshalling di un tipo sconosciuto a MIDL, usare il \[ [ \_ marshalling utente](/windows/desktop/Midl/user-marshal)dell'attributo ACF \] .</span><span class="sxs-lookup"><span data-stu-id="76d87-109">To marshal a type unknown to MIDL, use the ACF attribute \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\].</span></span>

<span data-ttu-id="76d87-110">Il tipo specifico dell'applicazione può essere un tipo semplice, composto o puntatore.</span><span class="sxs-lookup"><span data-stu-id="76d87-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="76d87-111">La restrizione principale è che l'istanza del tipo deve avere una dimensione di memoria fissa e ben definita.</span><span class="sxs-lookup"><span data-stu-id="76d87-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="76d87-112">Se è necessario modificare le dimensioni dell'istanza del tipo, utilizzare un campo puntatore anziché una matrice conforme.</span><span class="sxs-lookup"><span data-stu-id="76d87-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="76d87-113">In alternativa, è possibile definire un puntatore al tipo modificabile.</span><span class="sxs-lookup"><span data-stu-id="76d87-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="76d87-114">È necessario fornire le routine per il ridimensionamento, il marshalling e l'unmarshalling dei dati, oltre a liberare la memoria associata.</span><span class="sxs-lookup"><span data-stu-id="76d87-114">You must supply the routines for sizing, marshaling, and unmarshaling the data as well as freeing the associated memory.</span></span> <span data-ttu-id="76d87-115">Nella tabella seguente vengono descritti i quattro nomi di routine specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="76d87-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="76d87-116"><type>È il tipo utente specificato nella definizione del tipo di \[ **\_ marshalling di rete** \] .</span><span class="sxs-lookup"><span data-stu-id="76d87-116">The <type> is the userm-type specified in the \[**wire\_marshal**\] type definition.</span></span>



| <span data-ttu-id="76d87-117">Routine</span><span class="sxs-lookup"><span data-stu-id="76d87-117">Routine</span></span>                                                            | <span data-ttu-id="76d87-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76d87-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="76d87-119"><type>\_UserSize</span><span class="sxs-lookup"><span data-stu-id="76d87-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="76d87-120">Ridimensiona il buffer di dati RPC prima del marshalling sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="76d87-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="76d87-121"><type>\_UserMarshal</span><span class="sxs-lookup"><span data-stu-id="76d87-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="76d87-122">Esegue il marshalling dei dati sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="76d87-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="76d87-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="76d87-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="76d87-124">Esegue l'unmarshalling dei dati sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="76d87-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="76d87-125"><type>\_UserFree</span><span class="sxs-lookup"><span data-stu-id="76d87-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="76d87-126">Libera i dati sul lato server.</span><span class="sxs-lookup"><span data-stu-id="76d87-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="76d87-127">Queste routine fornite dal programmatore vengono fornite dal client o dall'applicazione server basata sugli attributi direzionali.</span><span class="sxs-lookup"><span data-stu-id="76d87-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span>

<span data-ttu-id="76d87-128">Se il parametro è \[ solo [in](/windows/desktop/Midl/in) \] , il client trasmette al server.</span><span class="sxs-lookup"><span data-stu-id="76d87-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="76d87-129">Il client richiede le funzioni **<type> \_ UserSize** e **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="76d87-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="76d87-130">Per il server sono necessarie le funzioni **<type> \_ UserUnmarshal** e **<type> \_ UserFree** .</span><span class="sxs-lookup"><span data-stu-id="76d87-130">The server needs the **<type>\_UserUnmarshal**, and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="76d87-131">Per un \[ [](/windows/desktop/Midl/out-idl) \] parametro di sola uscita, il server trasmette al client.</span><span class="sxs-lookup"><span data-stu-id="76d87-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="76d87-132">Il server necessita delle funzioni **<type> \_ UserSize** e **<type> \_ UserMarshal** , mentre il client richiede la funzione **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="76d87-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76d87-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76d87-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d87-134">\_Attributo Marshal utente</span><span class="sxs-lookup"><span data-stu-id="76d87-134">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="76d87-135">Regole di marshalling per \_ marshalling utente e \_ marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="76d87-135">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="76d87-136">\_marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="76d87-136">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="76d87-137">\_marshalling utente</span><span class="sxs-lookup"><span data-stu-id="76d87-137">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="76d87-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="76d87-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 