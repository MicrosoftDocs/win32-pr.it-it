---
title: Metodo INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient. h)
description: Viene usato da NapAgent per informare il client di imposizione delle modifiche del rapporto di integrità.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- NAP metodo NotifySoHChange
- Metodo NotifySoHChange NAP, interfaccia INapEnforcementClientCallback
- Interfaccia INapEnforcementClientCallback NAP, metodo NotifySoHChange
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121606"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a><span data-ttu-id="0e356-106">Metodo INapEnforcementClientCallback:: NotifySoHChange</span><span class="sxs-lookup"><span data-stu-id="0e356-106">INapEnforcementClientCallback::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="0e356-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="0e356-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0e356-108">Il metodo di callback **INapEnforcementClientCallback:: NotifySoHChange** viene usato da napagent per informare il client di imposizione delle modifiche del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="0e356-108">The **INapEnforcementClientCallback::NotifySoHChange** callback method is used by the NapAgent to inform the enforcement client of SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e356-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e356-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="0e356-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e356-110">Parameters</span></span>

<span data-ttu-id="0e356-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0e356-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e356-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e356-112">Return value</span></span>

<span data-ttu-id="0e356-113">Questo metodo di callback deve restituire uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="0e356-113">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="0e356-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0e356-114">Return code</span></span>                                                                                                | <span data-ttu-id="0e356-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e356-115">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e356-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e356-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="0e356-117">Restituisce questo valore se l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0e356-117">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="0e356-118"><dt>**\_server RPC \_ non \_ disponibile**</dt></span><span class="sxs-lookup"><span data-stu-id="0e356-118"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="0e356-119">Se si restituisce questo valore, l'imposizione viene rimossa dall'elenco associato-SHA e viene scaricata la voce della cache NapAgent corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0e356-119">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="0e356-120">L'SHA in errore può quindi reinizializzarsi con NapAgent.</span><span class="sxs-lookup"><span data-stu-id="0e356-120">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e356-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e356-121">Remarks</span></span>

<span data-ttu-id="0e356-122">Il completamento della correzione del sistema è un evento di modifica dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="0e356-122">The completion of system fix-up is a system health change event.</span></span> <span data-ttu-id="0e356-123">Ciò significa che è necessario chiamare **NotifySoHChange** quando una notifica [**INapSystemHealthAgentCallback:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indica che il client è fisso.</span><span class="sxs-lookup"><span data-stu-id="0e356-123">That means you must call **NotifySoHChange** when a [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) notification indicates that the client is fixed.</span></span> <span data-ttu-id="0e356-124">Quando un client viene risolto, il membro di **stato** della struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) restituito da **GetFixupInfo** ha il valore **fixupStateSuccess**.</span><span class="sxs-lookup"><span data-stu-id="0e356-124">When a client is fixed, the **state** member of the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure returned by **GetFixupInfo** has a value of **fixupStateSuccess**.</span></span>

<span data-ttu-id="0e356-125">Dopo essere stato chiamato da NapAgent tramite questo callback, l'agente di imposizione deve quindi chiamare [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) per recuperare la nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="0e356-125">After being called by the NapAgent via this callback, the enforcement agent must then call [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) to retrieve the new request.</span></span> <span data-ttu-id="0e356-126">Questa chiamata può essere eseguita sullo stesso thread di **INapEnforcementClientCallback:: NotifySoHChange**.</span><span class="sxs-lookup"><span data-stu-id="0e356-126">This call can be made on the same thread as **INapEnforcementClientCallback::NotifySoHChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e356-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e356-127">Requirements</span></span>



| <span data-ttu-id="0e356-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e356-128">Requirement</span></span> | <span data-ttu-id="0e356-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0e356-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e356-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e356-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0e356-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e356-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0e356-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e356-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0e356-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e356-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0e356-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e356-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e356-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e356-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e356-136">IDL</span><span class="sxs-lookup"><span data-stu-id="0e356-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0e356-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0e356-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e356-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e356-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e356-139">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="0e356-139">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





