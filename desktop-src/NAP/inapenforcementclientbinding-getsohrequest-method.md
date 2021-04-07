---
title: Metodo INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient. h)
description: Viene utilizzato dal client di imposizione per recuperare una richiesta di rapporto di integrità per una determinata connessione.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- NAP metodo GetSoHRequest
- Metodo GetSoHRequest NAP, interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964011"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a><span data-ttu-id="bbe18-106">Metodo INapEnforcementClientBinding:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="bbe18-106">INapEnforcementClientBinding::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="bbe18-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="bbe18-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bbe18-108">Il metodo **INapEnforcementClientBinding:: GetSoHRequest** viene usato dal client di imposizione per recuperare una richiesta di rapporto di integrità per una determinata connessione.</span><span class="sxs-lookup"><span data-stu-id="bbe18-108">The **INapEnforcementClientBinding::GetSoHRequest** method is used by the enforcement client to retrieve an SoH-request for a particular connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe18-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbe18-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a><span data-ttu-id="bbe18-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbe18-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe18-111">*connessione* \[ a in\]</span><span class="sxs-lookup"><span data-stu-id="bbe18-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe18-112">Puntatore COM a un'interfaccia [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe18-112">A COM pointer to an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface.</span></span> <span data-ttu-id="bbe18-113">Il NapAgent non tiene i riferimenti all'oggetto associato a questa interfaccia dopo il completamento del metodo.</span><span class="sxs-lookup"><span data-stu-id="bbe18-113">The NapAgent does not hold references to the object associated with this interface after the method completes.</span></span>

</dd> <dt>

<span data-ttu-id="bbe18-114">*retriggerHint* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bbe18-114">*retriggerHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe18-115">Puntatore a un **bool** che indica se la connessione deve essere riattivata.</span><span class="sxs-lookup"><span data-stu-id="bbe18-115">A pointer to a **BOOL** that indicates if the connection should be re-triggered.</span></span> <span data-ttu-id="bbe18-116">È **true** se [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è stato modificato dopo l'ultima chiamata a questa funzione o se [**ProbationTime**](nap-datatypes.md) è scaduto.</span><span class="sxs-lookup"><span data-stu-id="bbe18-116">It is **TRUE** if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) has changed since this function was last called or if [**ProbationTime**](nap-datatypes.md) has expired.</span></span> <span data-ttu-id="bbe18-117">In caso contrario, viene restituito **false** .</span><span class="sxs-lookup"><span data-stu-id="bbe18-117">Otherwise, **FALSE** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe18-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbe18-118">Return value</span></span>

<span data-ttu-id="bbe18-119">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="bbe18-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bbe18-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bbe18-120">Return code</span></span>                                                                                             | <span data-ttu-id="bbe18-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbe18-121">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbe18-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe18-122"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="bbe18-123">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="bbe18-123">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="bbe18-124"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe18-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="bbe18-125">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="bbe18-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bbe18-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe18-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="bbe18-127">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bbe18-127">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bbe18-128"><dt>**NAP \_ E \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe18-128"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="bbe18-129">L'applicazione non è stata inizializzata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="bbe18-129">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="bbe18-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbe18-130">Remarks</span></span>

<span data-ttu-id="bbe18-131">NapAgent imposta [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) per l'oggetto Connection.</span><span class="sxs-lookup"><span data-stu-id="bbe18-131">The NapAgent sets the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the connection object.</span></span>

<span data-ttu-id="bbe18-132">Se una [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è rimasta in attesa di questa connessione, viene ignorata e il Shas riceve una notifica di **SoHRequests** orfano.</span><span class="sxs-lookup"><span data-stu-id="bbe18-132">If an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was outstanding on this connection, then it is discarded, and the SHAs are notified of orphaned **SoHRequests**.</span></span>

<span data-ttu-id="bbe18-133">Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe18-133">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe18-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbe18-134">Requirements</span></span>



| <span data-ttu-id="bbe18-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe18-135">Requirement</span></span> | <span data-ttu-id="bbe18-136">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe18-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe18-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbe18-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe18-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bbe18-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bbe18-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbe18-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe18-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bbe18-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bbe18-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbe18-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbe18-142"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe18-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbe18-143">IDL</span><span class="sxs-lookup"><span data-stu-id="bbe18-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bbe18-144"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bbe18-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="bbe18-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bbe18-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbe18-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe18-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bbe18-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbe18-147">See also</span></span>

<dl> <span data-ttu-id="bbe18-148"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bbe18-148"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="bbe18-149">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="bbe18-149">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





