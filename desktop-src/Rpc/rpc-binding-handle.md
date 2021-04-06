---
title: RPC_BINDING_HANDLE (rpcdce. h)
description: Il \_ tipo di dati dell'handle di binding RPC dichiara un handle di associazione contenente le informazioni utilizzate dalla libreria di runtime RPC per accedere alle informazioni di binding.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743791"
---
# <a name="rpc_binding_handle"></a><span data-ttu-id="01087-104">\_handle di binding RPC \_</span><span class="sxs-lookup"><span data-stu-id="01087-104">RPC\_BINDING\_HANDLE</span></span>

<span data-ttu-id="01087-105">Il tipo di dati dell' **\_ handle di binding RPC** dichiara un handle di associazione contenente le informazioni utilizzate dalla libreria di runtime RPC per accedere alle informazioni di binding.</span><span class="sxs-lookup"><span data-stu-id="01087-105">The **RPC\_BINDING HANDLE** data type declares a binding handle containing information that the RPC run-time library uses to access binding information.</span></span>


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="01087-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="01087-106">Remarks</span></span>

<span data-ttu-id="01087-107">La libreria di runtime utilizza le informazioni di binding per stabilire una relazione client-server che consente l'esecuzione di chiamate di procedure remote.</span><span class="sxs-lookup"><span data-stu-id="01087-107">The run-time library uses binding information to establish a client-server relationship that allows the execution of remote procedure calls.</span></span> <span data-ttu-id="01087-108">In base al contesto in cui viene creato un handle di associazione, viene considerato un handle di associazione server o un handle di associazione client.</span><span class="sxs-lookup"><span data-stu-id="01087-108">Based on the context in which a binding handle is created, it is considered a server-binding handle or a client-binding handle.</span></span>

<span data-ttu-id="01087-109">Un handle di associazione server contiene le informazioni necessarie a un client per stabilire una relazione con un server specifico.</span><span class="sxs-lookup"><span data-stu-id="01087-109">A server-binding handle contains the information necessary for a client to establish a relationship with a specific server.</span></span> <span data-ttu-id="01087-110">Un numero qualsiasi di routine di Runtime API RPC restituisce un handle di associazione server che può essere utilizzato per eseguire una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="01087-110">Any number of RPC API run-time routines return a server-binding handle that can be used for making a remote procedure call.</span></span>

<span data-ttu-id="01087-111">Non è possibile usare un handle di associazione client per eseguire una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="01087-111">A client-binding handle cannot be used to make a remote procedure call.</span></span> <span data-ttu-id="01087-112">La libreria di runtime RPC crea e fornisce un handle di associazione client a una procedura denominata-Server (detta anche routine Server-Manager) come parametro dell'handle di \_ binding RPC \_ .</span><span class="sxs-lookup"><span data-stu-id="01087-112">The RPC run-time library creates and provides a client-binding handle to a called-server procedure (also called a server-manager routine) as the RPC\_BINDING\_HANDLE parameter.</span></span> <span data-ttu-id="01087-113">L'handle di associazione client contiene informazioni sul client chiamante.</span><span class="sxs-lookup"><span data-stu-id="01087-113">The client-binding handle contains information about the calling client.</span></span>

<span data-ttu-id="01087-114">Le funzioni \*\* \* RpcBinding\* _ _*e \* RpcNsBinding*_ RESTITUIscono il \_ tipo di associazione RPC del codice di stato \_ errato \_ \_ \_ quando un'applicazione fornisce il tipo di handle di binding errato.</span><span class="sxs-lookup"><span data-stu-id="01087-114">The **RpcBinding\** _ and _*RpcNsBinding\*\*_ functions return the status code RPC\_S\_WRONG\_KIND\_OF\_BINDING when an application provides the incorrect binding-handle type.</span></span>

<span data-ttu-id="01087-115">Un'applicazione può condividere un singolo handle di binding tra più thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="01087-115">An application can share a single binding handle across multiple threads of execution.</span></span> <span data-ttu-id="01087-116">La libreria di runtime RPC gestisce le chiamate a procedure remote simultanee che utilizzano un singolo handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="01087-116">The RPC run-time library manages concurrent remote procedure calls that use a single binding handle.</span></span> <span data-ttu-id="01087-117">Tuttavia, l'applicazione è responsabile del controllo della concorrenza dell'handle di associazione per le operazioni che modificano un handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="01087-117">However, the application is responsible for binding handle concurrency control for operations that modify a binding handle.</span></span> <span data-ttu-id="01087-118">Queste operazioni includono le routine seguenti:</span><span class="sxs-lookup"><span data-stu-id="01087-118">These operations include the following routines:</span></span>

-   [<span data-ttu-id="01087-119">_ *RpcBindingFree*\*</span><span class="sxs-lookup"><span data-stu-id="01087-119">_ *RpcBindingFree*\*</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [<span data-ttu-id="01087-120">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="01087-120">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [<span data-ttu-id="01087-121">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="01087-121">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [<span data-ttu-id="01087-122">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="01087-122">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

<span data-ttu-id="01087-123">Se, ad esempio, un'applicazione condivide un handle di associazione tra due thread di esecuzione e Reimposta l'endpoint dell'associazione-handle in uno dei thread chiamando [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="01087-123">For example, if an application shares a binding handle across two threads of execution and resets the binding-handle endpoint in one of the threads by calling [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), the results are undefined.</span></span> <span data-ttu-id="01087-124">È possibile che venga reimpostato anche l'handle dell'associazione sull'altro thread oppure l'operazione potrebbe non riuscire oppure il processo potrebbe arrestarsi in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="01087-124">The binding handle on the other thread may also be reset, or the operation may fail, or the process may crash.</span></span> <span data-ttu-id="01087-125">Un errore comune è quello di liberare un handle di associazione mentre è in corso una chiamata al suo interno. Questo problema in genere blocca il processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="01087-125">A common error is freeing a binding handle while a call on it is in progress; this usually crashes the calling process.</span></span>

<span data-ttu-id="01087-126">Se non si desidera la concorrenza, è possibile progettare un'applicazione per creare una copia di un handle di associazione chiamando [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span><span class="sxs-lookup"><span data-stu-id="01087-126">If you do not want concurrency, you can design an application to create a copy of a binding handle by calling [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span></span> <span data-ttu-id="01087-127">In questo caso, un'operazione al primo handle di associazione non ha alcun effetto sul secondo handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="01087-127">In this case, an operation to the first binding handle has no effect on the second binding handle.</span></span>

<span data-ttu-id="01087-128">Le routine che richiedono un handle di associazione come parametro mostrano un tipo di dati **dell' \_ \_ handle di binding RPC**.</span><span class="sxs-lookup"><span data-stu-id="01087-128">Routines requiring a binding handle as a parameter show a data type of **RPC\_BINDING\_HANDLE**.</span></span> <span data-ttu-id="01087-129">I parametri dell'handle di binding vengono passati per valore.</span><span class="sxs-lookup"><span data-stu-id="01087-129">Binding-handle parameters are passed by value.</span></span>

## <a name="requirements"></a><span data-ttu-id="01087-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01087-130">Requirements</span></span>



| <span data-ttu-id="01087-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="01087-131">Requirement</span></span> | <span data-ttu-id="01087-132">Valore</span><span class="sxs-lookup"><span data-stu-id="01087-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01087-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01087-133">Minimum supported client</span></span><br/> | <span data-ttu-id="01087-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01087-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="01087-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01087-135">Minimum supported server</span></span><br/> | <span data-ttu-id="01087-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01087-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="01087-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01087-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="01087-138"><dt>Rpcdce. h (include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01087-138"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





