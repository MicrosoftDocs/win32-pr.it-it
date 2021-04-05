---
title: Metodo GetConnection INapEnforcementClientCallback (NapEnforcementClient. h)
description: Viene chiamato da NapAgent e implementato dal client di imposizione per restituire un set di connessioni.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Metodo GetConnection NAP
- Metodo GetConnection NAP, interfaccia INapEnforcementClientCallback
- Interfaccia NAP di INapEnforcementClientCallback, Metodo GetConnection
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874582"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a><span data-ttu-id="e9758-106">Metodo INapEnforcementClientCallback:: GetConnection</span><span class="sxs-lookup"><span data-stu-id="e9758-106">INapEnforcementClientCallback::GetConnections method</span></span>

> [!Note]  
> <span data-ttu-id="e9758-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="e9758-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e9758-108">Il metodo di callback **INapEnforcementClientCallback:: GetConnection** viene chiamato da napagent e implementato dal client di imposizione per restituire un set di connessioni.</span><span class="sxs-lookup"><span data-stu-id="e9758-108">The **INapEnforcementClientCallback::GetConnections** callback method is called by the NapAgent and implemented by the enforcement client to return a set of connections.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9758-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9758-109">Syntax</span></span>


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a><span data-ttu-id="e9758-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9758-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9758-111">*connessioni* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e9758-111">*connections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9758-112">Puntatore al set corrente di [**connessioni**](connections-struct.md)gestite.</span><span class="sxs-lookup"><span data-stu-id="e9758-112">A pointer to the current set of maintained [**Connections**](connections-struct.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9758-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9758-113">Return value</span></span>

<span data-ttu-id="e9758-114">Questo metodo di callback deve restituire uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="e9758-114">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="e9758-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e9758-115">Return code</span></span>                                                                                                | <span data-ttu-id="e9758-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9758-116">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9758-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e9758-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e9758-118">Restituisce questo valore se l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e9758-118">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="e9758-119"><dt>**\_server RPC \_ non \_ disponibile**</dt></span><span class="sxs-lookup"><span data-stu-id="e9758-119"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="e9758-120">Se si restituisce questo valore, l'imposizione viene rimossa dall'elenco associato-SHA e viene scaricata la voce della cache NapAgent corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e9758-120">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="e9758-121">L'SHA in errore può quindi reinizializzarsi con NapAgent.</span><span class="sxs-lookup"><span data-stu-id="e9758-121">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e9758-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9758-122">Requirements</span></span>



| <span data-ttu-id="e9758-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9758-123">Requirement</span></span> | <span data-ttu-id="e9758-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e9758-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9758-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9758-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e9758-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9758-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e9758-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9758-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e9758-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9758-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e9758-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9758-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9758-130"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9758-130"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9758-131">IDL</span><span class="sxs-lookup"><span data-stu-id="e9758-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9758-132"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9758-132"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9758-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9758-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9758-134">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="e9758-134">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





