---
title: Metodo INapSystemHealthAgentRequest GetCorrelationId (NapSystemHealthAgent. h)
description: Viene usato dagli agenti di integrità del sistema per correlare le risposte SOH e SoH.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- NAP metodo GetCorrelationId
- Metodo GetCorrelationId NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519270"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a><span data-ttu-id="9eae2-106">Metodo INapSystemHealthAgentRequest:: GetCorrelationId</span><span class="sxs-lookup"><span data-stu-id="9eae2-106">INapSystemHealthAgentRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="9eae2-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="9eae2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9eae2-108">Il metodo **INapSystemHealthAgentRequest:: GetCorrelationId** viene usato dagli agenti di integrità del sistema per correlare le risposte SoH e SOH.</span><span class="sxs-lookup"><span data-stu-id="9eae2-108">The **INapSystemHealthAgentRequest::GetCorrelationId** method is used by system health agents to correlate SoH's and SoH-Responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eae2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eae2-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="9eae2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eae2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eae2-111">ID correlazione  \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9eae2-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eae2-112">Puntatore a un [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) univoco per lo scambio di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="9eae2-112">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eae2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eae2-113">Return value</span></span>

<span data-ttu-id="9eae2-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="9eae2-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9eae2-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9eae2-115">Return code</span></span>                                                                                     | <span data-ttu-id="9eae2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eae2-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9eae2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9eae2-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9eae2-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="9eae2-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9eae2-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="9eae2-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9eae2-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="9eae2-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9eae2-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9eae2-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9eae2-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9eae2-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9eae2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eae2-123">Requirements</span></span>



| <span data-ttu-id="9eae2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eae2-124">Requirement</span></span> | <span data-ttu-id="9eae2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9eae2-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eae2-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eae2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9eae2-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9eae2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9eae2-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eae2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9eae2-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9eae2-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9eae2-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9eae2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eae2-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eae2-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="9eae2-132">IDL</span><span class="sxs-lookup"><span data-stu-id="9eae2-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9eae2-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9eae2-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="9eae2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9eae2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eae2-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eae2-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="9eae2-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eae2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eae2-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="9eae2-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





