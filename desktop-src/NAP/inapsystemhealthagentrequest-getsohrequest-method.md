---
title: Metodo INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent. h)
description: Può essere usato da SHAs Get invieranno precedentemente memorizzato nella cache da NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- NAP metodo GetSoHRequest
- Metodo GetSoHRequest NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048690"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a><span data-ttu-id="5ec76-106">Metodo INapSystemHealthAgentRequest:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="5ec76-106">INapSystemHealthAgentRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="5ec76-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="5ec76-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5ec76-108">Il metodo **INapSystemHealthAgentRequest:: GetSoHRequest** può essere usato da Shas Get invieranno precedentemente memorizzato nella cache da napagent.</span><span class="sxs-lookup"><span data-stu-id="5ec76-108">The **INapSystemHealthAgentRequest::GetSoHRequest** method can be used by SHAs get SoHs previously cached by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec76-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ec76-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="5ec76-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ec76-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ec76-111">*sohRequest* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ec76-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec76-112">Puntatore a un puntatore a un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="5ec76-112">A pointer to a pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ec76-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ec76-113">Return value</span></span>

<span data-ttu-id="5ec76-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="5ec76-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5ec76-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5ec76-115">Return code</span></span>                                                                                            | <span data-ttu-id="5ec76-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ec76-116">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ec76-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec76-117"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="5ec76-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5ec76-118">Operation succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="5ec76-119"><dt>**NAP \_ E \_ nessun rapporto di \_ integrità memorizzato nella cache \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec76-119"><dt>**NAP\_E\_NO\_CACHED\_SOH**</dt></span></span> </dl> | <span data-ttu-id="5ec76-120">Il rapporto di integrità non è stato trovato. NapAgent non dispone di una copia memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="5ec76-120">The SoH is not found; NapAgent does not have a cached copy.</span></span><br/> |
| <dl> <span data-ttu-id="5ec76-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec76-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="5ec76-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="5ec76-122">Permissions error, access denied.</span></span><br/>                           |
| <dl> <span data-ttu-id="5ec76-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec76-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="5ec76-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ec76-124">System resource limit, could not perform the operation.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="5ec76-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ec76-125">Requirements</span></span>



| <span data-ttu-id="5ec76-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec76-126">Requirement</span></span> | <span data-ttu-id="5ec76-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5ec76-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec76-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ec76-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5ec76-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ec76-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ec76-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ec76-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5ec76-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ec76-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ec76-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ec76-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ec76-133"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec76-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ec76-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5ec76-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ec76-135"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ec76-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="5ec76-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5ec76-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ec76-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ec76-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="5ec76-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ec76-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec76-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="5ec76-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





