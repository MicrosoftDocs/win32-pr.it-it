---
title: Metodo Initialize INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Inizializza l'agente integrità sistema (SHA) e associa l'SHA al servizio NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia NAP di INapSystemHealthAgentBinding, metodo Initialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340392"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a><span data-ttu-id="ca143-106">Metodo INapSystemHealthAgentBinding:: Initialize</span><span class="sxs-lookup"><span data-stu-id="ca143-106">INapSystemHealthAgentBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="ca143-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="ca143-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ca143-108">Il metodo **INapSystemHealthAgentBinding:: Initialize** Inizializza l'agente integrità sistema e associa l'Sha al servizio napagent.</span><span class="sxs-lookup"><span data-stu-id="ca143-108">The **INapSystemHealthAgentBinding::Initialize** method initializes the system health agent (SHA) and binds the SHA to the NapAgent service.</span></span> <span data-ttu-id="ca143-109">Questo metodo deve essere chiamato prima di chiamare qualsiasi altro metodo sull'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="ca143-109">This method must be called before calling any other method on the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca143-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca143-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="ca143-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca143-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca143-112">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca143-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca143-113">[SystemHealthEntityId](nap-datatypes.md) univoco che contiene l'ID dell'SHA associato al servizio napagent.</span><span class="sxs-lookup"><span data-stu-id="ca143-113">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA being bound to the NapAgent service.</span></span>

</dd> <dt>

<span data-ttu-id="ca143-114">*callback* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ca143-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca143-115">Puntatore COM a un'interfaccia [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) utilizzata da napagent per richiamare l'agente di integrità con una notifica o un processo.</span><span class="sxs-lookup"><span data-stu-id="ca143-115">A COM pointer to an [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) interface used by the NapAgent to callback the health agent with a notify/process.</span></span> <span data-ttu-id="ca143-116">NapAgent include un riferimento all'oggetto associato a questa interfaccia fino a quando non viene chiamato [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) .</span><span class="sxs-lookup"><span data-stu-id="ca143-116">The NapAgent holds a reference to the object associated with this interface until [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca143-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca143-117">Return value</span></span>

<span data-ttu-id="ca143-118">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="ca143-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ca143-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ca143-119">Return code</span></span>                                                                                                | <span data-ttu-id="ca143-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca143-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca143-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-121"><dt>**S\_OK** </dt></span></span> </dl>                      | <span data-ttu-id="ca143-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ca143-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="ca143-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>            | <span data-ttu-id="ca143-124">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ca143-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="ca143-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>             | <span data-ttu-id="ca143-126">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ca143-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="ca143-127"><dt>**ERRORE \_ già \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-127"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="ca143-128">Se SHA è stato inizializzato in precedenza, viene restituito questo errore.</span><span class="sxs-lookup"><span data-stu-id="ca143-128">If the SHA has initialized previously, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="ca143-129"><dt>**NAP \_ E \_ non \_ registrato**</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-129"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>     | <span data-ttu-id="ca143-130">Se SHA non è stato registrato in precedenza, viene restituito questo errore.</span><span class="sxs-lookup"><span data-stu-id="ca143-130">If the SHA has not registered earlier, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="ca143-131"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-131"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>        | <span data-ttu-id="ca143-132">Il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="ca143-132">The NapAgent has been stopped.</span></span> <span data-ttu-id="ca143-133">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="ca143-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca143-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca143-134">Remarks</span></span>

<span data-ttu-id="ca143-135">NapAgent non attiva uno scambio di rapporto di integrità come risultato dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ca143-135">The NapAgent does not trigger a SoH exchange as a result of initialization.</span></span> <span data-ttu-id="ca143-136">Un agente integrità sistema deve chiamare [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) per richiedere uno scambio di pacchetti SOH dopo l'inizializzazione con napagent.</span><span class="sxs-lookup"><span data-stu-id="ca143-136">A system health agent must call [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to request an exchange of SoH packets after initializing with the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca143-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca143-137">Requirements</span></span>



| <span data-ttu-id="ca143-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca143-138">Requirement</span></span> | <span data-ttu-id="ca143-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ca143-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca143-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca143-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ca143-141">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca143-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ca143-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca143-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ca143-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca143-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ca143-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca143-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca143-145"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-145"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca143-146">IDL</span><span class="sxs-lookup"><span data-stu-id="ca143-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca143-147"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-147"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="ca143-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ca143-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca143-149"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca143-149"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ca143-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca143-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca143-151">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="ca143-151">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





