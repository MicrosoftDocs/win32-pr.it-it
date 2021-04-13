---
title: callback (attributo)
description: L'attributo \ callback \ dichiara una funzione di callback statica esistente sul lato client dell'applicazione distribuita. Le funzioni di callback consentono al server di eseguire il codice sul client.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- attributo di callback MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398961"
---
# <a name="callback-attribute"></a><span data-ttu-id="e4d8a-105">callback (attributo)</span><span class="sxs-lookup"><span data-stu-id="e4d8a-105">callback attribute</span></span>

<span data-ttu-id="e4d8a-106">L'attributo **\[ callback \]** dichiara una funzione di callback statica esistente sul lato client dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-106">The **\[callback\]** attribute declares a static callback function that exists on the client side of the distributed application.</span></span> <span data-ttu-id="e4d8a-107">Le funzioni di callback consentono al server di eseguire il codice sul client.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-107">Callback functions provide a way for the server to execute code on the client.</span></span>

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="e4d8a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4d8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d8a-109">*Function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="e4d8a-109">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d8a-110">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="e4d8a-111">Gli attributi di funzione validi sono **\[** [**local**](local.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e4d8a-111">Valid function attributes are **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span> <span data-ttu-id="e4d8a-112">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e4d8a-113">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="e4d8a-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d8a-114">Specifica un [ \_ tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-114">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="e4d8a-115">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e4d8a-116">*PTR-dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="e4d8a-116">*ptr-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d8a-117">Specifica zero o più dichiaratori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-117">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="e4d8a-118">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="e4d8a-118">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4d8a-119">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="e4d8a-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d8a-120">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-120">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e4d8a-121">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="e4d8a-121">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d8a-122">Specifica zero o più attributi direzionali, attributi di campo, attributi di utilizzo e attributi del puntatore appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-122">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="e4d8a-123">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-123">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e4d8a-124">*dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="e4d8a-124">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d8a-125">Specifica un dichiaratore C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-125">Specifies a standard C declarator such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e4d8a-126">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e4d8a-126">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e4d8a-127">L'identificatore del nome del parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-127">The parameter-name identifier is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4d8a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4d8a-128">Remarks</span></span>

<span data-ttu-id="e4d8a-129">La funzione di **\[ callback \]** è utile quando il server deve ottenere informazioni dal client.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-129">The **\[callback\]** function is useful when the server must obtain information from the client.</span></span> <span data-ttu-id="e4d8a-130">Se le applicazioni server sono supportate in Windows 3. *x*, il server può effettuare una chiamata a una procedura remota in Windows 3. Server *x* per ottenere le informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-130">If server applications were supported on Windows 3.*x*, the server could make a call to a remote procedure on the Windows 3.*x* server to obtain the needed information.</span></span> <span data-ttu-id="e4d8a-131">La funzione di callback ha lo stesso scopo e consente al server di eseguire una query sul client per ottenere informazioni nel contesto della chiamata originale.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-131">The callback function accomplishes the same purpose and lets the server query the client for information in the context of the original call.</span></span>

<span data-ttu-id="e4d8a-132">I callback sono casi speciali di chiamate remote eseguite come parte di un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-132">Callbacks are special cases of remote calls that execute as part of a single thread.</span></span> <span data-ttu-id="e4d8a-133">Viene emesso un callback nel contesto di una chiamata remota.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-133">A callback is issued in the context of a remote call.</span></span> <span data-ttu-id="e4d8a-134">Qualsiasi procedura remota definita come parte della stessa interfaccia della funzione di callback statica può chiamare la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-134">Any remote procedure defined as part of the same interface as the static callback function can call the callback function.</span></span>

<span data-ttu-id="e4d8a-135">È importante notare che l'uso del \[ callback \] non è consigliato nella programmazione multithread.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-135">It is important to note that the use of \[callback\] is not recommended in multi-thread programming.</span></span> <span data-ttu-id="e4d8a-136">Come funzione di programmazione a thread singolo, non è disponibile per supportare le richieste di sicurezza offerte da un ambiente multithread.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-136">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

<span data-ttu-id="e4d8a-137">Impossibile utilizzare la funzione **RpcCancelThread** per annullare una chiamata che può inviare un callback statico.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-137">The **RpcCancelThread** function cannot be used to cancel a call that may dispatch a static callback.</span></span> <span data-ttu-id="e4d8a-138">Se una particolare chiamata a una procedura remota non comporterà mai un callback, può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-138">If a particular remote procedure call will never result in a callback, then it can be canceled.</span></span> <span data-ttu-id="e4d8a-139">In caso contrario, una chiamata può essere annullata solo se è possibile garantire che non sia stato emesso un callback per esso.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-139">Otherwise, a call can be canceled only if it can be guaranteed that a callback for it has not been issued.</span></span>

<span data-ttu-id="e4d8a-140">Solo le sequenze orientate alla connessione e del protocollo locale supportano l'attributo callback.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-140">Only the connection-oriented and local-protocol sequences support the callback attribute.</span></span> <span data-ttu-id="e4d8a-141">La dimensione dei \[ dati out \] per i callback sulla sequenza del protocollo locale è limitata a 150 byte.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-141">The size of the \[out\] data for callbacks over the local-protocol sequence is limited to 150 bytes.</span></span> <span data-ttu-id="e4d8a-142">Se un'interfaccia RPC usa una sequenza di protocollo senza connessione (datagramma), le chiamate a procedure con l'attributo di callback avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-142">If an RPC interface uses a connectionless (datagram) protocol sequence, calls to procedures with the callback attribute will fail.</span></span>

<span data-ttu-id="e4d8a-143">Non è possibile utilizzare gli handle come parametri nelle funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-143">Handles cannot be used as parameters in callback functions.</span></span> <span data-ttu-id="e4d8a-144">Poiché i callback vengono sempre eseguiti nel contesto di una chiamata, l'handle di associazione utilizzato dal client per effettuare la chiamata al server viene utilizzato anche come handle di binding dal server al client.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-144">Because callbacks always execute in the context of a call, the binding handle used by the client to make the call to the server is also used as the binding handle from the server to the client.</span></span>

<span data-ttu-id="e4d8a-145">I callback possono annidarsi in qualsiasi profondità.</span><span class="sxs-lookup"><span data-stu-id="e4d8a-145">Callbacks can nest to any depth.</span></span>

## <a name="examples"></a><span data-ttu-id="e4d8a-146">Esempi</span><span class="sxs-lookup"><span data-stu-id="e4d8a-146">Examples</span></span>

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a><span data-ttu-id="e4d8a-147">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e4d8a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d8a-148">**matrici**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-148">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-149">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="e4d8a-149">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-150">**const**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-150">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-151">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-151">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-152">**enum**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-152">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-153">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="e4d8a-153">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-154">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-154">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-155">**locale**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-155">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-156">**/osf**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-156">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-157">**ref**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-157">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-158">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-158">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-159">**string**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-159">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-160">**struct**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-160">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-161">**Unione**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-161">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-162">**unico**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-162">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="e4d8a-163">**RpcCancelThread**</span><span class="sxs-lookup"><span data-stu-id="e4d8a-163">**RpcCancelThread**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 