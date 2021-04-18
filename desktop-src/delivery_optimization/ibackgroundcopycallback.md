---
title: Interfaccia IBackgroundCopyCallback (Deliveryoptimization. h)
description: Implementare l'interfaccia IBackgroundCopyCallback per ricevere una notifica che indica che il processo è stato completato, è stato modificato o è in errore. I client usano questa interfaccia anziché eseguire il polling dello stato del processo.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Interfaccia IBackgroundCopyCallback
- Interfaccia IBackgroundCopyCallback, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301487"
---
# <a name="ibackgroundcopycallback-interface"></a><span data-ttu-id="90158-106">Interfaccia IBackgroundCopyCallback</span><span class="sxs-lookup"><span data-stu-id="90158-106">IBackgroundCopyCallback interface</span></span>

<span data-ttu-id="90158-107">Implementare l'interfaccia **IBackgroundCopyCallback** per ricevere una notifica che indica che il processo è stato completato, è stato modificato o è in errore.</span><span class="sxs-lookup"><span data-stu-id="90158-107">Implement the **IBackgroundCopyCallback** interface to receive notification that a job is complete, has been modified, or is in error.</span></span> <span data-ttu-id="90158-108">I client usano questa interfaccia anziché eseguire il polling dello stato del processo.</span><span class="sxs-lookup"><span data-stu-id="90158-108">Clients use this interface instead of polling for the status of the job.</span></span>

## <a name="members"></a><span data-ttu-id="90158-109">Membri</span><span class="sxs-lookup"><span data-stu-id="90158-109">Members</span></span>

<span data-ttu-id="90158-110">L'interfaccia **IBackgroundCopyCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="90158-110">The **IBackgroundCopyCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="90158-111">**IBackgroundCopyCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="90158-111">**IBackgroundCopyCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="90158-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="90158-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="90158-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="90158-113">Methods</span></span>

<span data-ttu-id="90158-114">L'interfaccia **IBackgroundCopyCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="90158-114">The **IBackgroundCopyCallback** interface has these methods.</span></span>



| <span data-ttu-id="90158-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="90158-115">Method</span></span>                                                                    | <span data-ttu-id="90158-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90158-116">Description</span></span>                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="90158-117">**JobError**</span><span class="sxs-lookup"><span data-stu-id="90158-117">**JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)               | <span data-ttu-id="90158-118">Chiamato quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="90158-118">Called when an error occurs.</span></span><br/>                                           |
| [<span data-ttu-id="90158-119">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="90158-119">**JobModification**</span></span>](ibackgroundcopycallback-jobmodification-method.md) | <span data-ttu-id="90158-120">Chiamato quando un processo viene modificato.</span><span class="sxs-lookup"><span data-stu-id="90158-120">Called when a job is modified.</span></span><br/>                                         |
| [<span data-ttu-id="90158-121">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="90158-121">**JobTransferred**</span></span>](ibackgroundcopycallback-jobtransferred.md)          | <span data-ttu-id="90158-122">Chiamato quando tutti i file del processo sono stati trasferiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="90158-122">Called when all of the files in the job have successfully transferred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90158-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="90158-123">Remarks</span></span>

<span data-ttu-id="90158-124">Per ricevere le notifiche, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) per specificare il puntatore di interfaccia all'implementazione di **IBackgroundCopyCallback** .</span><span class="sxs-lookup"><span data-stu-id="90158-124">To receive notifications, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to specify the interface pointer to your **IBackgroundCopyCallback** implementation.</span></span> <span data-ttu-id="90158-125">Per specificare quali notifiche si desidera ricevere, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) .</span><span class="sxs-lookup"><span data-stu-id="90158-125">To specify which notifications you want to receive, call the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method.</span></span>

<span data-ttu-id="90158-126">La funzione chiamerà i callback purché il puntatore all'interfaccia sia valido.</span><span class="sxs-lookup"><span data-stu-id="90158-126">DO will call your callbacks as long as the interface pointer is valid.</span></span> <span data-ttu-id="90158-127">L'interfaccia di notifica non è più valida quando l'applicazione termina; DO non rende persistente l'interfaccia Notify.</span><span class="sxs-lookup"><span data-stu-id="90158-127">The notification interface is no longer valid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="90158-128">Di conseguenza, il processo di inizializzazione dell'applicazione deve chiamare il metodo [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) nei processi esistenti per i quali si desidera ricevere la notifica.</span><span class="sxs-lookup"><span data-stu-id="90158-128">As a result, your application's initialization process should call the [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method on those existing jobs for which you want to receive notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="90158-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90158-129">Requirements</span></span>



| <span data-ttu-id="90158-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="90158-130">Requirement</span></span> | <span data-ttu-id="90158-131">Valore</span><span class="sxs-lookup"><span data-stu-id="90158-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90158-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90158-132">Minimum supported client</span></span><br/> | <span data-ttu-id="90158-133">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="90158-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="90158-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90158-134">Minimum supported server</span></span><br/> | <span data-ttu-id="90158-135">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90158-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="90158-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90158-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="90158-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="90158-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="90158-138">IDL</span><span class="sxs-lookup"><span data-stu-id="90158-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90158-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90158-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="90158-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="90158-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="90158-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90158-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="90158-142">DLL</span><span class="sxs-lookup"><span data-stu-id="90158-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90158-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90158-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="90158-144">IID</span><span class="sxs-lookup"><span data-stu-id="90158-144">IID</span></span><br/>                      | <span data-ttu-id="90158-145">IID_IBackgroundCopyCallback viene definito come 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="90158-145">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="90158-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90158-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90158-147">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="90158-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="90158-148">**Metodo ibackgroundcopyjob:: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="90158-148">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="90158-149">**Metodo ibackgroundcopyjob:: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="90158-149">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

