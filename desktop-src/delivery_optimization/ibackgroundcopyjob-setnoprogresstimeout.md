---
title: Metodo metodo ibackgroundcopyjob SetNoProgressTimeout (Deliveryoptimization. h)
description: Imposta il periodo di tempo durante il quale l'ottimizzazione del recapito tenta di trasferire il file dopo che si è verificata una condizione di errore temporaneo. Se è presente lo stato di avanzamento, il timer viene reimpostato.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Metodo SetNoProgressTimeout
- Metodo SetNoProgressTimeout, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo SetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048430"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a><span data-ttu-id="bf420-107">Metodo metodo ibackgroundcopyjob:: SetNoProgressTimeout</span><span class="sxs-lookup"><span data-stu-id="bf420-107">IBackgroundCopyJob::SetNoProgressTimeout method</span></span>

<span data-ttu-id="bf420-108">Imposta il periodo di tempo durante il quale l'ottimizzazione del recapito tenta di trasferire il file dopo che si è verificata una condizione di errore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="bf420-108">Sets the length of time that Delivery Optimization (DO) tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="bf420-109">Se è presente lo stato di avanzamento, il timer viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="bf420-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf420-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf420-110">Syntax</span></span>


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="bf420-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf420-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf420-112">*RetryPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf420-112">*RetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf420-113">Periodo di tempo, in secondi, che tenta di trasferire il file dopo che non è stato eseguito alcun avanzamento.</span><span class="sxs-lookup"><span data-stu-id="bf420-113">Length of time, in seconds, that DO tries to transfer the file after there has been no progress made.</span></span> <span data-ttu-id="bf420-114">Il periodo di ripetizione predefinito per il processo con priorità alta è 3600 secondi (1 ora) e per il processo con priorità bassa è 86400 secondi (24 ore).</span><span class="sxs-lookup"><span data-stu-id="bf420-114">The default retry period for high priority job is 3600 seconds (1 hour) and for low priority job is 86400 seconds (24 hours).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf420-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf420-115">Return value</span></span>

<span data-ttu-id="bf420-116">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="bf420-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="bf420-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bf420-117">Return code</span></span>                                                                                          | <span data-ttu-id="bf420-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf420-118">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf420-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="bf420-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="bf420-120">Il periodo di ripetizione dei tentativi è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="bf420-120">Retry period successfully set.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="bf420-121"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="bf420-121"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="bf420-122">Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="bf420-122">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf420-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf420-123">Remarks</span></span>

<span data-ttu-id="bf420-124">Se DO non avanza durante il periodo di ripetizione dei tentativi, sposta lo stato del processo da BG_JOB_STATE_TRANSIENT_ERROR a BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="bf420-124">If DO does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR.</span></span> <span data-ttu-id="bf420-125">Se si richiede la notifica di errore, chiamare il callback [**JobError**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="bf420-125">If you request error notification, DO then calls your [**JobError**](https://www.bing.com/search?q=**JobError**) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf420-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf420-126">Requirements</span></span>



| <span data-ttu-id="bf420-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf420-127">Requirement</span></span> | <span data-ttu-id="bf420-128">Valore</span><span class="sxs-lookup"><span data-stu-id="bf420-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf420-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf420-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bf420-130">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf420-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bf420-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf420-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bf420-132">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf420-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bf420-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf420-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf420-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf420-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf420-135">IDL</span><span class="sxs-lookup"><span data-stu-id="bf420-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf420-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf420-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="bf420-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf420-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf420-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf420-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="bf420-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bf420-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf420-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf420-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="bf420-141">IID</span><span class="sxs-lookup"><span data-stu-id="bf420-141">IID</span></span><br/>                      | <span data-ttu-id="bf420-142">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="bf420-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="bf420-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf420-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf420-144">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="bf420-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="bf420-145">**Metodo ibackgroundcopyjob:: GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="bf420-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span></span>](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





