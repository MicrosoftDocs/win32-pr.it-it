---
title: Enumerazione BG_JOB_STATE (Deliveryoptimization. h)
description: L'enumerazione BG_JOB_STATE definisce i valori costanti per i diversi Stati di un processo.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Enumerazione BG_JOB_STATE
- Enumerazione BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301091"
---
# <a name="bg_job_state-enumeration"></a><span data-ttu-id="fc0ac-105">Enumerazione BG_JOB_STATE</span><span class="sxs-lookup"><span data-stu-id="fc0ac-105">BG_JOB_STATE enumeration</span></span>

<span data-ttu-id="fc0ac-106">L'enumerazione **BG_JOB_STATE** definisce i valori costanti per i diversi Stati di un processo.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-106">The **BG_JOB_STATE** enumeration defines constant values for the different states of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0ac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc0ac-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a><span data-ttu-id="fc0ac-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="fc0ac-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fc0ac-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-110">Specifica che il processo è in coda e in attesa di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-110">Specifies that the job is in the queue and waiting to run.</span></span> <span data-ttu-id="fc0ac-111">Se un utente si disconnette durante il trasferimento del processo, il processo passa allo stato in coda.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-111">If a user logs off while their job is transferring, the job transitions to the queued state.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ac-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-113">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ac-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-115">Specifica che il trasferimento dei dati per il processo è in corso.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-115">Specifies that DO is transferring data for the job.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ac-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-117">Specifica che il processo è sospeso (in pausa).</span><span class="sxs-lookup"><span data-stu-id="fc0ac-117">Specifies that the job is suspended (paused).</span></span> <span data-ttu-id="fc0ac-118">Per sospendere un processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md) .</span><span class="sxs-lookup"><span data-stu-id="fc0ac-118">To suspend a job, call the [**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md) method.</span></span> <span data-ttu-id="fc0ac-119">Il processo resta sospeso fino a quando non viene chiamato il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md), [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md)o [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="fc0ac-119">The job remains suspended until you call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md), or [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ac-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-121">Specifica che si è verificato un errore irreversibile (il servizio non è in grado di trasferire il file).</span><span class="sxs-lookup"><span data-stu-id="fc0ac-121">Specifies that a nonrecoverable error occurred (the service is unable to transfer the file).</span></span> <span data-ttu-id="fc0ac-122">Se è possibile correggere l'errore, ad esempio un errore di accesso negato, chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) dopo che l'errore è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-122">If the error, such as an access-denied error, can be corrected, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method after the error is fixed.</span></span> <span data-ttu-id="fc0ac-123">Tuttavia, se non è possibile correggere l'errore, chiamare il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) per annullare il processo oppure chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) per accettare la parte di un processo di download che è stato trasferito correttamente.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-123">However, if the error cannot be corrected, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job, or call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to accept the portion of a download job that transferred successfully.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ac-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-125">Specifica che si è verificato un errore reversibile.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-125">Specifies that a recoverable error occurred.</span></span> <span data-ttu-id="fc0ac-126">I processi vengono ritentati nello stato di errore temporaneo in base alla configurazione di ripetizione dei tentativi interna.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-126">DO will retry jobs in the transient error state based on the internal retry configuration.</span></span> <span data-ttu-id="fc0ac-127">Lo stato del processo viene modificato in **BG_JOB_STATE_ERROR** se il processo non riesce a eseguire lo stato di avanzamento (vedere [**Metodo ibackgroundcopyjob:: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span><span class="sxs-lookup"><span data-stu-id="fc0ac-127">The state of the job changes to **BG_JOB_STATE_ERROR** if the job fails to make progress (see [**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fc0ac-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-129">Specifica che il processo è stato elaborato correttamente.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-129">Specifies that your job was successfully processed.</span></span> <span data-ttu-id="fc0ac-130">È necessario chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) per confermare il completamento del processo e rendere i file disponibili per il client.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-130">You must call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge completion of the job and to make the files available to the client.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ac-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-132">Specifica che è stato chiamato il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) per confermare che il processo è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-132">Specifies that you called the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that your job completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="fc0ac-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="fc0ac-134">Specifica che è stato chiamato il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) per annullare il processo, ovvero rimuovere il processo dalla coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="fc0ac-134">Specifies that you called the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job (remove the job from the transfer queue).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc0ac-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc0ac-135">Requirements</span></span>



| <span data-ttu-id="fc0ac-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc0ac-136">Requirement</span></span> | <span data-ttu-id="fc0ac-137">Valore</span><span class="sxs-lookup"><span data-stu-id="fc0ac-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc0ac-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc0ac-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fc0ac-139">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc0ac-139">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fc0ac-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc0ac-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fc0ac-141">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc0ac-141">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fc0ac-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc0ac-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc0ac-143"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc0ac-143"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc0ac-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc0ac-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc0ac-145">**Metodo ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="fc0ac-145">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





