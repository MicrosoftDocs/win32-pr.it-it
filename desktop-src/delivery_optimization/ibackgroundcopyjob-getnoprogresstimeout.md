---
title: Metodo metodo ibackgroundcopyjob GetNoProgressTimeout (Deliveryoptimization. h)
description: Recupera il periodo di tempo durante il quale il servizio tenta di trasferire il file dopo che si è verificata una condizione di errore temporaneo. Se è presente lo stato di avanzamento, il timer viene reimpostato.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Metodo GetNoProgressTimeout
- Metodo GetNoProgressTimeout, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477033"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a><span data-ttu-id="3ea89-107">Metodo metodo ibackgroundcopyjob:: GetNoProgressTimeout</span><span class="sxs-lookup"><span data-stu-id="3ea89-107">IBackgroundCopyJob::GetNoProgressTimeout method</span></span>

<span data-ttu-id="3ea89-108">Recupera il periodo di tempo durante il quale il servizio tenta di trasferire il file dopo che si è verificata una condizione di errore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="3ea89-108">Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="3ea89-109">Se è presente lo stato di avanzamento, il timer viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="3ea89-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ea89-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ea89-110">Syntax</span></span>


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3ea89-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ea89-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ea89-112">*pRetryPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ea89-112">*pRetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea89-113">Periodo di tempo, espresso in secondi, durante il quale il servizio tenta di trasferire il file dopo che si è verificato un errore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="3ea89-113">Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ea89-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ea89-114">Return value</span></span>

<span data-ttu-id="3ea89-115">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="3ea89-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="3ea89-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3ea89-116">Return code</span></span>                                                                              | <span data-ttu-id="3ea89-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ea89-117">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="3ea89-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="3ea89-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="3ea89-119">Timeout recuperato.</span><span class="sxs-lookup"><span data-stu-id="3ea89-119">Time-out was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ea89-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ea89-120">Requirements</span></span>



| <span data-ttu-id="3ea89-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ea89-121">Requirement</span></span> | <span data-ttu-id="3ea89-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3ea89-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea89-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ea89-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea89-124">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ea89-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3ea89-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ea89-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea89-126">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ea89-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3ea89-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ea89-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ea89-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ea89-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ea89-129">IDL</span><span class="sxs-lookup"><span data-stu-id="3ea89-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ea89-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ea89-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ea89-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ea89-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ea89-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ea89-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3ea89-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3ea89-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ea89-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ea89-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3ea89-135">IID</span><span class="sxs-lookup"><span data-stu-id="3ea89-135">IID</span></span><br/>                      | <span data-ttu-id="3ea89-136">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="3ea89-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3ea89-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ea89-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ea89-138">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="3ea89-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="3ea89-139">**Metodo ibackgroundcopyjob:: SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="3ea89-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span></span>](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





