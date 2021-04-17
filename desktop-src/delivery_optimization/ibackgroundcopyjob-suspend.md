---
title: Metodo Suspend metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Sospende un processo. I nuovi processi, i processi in errore e i processi che hanno terminato il trasferimento dei file vengono sospesi automaticamente.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Metodo Suspend
- Metodo Suspend, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo Suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd4464a04f87a7759e9b51974eef2188ba1d0c2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400622"
---
# <a name="ibackgroundcopyjobsuspend-method"></a><span data-ttu-id="0703b-107">Metodo metodo ibackgroundcopyjob:: Suspend</span><span class="sxs-lookup"><span data-stu-id="0703b-107">IBackgroundCopyJob::Suspend method</span></span>

<span data-ttu-id="0703b-108">Sospende un processo.</span><span class="sxs-lookup"><span data-stu-id="0703b-108">Suspends a job.</span></span> <span data-ttu-id="0703b-109">I nuovi processi, i processi in errore e i processi che hanno terminato il trasferimento dei file vengono sospesi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0703b-109">New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="0703b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0703b-110">Syntax</span></span>


```C++
HRESULT Suspend();
```



## <a name="parameters"></a><span data-ttu-id="0703b-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="0703b-111">Parameters</span></span>

<span data-ttu-id="0703b-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0703b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0703b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0703b-113">Return value</span></span>

<span data-ttu-id="0703b-114">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="0703b-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="0703b-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0703b-115">Return code</span></span>                                                                                          | <span data-ttu-id="0703b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0703b-116">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0703b-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="0703b-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="0703b-118">Il processo è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="0703b-118">Successfully suspended the job.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="0703b-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="0703b-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="0703b-120">Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="0703b-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0703b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0703b-121">Requirements</span></span>



| <span data-ttu-id="0703b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0703b-122">Requirement</span></span> | <span data-ttu-id="0703b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0703b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0703b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0703b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0703b-125">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0703b-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0703b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0703b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0703b-127">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0703b-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0703b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0703b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0703b-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0703b-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0703b-130">IDL</span><span class="sxs-lookup"><span data-stu-id="0703b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0703b-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0703b-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0703b-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="0703b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0703b-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0703b-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0703b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0703b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0703b-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0703b-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0703b-136">IID</span><span class="sxs-lookup"><span data-stu-id="0703b-136">IID</span></span><br/>                      | <span data-ttu-id="0703b-137">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="0703b-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0703b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0703b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0703b-139">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="0703b-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="0703b-140">**Metodo ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="0703b-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="0703b-141">**Metodo ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="0703b-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





