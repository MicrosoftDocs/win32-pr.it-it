---
title: Attributo user_marshal
description: L'attributo \ User \_ Marshal \ è un attributo di tipo ACF simile alla sintassi di \ rappresenta \_ come \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- RPC, attributi, user_marshal di procedura remota
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473806"
---
# <a name="the-user_marshal-attribute"></a><span data-ttu-id="f4175-105">\_Attributo Marshal utente</span><span class="sxs-lookup"><span data-stu-id="f4175-105">The user\_marshal Attribute</span></span>

<span data-ttu-id="f4175-106">L' \[ [attributo \_ Marshal utente](/windows/desktop/Midl/user-marshal) \] è un attributo di tipo ACF simile a sintassi per \[ [rappresentare \_ come](/windows/desktop/Midl/represent-as) \] .</span><span class="sxs-lookup"><span data-stu-id="f4175-106">The \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attribute is an ACF-type attribute similar in syntax to \[ [represent\_as](/windows/desktop/Midl/represent-as)\].</span></span> <span data-ttu-id="f4175-107">Come per l'attributo IDL, \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] , offre un modo più efficiente per effettuare il marshalling dei dati in una rete.</span><span class="sxs-lookup"><span data-stu-id="f4175-107">As with the IDL attribute, \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\], it offers a more efficient way to marshal data across a network.</span></span> <span data-ttu-id="f4175-108">Come attributo ACF, il **\[ \_ marshalling \] degli utenti** consente di effettuare il marshalling dei tipi di dati personalizzati sconosciuti a MIDL.</span><span class="sxs-lookup"><span data-stu-id="f4175-108">As an ACF attribute, **\[user\_marshal\]** lets you marshal custom data types that are unknown to MIDL.</span></span> <span data-ttu-id="f4175-109">Ogni tipo specifico dell'applicazione ha un tipo transmittable corrispondente che definisce la rappresentazione in transito.</span><span class="sxs-lookup"><span data-stu-id="f4175-109">Each application-specific type has a corresponding transmittable type that defines the wire representation.</span></span>

<span data-ttu-id="f4175-110">Il tipo specifico dell'applicazione può essere un tipo semplice, composto o puntatore.</span><span class="sxs-lookup"><span data-stu-id="f4175-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="f4175-111">La restrizione principale è che l'istanza del tipo deve avere una dimensione di memoria fissa e ben definita.</span><span class="sxs-lookup"><span data-stu-id="f4175-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="f4175-112">Se è necessario modificare le dimensioni dell'istanza del tipo, utilizzare un campo puntatore anziché una matrice conforme.</span><span class="sxs-lookup"><span data-stu-id="f4175-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="f4175-113">In alternativa, è possibile definire un puntatore al tipo modificabile.</span><span class="sxs-lookup"><span data-stu-id="f4175-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="f4175-114">Come per l'attributo **\[ Wire \_ Marshal \]** , vengono fornite routine per il ridimensionamento, il marshalling, l'unmarshalling e il rilascio di passaggi.</span><span class="sxs-lookup"><span data-stu-id="f4175-114">As with the **\[wire\_marshal\]** attribute, you supply routines for the sizing, marshaling, unmarshaling, and freeing passes.</span></span> <span data-ttu-id="f4175-115">Nella tabella seguente vengono descritti i quattro nomi di routine specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f4175-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="f4175-116"><type>È il *tipo* di utente specificato nella definizione del tipo di **\[ \_ marshalling \] dell'utente** .</span><span class="sxs-lookup"><span data-stu-id="f4175-116">The <type> is the userm-*type* specified in the **\[user\_marshal\]** type definition.</span></span>



| <span data-ttu-id="f4175-117">Routine</span><span class="sxs-lookup"><span data-stu-id="f4175-117">Routine</span></span>                                                            | <span data-ttu-id="f4175-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4175-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="f4175-119"><type>\_UserSize</span><span class="sxs-lookup"><span data-stu-id="f4175-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="f4175-120">Ridimensiona il buffer di dati RPC prima del marshalling sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="f4175-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="f4175-121"><type>\_UserMarshal</span><span class="sxs-lookup"><span data-stu-id="f4175-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="f4175-122">Esegue il marshalling dei dati sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="f4175-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="f4175-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="f4175-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="f4175-124">Esegue l'unmarshalling dei dati sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="f4175-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="f4175-125"><type>\_UserFree</span><span class="sxs-lookup"><span data-stu-id="f4175-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="f4175-126">Libera i dati sul lato server.</span><span class="sxs-lookup"><span data-stu-id="f4175-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="f4175-127">Queste routine fornite dall'utente vengono fornite dal client o dall'applicazione server, in base agli attributi direzionali.</span><span class="sxs-lookup"><span data-stu-id="f4175-127">These user-supplied routines are provided by either the client or the server application, based on the directional attributes.</span></span>

<span data-ttu-id="f4175-128">Se il parametro è \[ solo [in](/windows/desktop/Midl/in) \] , il client trasmette al server.</span><span class="sxs-lookup"><span data-stu-id="f4175-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="f4175-129">Il client richiede le funzioni **<type> \_ UserSize** e **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="f4175-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="f4175-130">Per il server sono necessarie le funzioni **<type> \_ UserUnmarshal** e **<type> \_ UserFree** .</span><span class="sxs-lookup"><span data-stu-id="f4175-130">The server needs the **<type>\_UserUnmarshal** and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="f4175-131">Per un \[ [](/windows/desktop/Midl/out-idl) \] parametro di sola uscita, il server trasmette al client.</span><span class="sxs-lookup"><span data-stu-id="f4175-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="f4175-132">Il server necessita delle funzioni **<type> \_ UserSize** e **<type> \_ UserMarshal** , mentre il client richiede la funzione **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="f4175-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4175-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4175-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4175-134">Attributo Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="f4175-134">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="f4175-135">Regole di marshalling per marshalling utente e \_ marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="f4175-135">Marshaling Rules for user marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="f4175-136">\_marshalling utente</span><span class="sxs-lookup"><span data-stu-id="f4175-136">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="f4175-137">\_marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="f4175-137">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="f4175-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="f4175-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 