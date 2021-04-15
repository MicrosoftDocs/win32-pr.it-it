---
title: Metodo INapSystemHealthValidationRequest GetCorrelationId (NapSystemHealthValidator. h)
description: Viene usato da convalida integrità sistema (SHV) per recuperare l'ID di correlazione. Il servizio di convalida dell'integrità deve quindi registrare queste informazioni.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- NAP metodo GetCorrelationId
- Metodo GetCorrelationId NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476468"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a><span data-ttu-id="4192d-107">Metodo INapSystemHealthValidationRequest:: GetCorrelationId</span><span class="sxs-lookup"><span data-stu-id="4192d-107">INapSystemHealthValidationRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="4192d-108">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="4192d-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4192d-109">Il metodo **INapSystemHealthValidationRequest:: GetCorrelationId** viene usato da convalida integrità sistema (SHV) per recuperare l'ID di correlazione.</span><span class="sxs-lookup"><span data-stu-id="4192d-109">The **INapSystemHealthValidationRequest::GetCorrelationId** method is used by System Health Validators (SHVs) to retrieve the correlation ID.</span></span> <span data-ttu-id="4192d-110">Il servizio di convalida dell'integrità deve quindi registrare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="4192d-110">The SHV must then log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4192d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4192d-111">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="4192d-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="4192d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4192d-113">ID correlazione  \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4192d-113">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4192d-114">Puntatore a un [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) univoco per lo scambio di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="4192d-114">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4192d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4192d-115">Return value</span></span>

<span data-ttu-id="4192d-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="4192d-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4192d-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4192d-117">Return code</span></span>                                                                                     | <span data-ttu-id="4192d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4192d-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4192d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4192d-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4192d-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="4192d-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4192d-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4192d-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4192d-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="4192d-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4192d-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4192d-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4192d-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4192d-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4192d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4192d-125">Requirements</span></span>



| <span data-ttu-id="4192d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4192d-126">Requirement</span></span> | <span data-ttu-id="4192d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4192d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4192d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4192d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4192d-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4192d-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="4192d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4192d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4192d-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4192d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4192d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4192d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4192d-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="4192d-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="4192d-134">IDL</span><span class="sxs-lookup"><span data-stu-id="4192d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4192d-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4192d-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="4192d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4192d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4192d-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4192d-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="4192d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4192d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4192d-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="4192d-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





