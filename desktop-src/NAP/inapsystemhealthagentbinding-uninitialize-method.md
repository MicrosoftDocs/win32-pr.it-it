---
title: Metodo Uninitialize INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Fa in modo che NapAgent rilasci tutti i relativi riferimenti ai puntatori COM degli agenti di integrità del sistema.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Uninitialize metodo NAP
- Uninitialize metodo NAP, interfaccia INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding Interface NAP, Uninitialize (metodo)
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301812"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a><span data-ttu-id="fe1b2-106">Metodo INapSystemHealthAgentBinding:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="fe1b2-106">INapSystemHealthAgentBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="fe1b2-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe1b2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fe1b2-108">Il metodo **INapSystemHealthAgentBinding:: Uninitialize** induce il napagent a rilasciare tutti i riferimenti ai puntatori com degli agenti di integrità del sistema.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-108">The **INapSystemHealthAgentBinding::Uninitialize** method causes the NapAgent to release all its references to system health agent COM pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe1b2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe1b2-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="fe1b2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe1b2-110">Parameters</span></span>

<span data-ttu-id="fe1b2-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe1b2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe1b2-112">Return value</span></span>

<span data-ttu-id="fe1b2-113">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fe1b2-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fe1b2-114">Return code</span></span>                                                                                             | <span data-ttu-id="fe1b2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe1b2-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe1b2-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe1b2-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="fe1b2-117">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="fe1b2-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fe1b2-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="fe1b2-119">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="fe1b2-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fe1b2-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="fe1b2-121">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="fe1b2-122"><dt>**NAP \_ E \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="fe1b2-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="fe1b2-123">SHA non è stato inizializzato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="fe1b2-124"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="fe1b2-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="fe1b2-125">Il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="fe1b2-126">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe1b2-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe1b2-127">Remarks</span></span>

<span data-ttu-id="fe1b2-128">Il NapAgent blocca l'esecuzione di questa chiamata al metodo fino al completamento di tutte le chiamate esistenti sulle interfacce di binding e callback.</span><span class="sxs-lookup"><span data-stu-id="fe1b2-128">The NapAgent blocks execution of this method call until all existing calls on the Binding and Callback interfaces complete.</span></span>

<span data-ttu-id="fe1b2-129">SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="fe1b2-129">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe1b2-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe1b2-130">Requirements</span></span>



| <span data-ttu-id="fe1b2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe1b2-131">Requirement</span></span> | <span data-ttu-id="fe1b2-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fe1b2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe1b2-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe1b2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fe1b2-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe1b2-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe1b2-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe1b2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fe1b2-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe1b2-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe1b2-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe1b2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe1b2-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe1b2-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe1b2-139">IDL</span><span class="sxs-lookup"><span data-stu-id="fe1b2-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe1b2-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe1b2-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="fe1b2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fe1b2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe1b2-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe1b2-142"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fe1b2-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe1b2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe1b2-144">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="fe1b2-144">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





