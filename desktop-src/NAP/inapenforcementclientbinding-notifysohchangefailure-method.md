---
title: Metodo INapEnforcementClientBinding NotifySoHChangeFailure (NapEnforcementClient. h)
description: Viene usato dal client di imposizione per informare NapAgent che non è stato in grado di elaborare un NotifySoHChange INapEnforcementClientCallback precedente.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- NAP metodo NotifySoHChangeFailure
- Metodo NotifySoHChangeFailure NAP, interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding NAP, metodo NotifySoHChangeFailure
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479264"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a><span data-ttu-id="4c786-106">Metodo INapEnforcementClientBinding:: NotifySoHChangeFailure</span><span class="sxs-lookup"><span data-stu-id="4c786-106">INapEnforcementClientBinding::NotifySoHChangeFailure method</span></span>

> [!Note]  
> <span data-ttu-id="4c786-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="4c786-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4c786-108">Il metodo **INapEnforcementClientBinding:: NotifySoHChangeFailure** viene usato dal client di imposizione per informare il napagent che non è stato possibile elaborare un [**INapEnforcementClientCallback precedente:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="4c786-108">The **INapEnforcementClientBinding::NotifySoHChangeFailure** method is used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c786-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c786-109">Syntax</span></span>


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a><span data-ttu-id="4c786-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c786-110">Parameters</span></span>

<span data-ttu-id="4c786-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4c786-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c786-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c786-112">Return value</span></span>

<span data-ttu-id="4c786-113">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="4c786-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4c786-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4c786-114">Return code</span></span>                                                                                             | <span data-ttu-id="4c786-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c786-115">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c786-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c786-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="4c786-117">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="4c786-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="4c786-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4c786-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="4c786-119">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="4c786-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4c786-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4c786-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="4c786-121">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4c786-121">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4c786-122"><dt>**NAP \_ E \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="4c786-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="4c786-123">L'applicazione non è stata inizializzata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4c786-123">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="4c786-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c786-124">Remarks</span></span>

<span data-ttu-id="4c786-125">Come risultato di questo metodo, chiamare NapAgent ritenta di applicare la modifica del rapporto di integrità in un secondo momento chiamando [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) .</span><span class="sxs-lookup"><span data-stu-id="4c786-125">As a result of this method call the NapAgent retries applying the SoH change at a later time by calling [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) again.</span></span> <span data-ttu-id="4c786-126">Quando il client di imposizione ha chiamato [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), deve applicare la modifica, ovvero nessun errore viene gestito dal napagent dopo questo punto.</span><span class="sxs-lookup"><span data-stu-id="4c786-126">Once the enforcement client has called [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), it then must apply the change, i.e. no failures are handled by the NapAgent after this point.</span></span>

<span data-ttu-id="4c786-127">Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="4c786-127">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c786-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c786-128">Requirements</span></span>



| <span data-ttu-id="4c786-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c786-129">Requirement</span></span> | <span data-ttu-id="4c786-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4c786-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c786-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c786-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4c786-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c786-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4c786-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c786-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4c786-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c786-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4c786-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c786-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c786-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c786-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c786-137">IDL</span><span class="sxs-lookup"><span data-stu-id="4c786-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c786-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c786-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="4c786-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4c786-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c786-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c786-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4c786-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c786-141">See also</span></span>

<dl> <span data-ttu-id="4c786-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4c786-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="4c786-143">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="4c786-143">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="4c786-144">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="4c786-144">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[<span data-ttu-id="4c786-145">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="4c786-145">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





