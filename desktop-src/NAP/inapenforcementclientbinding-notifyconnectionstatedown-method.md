---
title: Metodo INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient. h)
description: Viene usato per indicare al NapAgent che una connessione a un client di imposizione è diminuita.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- NAP metodo NotifyConnectionStateDown
- Metodo NotifyConnectionStateDown NAP, interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding NAP, metodo NotifyConnectionStateDown
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519278"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a><span data-ttu-id="4b21b-106">Metodo INapEnforcementClientBinding:: NotifyConnectionStateDown</span><span class="sxs-lookup"><span data-stu-id="4b21b-106">INapEnforcementClientBinding::NotifyConnectionStateDown method</span></span>

> [!Note]  
> <span data-ttu-id="4b21b-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="4b21b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4b21b-108">Il metodo **INapEnforcementClientBinding:: NotifyConnectionStateDown** viene usato per indicare al napagent che una connessione a un client di imposizione è diminuita.</span><span class="sxs-lookup"><span data-stu-id="4b21b-108">The **INapEnforcementClientBinding::NotifyConnectionStateDown** method is used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b21b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b21b-109">Syntax</span></span>


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a><span data-ttu-id="4b21b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b21b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b21b-111">*downCxn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b21b-111">*downCxn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b21b-112">Puntatore COM all'interfaccia [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) della connessione in basso.</span><span class="sxs-lookup"><span data-stu-id="4b21b-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the down connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b21b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b21b-113">Return value</span></span>

<span data-ttu-id="4b21b-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="4b21b-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4b21b-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4b21b-115">Return code</span></span>                                                                                             | <span data-ttu-id="4b21b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b21b-116">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b21b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b21b-117"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="4b21b-118">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="4b21b-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="4b21b-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4b21b-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="4b21b-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="4b21b-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4b21b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4b21b-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="4b21b-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4b21b-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4b21b-123"><dt>**NAP \_ E \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="4b21b-123"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="4b21b-124">L'applicazione non è stata inizializzata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4b21b-124">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="4b21b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b21b-125">Remarks</span></span>

<span data-ttu-id="4b21b-126">Quando una delle connessioni stabilite da un client di imposizione si arresta, il client di imposizione deve rimuovere la connessione dall'elenco attivo e informare il NapAgent usando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4b21b-126">When any of the connections established by an enforcement client go down, the enforcement client should remove the connection from its active list and inform the NapAgent using this method.</span></span> <span data-ttu-id="4b21b-127">Non appena la chiamata restituisce, l'oggetto connessione può essere rilasciato e liberato.</span><span class="sxs-lookup"><span data-stu-id="4b21b-127">As soon as this call returns, the connection object can be released and freed.</span></span> <span data-ttu-id="4b21b-128">NapAgent non conterrà riferimenti all'oggetto Connection.</span><span class="sxs-lookup"><span data-stu-id="4b21b-128">The NapAgent will not hold references to the connection object.</span></span>

<span data-ttu-id="4b21b-129">In seguito a questa notifica, il NapAgent aggiorna lo stato di protezione accesso alla rete del sistema in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="4b21b-129">As a result of this notification, the NapAgent updates its system NAP state as appropriate.</span></span>

<span data-ttu-id="4b21b-130">Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="4b21b-130">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b21b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b21b-131">Requirements</span></span>



| <span data-ttu-id="4b21b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b21b-132">Requirement</span></span> | <span data-ttu-id="4b21b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4b21b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b21b-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b21b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4b21b-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b21b-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4b21b-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b21b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4b21b-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b21b-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4b21b-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b21b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b21b-139"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b21b-139"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b21b-140">IDL</span><span class="sxs-lookup"><span data-stu-id="4b21b-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b21b-141"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b21b-141"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="4b21b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4b21b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b21b-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b21b-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4b21b-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b21b-144">See also</span></span>

<dl> <span data-ttu-id="4b21b-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4b21b-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="4b21b-146">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="4b21b-146">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





