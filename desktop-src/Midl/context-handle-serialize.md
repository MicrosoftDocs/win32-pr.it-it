---
title: attributo context_handle_serialize
description: L'attributo \ Context \_ handle \_ Serialize \ ACF garantisce che un handle di contesto venga sempre serializzato, indipendentemente dal comportamento predefinito dell'applicazione.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- attributo context_handle_serialize MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299624"
---
# <a name="context_handle_serialize-attribute"></a><span data-ttu-id="1d571-104">\_attributo di serializzazione dell'handle di contesto \_</span><span class="sxs-lookup"><span data-stu-id="1d571-104">context\_handle\_serialize attribute</span></span>

<span data-ttu-id="1d571-105">L' **\[ handle del contesto \_ \_ serializzare \]** l'attributo ACF garantisce che un handle di contesto venga sempre serializzato, indipendentemente dal comportamento predefinito dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d571-105">The **\[context\_handle\_serialize\]** ACF attribute guarantees that a context handle will always be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="1d571-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d571-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d571-107">*tipo-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="1d571-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1d571-108">Qualsiasi altro attributo ACF applicabile al tipo.</span><span class="sxs-lookup"><span data-stu-id="1d571-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="1d571-109">*context-handle-tipo*</span><span class="sxs-lookup"><span data-stu-id="1d571-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1d571-110">Identificatore che specifica il tipo di handle del contesto, come definito in una Dichiarazione [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="1d571-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="1d571-111">Si tratta del tipo che riceve l'attributo di **\[ \_ \_ serializzazione \] dell'handle del contesto** nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="1d571-111">This is the type that receives the **\[context\_handle\_serialize\]** attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="1d571-112">*funzione-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="1d571-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1d571-113">Eventuali attributi ACF aggiuntivi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="1d571-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="1d571-114">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="1d571-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1d571-115">Nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="1d571-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="1d571-116">*parametro-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="1d571-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1d571-117">Qualsiasi altro attributo ACF applicabile al parametro.</span><span class="sxs-lookup"><span data-stu-id="1d571-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1d571-118">*nome param*</span><span class="sxs-lookup"><span data-stu-id="1d571-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1d571-119">Nome del parametro come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="1d571-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d571-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d571-120">Remarks</span></span>

<span data-ttu-id="1d571-121">L'attributo di **\[ \_ \_ serializzazione \] dell'handle di contesto** identifica un handle di associazione che mantiene le informazioni sul contesto o sullo stato sul server tra le chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="1d571-121">The **\[context\_handle\_serialize\]** attribute identifies a binding handle that maintains context or state information on the server between remote procedure calls.</span></span> <span data-ttu-id="1d571-122">L'attributo può essere visualizzato come un attributo di tipo [**typedef**](typedef.md) IDL, come attributo di tipo restituito della funzione o come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="1d571-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="1d571-123">Per impostazione predefinita, le chiamate agli handle di contesto vengono serializzate, ma un'applicazione può chiamare [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) per eseguire l'override di questo comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="1d571-123">By default, calls on context handles are serialized, but an application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="1d571-124">L'utilizzo dell'attributo di **\[ \_ \_ serializzazione \] dell'handle di contesto** in un file ACF garantisce che le chiamate su questo particolare handle di contesto verranno serializzate, anche se l'applicazione chiamante ha eseguito l'override della serializzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1d571-124">Using the **\[context\_handle\_serialize\]** attribute in an ACF file guarantees that calls on this particular context handle will be serialized, even if the calling application has overridden the default serialization.</span></span> <span data-ttu-id="1d571-125">Una routine di rundown del contesto è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="1d571-125">A context rundown routine is optional.</span></span>

<span data-ttu-id="1d571-126">Questo attributo è disponibile nella versione MIDL 5,0.</span><span class="sxs-lookup"><span data-stu-id="1d571-126">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="1d571-127">**Windows server 2003 e Windows XP o versione successiva:** Una singola interfaccia può supportare sia gli handle di contesto serializzati che quelli non serializzati, consentendo a un metodo su un'interfaccia di accedere a un handle di contesto esclusivamente (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzato).</span><span class="sxs-lookup"><span data-stu-id="1d571-127">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="1d571-128">Queste funzionalità di accesso sono confrontabili con i meccanismi di blocco in lettura/scrittura; i metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori).</span><span class="sxs-lookup"><span data-stu-id="1d571-128">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="1d571-129">I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati.</span><span class="sxs-lookup"><span data-stu-id="1d571-129">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="1d571-130">I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che leggono semplicemente da un handle di contesto, possono essere non serializzati.</span><span class="sxs-lookup"><span data-stu-id="1d571-130">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="1d571-131">Si noti che i metodi di creazione vengono serializzati in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="1d571-131">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="1d571-132">Esempi</span><span class="sxs-lookup"><span data-stu-id="1d571-132">Examples</span></span>

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="1d571-133">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1d571-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d571-134">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="1d571-134">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="1d571-135">Attributi ACF</span><span class="sxs-lookup"><span data-stu-id="1d571-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d571-136">**gestore del contesto \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="1d571-136">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="1d571-137">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="1d571-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="1d571-138">Handle di contesto</span><span class="sxs-lookup"><span data-stu-id="1d571-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="1d571-139">**RpcSsDontSerializeContext**</span><span class="sxs-lookup"><span data-stu-id="1d571-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="1d571-140">Routine di esecuzione del contesto del server</span><span class="sxs-lookup"><span data-stu-id="1d571-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="1d571-141">Client multithreading e handle di contesto</span><span class="sxs-lookup"><span data-stu-id="1d571-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="1d571-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="1d571-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 