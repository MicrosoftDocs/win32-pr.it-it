---
title: Metodo metodo ibackgroundcopyjob GetNotifyFlags (Deliveryoptimization. h)
description: Recupera i flag di notifica degli eventi per il processo.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Metodo GetNotifyFlags
- Metodo GetNotifyFlags, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e104857725849dfeb899b449ea055bc3cdb046bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340673"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a><span data-ttu-id="98cf0-106">Metodo metodo ibackgroundcopyjob:: GetNotifyFlags</span><span class="sxs-lookup"><span data-stu-id="98cf0-106">IBackgroundCopyJob::GetNotifyFlags method</span></span>

<span data-ttu-id="98cf0-107">Recupera i flag di notifica degli eventi per il processo.</span><span class="sxs-lookup"><span data-stu-id="98cf0-107">Retrieves the event notification flags for the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="98cf0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98cf0-108">Syntax</span></span>


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="98cf0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="98cf0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98cf0-110">*pNotifyFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="98cf0-110">*pNotifyFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98cf0-111">Identifica gli eventi ricevuti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="98cf0-111">Identifies the events that your application receives.</span></span> <span data-ttu-id="98cf0-112">Nella tabella seguente sono elencati i valori dei flag di notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="98cf0-112">The following table lists the event notification flag values.</span></span>



| <span data-ttu-id="98cf0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="98cf0-113">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="98cf0-114">Significato</span><span class="sxs-lookup"><span data-stu-id="98cf0-114">Meaning</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="98cf0-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span></span> </dl>    | <span data-ttu-id="98cf0-116">Tutti i file del processo sono stati trasferiti.</span><span class="sxs-lookup"><span data-stu-id="98cf0-116">All of the files in the job have been transferred.</span></span><br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="98cf0-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span></span> </dl>                      | <span data-ttu-id="98cf0-118">un errore.</span><span class="sxs-lookup"><span data-stu-id="98cf0-118">An error has occurred.</span></span><br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="98cf0-119"><dt>**BG_NOTIFY_DISABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-119"><dt>**BG_NOTIFY_DISABLE**</dt></span></span> </dl>                             | <span data-ttu-id="98cf0-120">La notifica degli eventi è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="98cf0-120">Event notification is disabled.</span></span> <span data-ttu-id="98cf0-121">Se impostato, ignora gli altri flag.</span><span class="sxs-lookup"><span data-stu-id="98cf0-121">If set, DO ignores the other flags.</span></span><br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="98cf0-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span></span> </dl> | <span data-ttu-id="98cf0-123">Il processo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="98cf0-123">The job has been modified.</span></span><br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98cf0-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98cf0-124">Return value</span></span>

<span data-ttu-id="98cf0-125">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="98cf0-125">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="98cf0-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="98cf0-126">Return code</span></span>                                                                              | <span data-ttu-id="98cf0-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98cf0-127">Description</span></span>                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="98cf0-128"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-128"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="98cf0-129">I flag di notifica degli eventi sono stati recuperati correttamente.</span><span class="sxs-lookup"><span data-stu-id="98cf0-129">Event notify flags were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98cf0-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98cf0-130">Requirements</span></span>



| <span data-ttu-id="98cf0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="98cf0-131">Requirement</span></span> | <span data-ttu-id="98cf0-132">Valore</span><span class="sxs-lookup"><span data-stu-id="98cf0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98cf0-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98cf0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="98cf0-134">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="98cf0-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="98cf0-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98cf0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="98cf0-136">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98cf0-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="98cf0-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98cf0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="98cf0-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="98cf0-139">IDL</span><span class="sxs-lookup"><span data-stu-id="98cf0-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98cf0-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="98cf0-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="98cf0-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="98cf0-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="98cf0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="98cf0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98cf0-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98cf0-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="98cf0-145">IID</span><span class="sxs-lookup"><span data-stu-id="98cf0-145">IID</span></span><br/>                      | <span data-ttu-id="98cf0-146">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="98cf0-146">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="98cf0-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98cf0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98cf0-148">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="98cf0-148">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="98cf0-149">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="98cf0-149">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="98cf0-150">**Metodo ibackgroundcopyjob:: GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="98cf0-150">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="98cf0-151">**Metodo ibackgroundcopyjob:: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="98cf0-151">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





