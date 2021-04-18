---
title: Metodo IBackgroundCopyManager GetJob (Deliveryoptimization. h)
description: Recupera un processo specificato dalla coda di trasferimento. In genere, l'applicazione salva in modo permanente l'identificatore del processo, quindi è possibile recuperare il processo dalla coda in un secondo momento.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Metodo GetJob
- Metodo GetJob, interfaccia IBackgroundCopyManager
- Interfaccia IBackgroundCopyManager, metodo GetJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301726"
---
# <a name="ibackgroundcopymanagergetjob-method"></a><span data-ttu-id="4da60-107">Metodo IBackgroundCopyManager:: GetJob</span><span class="sxs-lookup"><span data-stu-id="4da60-107">IBackgroundCopyManager::GetJob method</span></span>

<span data-ttu-id="4da60-108">Recupera un processo specificato dalla coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4da60-108">Retrieves a specified job from the transfer queue.</span></span> <span data-ttu-id="4da60-109">In genere, l'applicazione salva in modo permanente l'identificatore del processo, quindi è possibile recuperare il processo dalla coda in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="4da60-109">Typically, your application persists the job identifier, so you can later retrieve the job from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da60-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4da60-110">Syntax</span></span>


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="4da60-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4da60-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da60-112">*JobID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4da60-112">*JobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4da60-113">Identifica il processo da recuperare dalla coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4da60-113">Identifies the job to retrieve from the transfer queue.</span></span> <span data-ttu-id="4da60-114">Il metodo [**CreateJob**](ibackgroundcopymanager-createjob.md) restituisce l'identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="4da60-114">The [**CreateJob**](ibackgroundcopymanager-createjob.md) method returns the job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4da60-115">*ppJob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4da60-115">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4da60-116">Puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md) per il processo specificato da *JobID*.</span><span class="sxs-lookup"><span data-stu-id="4da60-116">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer to the job specified by *JobID*.</span></span> <span data-ttu-id="4da60-117">Al termine, rilasciare *ppJob*.</span><span class="sxs-lookup"><span data-stu-id="4da60-117">When done, release *ppJob*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da60-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4da60-118">Return value</span></span>

<span data-ttu-id="4da60-119">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="4da60-119">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="4da60-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4da60-120">Return code</span></span>                                                                                      | <span data-ttu-id="4da60-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4da60-121">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4da60-122"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="4da60-122"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>         | <span data-ttu-id="4da60-123">Il processo è stato recuperato dalla coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4da60-123">Job was successfully retrieved from the transfer queue.</span></span><br/> |
| <dl> <span data-ttu-id="4da60-124"><dt>**DO_E_NOT_FOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="4da60-124"><dt>**DO_E_NOT_FOUND**</dt></span></span> </dl> | <span data-ttu-id="4da60-125">Il processo non è stato trovato nella coda.</span><span class="sxs-lookup"><span data-stu-id="4da60-125">The job was not found in the queue.</span></span><br/>                     |
| <dl> <span data-ttu-id="4da60-126"><dt>**E_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4da60-126"><dt>**E_ACCESSDENIED**</dt></span></span> </dl>   | <span data-ttu-id="4da60-127">L'utente non dispone delle autorizzazioni necessarie per recuperare il processo.</span><span class="sxs-lookup"><span data-stu-id="4da60-127">User does not have permission to retrieve the job.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="4da60-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4da60-128">Requirements</span></span>



| <span data-ttu-id="4da60-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da60-129">Requirement</span></span> | <span data-ttu-id="4da60-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4da60-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da60-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4da60-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4da60-132">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="4da60-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4da60-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4da60-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4da60-134">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4da60-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4da60-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4da60-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da60-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da60-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4da60-137">IDL</span><span class="sxs-lookup"><span data-stu-id="4da60-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4da60-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4da60-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4da60-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="4da60-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="4da60-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4da60-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4da60-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4da60-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4da60-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4da60-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4da60-143">IID</span><span class="sxs-lookup"><span data-stu-id="4da60-143">IID</span></span><br/>                      | <span data-ttu-id="4da60-144">IID_IBackgroundCopyManager viene definito come 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="4da60-144">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4da60-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4da60-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da60-146">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="4da60-146">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="4da60-147">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="4da60-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="4da60-148">**Metodo ibackgroundcopyjob:: GetId**</span><span class="sxs-lookup"><span data-stu-id="4da60-148">**IBackgroundCopyJob::GetId**</span></span>](ibackgroundcopyjob-getid.md)
</dt> <dt>

[<span data-ttu-id="4da60-149">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="4da60-149">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





