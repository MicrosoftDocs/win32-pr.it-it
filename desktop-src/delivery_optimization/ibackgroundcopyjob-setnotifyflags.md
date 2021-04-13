---
title: Metodo metodo ibackgroundcopyjob SetNotifyFlags (Deliveryoptimization. h)
description: Specifica il tipo di notifica degli eventi che si desidera ricevere, ad esempio gli eventi trasferiti dal processo.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Metodo SetNotifyFlags
- Metodo SetNotifyFlags, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo SetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea754eeafca8f0efdcad5545cfc3a462c8b508cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517848"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a><span data-ttu-id="5354a-106">Metodo metodo ibackgroundcopyjob:: SetNotifyFlags</span><span class="sxs-lookup"><span data-stu-id="5354a-106">IBackgroundCopyJob::SetNotifyFlags method</span></span>

<span data-ttu-id="5354a-107">Specifica il tipo di notifica degli eventi che si desidera ricevere, ad esempio gli eventi trasferiti dal processo.</span><span class="sxs-lookup"><span data-stu-id="5354a-107">Specifies the type of event notification you want to receive, such as job transferred events.</span></span>

## <a name="syntax"></a><span data-ttu-id="5354a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5354a-108">Syntax</span></span>


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5354a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5354a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5354a-110">*NotifyFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5354a-110">*NotifyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5354a-111">Impostare uno o più dei flag seguenti per identificare gli eventi che si desidera ricevere.</span><span class="sxs-lookup"><span data-stu-id="5354a-111">Set one or more of the following flags to identify the events that you want to receive.</span></span>



| <span data-ttu-id="5354a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5354a-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="5354a-113">Significato</span><span class="sxs-lookup"><span data-stu-id="5354a-113">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="5354a-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="5354a-115">Tutti i file del processo sono stati trasferiti.</span><span class="sxs-lookup"><span data-stu-id="5354a-115">All of the files in the job have been transferred.</span></span><br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="5354a-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span></span> </dl>                                            | <span data-ttu-id="5354a-117">un errore.</span><span class="sxs-lookup"><span data-stu-id="5354a-117">An error has occurred.</span></span><br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="5354a-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span></span> </dl>                                                   | <span data-ttu-id="5354a-119">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5354a-119">Not supported.</span></span><br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="5354a-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span></span> </dl>                       | <span data-ttu-id="5354a-121">Il processo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="5354a-121">The job has been modified.</span></span> <span data-ttu-id="5354a-122">Il valore di una proprietà, ad esempio, è stato modificato, lo stato del processo è stato modificato o lo stato di avanzamento viene effettuato trasferendo i file.</span><span class="sxs-lookup"><span data-stu-id="5354a-122">For example, a property value changed, the state of the job changed, or progress is made transferring the files.</span></span> <span data-ttu-id="5354a-123">Questo flag viene ignorato se viene specificata la notifica della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5354a-123">This flag is ignored if command line notification is specified.</span></span><br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <span data-ttu-id="5354a-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span></span> </dl>                       | <span data-ttu-id="5354a-125">Un file nel processo è stato trasferito.</span><span class="sxs-lookup"><span data-stu-id="5354a-125">A file in the job has been transferred.</span></span> <span data-ttu-id="5354a-126">Questo flag viene ignorato se viene specificata la notifica della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5354a-126">This flag is ignored if command line notification is specified.</span></span><br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <span data-ttu-id="5354a-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="5354a-128">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5354a-128">Not supported.</span></span><br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5354a-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5354a-129">Return value</span></span>

<span data-ttu-id="5354a-130">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="5354a-130">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="5354a-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5354a-131">Return code</span></span>                                                                                          | <span data-ttu-id="5354a-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5354a-132">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5354a-133"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-133"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="5354a-134">Il tipo di notifica degli eventi è stato impostato correttamente.</span><span class="sxs-lookup"><span data-stu-id="5354a-134">Type of event notification was successfully set.</span></span><br/>                                          |
| <dl> <span data-ttu-id="5354a-135"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-135"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="5354a-136">Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="5354a-136">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5354a-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="5354a-137">Remarks</span></span>

<span data-ttu-id="5354a-138">Usare il metodo **SetNotifyFlags** insieme a [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span><span class="sxs-lookup"><span data-stu-id="5354a-138">Use the **SetNotifyFlags** method in conjunction with the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5354a-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5354a-139">Requirements</span></span>



| <span data-ttu-id="5354a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5354a-140">Requirement</span></span> | <span data-ttu-id="5354a-141">Valore</span><span class="sxs-lookup"><span data-stu-id="5354a-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5354a-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5354a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5354a-143">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="5354a-143">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5354a-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5354a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5354a-145">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5354a-145">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5354a-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5354a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5354a-147"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-147"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5354a-148">IDL</span><span class="sxs-lookup"><span data-stu-id="5354a-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5354a-149"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-149"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5354a-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="5354a-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="5354a-151"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-151"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5354a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5354a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5354a-153"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5354a-153"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5354a-154">IID</span><span class="sxs-lookup"><span data-stu-id="5354a-154">IID</span></span><br/>                      | <span data-ttu-id="5354a-155">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="5354a-155">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5354a-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5354a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5354a-157">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="5354a-157">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="5354a-158">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="5354a-158">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="5354a-159">**Metodo ibackgroundcopyjob:: GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="5354a-159">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="5354a-160">**Metodo ibackgroundcopyjob:: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="5354a-160">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





