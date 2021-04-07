---
title: attributo context_handle
description: L'attributo \ Context \_ handle \ identifica un handle di associazione che mantiene le informazioni sul contesto o sullo stato sul server tra le chiamate a procedure remote.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- attributo context_handle MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724959"
---
# <a name="context_handle-attribute"></a><span data-ttu-id="3a610-104">\_attributo handle di contesto</span><span class="sxs-lookup"><span data-stu-id="3a610-104">context\_handle attribute</span></span>

<span data-ttu-id="3a610-105">L'attributo dell' **\[ \_ handle \] di contesto** identifica un handle di associazione che mantiene le informazioni sul contesto o sullo stato sul server tra le chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="3a610-105">The **\[context\_handle\]** attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span>

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a><span data-ttu-id="3a610-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a610-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a610-107">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3a610-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3a610-108">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="3a610-108">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="3a610-109">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="3a610-109">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="3a610-110">Specifica un tipo di puntatore o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="3a610-110">Specifies a pointer type or a type identifier.</span></span> <span data-ttu-id="3a610-111">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="3a610-111">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="3a610-112">*dichiaratore e declarator-list*</span><span class="sxs-lookup"><span data-stu-id="3a610-112">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3a610-113">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="3a610-113">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="3a610-114">Il dichiaratore per un handle di contesto deve includere almeno un dichiaratore di puntatore.</span><span class="sxs-lookup"><span data-stu-id="3a610-114">The declarator for a context handle must include at least one pointer declarator.</span></span> <span data-ttu-id="3a610-115">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="3a610-115">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="3a610-116">Il *declarator-list* è costituito da uno o più dichiaratori, separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="3a610-116">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="3a610-117">L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3a610-117">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="3a610-118">*Function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="3a610-118">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3a610-119">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="3a610-119">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="3a610-120">Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[ Context \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="3a610-120">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="3a610-121">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="3a610-121">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="3a610-122">Specifica zero o più dichiaratori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="3a610-122">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="3a610-123">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' **\*** indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="3a610-123">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a610-124">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="3a610-124">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3a610-125">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="3a610-125">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="3a610-126">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3a610-126">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3a610-127">Specifica zero o più attributi direzionali, attributi di campo, attributi di utilizzo e attributi del puntatore appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="3a610-127">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="3a610-128">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="3a610-128">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="3a610-129">*context-handle-tipo*</span><span class="sxs-lookup"><span data-stu-id="3a610-129">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="3a610-130">Specifica l'identificatore che specifica il tipo di handle di contesto come definito in una Dichiarazione [**typedef**](typedef.md) che accetta l'attributo dell' **\[ \_ handle \] di contesto** .</span><span class="sxs-lookup"><span data-stu-id="3a610-130">Specifies the identifier that specifies the context handle type as defined in a [**typedef**](typedef.md) declaration that takes the **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="3a610-131">La routine di rundown è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="3a610-131">The rundown routine is optional.</span></span>

<span data-ttu-id="3a610-132">**Windows server 2003 e Windows XP:** Una singola interfaccia può supportare sia gli handle di contesto serializzati che quelli non serializzati, consentendo a un metodo su un'interfaccia di accedere a un handle di contesto esclusivamente (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzato).</span><span class="sxs-lookup"><span data-stu-id="3a610-132">**Windows ServerÂ 2003 and WindowsÂ XP:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="3a610-133">Queste funzionalità di accesso sono confrontabili con i meccanismi di blocco in lettura/scrittura; i metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori).</span><span class="sxs-lookup"><span data-stu-id="3a610-133">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="3a610-134">I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati.</span><span class="sxs-lookup"><span data-stu-id="3a610-134">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="3a610-135">I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che leggono semplicemente da un handle di contesto, possono essere non serializzati.</span><span class="sxs-lookup"><span data-stu-id="3a610-135">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="3a610-136">Si noti che i metodi di creazione vengono serializzati in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="3a610-136">Note that creation methods are implicitly serialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a610-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a610-137">Remarks</span></span>

<span data-ttu-id="3a610-138">L'attributo dell' **\[ \_ handle \] di contesto** può essere visualizzato come un attributo di tipo [**typedef**](typedef.md) IDL, come attributo di tipo restituito della funzione o come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="3a610-138">The **\[context\_handle\]** attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span> <span data-ttu-id="3a610-139">Quando si applica l'attributo dell' **\[ \_ handle \] di contesto** a una definizione di tipo, è necessario fornire anche una routine di rundown del contesto.</span><span class="sxs-lookup"><span data-stu-id="3a610-139">When you apply the **\[context\_handle\]** attribute to a type definition, you must also provide a context rundown routine.</span></span> <span data-ttu-id="3a610-140">Per informazioni dettagliate, vedere [routine di esecuzione del contesto server](/windows/desktop/Rpc/server-context-run-down-routine) .</span><span class="sxs-lookup"><span data-stu-id="3a610-140">See [Server Context Run-down Routine](/windows/desktop/Rpc/server-context-run-down-routine) for details.</span></span>

<span data-ttu-id="3a610-141">Quando si usa il compilatore MIDL in modalità predefinita ([**/MS \_ ext**](-ms-ext.md)), un handle di contesto può essere qualsiasi tipo di puntatore selezionato dall'utente, purché sia conforme ai requisiti per gli handle di contesto descritti qui.</span><span class="sxs-lookup"><span data-stu-id="3a610-141">When you use the MIDL compiler in default ([**/ms\_ext**](-ms-ext.md)) mode, a context handle can be any pointer type selected by the user, as long as it complies with the requirements for context handles described here.</span></span> <span data-ttu-id="3a610-142">I dati associati a tale tipo di handle del contesto non vengono trasmessi sulla rete e devono essere modificati solo dall'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="3a610-142">The data associated with such a context handle type is not transmitted on the network and should only be manipulated by the server application.</span></span> <span data-ttu-id="3a610-143">I compilatori IDL DCE limitano gli handle di contesto ai puntatori di tipo [**void**](void.md) **\*** .</span><span class="sxs-lookup"><span data-stu-id="3a610-143">DCE IDL compilers restrict context handles to pointers of type [**void**](void.md) **\***.</span></span> <span data-ttu-id="3a610-144">Questa funzionalità non è pertanto disponibile quando si usa l'opzione [**/OSF**](-osf.md) del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="3a610-144">Therefore this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="3a610-145">Come per gli altri tipi di handle, l'handle di contesto è opaco per l'applicazione client e qualsiasi dato associato non viene trasmesso.</span><span class="sxs-lookup"><span data-stu-id="3a610-145">As with other handle types, the context handle is opaque to the client application, and any data associated with it is not transmitted.</span></span> <span data-ttu-id="3a610-146">Sul server, l'handle di contesto funge da handle sul contesto attivo e tutti i dati associati al tipo di handle di contesto sono accessibili.</span><span class="sxs-lookup"><span data-stu-id="3a610-146">On the server, the context handle serves as a handle on active context, and all data associated with the context handle type is accessible.</span></span>

<span data-ttu-id="3a610-147">Per creare un handle di contesto, il client passa al server un **\[** [](out-idl.md) **\]** puntatore out, **\[** [**ref**](ref.md) **\]** a un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="3a610-147">To create a context handle, the client passes to the server an **\[**[**out**](out-idl.md)**\]**, **\[**[**ref**](ref.md)**\]** pointer to a context handle.</span></span> <span data-ttu-id="3a610-148">Il punto di controllo del contesto può avere un valore **null** o non **null** , purché il relativo valore sia coerente con i relativi attributi del puntatore.</span><span class="sxs-lookup"><span data-stu-id="3a610-148">(The context handle itself can have a **NULL** or non-**NULL** value—as long as its value is consistent with its pointer attributes.</span></span> <span data-ttu-id="3a610-149">Ad esempio, quando al tipo di handle del contesto è **\[** [](ref.md) **\]** applicato l'attributo ref, non può avere un valore **null** . È necessario fornire un altro handle di binding per completare l'associazione fino a quando non viene creato l'handle del contesto.</span><span class="sxs-lookup"><span data-stu-id="3a610-149">For example, when the context handle type has the **\[**[**ref**](ref.md)**\]** attribute applied to it, it cannot have a **NULL** value.) Another binding handle must be supplied to accomplish the binding until the context handle is created.</span></span> <span data-ttu-id="3a610-150">Quando non viene specificato alcun handle esplicito, viene usata l'associazione implicita.</span><span class="sxs-lookup"><span data-stu-id="3a610-150">When no explicit handle is specified, implicit binding is used.</span></span> <span data-ttu-id="3a610-151">Quando non **\[** è presente alcun attributo [**\_ handle implicito**](implicit-handle.md) **\]** , viene usato un handle automatico.</span><span class="sxs-lookup"><span data-stu-id="3a610-151">When no **\[**[**implicit\_handle**](implicit-handle.md)**\]** attribute is present, an auto handle is used.</span></span>

<span data-ttu-id="3a610-152">La procedura remota nel server crea un handle di contesto attivo.</span><span class="sxs-lookup"><span data-stu-id="3a610-152">The remote procedure on the server creates an active context handle.</span></span> <span data-ttu-id="3a610-153">Il client deve usare tale handle di contesto come **\[** [**un**](in.md) **\]** parametro **\[** **out \]** in o in chiamate successive.</span><span class="sxs-lookup"><span data-stu-id="3a610-153">The client must use that context handle as an **\[**[**in**](in.md)**\]** or **\[in**, **out\]** parameter in subsequent calls.</span></span> <span data-ttu-id="3a610-154">Un handle **\[ \] di** contesto unico può essere usato come handle di associazione, quindi deve avere un valore non **null** .</span><span class="sxs-lookup"><span data-stu-id="3a610-154">An **\[in\]**-only context handle can be used as a binding handle, so it must have a non-**NULL** value.</span></span> <span data-ttu-id="3a610-155">Un handle **\[ di contesto in \]** sola non riflette le modifiche di stato nel server.</span><span class="sxs-lookup"><span data-stu-id="3a610-155">An **\[in\]**-only context handle does not reflect state changes on the server.</span></span>

<span data-ttu-id="3a610-156">Nel server, la procedura chiamata può interpretare l'handle del contesto in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="3a610-156">On the server, the called procedure can interpret the context handle as needed.</span></span> <span data-ttu-id="3a610-157">La stored procedure chiamata, ad esempio, può allocare l'archiviazione heap e utilizzare l'handle di contesto come puntatore a questa risorsa di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3a610-157">For example, the called procedure can allocate heap storage and use the context handle as a pointer to this storage.</span></span>

<span data-ttu-id="3a610-158">Per chiudere un handle di contesto, il client passa l'handle del contesto come un **\[** argomento [**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="3a610-158">To close a context handle, the client passes the context handle as an **\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]** argument.</span></span> <span data-ttu-id="3a610-159">Il server deve restituire un handle di contesto **null** quando non è più in grado di mantenere il contesto per conto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="3a610-159">The server must return a **NULL** context handle when it is no longer maintaining context on behalf of the caller.</span></span> <span data-ttu-id="3a610-160">Se, ad esempio, l'handle di contesto rappresenta un file aperto e la chiamata chiude il file, il server deve impostare l'handle di contesto su **null** e restituirlo al client.</span><span class="sxs-lookup"><span data-stu-id="3a610-160">For example, if the context handle represents an open file and the call closes the file, the server must set the context handle to **NULL** and return it to the client.</span></span> <span data-ttu-id="3a610-161">Un valore **null** non è valido come handle di associazione nelle chiamate successive.</span><span class="sxs-lookup"><span data-stu-id="3a610-161">A **NULL** value is invalid as a binding handle on subsequent calls.</span></span>

<span data-ttu-id="3a610-162">Un handle di contesto è valido solo per un server.</span><span class="sxs-lookup"><span data-stu-id="3a610-162">A context handle is only valid for one server.</span></span> <span data-ttu-id="3a610-163">Quando una funzione dispone di due parametri di handle e l'handle del contesto non è **null**, gli handle di associazione devono fare riferimento allo stesso spazio di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="3a610-163">When a function has two handle parameters and the context handle is not **NULL**, the binding handles must refer to the same address space.</span></span>

<span data-ttu-id="3a610-164">Quando una funzione dispone di un oggetto **\[** [**in**](in.md) **\]** o un oggetto **\[ in**, **\]** il relativo handle di contesto può essere utilizzato come handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="3a610-164">When a function has an **\[**[**in**](in.md)**\]** or an **\[in**, **out\]** context handle, its context handle can be used as the binding handle.</span></span> <span data-ttu-id="3a610-165">In questo caso, l'associazione implicita non viene utilizzata e l' **\[** [**\_ handle implicito**](implicit-handle.md) **\]** o l' **\[** attributo [**\_ handle automatico**](auto-handle.md) **\]** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3a610-165">In this case, implicit binding is not used and the **\[**[**implicit\_handle**](implicit-handle.md)**\]** or **\[**[**auto\_handle**](auto-handle.md)**\]** attribute is ignored.</span></span>

<span data-ttu-id="3a610-166">Per gli handle di contesto si applicano le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a610-166">The following restrictions apply to context handles:</span></span>

-   <span data-ttu-id="3a610-167">Gli handle del contesto non possono essere elementi della matrice, membri della struttura o membri di Unione.</span><span class="sxs-lookup"><span data-stu-id="3a610-167">Context handles cannot be array elements, structure members, or union members.</span></span> <span data-ttu-id="3a610-168">Possono essere solo parametri.</span><span class="sxs-lookup"><span data-stu-id="3a610-168">They can only be parameters.</span></span>
-   <span data-ttu-id="3a610-169">Gli handle del contesto non possono avere la **\[** [**trasmissione \_ As**](transmit-as.md) **\]** o **\[** [**rappresentare \_ come**](represent-as.md) **\]** attributo.</span><span class="sxs-lookup"><span data-stu-id="3a610-169">Context handles cannot have the **\[**[**transmit\_as**](transmit-as.md)**\]** or **\[**[**represent\_as**](represent-as.md)**\]** attribute.</span></span>
-   <span data-ttu-id="3a610-170">I parametri che sono puntatori a **\[** [](out-idl.md) **\]** handle di contesto out devono essere **\[** [](ref.md) **\]** puntatori Ref.</span><span class="sxs-lookup"><span data-stu-id="3a610-170">Parameters that are pointers to **\[**[**out**](out-idl.md)**\]** context handles must be **\[**[**ref**](ref.md)**\]** pointers.</span></span>
-   <span data-ttu-id="3a610-171">Un **\[** [](in.md) **\]** handle nel contesto può essere utilizzato come handle di associazione e non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3a610-171">An **\[**[**in**](in.md)**\]** context handle can be used as the binding handle and cannot be **NULL**.</span></span>
-   <span data-ttu-id="3a610-172">Un handle di contesto [**out**](out-idl.md) può essere **null** nell'input, ma solo se la stored procedure ha un altro parametro **\[ di** handle esplicito.</span><span class="sxs-lookup"><span data-stu-id="3a610-172">An **\[in**, [**out**](out-idl.md) context handle can be **NULL** on input, but only if the procedure has another explicit handle parameter.</span></span> <span data-ttu-id="3a610-173">Se non sono presenti altri parametri **\[ di handle di** contesto non **null** espliciti, l'handle di contesto in, **out \]** non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3a610-173">If there are no other explicit non-**NULL** context handle parameters, the **\[in**, **out\]** context handle cannot be **NULL**.</span></span>
-   <span data-ttu-id="3a610-174">Non è possibile usare un handle di contesto con i callback.</span><span class="sxs-lookup"><span data-stu-id="3a610-174">A context handle cannot be used with callbacks.</span></span>

## <a name="examples"></a><span data-ttu-id="3a610-175">Esempi</span><span class="sxs-lookup"><span data-stu-id="3a610-175">Examples</span></span>

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a><span data-ttu-id="3a610-176">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3a610-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a610-177">**matrici**</span><span class="sxs-lookup"><span data-stu-id="3a610-177">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="3a610-178">**\_handle automatico**</span><span class="sxs-lookup"><span data-stu-id="3a610-178">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="3a610-179">**callback**</span><span class="sxs-lookup"><span data-stu-id="3a610-179">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="3a610-180">Ripristino del contesto client</span><span class="sxs-lookup"><span data-stu-id="3a610-180">Client Context Reset</span></span>](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[<span data-ttu-id="3a610-181">**const**</span><span class="sxs-lookup"><span data-stu-id="3a610-181">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="3a610-182">Handle di contesto</span><span class="sxs-lookup"><span data-stu-id="3a610-182">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="3a610-183">**gestire**</span><span class="sxs-lookup"><span data-stu-id="3a610-183">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="3a610-184">Binding e handle</span><span class="sxs-lookup"><span data-stu-id="3a610-184">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="3a610-185">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="3a610-185">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="3a610-186">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="3a610-186">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="3a610-187">**in**</span><span class="sxs-lookup"><span data-stu-id="3a610-187">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="3a610-188">**locale**</span><span class="sxs-lookup"><span data-stu-id="3a610-188">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="3a610-189">Client multithreading e handle di contesto</span><span class="sxs-lookup"><span data-stu-id="3a610-189">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="3a610-190">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="3a610-190">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="3a610-191">**out**</span><span class="sxs-lookup"><span data-stu-id="3a610-191">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="3a610-192">**ptr**</span><span class="sxs-lookup"><span data-stu-id="3a610-192">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="3a610-193">**ref**</span><span class="sxs-lookup"><span data-stu-id="3a610-193">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="3a610-194">**rappresenta \_ come**</span><span class="sxs-lookup"><span data-stu-id="3a610-194">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="3a610-195">**RpcSsDestroyClientContext**</span><span class="sxs-lookup"><span data-stu-id="3a610-195">**RpcSsDestroyClientContext**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[<span data-ttu-id="3a610-196">Routine di esecuzione del contesto del server</span><span class="sxs-lookup"><span data-stu-id="3a610-196">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="3a610-197">**string**</span><span class="sxs-lookup"><span data-stu-id="3a610-197">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="3a610-198">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="3a610-198">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="3a610-199">**typedef**</span><span class="sxs-lookup"><span data-stu-id="3a610-199">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="3a610-200">**unico**</span><span class="sxs-lookup"><span data-stu-id="3a610-200">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="3a610-201">**void**</span><span class="sxs-lookup"><span data-stu-id="3a610-201">**void**</span></span>](void.md)
</dt> </dl>

 

 