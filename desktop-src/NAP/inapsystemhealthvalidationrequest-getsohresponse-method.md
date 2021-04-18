---
title: Metodo INapSystemHealthValidationRequest GetSoHResponse (NapSystemHealthValidator. h)
description: Recupera SoHResponse.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- NAP metodo GetSoHResponse
- Metodo GetSoHResponse NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302502"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a><span data-ttu-id="19df8-106">Metodo INapSystemHealthValidationRequest:: GetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="19df8-106">INapSystemHealthValidationRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="19df8-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="19df8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19df8-108">Il metodo **INapSystemHealthValidationRequest:: GetSoHResponse** Recupera il [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="19df8-108">The **INapSystemHealthValidationRequest::GetSoHResponse** method retrieves the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="19df8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19df8-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="19df8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="19df8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19df8-111">*sohResponse* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19df8-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19df8-112">Puntatore a un puntatore al [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)ricevuto.</span><span class="sxs-lookup"><span data-stu-id="19df8-112">A pointer to a pointer to the received [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19df8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19df8-113">Return value</span></span>

<span data-ttu-id="19df8-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="19df8-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="19df8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="19df8-115">Return code</span></span>                                                                                     | <span data-ttu-id="19df8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19df8-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="19df8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19df8-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="19df8-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="19df8-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="19df8-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="19df8-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="19df8-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="19df8-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="19df8-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="19df8-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="19df8-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="19df8-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19df8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19df8-123">Requirements</span></span>



| <span data-ttu-id="19df8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="19df8-124">Requirement</span></span> | <span data-ttu-id="19df8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="19df8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19df8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19df8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="19df8-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="19df8-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="19df8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19df8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="19df8-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19df8-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19df8-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19df8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="19df8-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="19df8-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="19df8-132">IDL</span><span class="sxs-lookup"><span data-stu-id="19df8-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19df8-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19df8-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="19df8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="19df8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19df8-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19df8-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="19df8-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19df8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19df8-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="19df8-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





