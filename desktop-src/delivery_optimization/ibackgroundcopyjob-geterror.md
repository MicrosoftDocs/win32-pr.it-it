---
title: Metodo GetError metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera l'interfaccia di errore dopo che si è verificato un errore.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Metodo GetError
- Metodo GetError, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo getError
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400624"
---
# <a name="ibackgroundcopyjobgeterror-method"></a><span data-ttu-id="68702-106">Metodo metodo ibackgroundcopyjob:: GetError</span><span class="sxs-lookup"><span data-stu-id="68702-106">IBackgroundCopyJob::GetError method</span></span>

<span data-ttu-id="68702-107">Recupera l'interfaccia di errore dopo che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="68702-107">Retrieves the error interface after an error occurs.</span></span>

<span data-ttu-id="68702-108">L'ottimizzazione recapito genera un oggetto Error quando lo stato del processo è BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="68702-108">Delivery Optimization (DO) generates an error object when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="68702-109">Il servizio non crea un oggetto Error quando una chiamata a un metodo di interfaccia **IBackgroundCopyXXXX** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="68702-109">The service does not create an error object when a call to an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="68702-110">L'oggetto Error è disponibile fino a quando non inizia il trasferimento dei dati (lo stato del processo viene modificato in BG_JOB_STATE_TRANSFERRING) per il processo o fino alla chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68702-110">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="68702-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68702-111">Syntax</span></span>


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a><span data-ttu-id="68702-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="68702-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68702-113">*ppError* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="68702-113">*ppError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68702-114">Interfaccia di errore che fornisce il codice di errore, una descrizione dell'errore e il contesto in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="68702-114">Error interface that provides the error code, a description of the error, and the context in which the error occurred.</span></span> <span data-ttu-id="68702-115">Questo parametro identifica anche il file da trasferire nel momento in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="68702-115">This parameter also identifies the file being transferred at the time the error occurred.</span></span> <span data-ttu-id="68702-116">Rilasciare *ppError* al termine.</span><span class="sxs-lookup"><span data-stu-id="68702-116">Release *ppError* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68702-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68702-117">Return value</span></span>

<span data-ttu-id="68702-118">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="68702-118">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="68702-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="68702-119">Return code</span></span>                                                                                                           | <span data-ttu-id="68702-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68702-120">Description</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68702-121"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="68702-121"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                              | <span data-ttu-id="68702-122">Generazione dell'oggetto Error completata.</span><span class="sxs-lookup"><span data-stu-id="68702-122">Successfully generated the error object.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="68702-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="68702-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="68702-124">L'interfaccia di errore è disponibile solo dopo che si è verificato un errore (BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR) e prima che inizi il trasferimento dei dati (BG_JOB_STATE_TRANSFERRING).</span><span class="sxs-lookup"><span data-stu-id="68702-124">The error interface is available only after an error occurs (BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR) and before DO begins transferring data (BG_JOB_STATE_TRANSFERRING).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68702-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="68702-125">Remarks</span></span>

<span data-ttu-id="68702-126">Il processo viene inserito in uno stato di errore in presenza di errori irreversibili.</span><span class="sxs-lookup"><span data-stu-id="68702-126">The job is placed in an error state on fatal errors.</span></span> <span data-ttu-id="68702-127">Per determinare se il processo è in errore, utilizzare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="68702-127">Use one of the following options to determine if the job is in error:</span></span>

-   <span data-ttu-id="68702-128">Per eseguire il polling dello stato del processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="68702-128">To poll for the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="68702-129">Il processo è in errore se lo stato è BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="68702-129">The job is in error if the state is BG_JOB_STATE_ERROR.</span></span>
-   <span data-ttu-id="68702-130">Per ricevere una notifica quando si verifica un errore, implementare l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (in particolare il metodo [**JobError**](https://www.bing.com/search?q=**JobError**) ).</span><span class="sxs-lookup"><span data-stu-id="68702-130">To receive notification when an error occurs, implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (specifically, the [**JobError**](https://www.bing.com/search?q=**JobError**) method).</span></span> <span data-ttu-id="68702-131">Chiamare quindi il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) per registrare il callback e il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) per impostare il flag BG_NOTIFY_JOB_ERROR.</span><span class="sxs-lookup"><span data-stu-id="68702-131">Then, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to register the callback and the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to set the BG_NOTIFY_JOB_ERROR flag.</span></span>

<span data-ttu-id="68702-132">L'interfaccia [**IBackgroundCopyError**](ibackgroundcopyerror.md) contiene le informazioni utilizzate per determinare la motivo dell'errore e se il processo di trasferimento può proseguire.</span><span class="sxs-lookup"><span data-stu-id="68702-132">The [**IBackgroundCopyError**](ibackgroundcopyerror.md) interface contains information that you use to determine the cause of the error and if the transfer process can proceed.</span></span> <span data-ttu-id="68702-133">Dopo aver determinato la cause dell'errore, eseguire una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="68702-133">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="68702-134">Per annullare il processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="68702-134">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="68702-135">Per salvare i file che sono stati trasferiti correttamente prima dell'errore, chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="68702-135">To save those files that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span>
-   <span data-ttu-id="68702-136">Per completare l'elaborazione del processo, risolvere il problema e quindi chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="68702-136">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="68702-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68702-137">Requirements</span></span>



| <span data-ttu-id="68702-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="68702-138">Requirement</span></span> | <span data-ttu-id="68702-139">Valore</span><span class="sxs-lookup"><span data-stu-id="68702-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68702-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68702-140">Minimum supported client</span></span><br/> | <span data-ttu-id="68702-141">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="68702-141">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="68702-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68702-142">Minimum supported server</span></span><br/> | <span data-ttu-id="68702-143">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68702-143">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="68702-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68702-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="68702-145"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="68702-145"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="68702-146">IDL</span><span class="sxs-lookup"><span data-stu-id="68702-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68702-147"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68702-147"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="68702-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="68702-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="68702-149"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68702-149"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="68702-150">DLL</span><span class="sxs-lookup"><span data-stu-id="68702-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68702-151"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68702-151"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="68702-152">IID</span><span class="sxs-lookup"><span data-stu-id="68702-152">IID</span></span><br/>                      | <span data-ttu-id="68702-153">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="68702-153">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="68702-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68702-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68702-155">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="68702-155">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="68702-156">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="68702-156">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[<span data-ttu-id="68702-157">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="68702-157">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="68702-158">**Metodo ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="68702-158">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





