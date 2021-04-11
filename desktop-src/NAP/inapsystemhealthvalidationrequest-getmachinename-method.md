---
title: Metodo GetMachineName INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: Viene utilizzato da convalida integrità sistema (SHV) per recuperare il nome del computer del client di protezione accesso alla rete. Il servizio di convalida dell'integrità registra quindi queste informazioni.
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- Metodo GetMachineName NAP
- Metodo GetMachineName NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetMachineName
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121655"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a><span data-ttu-id="f1fd9-107">Metodo INapSystemHealthValidationRequest:: GetMachineName</span><span class="sxs-lookup"><span data-stu-id="f1fd9-107">INapSystemHealthValidationRequest::GetMachineName method</span></span>

> [!Note]  
> <span data-ttu-id="f1fd9-108">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="f1fd9-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f1fd9-109">Il metodo **INapSystemHealthValidationRequest:: GetMachineName** viene usato da convalida integrità sistema (SHV) per recuperare il nome del computer del client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-109">The **INapSystemHealthValidationRequest::GetMachineName** method is used by System Health Validators (SHVs) to retrieve the machine name of the NAP client.</span></span> <span data-ttu-id="f1fd9-110">Il servizio di convalida dell'integrità registra quindi queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-110">The SHV then logs this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fd9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1fd9-111">Syntax</span></span>


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a><span data-ttu-id="f1fd9-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1fd9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1fd9-113">*nomecomputer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f1fd9-113">*machineName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1fd9-114">Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente il nome del computer del client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1fd9-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1fd9-115">Return value</span></span>

<span data-ttu-id="f1fd9-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f1fd9-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f1fd9-117">Return code</span></span>                                                                                     | <span data-ttu-id="f1fd9-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1fd9-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1fd9-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd9-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f1fd9-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f1fd9-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd9-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f1fd9-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f1fd9-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd9-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f1fd9-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f1fd9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1fd9-125">Requirements</span></span>



| <span data-ttu-id="f1fd9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1fd9-126">Requirement</span></span> | <span data-ttu-id="f1fd9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f1fd9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fd9-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1fd9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f1fd9-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f1fd9-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="f1fd9-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1fd9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f1fd9-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1fd9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1fd9-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1fd9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1fd9-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd9-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1fd9-134">IDL</span><span class="sxs-lookup"><span data-stu-id="f1fd9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1fd9-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd9-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="f1fd9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f1fd9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1fd9-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd9-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="f1fd9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1fd9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1fd9-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="f1fd9-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





