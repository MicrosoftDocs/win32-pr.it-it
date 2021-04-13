---
title: Metodo INapSystemHealthValidationRequest GetStringCorrelationId (NapSystemHealthValidator. h)
description: Viene usato da convalida integrità sistema (SHV) che devono registrare queste informazioni.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- NAP metodo GetStringCorrelationId
- Metodo GetStringCorrelationId NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 554a5a31f0aa46f6bcbd7a750662d47ab2c78040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519166"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a><span data-ttu-id="47733-106">Metodo INapSystemHealthValidationRequest:: GetStringCorrelationId</span><span class="sxs-lookup"><span data-stu-id="47733-106">INapSystemHealthValidationRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="47733-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="47733-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="47733-108">Il metodo **INapSystemHealthValidationRequest:: GetStringCorrelationId** viene usato da convalida integrità sistema (SHV) che devono registrare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="47733-108">The **INapSystemHealthValidationRequest::GetStringCorrelationId** method is used by System Health Validators (SHVs) which must log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="47733-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47733-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="47733-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="47733-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47733-111">ID correlazione  \[ out\]</span><span class="sxs-lookup"><span data-stu-id="47733-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47733-112">Puntatore a un puntatore a un [**StringCorrelationId**](nap-type-constants.md) univoco per lo scambio di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="47733-112">A pointer to a pointer to a unique [**StringCorrelationId**](nap-type-constants.md) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47733-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47733-113">Return value</span></span>

<span data-ttu-id="47733-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="47733-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="47733-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="47733-115">Return code</span></span>                                                                                     | <span data-ttu-id="47733-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47733-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="47733-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47733-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="47733-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="47733-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="47733-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="47733-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="47733-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="47733-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="47733-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="47733-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="47733-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="47733-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="47733-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47733-123">Requirements</span></span>



| <span data-ttu-id="47733-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="47733-124">Requirement</span></span> | <span data-ttu-id="47733-125">Valore</span><span class="sxs-lookup"><span data-stu-id="47733-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47733-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47733-126">Minimum supported client</span></span><br/> | <span data-ttu-id="47733-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="47733-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="47733-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47733-128">Minimum supported server</span></span><br/> | <span data-ttu-id="47733-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47733-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47733-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47733-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="47733-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="47733-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="47733-132">IDL</span><span class="sxs-lookup"><span data-stu-id="47733-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47733-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47733-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="47733-134">DLL</span><span class="sxs-lookup"><span data-stu-id="47733-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47733-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47733-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="47733-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47733-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47733-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="47733-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





