---
title: Metodo sepriority metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Specifica il livello di priorità del processo. Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- Metodo sepriority
- Metodo sepriority, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo sepriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741714"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a><span data-ttu-id="d06cc-107">Metodo metodo ibackgroundcopyjob:: sepriority</span><span class="sxs-lookup"><span data-stu-id="d06cc-107">IBackgroundCopyJob::SetPriority method</span></span>

<span data-ttu-id="d06cc-108">Specifica il livello di priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="d06cc-108">Specifies the priority level of your job.</span></span> <span data-ttu-id="d06cc-109">Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="d06cc-109">The priority level determines when your job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="d06cc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d06cc-110">Syntax</span></span>


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a><span data-ttu-id="d06cc-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d06cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d06cc-112">*Priorità* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d06cc-112">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d06cc-113">Specifica il livello di priorità del processo rispetto ad altri processi nella coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="d06cc-113">Specifies the priority level of your job relative to other jobs in the transfer queue.</span></span> <span data-ttu-id="d06cc-114">Il valore predefinito è BG_JOB_PRIORITY_NORMAL.</span><span class="sxs-lookup"><span data-stu-id="d06cc-114">The default is BG_JOB_PRIORITY_NORMAL.</span></span> <span data-ttu-id="d06cc-115">Per un elenco di livelli di priorità, vedere l'enumerazione [**BG_JOB_PRIORITY**](bg-job-priority-.md) .</span><span class="sxs-lookup"><span data-stu-id="d06cc-115">For a list of priority levels, see the [**BG_JOB_PRIORITY**](bg-job-priority-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d06cc-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d06cc-116">Return value</span></span>

<span data-ttu-id="d06cc-117">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="d06cc-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="d06cc-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d06cc-118">Return code</span></span>                                                                              | <span data-ttu-id="d06cc-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d06cc-119">Description</span></span>                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="d06cc-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d06cc-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="d06cc-121">La priorità del processo è stata impostata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d06cc-121">Job priority was successfully set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d06cc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d06cc-122">Requirements</span></span>



| <span data-ttu-id="d06cc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d06cc-123">Requirement</span></span> | <span data-ttu-id="d06cc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d06cc-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d06cc-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d06cc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d06cc-126">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d06cc-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d06cc-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d06cc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d06cc-128">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d06cc-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d06cc-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d06cc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d06cc-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d06cc-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d06cc-131">IDL</span><span class="sxs-lookup"><span data-stu-id="d06cc-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d06cc-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d06cc-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d06cc-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="d06cc-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="d06cc-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d06cc-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d06cc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d06cc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d06cc-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d06cc-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d06cc-137">IID</span><span class="sxs-lookup"><span data-stu-id="d06cc-137">IID</span></span><br/>                      | <span data-ttu-id="d06cc-138">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="d06cc-138">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d06cc-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d06cc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06cc-140">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="d06cc-140">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="d06cc-141">**BG_JOB_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="d06cc-141">**BG_JOB_PRIORITY**</span></span>](bg-job-priority-.md)
</dt> <dt>

[<span data-ttu-id="d06cc-142">**Metodo ibackgroundcopyjob:: GetPriority**</span><span class="sxs-lookup"><span data-stu-id="d06cc-142">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





