---
title: Metodo INapSystemHealthAgentRequest GetStringCorrelationId (NapSystemHealthAgent. h)
description: Viene usato dagli agenti di integrità del sistema per registrare l'ID di correlazione.
ms.assetid: 5d6f2392-2ada-474a-b150-31e0583c2ea7
keywords:
- NAP metodo GetStringCorrelationId
- Metodo GetStringCorrelationId NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetStringCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f33e98ae4b0fd76d97e85fb3588bcd1f2d33fd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740906"
---
# <a name="inapsystemhealthagentrequestgetstringcorrelationid-method"></a><span data-ttu-id="df324-106">Metodo INapSystemHealthAgentRequest:: GetStringCorrelationId</span><span class="sxs-lookup"><span data-stu-id="df324-106">INapSystemHealthAgentRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="df324-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="df324-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="df324-108">Il metodo **INapSystemHealthAgentRequest:: GetStringCorrelationId** viene usato dagli agenti di integrità del sistema per registrare l'ID di correlazione.</span><span class="sxs-lookup"><span data-stu-id="df324-108">The **INapSystemHealthAgentRequest::GetStringCorrelationId** method is used by system health agents to log the correlation ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="df324-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df324-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="df324-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="df324-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df324-111">ID correlazione  \[ out\]</span><span class="sxs-lookup"><span data-stu-id="df324-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df324-112">Puntatore a un puntatore a un valore [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) univoco per questo scambio di integrità.</span><span class="sxs-lookup"><span data-stu-id="df324-112">A pointer to a pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df324-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df324-113">Return value</span></span>

<span data-ttu-id="df324-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="df324-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="df324-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="df324-115">Return code</span></span>                                                                                     | <span data-ttu-id="df324-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df324-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="df324-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df324-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="df324-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="df324-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="df324-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="df324-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="df324-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="df324-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="df324-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="df324-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="df324-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="df324-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="df324-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df324-123">Requirements</span></span>



| <span data-ttu-id="df324-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="df324-124">Requirement</span></span> | <span data-ttu-id="df324-125">Valore</span><span class="sxs-lookup"><span data-stu-id="df324-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df324-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df324-126">Minimum supported client</span></span><br/> | <span data-ttu-id="df324-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df324-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="df324-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df324-128">Minimum supported server</span></span><br/> | <span data-ttu-id="df324-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df324-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="df324-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df324-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="df324-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="df324-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="df324-132">IDL</span><span class="sxs-lookup"><span data-stu-id="df324-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df324-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df324-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="df324-134">DLL</span><span class="sxs-lookup"><span data-stu-id="df324-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df324-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df324-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="df324-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df324-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df324-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="df324-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





