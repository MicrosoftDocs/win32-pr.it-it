---
title: Message (attributo)
description: L'attributo \ Message \ indica che la chiamata di procedura remota deve essere considerata come un messaggio dal client al server.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- MIDL attributo messaggio
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472939"
---
# <a name="message-attribute"></a><span data-ttu-id="35ab0-104">Message (attributo)</span><span class="sxs-lookup"><span data-stu-id="35ab0-104">message attribute</span></span>

<span data-ttu-id="35ab0-105">L'attributo **\[ message \]** indica che la chiamata di procedura remota deve essere considerata come un messaggio dal client al server.</span><span class="sxs-lookup"><span data-stu-id="35ab0-105">The **\[message\]** attribute indicates that the remote procedure call is to be treated as a message from the client to the server.</span></span>

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="35ab0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35ab0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ab0-107">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="35ab0-107">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="35ab0-108">Altri attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="35ab0-108">Other attributes that apply to the function.</span></span> <span data-ttu-id="35ab0-109">**\[** [](local.md) **\]** **\[** [](nocode.md) **\]** **\[** [](code.md)**\]** **\[** [](optimize.md) **\]** Con l'attributo **\[ message \]** è possibile utilizzare solo gli attributi local, NoCode, code e optimize.</span><span class="sxs-lookup"><span data-stu-id="35ab0-109">Only the **\[**[**local**](local.md)**\]**, **\[**[**nocode**](nocode.md)**\]**, **\[**[**code**](code.md)**\],** and **\[**[**optimize**](optimize.md)**\]** attributes may be used with the **\[message\]** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="35ab0-110">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="35ab0-110">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="35ab0-111">Nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="35ab0-111">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="35ab0-112">*facoltativo-parameter-attributes*</span><span class="sxs-lookup"><span data-stu-id="35ab0-112">*optional-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="35ab0-113">Zero o più attributi MIDL che verranno applicati al parametro.</span><span class="sxs-lookup"><span data-stu-id="35ab0-113">Zero or more MIDL attributes that will be applied to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="35ab0-114">*nome param*</span><span class="sxs-lookup"><span data-stu-id="35ab0-114">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="35ab0-115">Nome del parametro come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="35ab0-115">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35ab0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="35ab0-116">Remarks</span></span>

<span data-ttu-id="35ab0-117">Come messaggi dal client, le chiamate a procedure remote con l'attributo **\[ message \]** vengono recapitate al server in modo asincrono tramite il trasporto di Accodamento messaggi di [**ncadg \_ mq**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="35ab0-117">As messages from the client, remote procedure calls with the **\[message\]** attribute are delivered to the server asynchronously over the [**ncadg\_mq**](ncadg-mq.md) message-queuing transport.</span></span> <span data-ttu-id="35ab0-118">È possibile indicare la messaggistica in modalità sincrona specificando il protocollo di trasporto **ncadg \_ mq** senza usare l'attributo **\[ \] Message** .</span><span class="sxs-lookup"><span data-stu-id="35ab0-118">You can indicate synchronous-mode messaging by specifying the **ncadg\_mq** transport protocol without using the **\[message\]** attribute.</span></span>

<span data-ttu-id="35ab0-119">Specificando la messaggistica in modalità asincrona, l'attributo **\[ message \]** consente al client di eseguire la chiamata di procedura remota e restituire immediatamente un risultato, anche quando l'applicazione server non risponde.</span><span class="sxs-lookup"><span data-stu-id="35ab0-119">By specifying asynchronous-mode messaging, the **\[message\]** attribute allows the client to make the remote procedure call and return immediately, even when the server application is not responding.</span></span> <span data-ttu-id="35ab0-120">Se il server di destinazione non è disponibile, la chiamata verrà archiviata fino a quando il server non sarà disponibile.</span><span class="sxs-lookup"><span data-stu-id="35ab0-120">If the target server is not available, the call will be stored until the server becomes available.</span></span>

<span data-ttu-id="35ab0-121">La messaggistica in modalità asincrona consente inoltre di controllare le proprietà della coda di messaggi della coda di ricezione per il server.</span><span class="sxs-lookup"><span data-stu-id="35ab0-121">In addition, asynchronous-mode messaging lets you control message-queue properties of the receive queue for the server.</span></span> <span data-ttu-id="35ab0-122">Per ulteriori informazioni su come selezionare la qualità del servizio, la priorità delle chiamate e la durata delle chiamate per il processo server, vedere [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) .</span><span class="sxs-lookup"><span data-stu-id="35ab0-122">See [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) for more information on selecting quality of service, call priority, and call lifetime for the server process.</span></span>

<span data-ttu-id="35ab0-123">All'attributo del **\[ messaggio \]** si applicano anche le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="35ab0-123">The following restrictions also apply to the **\[message\]** attribute:</span></span>

-   <span data-ttu-id="35ab0-124">Microsoft Message Queuing deve essere implementato nei sistemi client e server e i sistemi devono essere visibili tra loro in base a quanto determinato dall'ambito dell'installazione della coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="35ab0-124">Microsoft Message Queuing must be implemented in the client and server systems and the systems must be visible to each other as determined by the scope of the message queue installation.</span></span>
-   <span data-ttu-id="35ab0-125">L'associazione deve usare endpoint noti e il protocollo di trasporto [**ncadg \_ mq**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="35ab0-125">The binding must use well-known endpoints and the [**ncadg\_mq**](ncadg-mq.md) transport protocol.</span></span>
-   <span data-ttu-id="35ab0-126">La funzione non può contenere parametri di output o un tipo restituito diverso da [**void**](void.md).</span><span class="sxs-lookup"><span data-stu-id="35ab0-126">The function cannot contain output parameters or a return type other than [**void**](void.md).</span></span> <span data-ttu-id="35ab0-127">Si noti che la seconda restrizione rende attualmente l'attributo del **\[ messaggio \]** non adatto per i metodi di interfaccia com (Object).</span><span class="sxs-lookup"><span data-stu-id="35ab0-127">Note that the latter restriction makes the **\[message\]** attribute unsuitable for COM (object) interface methods, at this time.</span></span> <span data-ttu-id="35ab0-128">La versione successiva di MIDL consentirà alle funzioni di **\[ \] messaggio** di restituire \_ lo stato di errore \_ t o HRESULT.</span><span class="sxs-lookup"><span data-stu-id="35ab0-128">The next release of MIDL will permit **\[message\]** functions to return error\_status\_t or HRESULT.</span></span>
-   <span data-ttu-id="35ab0-129">Qualsiasi interfaccia che contiene almeno una chiamata al **\[ \] messaggio** deve essere registrata chiamando [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) o [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) prima di chiamare [**RpcServerUseProtseqEpEx (ncadg \_ mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span><span class="sxs-lookup"><span data-stu-id="35ab0-129">Any interface that contains at least one **\[message\]** call must be registered by calling [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) or [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) before calling [**RpcServerUseProtseqEpEx(ncadg\_mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span></span> <span data-ttu-id="35ab0-130">In caso contrario, le chiamate in attesa nella coda per il server verranno lette prima che l'interfaccia venga registrata e le chiamate avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="35ab0-130">Otherwise, calls that were waiting on the queue for the server will be read before the interface is registered, and the calls will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="35ab0-131">Esempi</span><span class="sxs-lookup"><span data-stu-id="35ab0-131">Examples</span></span>

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a><span data-ttu-id="35ab0-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="35ab0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ab0-133">**codice**</span><span class="sxs-lookup"><span data-stu-id="35ab0-133">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="35ab0-134">**locale**</span><span class="sxs-lookup"><span data-stu-id="35ab0-134">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="35ab0-135">**ncadg \_ mq**</span><span class="sxs-lookup"><span data-stu-id="35ab0-135">**ncadg\_mq**</span></span>](ncadg-mq.md)
</dt> <dt>

[<span data-ttu-id="35ab0-136">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="35ab0-136">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="35ab0-137">**ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="35ab0-137">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="35ab0-138">Accodamento messaggi RPC</span><span class="sxs-lookup"><span data-stu-id="35ab0-138">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="35ab0-139">**RpcBindingSetOption**</span><span class="sxs-lookup"><span data-stu-id="35ab0-139">**RpcBindingSetOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[<span data-ttu-id="35ab0-140">**RpcBindingInqOption**</span><span class="sxs-lookup"><span data-stu-id="35ab0-140">**RpcBindingInqOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[<span data-ttu-id="35ab0-141">**void**</span><span class="sxs-lookup"><span data-stu-id="35ab0-141">**void**</span></span>](void.md)
</dt> </dl>

 

 