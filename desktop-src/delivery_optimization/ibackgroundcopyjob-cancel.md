---
title: Metodo Cancel metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Elimina il processo dalla coda di trasferimento e rimuove i file temporanei correlati dal client (download) e dal server (caricamenti).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Metodo Cancel
- Metodo Cancel, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo Cancel
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873685"
---
# <a name="ibackgroundcopyjobcancel-method"></a><span data-ttu-id="0921e-106">Metodo metodo ibackgroundcopyjob:: Cancel</span><span class="sxs-lookup"><span data-stu-id="0921e-106">IBackgroundCopyJob::Cancel method</span></span>

<span data-ttu-id="0921e-107">Elimina il processo dalla coda di trasferimento e rimuove i file temporanei correlati dal client (download) e dal server (caricamenti).</span><span class="sxs-lookup"><span data-stu-id="0921e-107">Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).</span></span>

## <a name="syntax"></a><span data-ttu-id="0921e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0921e-108">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="0921e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0921e-109">Parameters</span></span>

<span data-ttu-id="0921e-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0921e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0921e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0921e-111">Return value</span></span>

<span data-ttu-id="0921e-112">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="0921e-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="0921e-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0921e-113">Return code</span></span>                                                                                          | <span data-ttu-id="0921e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0921e-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0921e-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="0921e-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="0921e-116">Il processo è stato annullato.</span><span class="sxs-lookup"><span data-stu-id="0921e-116">Job was successfully canceled.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="0921e-117"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="0921e-117"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="0921e-118">Non è possibile annullare un processo il cui stato è BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="0921e-118">Cannot cancel a job whose state is BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0921e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0921e-119">Remarks</span></span>

<span data-ttu-id="0921e-120">È possibile annullare un processo in qualsiasi momento; Tuttavia, non è possibile recuperare il processo dopo che è stato annullato.</span><span class="sxs-lookup"><span data-stu-id="0921e-120">You can cancel a job at any time; however, the job cannot be recovered after it is canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="0921e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0921e-121">Requirements</span></span>



| <span data-ttu-id="0921e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0921e-122">Requirement</span></span> | <span data-ttu-id="0921e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0921e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0921e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0921e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0921e-125">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0921e-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0921e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0921e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0921e-127">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0921e-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0921e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0921e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0921e-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0921e-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0921e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="0921e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0921e-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0921e-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0921e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="0921e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0921e-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0921e-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0921e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0921e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0921e-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0921e-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0921e-136">IID</span><span class="sxs-lookup"><span data-stu-id="0921e-136">IID</span></span><br/>                      | <span data-ttu-id="0921e-137">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="0921e-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0921e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0921e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0921e-139">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="0921e-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="0921e-140">**Metodo ibackgroundcopyjob:: complete**</span><span class="sxs-lookup"><span data-stu-id="0921e-140">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="0921e-141">**Metodo ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="0921e-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> <dt>

[<span data-ttu-id="0921e-142">**Metodo ibackgroundcopyjob:: Suspend**</span><span class="sxs-lookup"><span data-stu-id="0921e-142">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





