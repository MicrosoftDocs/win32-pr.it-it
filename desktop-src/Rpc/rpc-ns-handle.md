---
title: RPC_NS_HANDLE (rpcnsi. h)
description: Il tipo di dati \_ handle NS RPC \_ definisce un handle del servizio nome.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518718"
---
# <a name="rpc_ns_handle"></a><span data-ttu-id="6b79c-104">\_handle NS \_ RPC</span><span class="sxs-lookup"><span data-stu-id="6b79c-104">RPC\_NS\_HANDLE</span></span>

<span data-ttu-id="6b79c-105">Il tipo di **dati \_ \_ handle NS RPC** definisce un handle del servizio nome.</span><span class="sxs-lookup"><span data-stu-id="6b79c-105">The data type **RPC\_NS\_HANDLE** defines a name-service handle.</span></span>


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="6b79c-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b79c-106">Remarks</span></span>

<span data-ttu-id="6b79c-107">Un handle del servizio nome è una variabile opaca che contiene informazioni utilizzate dalla libreria di runtime RPC per restituire i dati RPC seguenti dal nome del database del servizio:</span><span class="sxs-lookup"><span data-stu-id="6b79c-107">A name-service handle is an opaque variable containing information the RPC run-time library uses to return the following RPC data from the name-service database:</span></span>

-   <span data-ttu-id="6b79c-108">Handle di associazione server</span><span class="sxs-lookup"><span data-stu-id="6b79c-108">Server-binding handles</span></span>
-   <span data-ttu-id="6b79c-109">UUID delle risorse offerte dai membri del profilo del server</span><span class="sxs-lookup"><span data-stu-id="6b79c-109">UUIDs of resources offered by server profile members</span></span>
-   <span data-ttu-id="6b79c-110">Membri gruppo</span><span class="sxs-lookup"><span data-stu-id="6b79c-110">Group members</span></span>

<span data-ttu-id="6b79c-111">L'ambito di un handle del servizio Name è da una routine "Begin" tramite la routine "Done" corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6b79c-111">The scope of a name-service handle is from a "Begin" routine through the corresponding "Done" routine.</span></span>

<span data-ttu-id="6b79c-112">Le applicazioni sono responsabili del controllo della concorrenza degli handle del servizio nome nei thread.</span><span class="sxs-lookup"><span data-stu-id="6b79c-112">Applications are responsible for concurrency control of name-service handles across threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b79c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b79c-113">Requirements</span></span>



| <span data-ttu-id="6b79c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b79c-114">Requirement</span></span> | <span data-ttu-id="6b79c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6b79c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b79c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b79c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b79c-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b79c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6b79c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b79c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b79c-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b79c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6b79c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b79c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b79c-121"><dt>Rpcnsi. h (include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b79c-121"><dt>Rpcnsi.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b79c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b79c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b79c-123">**RpcNsBindingImportBegin**</span><span class="sxs-lookup"><span data-stu-id="6b79c-123">**RpcNsBindingImportBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[<span data-ttu-id="6b79c-124">**RpcNsBindingImportDone**</span><span class="sxs-lookup"><span data-stu-id="6b79c-124">**RpcNsBindingImportDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[<span data-ttu-id="6b79c-125">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="6b79c-125">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[<span data-ttu-id="6b79c-126">**RpcNsBindingLookupBegin**</span><span class="sxs-lookup"><span data-stu-id="6b79c-126">**RpcNsBindingLookupBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[<span data-ttu-id="6b79c-127">**RpcNsBindingLookupDone**</span><span class="sxs-lookup"><span data-stu-id="6b79c-127">**RpcNsBindingLookupDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[<span data-ttu-id="6b79c-128">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="6b79c-128">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





