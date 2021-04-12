---
title: Metodo INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent. h)
description: Viene usato da SHAs quando cambia il rapporto di integrità.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- NAP metodo NotifySoHChange
- Metodo NotifySoHChange NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP, metodo NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518946"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a><span data-ttu-id="c3a0d-106">Metodo INapSystemHealthAgentBinding:: NotifySoHChange</span><span class="sxs-lookup"><span data-stu-id="c3a0d-106">INapSystemHealthAgentBinding::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="c3a0d-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="c3a0d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c3a0d-108">Il metodo **INapSystemHealthAgentBinding:: NotifySoHChange** viene usato da Shas quando il rapporto di integrità viene modificato.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-108">The **INapSystemHealthAgentBinding::NotifySoHChange** method is used by SHAs when their SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a0d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3a0d-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="c3a0d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3a0d-110">Parameters</span></span>

<span data-ttu-id="c3a0d-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3a0d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3a0d-112">Return value</span></span>

<span data-ttu-id="c3a0d-113">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c3a0d-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c3a0d-114">Return code</span></span>                                                                                             | <span data-ttu-id="c3a0d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3a0d-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3a0d-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3a0d-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="c3a0d-117">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="c3a0d-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c3a0d-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="c3a0d-119">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="c3a0d-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c3a0d-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="c3a0d-121">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="c3a0d-122"><dt>**NAP \_ E \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="c3a0d-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="c3a0d-123">SHA non è stato inizializzato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="c3a0d-124"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="c3a0d-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="c3a0d-125">Il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="c3a0d-126">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3a0d-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3a0d-127">Remarks</span></span>

<span data-ttu-id="c3a0d-128">SHAs non deve chiamare questa API speculativamente perché comporta uno scambio di rapporto di integrità in rete.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-128">SHAs must not call this API speculatively since it results in an SoH exchange on the wire.</span></span> <span data-ttu-id="c3a0d-129">Le chiamate a questa API devono essere effettuate solo quando necessario.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-129">Calls to this API should only be made when necessary.</span></span>

<span data-ttu-id="c3a0d-130">Il NapAgent non tiene presente questo thread per elaborare la modifica del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-130">The NapAgent does not hold this thread to process the SoH change.</span></span> <span data-ttu-id="c3a0d-131">Viene invece restituito immediatamente e la modifica viene elaborata in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="c3a0d-131">Instead, it returns immediately and processes the change asynchronously.</span></span>

<span data-ttu-id="c3a0d-132">SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="c3a0d-132">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a0d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3a0d-133">Requirements</span></span>



| <span data-ttu-id="c3a0d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a0d-134">Requirement</span></span> | <span data-ttu-id="c3a0d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c3a0d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a0d-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3a0d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a0d-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3a0d-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c3a0d-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3a0d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a0d-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c3a0d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c3a0d-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3a0d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3a0d-141"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3a0d-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3a0d-142">IDL</span><span class="sxs-lookup"><span data-stu-id="c3a0d-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3a0d-143"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3a0d-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="c3a0d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c3a0d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3a0d-145"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3a0d-145"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c3a0d-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3a0d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a0d-147">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="c3a0d-147">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





