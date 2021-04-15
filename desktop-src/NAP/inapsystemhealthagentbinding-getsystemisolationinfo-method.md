---
title: Metodo INapSystemHealthAgentBinding GetSystemIsolationInfo (NapSystemHealthAgent. h)
description: Viene chiamato da SHAs per determinare lo stato di isolamento del sistema.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- NAP metodo GetSystemIsolationInfo
- Metodo GetSystemIsolationInfo NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP, metodo GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479048"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a><span data-ttu-id="c8e9e-106">Metodo INapSystemHealthAgentBinding:: GetSystemIsolationInfo</span><span class="sxs-lookup"><span data-stu-id="c8e9e-106">INapSystemHealthAgentBinding::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="c8e9e-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="c8e9e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c8e9e-108">Il metodo **INapSystemHealthAgentBinding:: GetSystemIsolationInfo** viene chiamato da Shas per determinare lo stato di isolamento del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-108">The **INapSystemHealthAgentBinding::GetSystemIsolationInfo** method is called by SHAs to determine the system isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="c8e9e-109">Usare [**INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) per determinare lo stato di isolamento esteso del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-109">Use [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) in order to determine the extended isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c8e9e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8e9e-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a><span data-ttu-id="c8e9e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8e9e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e9e-112">*isolationInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8e9e-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8e9e-113">Puntatore a un puntatore a una struttura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene lo stato di isolamento del sistema per le connessioni note.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-113">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the isolation state of the system for known connections.</span></span> <span data-ttu-id="c8e9e-114">*isolationInfoindicates* se il sistema è in uno stato di accesso limitato, di prova o senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-114">*isolationInfoindicates* if the system is in a state of restricted access, probation, or unrestricted access.</span></span>

</dd> <dt>

<span data-ttu-id="c8e9e-115">*unknownConnections* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8e9e-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8e9e-116">Puntatore a un **bool** che è **true** se le connessioni sono in uno stato sconosciuto e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e9e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8e9e-117">Return value</span></span>

<span data-ttu-id="c8e9e-118">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c8e9e-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c8e9e-119">Return code</span></span>                                                                                             | <span data-ttu-id="c8e9e-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8e9e-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8e9e-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c8e9e-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="c8e9e-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="c8e9e-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c8e9e-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="c8e9e-124">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="c8e9e-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c8e9e-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="c8e9e-126">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="c8e9e-127"><dt>**NAP \_ E \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="c8e9e-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="c8e9e-128">SHA non è stato inizializzato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="c8e9e-129"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="c8e9e-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="c8e9e-130">Il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="c8e9e-131">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="c8e9e-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c8e9e-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8e9e-132">Remarks</span></span>

<span data-ttu-id="c8e9e-133">SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="c8e9e-133">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e9e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8e9e-134">Requirements</span></span>



| <span data-ttu-id="c8e9e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e9e-135">Requirement</span></span> | <span data-ttu-id="c8e9e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c8e9e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e9e-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8e9e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c8e9e-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8e9e-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c8e9e-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8e9e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c8e9e-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c8e9e-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8e9e-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8e9e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8e9e-142"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e9e-142"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8e9e-143">IDL</span><span class="sxs-lookup"><span data-stu-id="c8e9e-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8e9e-144"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8e9e-144"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="c8e9e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c8e9e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8e9e-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8e9e-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c8e9e-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8e9e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e9e-148">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="c8e9e-148">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





