---
title: Metodo INapSystemHealthValidationRequest SetSoHResponse (NapSystemHealthValidator. h)
description: Consente la convalida dell'integrità di sistema (SHV) per impostare il SoHResponse da inviare alla rispettiva controparte Agente integrità sistema (SHA) sul lato client.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- NAP metodo SetSoHResponse
- Metodo SetSoHResponse NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo SetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400822"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a><span data-ttu-id="8672c-106">Metodo INapSystemHealthValidationRequest:: SetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="8672c-106">INapSystemHealthValidationRequest::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="8672c-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8672c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8672c-108">Il metodo **INapSystemHealthValidationRequest:: SetSoHResponse** consente ai validator di integrità del sistema (SHV) di impostare il [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) da inviare alla rispettiva controparte dell'agente integrità sistema (SHA) sul lato client.</span><span class="sxs-lookup"><span data-stu-id="8672c-108">The **INapSystemHealthValidationRequest::SetSoHResponse** method allows System Health Validators (SHVs) to set the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) to be sent to its System Health Agent (SHA) counterpart on the client-side.</span></span>

## <a name="syntax"></a><span data-ttu-id="8672c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8672c-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="8672c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8672c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8672c-111">*sohResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8672c-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8672c-112">Puntatore a una struttura [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="8672c-112">A pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8672c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8672c-113">Return value</span></span>

<span data-ttu-id="8672c-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="8672c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8672c-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8672c-115">Return code</span></span>                                                                                     | <span data-ttu-id="8672c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8672c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8672c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8672c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8672c-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="8672c-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8672c-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8672c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8672c-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="8672c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8672c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8672c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8672c-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8672c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8672c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8672c-123">Requirements</span></span>



| <span data-ttu-id="8672c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8672c-124">Requirement</span></span> | <span data-ttu-id="8672c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8672c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8672c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8672c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8672c-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8672c-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="8672c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8672c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8672c-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8672c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8672c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8672c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8672c-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="8672c-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="8672c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="8672c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8672c-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8672c-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="8672c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8672c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8672c-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8672c-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="8672c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8672c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8672c-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="8672c-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





