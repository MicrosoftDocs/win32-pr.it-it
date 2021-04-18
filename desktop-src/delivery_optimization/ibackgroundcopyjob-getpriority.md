---
title: Metodo GetPriority metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera il livello di priorità per il processo. Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- GetPriority (metodo)
- Metodo GetPriority, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301727"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a><span data-ttu-id="0f251-107">Metodo metodo ibackgroundcopyjob:: GetPriority</span><span class="sxs-lookup"><span data-stu-id="0f251-107">IBackgroundCopyJob::GetPriority method</span></span>

<span data-ttu-id="0f251-108">Recupera il livello di priorità per il processo.</span><span class="sxs-lookup"><span data-stu-id="0f251-108">Retrieves the priority level for the job.</span></span> <span data-ttu-id="0f251-109">Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="0f251-109">The priority level determines when the job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f251-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f251-110">Syntax</span></span>


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="0f251-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f251-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f251-112">*pPriority* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0f251-112">*pPriority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f251-113">Priorità del processo rispetto ad altri processi nella coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="0f251-113">Priority of the job relative to other jobs in the transfer queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f251-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f251-114">Return value</span></span>

<span data-ttu-id="0f251-115">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="0f251-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="0f251-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0f251-116">Return code</span></span>                                                                              | <span data-ttu-id="0f251-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f251-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="0f251-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="0f251-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="0f251-119">Il livello di priorità è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="0f251-119">Priority level was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f251-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f251-120">Requirements</span></span>



| <span data-ttu-id="0f251-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f251-121">Requirement</span></span> | <span data-ttu-id="0f251-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0f251-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f251-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f251-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0f251-124">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f251-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0f251-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f251-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0f251-126">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f251-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0f251-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f251-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f251-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f251-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f251-129">IDL</span><span class="sxs-lookup"><span data-stu-id="0f251-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f251-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f251-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f251-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0f251-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f251-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f251-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0f251-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0f251-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f251-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f251-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0f251-135">IID</span><span class="sxs-lookup"><span data-stu-id="0f251-135">IID</span></span><br/>                      | <span data-ttu-id="0f251-136">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="0f251-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0f251-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f251-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f251-138">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="0f251-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="0f251-139">**Metodo ibackgroundcopyjob:: sepriority**</span><span class="sxs-lookup"><span data-stu-id="0f251-139">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





