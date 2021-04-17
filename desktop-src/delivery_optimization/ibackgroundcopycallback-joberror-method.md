---
title: Metodo IBackgroundCopyCallback JobError (Deliveryoptimization. h)
description: Ottimizzazione recapito chiama l'implementazione del metodo JobError quando lo stato del processo viene modificato in BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Metodo JobError
- Metodo JobError, interfaccia IBackgroundCopyCallback
- Interfaccia IBackgroundCopyCallback, metodo JobError
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400553"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a><span data-ttu-id="aa07e-106">Metodo IBackgroundCopyCallback:: JobError</span><span class="sxs-lookup"><span data-stu-id="aa07e-106">IBackgroundCopyCallback::JobError method</span></span>

<span data-ttu-id="aa07e-107">Ottimizzazione recapito chiama l'implementazione del metodo [**JobError**](https://www.bing.com/search?q=**JobError**) quando lo stato del processo viene modificato in BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="aa07e-107">Delivery Optimization (DO) calls your implementation of the [**JobError**](https://www.bing.com/search?q=**JobError**) method when the state of the job changes to BG_JOB_STATE_ERROR.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa07e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa07e-108">Syntax</span></span>


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a><span data-ttu-id="aa07e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa07e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa07e-110">*pJob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa07e-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa07e-111">Contiene informazioni relative al processo, ad esempio il numero di byte e i file trasferiti prima che si verifichi l'errore.</span><span class="sxs-lookup"><span data-stu-id="aa07e-111">Contains job-related information, such as the number of bytes and files transferred before the error occurred.</span></span> <span data-ttu-id="aa07e-112">Contiene inoltre i metodi per riprendere e annullare il processo.</span><span class="sxs-lookup"><span data-stu-id="aa07e-112">It also contains the methods to resume and cancel the job.</span></span> <span data-ttu-id="aa07e-113">Non rilasciare *pJob*; Rilascia l'interfaccia quando il metodo [**JobError**](https://www.bing.com/search?q=**JobError**) restituisce.</span><span class="sxs-lookup"><span data-stu-id="aa07e-113">Do not release *pJob*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="aa07e-114">*perror* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa07e-114">*pError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa07e-115">Contiene informazioni sull'errore, ad esempio il file elaborato al momento in cui si è verificato l'errore irreversibile e una descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="aa07e-115">Contains error information, such as the file being processed at the time the fatal error occurred and a description of the error.</span></span> <span data-ttu-id="aa07e-116">Non rilasciare *perror*; Rilascia l'interfaccia quando il metodo [**JobError**](https://www.bing.com/search?q=**JobError**) restituisce.</span><span class="sxs-lookup"><span data-stu-id="aa07e-116">Do not release *pError*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa07e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa07e-117">Return value</span></span>

<span data-ttu-id="aa07e-118">Questo metodo deve restituire **S_OK**; in caso contrario, continuare a chiamare questo metodo fino a quando non viene restituito **S_OK** .</span><span class="sxs-lookup"><span data-stu-id="aa07e-118">This method should return **S_OK**; otherwise, DO continues to call this method until **S_OK** is returned.</span></span> <span data-ttu-id="aa07e-119">Per motivi di prestazioni, è consigliabile limitare il numero di volte in cui viene restituito un valore diverso da **S_OK** per alcune volte.</span><span class="sxs-lookup"><span data-stu-id="aa07e-119">For performance reasons, you should limit the number of times you return a value other than **S_OK** to a few times.</span></span> <span data-ttu-id="aa07e-120">In alternativa alla restituzione di un codice di errore, è consigliabile restituire sempre **S_OK** e gestire l'errore internamente.</span><span class="sxs-lookup"><span data-stu-id="aa07e-120">As an alternative to returning an error code, consider always returning **S_OK** and handling the error internally.</span></span> <span data-ttu-id="aa07e-121">L'intervallo in cui viene chiamato questo metodo è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="aa07e-121">The interval at which this method is called is arbitrary.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa07e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa07e-122">Remarks</span></span>

<span data-ttu-id="aa07e-123">Dopo aver determinato la cause dell'errore, eseguire una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="aa07e-123">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="aa07e-124">Per annullare il processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="aa07e-124">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="aa07e-125">Per accettare la parte del processo che è stata trasferita correttamente prima dell'errore, chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="aa07e-125">To accept the portion of the job that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="aa07e-126">Questa opzione non è applicabile ai processi di caricamento. non è possibile completare una parte di un processo di caricamento.</span><span class="sxs-lookup"><span data-stu-id="aa07e-126">This option does not apply to upload jobs; you cannot complete a portion of an upload job.</span></span>
-   <span data-ttu-id="aa07e-127">Per completare l'elaborazione del processo, risolvere il problema e quindi chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="aa07e-127">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

<span data-ttu-id="aa07e-128">Gli errori temporanei non generano chiamate al metodo [**JobError**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="aa07e-128">Transient errors do not generate calls to the [**JobError**](https://www.bing.com/search?q=**JobError**) method.</span></span>

<span data-ttu-id="aa07e-129">Restituisce BG_ERROR_CONTEXT_REMOTE_FILE se il processo ha raggiunto un errore HTTP 403. in caso contrario, BG_ERROR_CONTEXT_NONE.</span><span class="sxs-lookup"><span data-stu-id="aa07e-129">DO returns BG_ERROR_CONTEXT_REMOTE_FILE if the job hit a HTTP 403 error, BG_ERROR_CONTEXT_NONE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa07e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa07e-130">Requirements</span></span>



| <span data-ttu-id="aa07e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa07e-131">Requirement</span></span> | <span data-ttu-id="aa07e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="aa07e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa07e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa07e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="aa07e-134">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa07e-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aa07e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa07e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="aa07e-136">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa07e-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aa07e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa07e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa07e-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa07e-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa07e-139">IDL</span><span class="sxs-lookup"><span data-stu-id="aa07e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa07e-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa07e-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="aa07e-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa07e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa07e-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa07e-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="aa07e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="aa07e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa07e-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa07e-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="aa07e-145">IID</span><span class="sxs-lookup"><span data-stu-id="aa07e-145">IID</span></span><br/>                      | <span data-ttu-id="aa07e-146">IID_IBackgroundCopyCallback viene definito come 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="aa07e-146">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="aa07e-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa07e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa07e-148">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="aa07e-148">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="aa07e-149">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="aa07e-149">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="aa07e-150">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="aa07e-150">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="aa07e-151">**Metodo ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="aa07e-151">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="aa07e-152">**Metodo ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="aa07e-152">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





