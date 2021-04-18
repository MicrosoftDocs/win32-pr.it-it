---
title: Metodo INapSystemHealthAgentBinding FlushCache (NapSystemHealthAgent. h)
description: Viene chiamato da un SHA per scaricare la cache del rapporto di integrità.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- NAP Metodo FlushCache
- Metodo FlushCache NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP, Metodo FlushCache
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300956"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a><span data-ttu-id="43d19-106">Metodo INapSystemHealthAgentBinding:: FlushCache</span><span class="sxs-lookup"><span data-stu-id="43d19-106">INapSystemHealthAgentBinding::FlushCache method</span></span>

> [!Note]  
> <span data-ttu-id="43d19-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="43d19-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="43d19-108">Il metodo **INapSystemHealthAgentBinding:: FlushCache** viene chiamato da un SHA per scaricare la cache del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="43d19-108">The **INapSystemHealthAgentBinding::FlushCache** method is called by an SHA to flush its SoH cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d19-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43d19-109">Syntax</span></span>


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a><span data-ttu-id="43d19-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="43d19-110">Parameters</span></span>

<span data-ttu-id="43d19-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="43d19-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43d19-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43d19-112">Return value</span></span>

<span data-ttu-id="43d19-113">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="43d19-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="43d19-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="43d19-114">Return code</span></span>                                                                                         | <span data-ttu-id="43d19-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43d19-115">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43d19-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43d19-116"><dt>**S\_OK** </dt></span></span> </dl>               | <span data-ttu-id="43d19-117">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="43d19-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="43d19-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="43d19-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>     | <span data-ttu-id="43d19-119">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="43d19-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="43d19-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="43d19-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>      | <span data-ttu-id="43d19-121">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="43d19-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="43d19-122"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="43d19-122"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="43d19-123">Il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="43d19-123">The NapAgent has been stopped.</span></span> <span data-ttu-id="43d19-124">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="43d19-124">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43d19-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="43d19-125">Remarks</span></span>

<span data-ttu-id="43d19-126">NapAgent gestisce una cache di invieranno recenti forniti da SHAs diversi.</span><span class="sxs-lookup"><span data-stu-id="43d19-126">The NapAgent maintains a cache of recent SoHs provided by different SHAs.</span></span> <span data-ttu-id="43d19-127">Questa cache è utile per ottimizzare le prestazioni in fase di avvio, quando SHAs può o meno essere associato al sistema.</span><span class="sxs-lookup"><span data-stu-id="43d19-127">This cache is useful to optimize boot-time performance, when SHAs may or may not be bound to the system.</span></span>

<span data-ttu-id="43d19-128">SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="43d19-128">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d19-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43d19-129">Requirements</span></span>



| <span data-ttu-id="43d19-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="43d19-130">Requirement</span></span> | <span data-ttu-id="43d19-131">Valore</span><span class="sxs-lookup"><span data-stu-id="43d19-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d19-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43d19-132">Minimum supported client</span></span><br/> | <span data-ttu-id="43d19-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43d19-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="43d19-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43d19-134">Minimum supported server</span></span><br/> | <span data-ttu-id="43d19-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43d19-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="43d19-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43d19-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="43d19-137"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="43d19-137"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="43d19-138">IDL</span><span class="sxs-lookup"><span data-stu-id="43d19-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43d19-139"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43d19-139"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="43d19-140">DLL</span><span class="sxs-lookup"><span data-stu-id="43d19-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43d19-141"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43d19-141"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="43d19-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43d19-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d19-143">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="43d19-143">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





