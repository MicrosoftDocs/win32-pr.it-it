---
title: Metodo Uninitialize INapEnforcementClientBinding (NapEnforcementClient. h)
description: Conclude il servizio NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Uninitialize metodo NAP
- Uninitialize metodo NAP, interfaccia INapEnforcementClientBinding
- INapEnforcementClientBinding Interface NAP, Uninitialize (metodo)
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302718"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a><span data-ttu-id="96a94-106">Metodo INapEnforcementClientBinding:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="96a94-106">INapEnforcementClientBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="96a94-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="96a94-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="96a94-108">Il metodo **INapEnforcementClientBinding:: Uninitialize** conclude il servizio napagent.</span><span class="sxs-lookup"><span data-stu-id="96a94-108">The **INapEnforcementClientBinding::Uninitialize** method concludes the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a94-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96a94-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="96a94-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="96a94-110">Parameters</span></span>

<span data-ttu-id="96a94-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="96a94-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96a94-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96a94-112">Return value</span></span>

<span data-ttu-id="96a94-113">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="96a94-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="96a94-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="96a94-114">Return code</span></span>                                                                                     | <span data-ttu-id="96a94-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96a94-115">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="96a94-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96a94-116"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="96a94-117">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="96a94-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="96a94-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="96a94-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="96a94-119">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="96a94-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="96a94-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="96a94-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="96a94-121">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="96a94-121">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96a94-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="96a94-122">Remarks</span></span>

<span data-ttu-id="96a94-123">Il NapAgent blocca l'ulteriore elaborazione fino al completamento di tutte le chiamate esistenti sulle interfacce [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) e [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="96a94-123">The NapAgent blocks further processing until all existing calls on the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) and [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interfaces complete.</span></span> <span data-ttu-id="96a94-124">Al termine di questa chiamata, il NapAgent rilascia tutti i riferimenti sui puntatori COM del client di imposizione.</span><span class="sxs-lookup"><span data-stu-id="96a94-124">At the end of this call, the NapAgent releases all its references on enforcement client COM pointers.</span></span>

<span data-ttu-id="96a94-125">Prima che questa funzione venga chiamata, l'applicazione deve chiamare [**INapEnforcementClientBinding:: NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) in tutte le connessioni attive, quindi il Shas può ricevere una notifica in caso di SoH-Requests orfano.</span><span class="sxs-lookup"><span data-stu-id="96a94-125">Before this function is called, the enforcer must call [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) on all its active connections, so the SHAs can be notified if any of their SoH-Requests were orphaned.</span></span>

<span data-ttu-id="96a94-126">Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="96a94-126">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a94-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96a94-127">Requirements</span></span>



| <span data-ttu-id="96a94-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="96a94-128">Requirement</span></span> | <span data-ttu-id="96a94-129">Valore</span><span class="sxs-lookup"><span data-stu-id="96a94-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a94-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96a94-130">Minimum supported client</span></span><br/> | <span data-ttu-id="96a94-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96a94-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="96a94-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96a94-132">Minimum supported server</span></span><br/> | <span data-ttu-id="96a94-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96a94-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="96a94-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96a94-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="96a94-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="96a94-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="96a94-136">IDL</span><span class="sxs-lookup"><span data-stu-id="96a94-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96a94-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96a94-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="96a94-138">DLL</span><span class="sxs-lookup"><span data-stu-id="96a94-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96a94-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96a94-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="96a94-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96a94-140">See also</span></span>

<dl> <span data-ttu-id="96a94-141"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="96a94-141"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="96a94-142">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="96a94-142">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="96a94-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="96a94-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[<span data-ttu-id="96a94-144">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="96a94-144">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





