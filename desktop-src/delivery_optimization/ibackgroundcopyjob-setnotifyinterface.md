---
title: Metodo metodo ibackgroundcopyjob SetNotifyInterface (Deliveryoptimization. h)
description: Identifica l'implementazione dell'interfaccia IBackgroundCopyCallback da eseguire. Usare l'interfaccia IBackgroundCopyCallback per ricevere notifiche di eventi correlati al processo.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Metodo SetNotifyInterface
- Metodo SetNotifyInterface, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo SetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340622"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a><span data-ttu-id="5c61a-107">Metodo metodo ibackgroundcopyjob:: SetNotifyInterface</span><span class="sxs-lookup"><span data-stu-id="5c61a-107">IBackgroundCopyJob::SetNotifyInterface method</span></span>

<span data-ttu-id="5c61a-108">Identifica l'implementazione dell'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5c61a-108">Identifies your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to DO.</span></span> <span data-ttu-id="5c61a-109">Usare l'interfaccia **IBackgroundCopyCallback** per ricevere notifiche di eventi correlati al processo.</span><span class="sxs-lookup"><span data-stu-id="5c61a-109">Use the **IBackgroundCopyCallback** interface to receive notification of job-related events.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c61a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c61a-110">Syntax</span></span>


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="5c61a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c61a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c61a-112">*pNotifyInterface*</span><span class="sxs-lookup"><span data-stu-id="5c61a-112">*pNotifyInterface*</span></span> 
</dt> <dd>

<span data-ttu-id="5c61a-113">Puntatore di interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="5c61a-113">An [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface pointer.</span></span> <span data-ttu-id="5c61a-114">Per rimuovere il puntatore all'interfaccia di callback corrente, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="5c61a-114">To remove the current callback interface pointer, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c61a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c61a-115">Return value</span></span>

<span data-ttu-id="5c61a-116">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="5c61a-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="5c61a-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5c61a-117">Return code</span></span>                                                                              | <span data-ttu-id="5c61a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c61a-118">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5c61a-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="5c61a-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="5c61a-120">Il puntatore all'interfaccia di notifica è stato impostato correttamente.</span><span class="sxs-lookup"><span data-stu-id="5c61a-120">Notification interface pointer was successfully set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c61a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c61a-121">Remarks</span></span>

<span data-ttu-id="5c61a-122">Chiamare questo metodo solo se si implementa l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="5c61a-122">Call this method only if you implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="5c61a-123">Utilizzare il metodo **SetNotifyInterface** insieme al metodo [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) per specificare il tipo di notifica che si desidera ricevere.</span><span class="sxs-lookup"><span data-stu-id="5c61a-123">Use the **SetNotifyInterface** method in conjunction with the [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to specify the type of notification that you want to receive.</span></span>

<span data-ttu-id="5c61a-124">L'interfaccia di notifica diventa non valida al termine dell'applicazione; DO non rende persistente l'interfaccia Notify.</span><span class="sxs-lookup"><span data-stu-id="5c61a-124">The notification interface becomes invalid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="5c61a-125">Di conseguenza, il processo di inizializzazione dell'applicazione deve chiamare il metodo **SetNotifyInterface** nei processi esistenti per i quali si desidera ricevere la notifica.</span><span class="sxs-lookup"><span data-stu-id="5c61a-125">As a result, your application's initialization process should call the **SetNotifyInterface** method on those existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="5c61a-126">Se è necessario acquisire informazioni sullo stato e sullo stato di avanzamento dopo l'ultima esecuzione dell'applicazione, eseguire il polling delle informazioni sullo stato e sullo stato durante l'inizializzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c61a-126">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="5c61a-127">Solo il proprietario/autore del processo o un amministratore può registrarsi per le notifiche.</span><span class="sxs-lookup"><span data-stu-id="5c61a-127">Only the job owner/creator or an administrator can register for notifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c61a-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c61a-128">Requirements</span></span>



| <span data-ttu-id="5c61a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c61a-129">Requirement</span></span> | <span data-ttu-id="5c61a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5c61a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c61a-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c61a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5c61a-132">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c61a-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5c61a-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c61a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5c61a-134">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c61a-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5c61a-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c61a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c61a-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c61a-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c61a-137">IDL</span><span class="sxs-lookup"><span data-stu-id="5c61a-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c61a-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c61a-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5c61a-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c61a-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c61a-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c61a-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5c61a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5c61a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c61a-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c61a-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5c61a-143">IID</span><span class="sxs-lookup"><span data-stu-id="5c61a-143">IID</span></span><br/>                      | <span data-ttu-id="5c61a-144">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="5c61a-144">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5c61a-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c61a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c61a-146">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="5c61a-146">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="5c61a-147">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="5c61a-147">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="5c61a-148">**Metodo ibackgroundcopyjob:: GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="5c61a-148">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="5c61a-149">**Metodo ibackgroundcopyjob:: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="5c61a-149">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





