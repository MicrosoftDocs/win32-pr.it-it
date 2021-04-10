---
title: Metodo INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator. h)
description: Consente ai validator di integrità del sistema (SHV) di recuperare e convalidare le informazioni SoHRequest inviate dalle relative controparti Agente integrità sistema nel client.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- NAP metodo GetSoHRequest
- Metodo GetSoHRequest NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121595"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a><span data-ttu-id="d89f6-106">Metodo INapSystemHealthValidationRequest:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="d89f6-106">INapSystemHealthValidationRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="d89f6-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="d89f6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d89f6-108">Il metodo **INapSystemHealthValidationRequest:: GetSoHRequest** consente ai validator di integrità del sistema (SHV) di recuperare e convalidare le informazioni [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) inviate dalle controparti dell'agente integrità sistema (SHA) sul client.</span><span class="sxs-lookup"><span data-stu-id="d89f6-108">The **INapSystemHealthValidationRequest::GetSoHRequest** method allows System Health Validators (SHVs) to retrieve and validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) information sent by their System Health Agent (SHA) counterparts on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89f6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d89f6-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a><span data-ttu-id="d89f6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d89f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d89f6-111">*sohRequest* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d89f6-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d89f6-112">Puntatore a un puntatore a una struttura [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="d89f6-112">A pointer to a pointer to an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d89f6-113">*napSystemGenerated* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d89f6-113">*napSystemGenerated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d89f6-114">**Bool** che è **true** se il rapporto di integrità è stato creato da NAPAGENT per conto dell'SHA e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d89f6-114">A **BOOL** that is **TRUE** if the SoH was created by the NapAgent on behalf of the SHA and **FALSE** otherwise.</span></span> <span data-ttu-id="d89f6-115">Viene utilizzato principalmente per indicare un errore SHA per il servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="d89f6-115">It is primarily used to indicate an SHA failure to the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d89f6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d89f6-116">Return value</span></span>

<span data-ttu-id="d89f6-117">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="d89f6-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d89f6-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d89f6-118">Return code</span></span>                                                                                     | <span data-ttu-id="d89f6-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d89f6-119">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d89f6-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d89f6-120"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d89f6-121">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="d89f6-121">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d89f6-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d89f6-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d89f6-123">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d89f6-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d89f6-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d89f6-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d89f6-125">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d89f6-125">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d89f6-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d89f6-126">Remarks</span></span>

<span data-ttu-id="d89f6-127">Il parametro *sohRequest* può restituire **null** se il client non ha inviato un [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) al servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="d89f6-127">The *sohRequest* parameter may return **NULL** if the client did not send an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the SHV.</span></span> <span data-ttu-id="d89f6-128">In questo scenario, il servizio di convalida dell'integrità di sistema può popolare un **SoHResponse** con il codice di errore [**NAP \_ E \_ Missing \_ SOH**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d89f6-128">In that scenario the SHV can populate an **SoHResponse** with the error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>

<span data-ttu-id="d89f6-129">Se il parametro *napSystemGenerated* è **true**, il formato di *SoHRequest* è il seguente:</span><span class="sxs-lookup"><span data-stu-id="d89f6-129">If the *napSystemGenerated* parameter is **TRUE**, the format of *SoHRequest* is as follows:</span></span>

-   <span data-ttu-id="d89f6-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="d89f6-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="d89f6-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="d89f6-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="d89f6-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<Sha-Failure-Error-Code>**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d89f6-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**<sha-failure-error-code>**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="d89f6-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d89f6-133">Requirements</span></span>



| <span data-ttu-id="d89f6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d89f6-134">Requirement</span></span> | <span data-ttu-id="d89f6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d89f6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d89f6-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d89f6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d89f6-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d89f6-137">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="d89f6-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d89f6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d89f6-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d89f6-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d89f6-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d89f6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d89f6-141"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="d89f6-141"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="d89f6-142">IDL</span><span class="sxs-lookup"><span data-stu-id="d89f6-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d89f6-143"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d89f6-143"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="d89f6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d89f6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d89f6-145"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d89f6-145"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="d89f6-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d89f6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89f6-147">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="d89f6-147">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





