---
title: Metodo Initialize INapEnforcementClientBinding (NapEnforcementClient. h)
description: Avvia automaticamente il servizio NapAgent.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapEnforcementClientBinding
- Interfaccia NAP di INapEnforcementClientBinding, metodo Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476000"
---
# <a name="inapenforcementclientbindinginitialize-method"></a><span data-ttu-id="8be97-106">Metodo INapEnforcementClientBinding:: Initialize</span><span class="sxs-lookup"><span data-stu-id="8be97-106">INapEnforcementClientBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="8be97-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8be97-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8be97-108">Il metodo **INapEnforcementClientBinding:: Initialize** avvia automaticamente il servizio napagent.</span><span class="sxs-lookup"><span data-stu-id="8be97-108">The **INapEnforcementClientBinding::Initialize** method starts up the NapAgent service automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be97-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8be97-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="8be97-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8be97-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be97-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8be97-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be97-112">Un [**EnforcementEntityId**](nap-datatypes.md) che identifica il client di imposizione e la relativa versione.</span><span class="sxs-lookup"><span data-stu-id="8be97-112">An [**EnforcementEntityId**](nap-datatypes.md) that identifies the enforcement client and its version.</span></span>

</dd> <dt>

<span data-ttu-id="8be97-113">*callback* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8be97-113">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be97-114">Puntatore COM a un'interfaccia [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) usata da napagent per richiamare i client di imposizione con Notify/Process.</span><span class="sxs-lookup"><span data-stu-id="8be97-114">A COM pointer to an [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interface used by the NapAgent to callback the enforcement clients with notify/process.</span></span> <span data-ttu-id="8be97-115">NapAgent include un riferimento all'oggetto associato a questa interfaccia fino a quando non viene chiamato [**INapEnforcementClientBinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) .</span><span class="sxs-lookup"><span data-stu-id="8be97-115">The NapAgent holds a reference to the object associated with this interface until [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be97-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8be97-116">Return value</span></span>

<span data-ttu-id="8be97-117">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="8be97-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8be97-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8be97-118">Return code</span></span>                                                                                                         | <span data-ttu-id="8be97-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8be97-119">Description</span></span>                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8be97-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8be97-120"><dt>**S\_OK** </dt></span></span> </dl>                               | <span data-ttu-id="8be97-121">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="8be97-121">The operation is successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="8be97-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8be97-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>                     | <span data-ttu-id="8be97-123">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="8be97-123">Permissions error, access denied.</span></span><br/>                                             |
| <dl> <span data-ttu-id="8be97-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8be97-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>                      | <span data-ttu-id="8be97-125">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8be97-125">System resource limit, could not perform the operation.</span></span><br/>                       |
| <dl> <span data-ttu-id="8be97-126"><dt>**HRESULT (errore \_ già \_ inizializzato)**</dt></span><span class="sxs-lookup"><span data-stu-id="8be97-126"><dt>**HRESULT(ERROR\_ALREADY\_INITIALIZED)**</dt></span></span> </dl> | <span data-ttu-id="8be97-127">Se l'applicazione è stata inizializzata in precedenza, viene restituito questo codice di errore.</span><span class="sxs-lookup"><span data-stu-id="8be97-127">If the enforcer has initialized previously, then this error code is returned.</span></span><br/> |
| <dl> <span data-ttu-id="8be97-128"><dt>**NAP \_ E \_ non \_ registrato**</dt></span><span class="sxs-lookup"><span data-stu-id="8be97-128"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>              | <span data-ttu-id="8be97-129">Se l'applicazione non è stata registrata in precedenza, viene restituito questo codice di errore.</span><span class="sxs-lookup"><span data-stu-id="8be97-129">If the enforcer has not registered earlier, this error code is returned.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="8be97-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="8be97-130">Remarks</span></span>

<span data-ttu-id="8be97-131">Il client di imposizione deve chiamare il metodo **INapEnforcementClientBinding:: Initialize** prima di chiamare qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="8be97-131">The enforcement client must call the **INapEnforcementClientBinding::Initialize** method before calling any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be97-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8be97-132">Requirements</span></span>



| <span data-ttu-id="8be97-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be97-133">Requirement</span></span> | <span data-ttu-id="8be97-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8be97-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be97-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8be97-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8be97-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8be97-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8be97-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8be97-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8be97-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8be97-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8be97-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8be97-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8be97-140"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8be97-140"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="8be97-141">IDL</span><span class="sxs-lookup"><span data-stu-id="8be97-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8be97-142"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8be97-142"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="8be97-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8be97-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8be97-144"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8be97-144"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8be97-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8be97-145">See also</span></span>

<dl> <span data-ttu-id="8be97-146"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8be97-146"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="8be97-147">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="8be97-147">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="8be97-148">**INapEnforcementClientBinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="8be97-148">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





