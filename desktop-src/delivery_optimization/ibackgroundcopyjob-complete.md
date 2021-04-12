---
title: Metodo Complete metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Termina il processo e salva i file trasferiti nel client.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Metodo complete
- Metodo complete, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo complete
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119755"
---
# <a name="ibackgroundcopyjobcomplete-method"></a><span data-ttu-id="a2327-106">Metodo metodo ibackgroundcopyjob:: complete</span><span class="sxs-lookup"><span data-stu-id="a2327-106">IBackgroundCopyJob::Complete method</span></span>

<span data-ttu-id="a2327-107">Termina il processo e salva i file trasferiti nel client.</span><span class="sxs-lookup"><span data-stu-id="a2327-107">Ends the job and saves the transferred files on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2327-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2327-108">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="a2327-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2327-109">Parameters</span></span>

<span data-ttu-id="a2327-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a2327-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2327-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2327-111">Return value</span></span>

<span data-ttu-id="a2327-112">Questo metodo restituisce i valori **HRESULT** seguenti.</span><span class="sxs-lookup"><span data-stu-id="a2327-112">This method returns the following **HRESULT** values.</span></span> <span data-ttu-id="a2327-113">Il metodo può inoltre restituire errori correlati alla ridenominazione delle copie temporanee dei file trasferiti nei nomi specificati.</span><span class="sxs-lookup"><span data-stu-id="a2327-113">The method can also return errors related to renaming the temporary copies of the transferred files to their given names.</span></span>



| <span data-ttu-id="a2327-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a2327-114">Return code</span></span>                                                                                          | <span data-ttu-id="a2327-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2327-115">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2327-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a2327-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="a2327-117">Tutti i file sono stati trasferiti.</span><span class="sxs-lookup"><span data-stu-id="a2327-117">All files transferred successfully.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="a2327-118"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="a2327-118"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="a2327-119">Per i download, lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="a2327-119">For downloads, the state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span> <br/> <span data-ttu-id="a2327-120">Per i caricamenti, lo stato del processo deve essere BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="a2327-120">For uploads, the state of the job must be BG_JOB_STATE_TRANSFERRED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2327-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2327-121">Remarks</span></span>

<span data-ttu-id="a2327-122">Tutti i file sono stati trasferiti se lo stato del processo è **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="a2327-122">All of the files have been successfully transferred if the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span> <span data-ttu-id="a2327-123">Per controllare lo stato del processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="a2327-123">To check the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="a2327-124">È anche possibile implementare l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) per ricevere una notifica quando tutti i file sono stati trasferiti al client.</span><span class="sxs-lookup"><span data-stu-id="a2327-124">You can also implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to receive notification when all of the files have been transferred to the client.</span></span>

<span data-ttu-id="a2327-125">Mantiene i processi che sono solo di meno di 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="a2327-125">DO retains jobs that are less than 30 days only.</span></span> <span data-ttu-id="a2327-126">Tutti i processi meno recenti verranno rimossi.</span><span class="sxs-lookup"><span data-stu-id="a2327-126">All older jobs will be removed.</span></span> <span data-ttu-id="a2327-127">DO non supporta il Criteri di gruppo [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) .</span><span class="sxs-lookup"><span data-stu-id="a2327-127">DO does not support the [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) Group Policy.</span></span>

<span data-ttu-id="a2327-128">Per i processi di download, è possibile chiamare il metodo **completo** in qualsiasi momento durante il processo di trasferimento. Tuttavia, vengono salvati solo i file che sono stati trasferiti correttamente al client prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="a2327-128">For download jobs, you can call the **Complete** method at anytime during the transfer process; however, only files that were successfully transferred to the client before calling this method are saved.</span></span> <span data-ttu-id="a2327-129">Se, ad esempio, si chiama il metodo **complete** mentre si elabora il terzo di cinque file, vengono salvati solo i primi due file.</span><span class="sxs-lookup"><span data-stu-id="a2327-129">For example, if you call the **Complete** method while DO is processing the third of five files, only the first two files are saved.</span></span> <span data-ttu-id="a2327-130">Per determinare quali file sono stati trasferiti, chiamare il metodo [**IBackgroundCopyFile:: getProgress**](ibackgroundcopyfile-getprogress-method.md) e confrontare il membro **byte trasferiti** con il membro **bytesTotal** della struttura [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="a2327-130">To determine which files have been transferred, call the [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) method and compare the **BytesTransferred** member to the **BytesTotal** member of the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

<span data-ttu-id="a2327-131">Per i processi di caricamento, è possibile chiamare il metodo **complete** solo quando lo stato del processo è **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="a2327-131">For upload jobs, you can call the **Complete** method only when the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span>

<span data-ttu-id="a2327-132">Il proprietario del file è l'utente che ha effettuato la chiamata.</span><span class="sxs-lookup"><span data-stu-id="a2327-132">The owner of the file is the user who made the call.</span></span> <span data-ttu-id="a2327-133">Se, ad esempio, un amministratore completa il processo di un altro utente, l'amministratore non è proprietario del processo.</span><span class="sxs-lookup"><span data-stu-id="a2327-133">For example, if an administrator completes someone else's job, the administrator not the owner of the job owns the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2327-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2327-134">Requirements</span></span>



| <span data-ttu-id="a2327-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2327-135">Requirement</span></span> | <span data-ttu-id="a2327-136">Valore</span><span class="sxs-lookup"><span data-stu-id="a2327-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2327-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2327-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a2327-138">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2327-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2327-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2327-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a2327-140">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2327-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a2327-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2327-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2327-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2327-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2327-143">IDL</span><span class="sxs-lookup"><span data-stu-id="a2327-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2327-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2327-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a2327-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="a2327-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2327-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2327-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a2327-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a2327-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2327-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2327-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a2327-149">IID</span><span class="sxs-lookup"><span data-stu-id="a2327-149">IID</span></span><br/>                      | <span data-ttu-id="a2327-150">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="a2327-150">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a2327-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2327-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2327-152">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="a2327-152">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a2327-153">**Metodo ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="a2327-153">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="a2327-154">**Metodo ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="a2327-154">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





