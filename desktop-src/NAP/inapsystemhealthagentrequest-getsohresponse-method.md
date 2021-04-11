---
title: Metodo INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent. h)
description: Viene usato dall'agente per l'integrità per recuperare il BLOB SoHResponse quando NapAgent chiama INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- NAP metodo GetSoHResponse
- Metodo GetSoHResponse NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119399"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a><span data-ttu-id="332d1-106">Metodo INapSystemHealthAgentRequest:: GetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="332d1-106">INapSystemHealthAgentRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="332d1-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="332d1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="332d1-108">Il metodo **INapSystemHealthAgentRequest:: GetSoHResponse** viene usato dall'agente per l'integrità per recuperare il BLOB SoHResponse quando napagent chiama [**INapSystemHealthAgentCallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span><span class="sxs-lookup"><span data-stu-id="332d1-108">The **INapSystemHealthAgentRequest::GetSoHResponse** method is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls [**INapSystemHealthAgentCallback::ProcessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="332d1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="332d1-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a><span data-ttu-id="332d1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="332d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="332d1-111">*sohResponse* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="332d1-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="332d1-112">Puntatore a un puntatore a un pacchetto [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="332d1-112">A pointer to a pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="332d1-113">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="332d1-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="332d1-114">Puntatore a un flag che consente la correzione da parte di SHA se il bit [**shaFixup**](nap-type-constants.md) è impostato; in caso contrario, la correzione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="332d1-114">A pointer to a flag that enables fix-up by the SHA if the [**shaFixup**](nap-type-constants.md) bit is set, otherwise fix-up is disabled.</span></span>



| <span data-ttu-id="332d1-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="332d1-115">Possible Values</span></span>                                                                                                                                                          | <span data-ttu-id="332d1-116">Significato</span><span class="sxs-lookup"><span data-stu-id="332d1-116">Meaning</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <span data-ttu-id="332d1-117"><dt>**shaFixup**</dt></span><span class="sxs-lookup"><span data-stu-id="332d1-117"><dt>**shaFixup**</dt></span></span> </dl> | <span data-ttu-id="332d1-118">Si prevede che l'SHA esegua la correzione in base alla risposta.</span><span class="sxs-lookup"><span data-stu-id="332d1-118">The SHA is expected to perform the fixup based on the response.</span></span> <span data-ttu-id="332d1-119">Se questo flag non è impostato, SHA non deve eseguire una correzione anche se [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indica che non è integro.</span><span class="sxs-lookup"><span data-stu-id="332d1-119">If this flag is not set, the SHA should not perform a fix-up even though the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indicates that it is unhealthy.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="332d1-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="332d1-120">Return value</span></span>

<span data-ttu-id="332d1-121">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="332d1-121">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="332d1-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="332d1-122">Return code</span></span>                                                                                     | <span data-ttu-id="332d1-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="332d1-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="332d1-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="332d1-124"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="332d1-125">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="332d1-125">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="332d1-126"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="332d1-126"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="332d1-127">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="332d1-127">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="332d1-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="332d1-128"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="332d1-129">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="332d1-129">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="332d1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="332d1-130">Requirements</span></span>



| <span data-ttu-id="332d1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="332d1-131">Requirement</span></span> | <span data-ttu-id="332d1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="332d1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332d1-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="332d1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="332d1-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="332d1-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="332d1-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="332d1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="332d1-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="332d1-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="332d1-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="332d1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="332d1-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="332d1-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="332d1-139">IDL</span><span class="sxs-lookup"><span data-stu-id="332d1-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="332d1-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="332d1-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="332d1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="332d1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="332d1-142"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="332d1-142"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="332d1-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="332d1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332d1-144">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="332d1-144">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





