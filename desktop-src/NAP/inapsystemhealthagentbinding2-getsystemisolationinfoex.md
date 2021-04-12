---
title: Metodo INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent. h)
description: Viene chiamato da SHAs per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- NAP metodo GetSystemIsolationInfoEx
- Metodo GetSystemIsolationInfoEx NAP, interfaccia INapSystemHealthAgentBinding2
- Interfaccia INapSystemHealthAgentBinding2 NAP, metodo GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517932"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a><span data-ttu-id="922df-106">Metodo INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="922df-106">INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="922df-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="922df-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="922df-108">Il metodo **INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx** viene chiamato da Shas per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.</span><span class="sxs-lookup"><span data-stu-id="922df-108">The **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** method is called by SHAs to determine the system isolation state and extended isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="922df-109">Usare [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) per determinare solo lo stato di isolamento del sistema.</span><span class="sxs-lookup"><span data-stu-id="922df-109">Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) in order to only determine the isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="922df-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="922df-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="922df-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="922df-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="922df-112">*isolationInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="922df-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="922df-113">Puntatore a un puntatore a una struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) che contiene lo stato di isolamento esteso del sistema per le connessioni note.</span><span class="sxs-lookup"><span data-stu-id="922df-113">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the extended isolation state of the system for known connections.</span></span> <span data-ttu-id="922df-114">*isolationInfo* indica se il sistema è in uno stato di accesso limitato, di prova o senza restrizioni, nonché di informazioni [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .</span><span class="sxs-lookup"><span data-stu-id="922df-114">*isolationInfo* indicates if the system is in a state of restricted access, probation, or unrestricted access, as well as [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) information.</span></span>

</dd> <dt>

<span data-ttu-id="922df-115">*unknownConnections* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="922df-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="922df-116">Puntatore a un **bool** che è **true** se le connessioni sono in uno stato sconosciuto e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="922df-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="922df-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="922df-117">Return value</span></span>

<span data-ttu-id="922df-118">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="922df-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="922df-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="922df-119">Return code</span></span>                                                                                             | <span data-ttu-id="922df-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="922df-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="922df-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="922df-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="922df-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="922df-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="922df-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="922df-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="922df-124">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="922df-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="922df-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="922df-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="922df-126">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="922df-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="922df-127"><dt>**NAP \_ E \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="922df-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="922df-128">SHA non è stato inizializzato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="922df-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="922df-129"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="922df-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="922df-130">Il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="922df-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="922df-131">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="922df-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="922df-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="922df-132">Remarks</span></span>

<span data-ttu-id="922df-133">SHA deve liberare la struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chiamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="922df-133">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

<span data-ttu-id="922df-134">SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="922df-134">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="922df-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="922df-135">Requirements</span></span>



| <span data-ttu-id="922df-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="922df-136">Requirement</span></span> | <span data-ttu-id="922df-137">Valore</span><span class="sxs-lookup"><span data-stu-id="922df-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="922df-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="922df-138">Minimum supported client</span></span><br/> | <span data-ttu-id="922df-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="922df-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="922df-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="922df-140">Minimum supported server</span></span><br/> | <span data-ttu-id="922df-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="922df-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="922df-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="922df-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="922df-143"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="922df-143"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="922df-144">IDL</span><span class="sxs-lookup"><span data-stu-id="922df-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="922df-145"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="922df-145"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="922df-146">DLL</span><span class="sxs-lookup"><span data-stu-id="922df-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="922df-147"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="922df-147"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="922df-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="922df-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="922df-149">**INapSystemHealthAgentBinding2**</span><span class="sxs-lookup"><span data-stu-id="922df-149">**INapSystemHealthAgentBinding2**</span></span>](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





