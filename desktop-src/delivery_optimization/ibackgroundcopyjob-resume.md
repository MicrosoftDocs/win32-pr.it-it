---
title: Metodo Resume Metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Attiva un nuovo processo o riavvia un processo sospeso.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Metodo Resume
- Metodo Resume, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo Resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119347"
---
# <a name="ibackgroundcopyjobresume-method"></a><span data-ttu-id="20d15-106">Metodo metodo ibackgroundcopyjob:: Resume</span><span class="sxs-lookup"><span data-stu-id="20d15-106">IBackgroundCopyJob::Resume method</span></span>

<span data-ttu-id="20d15-107">Attiva un nuovo processo o riavvia un processo sospeso.</span><span class="sxs-lookup"><span data-stu-id="20d15-107">Activates a new job or restarts a job that has been suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d15-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20d15-108">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="20d15-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="20d15-109">Parameters</span></span>

<span data-ttu-id="20d15-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="20d15-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20d15-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20d15-111">Return value</span></span>

<span data-ttu-id="20d15-112">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="20d15-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="20d15-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="20d15-113">Return code</span></span>                                                                                          | <span data-ttu-id="20d15-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20d15-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20d15-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="20d15-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="20d15-116">Il processo è stato riavviato.</span><span class="sxs-lookup"><span data-stu-id="20d15-116">Job was successfully restarted.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="20d15-117"><dt>**DO_E_EMPTY**</dt></span><span class="sxs-lookup"><span data-stu-id="20d15-117"><dt>**DO_E_EMPTY**</dt></span></span> </dl>          | <span data-ttu-id="20d15-118">Nessun file da trasferire.</span><span class="sxs-lookup"><span data-stu-id="20d15-118">There are no files to transfer.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="20d15-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="20d15-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="20d15-120">Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="20d15-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20d15-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="20d15-121">Remarks</span></span>

<span data-ttu-id="20d15-122">Quando si crea un processo, il processo viene inizialmente sospeso.</span><span class="sxs-lookup"><span data-stu-id="20d15-122">When you create a job, the job is initially suspended.</span></span> <span data-ttu-id="20d15-123">La chiamata di **Resume** sposta il processo nello stato trasferendo.</span><span class="sxs-lookup"><span data-stu-id="20d15-123">Calling **Resume** moves the job to the Transferring state.</span></span> <span data-ttu-id="20d15-124">Si noti che il processo deve contenere uno o più file prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="20d15-124">Note that the job must contain one or more files before calling this method.</span></span>

<span data-ttu-id="20d15-125">Se un processo che si trova nello stato BG_JOB_STATE_TRANSIENT_ERROR o BG_JOB_STATE_ERROR, chiamare il metodo **Resume** per riavviare il processo dopo aver risolto l'errore.</span><span class="sxs-lookup"><span data-stu-id="20d15-125">If a job that is in the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state, call the **Resume** method to restart the job after you fix the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="20d15-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20d15-126">Requirements</span></span>



| <span data-ttu-id="20d15-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d15-127">Requirement</span></span> | <span data-ttu-id="20d15-128">Valore</span><span class="sxs-lookup"><span data-stu-id="20d15-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d15-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20d15-129">Minimum supported client</span></span><br/> | <span data-ttu-id="20d15-130">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="20d15-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="20d15-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20d15-131">Minimum supported server</span></span><br/> | <span data-ttu-id="20d15-132">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="20d15-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="20d15-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20d15-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="20d15-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="20d15-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="20d15-135">IDL</span><span class="sxs-lookup"><span data-stu-id="20d15-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20d15-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20d15-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="20d15-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="20d15-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="20d15-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20d15-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="20d15-139">DLL</span><span class="sxs-lookup"><span data-stu-id="20d15-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20d15-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20d15-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="20d15-141">IID</span><span class="sxs-lookup"><span data-stu-id="20d15-141">IID</span></span><br/>                      | <span data-ttu-id="20d15-142">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="20d15-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="20d15-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20d15-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d15-144">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="20d15-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="20d15-145">**Metodo ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="20d15-145">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="20d15-146">**Metodo ibackgroundcopyjob:: Suspend**</span><span class="sxs-lookup"><span data-stu-id="20d15-146">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





