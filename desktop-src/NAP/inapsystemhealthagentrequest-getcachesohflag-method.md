---
title: Metodo INapSystemHealthAgentRequest GetCacheSoHFlag (NapSystemHealthAgent. h)
description: Viene usato solo da NapAgent.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- NAP metodo GetCacheSoHFlag
- Metodo GetCacheSoHFlag NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo GetCacheSoHFlag
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518418"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a><span data-ttu-id="967fa-106">Metodo INapSystemHealthAgentRequest:: GetCacheSoHFlag</span><span class="sxs-lookup"><span data-stu-id="967fa-106">INapSystemHealthAgentRequest::GetCacheSoHFlag method</span></span>

> [!Note]  
> <span data-ttu-id="967fa-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="967fa-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="967fa-108">Il metodo **INapSystemHealthAgentRequest:: GetCacheSoHFlag** viene usato solo da napagent.</span><span class="sxs-lookup"><span data-stu-id="967fa-108">The **INapSystemHealthAgentRequest::GetCacheSoHFlag** method is used only by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="967fa-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="967fa-109">Syntax</span></span>


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="967fa-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="967fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="967fa-111">*cacheSohForLaterUse*</span><span class="sxs-lookup"><span data-stu-id="967fa-111">*cacheSohForLaterUse*</span></span> 
</dt> <dd>

<span data-ttu-id="967fa-112">**Bool** che è **true** se il napagent deve memorizzare nella cache il rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="967fa-112">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="967fa-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="967fa-113">Return value</span></span>

<span data-ttu-id="967fa-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="967fa-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="967fa-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="967fa-115">Return code</span></span>                                                                                     | <span data-ttu-id="967fa-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="967fa-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="967fa-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="967fa-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="967fa-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="967fa-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="967fa-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="967fa-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="967fa-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="967fa-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="967fa-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="967fa-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="967fa-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="967fa-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="967fa-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="967fa-123">Requirements</span></span>



| <span data-ttu-id="967fa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="967fa-124">Requirement</span></span> | <span data-ttu-id="967fa-125">Valore</span><span class="sxs-lookup"><span data-stu-id="967fa-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="967fa-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="967fa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="967fa-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="967fa-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="967fa-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="967fa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="967fa-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="967fa-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="967fa-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="967fa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="967fa-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="967fa-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="967fa-132">IDL</span><span class="sxs-lookup"><span data-stu-id="967fa-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="967fa-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="967fa-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="967fa-134">DLL</span><span class="sxs-lookup"><span data-stu-id="967fa-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="967fa-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="967fa-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="967fa-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="967fa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967fa-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="967fa-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





