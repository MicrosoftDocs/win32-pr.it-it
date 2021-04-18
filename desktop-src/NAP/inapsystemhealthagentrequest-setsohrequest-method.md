---
title: Metodo INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent. h)
description: Viene usato dagli agenti di integrità per scrivere la richiesta di rapporto di integrità risultante dalla chiamata a INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- NAP metodo SetSoHRequest
- Metodo SetSoHRequest NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301363"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a><span data-ttu-id="8b52b-106">Metodo INapSystemHealthAgentRequest:: SetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="8b52b-106">INapSystemHealthAgentRequest::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="8b52b-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8b52b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8b52b-108">Il metodo **INapSystemHealthAgentRequest:: SetSoHRequest** viene usato dagli agenti di integrità per scrivere la richiesta di rapporto di integrità risultante dalla chiamata a [**INapSystemHealthAgentCallback:: GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b52b-108">The **INapSystemHealthAgentRequest::SetSoHRequest** method is used by health agents to write their SoH request resulting from the call to [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b52b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b52b-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="8b52b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b52b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b52b-111">*sohRequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b52b-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b52b-112">Puntatore a un pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="8b52b-112">A pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="8b52b-113">*cacheSohForLaterUse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b52b-113">*cacheSohForLaterUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b52b-114">**Bool** che è **true** se il napagent deve memorizzare nella cache il rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8b52b-114">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b52b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b52b-115">Return value</span></span>

<span data-ttu-id="8b52b-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="8b52b-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8b52b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8b52b-117">Return code</span></span>                                                                                     | <span data-ttu-id="8b52b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b52b-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b52b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b52b-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8b52b-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="8b52b-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8b52b-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8b52b-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8b52b-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="8b52b-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8b52b-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8b52b-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8b52b-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8b52b-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8b52b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b52b-125">Requirements</span></span>



| <span data-ttu-id="8b52b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b52b-126">Requirement</span></span> | <span data-ttu-id="8b52b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8b52b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b52b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b52b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8b52b-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b52b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8b52b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b52b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8b52b-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b52b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8b52b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b52b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b52b-133"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b52b-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b52b-134">IDL</span><span class="sxs-lookup"><span data-stu-id="8b52b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b52b-135"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b52b-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="8b52b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8b52b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b52b-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b52b-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="8b52b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b52b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b52b-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="8b52b-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





