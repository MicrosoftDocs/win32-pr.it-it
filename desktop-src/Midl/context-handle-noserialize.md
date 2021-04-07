---
title: attributo context_handle_noserialize
description: L'attributo \ Context \_ handle \_ noserialize \ ACF garantisce che un handle di contesto non verrà mai serializzato, indipendentemente dal comportamento predefinito dell'applicazione.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- attributo context_handle_noserialize MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724962"
---
# <a name="context_handle_noserialize-attribute"></a><span data-ttu-id="679ba-104">\_attributo noserialize dell'handle di contesto \_</span><span class="sxs-lookup"><span data-stu-id="679ba-104">context\_handle\_noserialize attribute</span></span>

<span data-ttu-id="679ba-105">L'attributo dell' **\[ handle di contesto \_ \_ noserialize \]** ACF garantisce che un handle di contesto non venga mai serializzato, indipendentemente dal comportamento predefinito dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="679ba-105">The **\[context\_handle\_noserialize\]** ACF attribute guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="679ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="679ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="679ba-107">*tipo-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="679ba-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="679ba-108">Qualsiasi altro attributo ACF applicabile al tipo.</span><span class="sxs-lookup"><span data-stu-id="679ba-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="679ba-109">*context-handle-tipo*</span><span class="sxs-lookup"><span data-stu-id="679ba-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="679ba-110">Identificatore che specifica il tipo di handle del contesto, come definito in una Dichiarazione [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="679ba-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="679ba-111">Si tratta del tipo che riceve l'attributo dell' [**\[ \_ handle \] del contesto**](context-handle.md) nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="679ba-111">This is the type that receives the [**\[context\_handle\]**](context-handle.md) attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="679ba-112">*funzione-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="679ba-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="679ba-113">Eventuali attributi ACF aggiuntivi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="679ba-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="679ba-114">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="679ba-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="679ba-115">Nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="679ba-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="679ba-116">*parametro-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="679ba-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="679ba-117">Qualsiasi altro attributo ACF applicabile al parametro.</span><span class="sxs-lookup"><span data-stu-id="679ba-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="679ba-118">*nome param*</span><span class="sxs-lookup"><span data-stu-id="679ba-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="679ba-119">Nome del parametro come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="679ba-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="679ba-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="679ba-120">Remarks</span></span>

<span data-ttu-id="679ba-121">L'attributo dell' [**\[ \_ handle \] di contesto**](context-handle.md) identifica un handle di associazione che mantiene le informazioni sul contesto o sullo stato sul server tra le chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="679ba-121">The [**\[context\_handle\]**](context-handle.md) attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span> <span data-ttu-id="679ba-122">L'attributo può essere visualizzato come un attributo di tipo [**typedef**](typedef.md) IDL, come attributo di tipo restituito della funzione o come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="679ba-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="679ba-123">Per impostazione predefinita, le chiamate agli handle di contesto vengono serializzate.</span><span class="sxs-lookup"><span data-stu-id="679ba-123">By default, calls on context handles are serialized.</span></span> <span data-ttu-id="679ba-124">Un'applicazione può chiamare [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) per eseguire l'override di questo comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="679ba-124">An application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="679ba-125">L'utilizzo dell'attributo [**\[ \_ handle \] di contesto**](context-handle.md) in un file ACF garantisce che le chiamate su questo particolare handle di contesto non verranno serializzate, indipendentemente dal comportamento dell'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="679ba-125">Using the [**\[context\_handle\]**](context-handle.md) attribute in an ACF file guarantees that calls on this particular context handle will not be serialized, regardless of the calling application's behavior.</span></span> <span data-ttu-id="679ba-126">La fornitura di una routine di rundown del contesto è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="679ba-126">Providing a context rundown routine is optional.</span></span>

<span data-ttu-id="679ba-127">Questo attributo è disponibile nella versione MIDL 5,0.</span><span class="sxs-lookup"><span data-stu-id="679ba-127">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="679ba-128">**Windows server 2003 e Windows XP o versione successiva:** Una singola interfaccia può supportare sia gli handle di contesto serializzati che quelli non serializzati, consentendo a un metodo su un'interfaccia di accedere a un handle di contesto esclusivamente (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzato).</span><span class="sxs-lookup"><span data-stu-id="679ba-128">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="679ba-129">Queste funzionalità di accesso sono confrontabili con i meccanismi di blocco in lettura/scrittura; i metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori).</span><span class="sxs-lookup"><span data-stu-id="679ba-129">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="679ba-130">I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati.</span><span class="sxs-lookup"><span data-stu-id="679ba-130">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="679ba-131">I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che leggono semplicemente da un handle di contesto, possono essere non serializzati.</span><span class="sxs-lookup"><span data-stu-id="679ba-131">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="679ba-132">Si noti che i metodi di creazione vengono serializzati in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="679ba-132">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="679ba-133">Esempi</span><span class="sxs-lookup"><span data-stu-id="679ba-133">Examples</span></span>

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="679ba-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="679ba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="679ba-135">Attributi ACF</span><span class="sxs-lookup"><span data-stu-id="679ba-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="679ba-136">**\_serializzazione handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="679ba-136">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="679ba-137">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="679ba-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="679ba-138">Handle di contesto</span><span class="sxs-lookup"><span data-stu-id="679ba-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="679ba-139">**RpcSsDontSerializeContext**</span><span class="sxs-lookup"><span data-stu-id="679ba-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="679ba-140">Routine di esecuzione del contesto del server</span><span class="sxs-lookup"><span data-stu-id="679ba-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="679ba-141">Client multithreading e handle di contesto</span><span class="sxs-lookup"><span data-stu-id="679ba-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="679ba-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="679ba-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 