---
title: Costanti di timeout di binding (rpcdce. h)
description: La libreria RPC utilizza le costanti di timeout dell'associazione per specificare la quantità relativa di tempo che deve trascorrere per stabilire un'associazione al server prima di rinunciare.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301351"
---
# <a name="binding-time-out-constants"></a><span data-ttu-id="04773-103">Costanti di timeout di binding</span><span class="sxs-lookup"><span data-stu-id="04773-103">Binding Time-out Constants</span></span>

<span data-ttu-id="04773-104">La libreria RPC utilizza le costanti di timeout dell'associazione per specificare la quantità relativa di tempo che deve trascorrere per stabilire un'associazione al server prima di rinunciare.</span><span class="sxs-lookup"><span data-stu-id="04773-104">The RPC library uses the binding time-out constants to specify the relative amount of time that should be spent to establish a binding to the server before giving up.</span></span> <span data-ttu-id="04773-105">Il timeout può essere abilitato con una chiamata alla funzione [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) .</span><span class="sxs-lookup"><span data-stu-id="04773-105">The timeout can be enabled with a call to the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function.</span></span> <span data-ttu-id="04773-106">L'elenco seguente contiene i valori di timeout validi.</span><span class="sxs-lookup"><span data-stu-id="04773-106">The following list contains the valid time-out values.</span></span>



| <span data-ttu-id="04773-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="04773-107">Constant/value</span></span>                                                                                                                                                                                                                                                                | <span data-ttu-id="04773-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04773-108">Description</span></span>                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <span data-ttu-id="04773-109"><dt>**RPC \_ \_ \_ \_ Timeout di binding C infinito**</dt> <dt> 10</dt></span><span class="sxs-lookup"><span data-stu-id="04773-109"><dt>**RPC\_C\_BINDING\_INFINITE\_TIMEOUT**</dt> <dt> 10 </dt></span></span> </dl> | <span data-ttu-id="04773-110">Continua a tentare di stabilire le comunicazioni per sempre.</span><span class="sxs-lookup"><span data-stu-id="04773-110">Keeps trying to establish communications forever.</span></span><br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <span data-ttu-id="04773-111"><dt>**RPC \_ \_ \_ \_ Timeout binding C minimo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04773-111"><dt>**RPC\_C\_BINDING\_MIN\_TIMEOUT**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="04773-112">Tenta la quantità minima di tempo per il protocollo di rete utilizzato.</span><span class="sxs-lookup"><span data-stu-id="04773-112">Tries the minimum amount of time for the network protocol being used.</span></span> <span data-ttu-id="04773-113">Questo valore predilige il tempo di risposta rispetto alla correttezza per determinare se il server è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="04773-113">This value favors response time over correctness in determining whether the server is running.</span></span><br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <span data-ttu-id="04773-114"><dt>**RPC \_ \_ \_ \_ Timeout predefinito associazione C**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="04773-114"><dt>**RPC\_C\_BINDING\_DEFAULT\_TIMEOUT**</dt> <dt>5</dt></span></span> </dl>       | <span data-ttu-id="04773-115">Tenta un periodo di tempo medio per l'utilizzo del protocollo di rete.</span><span class="sxs-lookup"><span data-stu-id="04773-115">Tries an average amount of time for the network protocol being used.</span></span> <span data-ttu-id="04773-116">Questo valore fornisce la correttezza per determinare se un server è in esecuzione e restituisce il peso del tempo di risposta uguale.</span><span class="sxs-lookup"><span data-stu-id="04773-116">This value gives correctness in determining whether a server is running and gives response time equal weight.</span></span> <span data-ttu-id="04773-117">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="04773-117">This is the default value.</span></span><br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <span data-ttu-id="04773-118"><dt>**RPC \_ \_ \_ \_ Timeout max binding C**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="04773-118"><dt>**RPC\_C\_BINDING\_MAX\_TIMEOUT**</dt> <dt>9</dt></span></span> </dl>                   | <span data-ttu-id="04773-119">Tenta la quantità di tempo più lungo per il protocollo di rete utilizzato.</span><span class="sxs-lookup"><span data-stu-id="04773-119">Tries the longest amount of time for the network protocol being used.</span></span> <span data-ttu-id="04773-120">Questo valore predilige la correttezza per determinare se un server viene eseguito nel tempo di risposta.</span><span class="sxs-lookup"><span data-stu-id="04773-120">This value favors correctness in determining whether a server is running over response time.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="04773-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="04773-121">Remarks</span></span>

<span data-ttu-id="04773-122">I valori nella tabella precedente non sono in secondi.</span><span class="sxs-lookup"><span data-stu-id="04773-122">The values in the preceding table are not in seconds.</span></span> <span data-ttu-id="04773-123">Questi valori rappresentano una quantità di tempo relativa su una scala da zero a 10.</span><span class="sxs-lookup"><span data-stu-id="04773-123">These values represent a relative amount of time on a scale of zero to 10.</span></span> <span data-ttu-id="04773-124">Per altre informazioni su come evitare i ritardi di comunicazione, vedere impedire blocchi lato client.</span><span class="sxs-lookup"><span data-stu-id="04773-124">For more information on avoiding communication delays, refer to Preventing Client-side Hangs.</span></span>

## <a name="requirements"></a><span data-ttu-id="04773-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04773-125">Requirements</span></span>



| <span data-ttu-id="04773-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="04773-126">Requirement</span></span> | <span data-ttu-id="04773-127">Valore</span><span class="sxs-lookup"><span data-stu-id="04773-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="04773-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04773-128">Minimum supported client</span></span><br/> | <span data-ttu-id="04773-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04773-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="04773-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04773-130">Minimum supported server</span></span><br/> | <span data-ttu-id="04773-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04773-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="04773-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04773-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="04773-133"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="04773-133"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





