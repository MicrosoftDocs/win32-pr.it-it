---
title: Metodo GetState Metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera lo stato del processo.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Metodo GetState
- Metodo GetState, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetState
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741719"
---
# <a name="ibackgroundcopyjobgetstate-method"></a><span data-ttu-id="57bd3-106">Metodo metodo ibackgroundcopyjob:: GetState</span><span class="sxs-lookup"><span data-stu-id="57bd3-106">IBackgroundCopyJob::GetState method</span></span>

<span data-ttu-id="57bd3-107">Recupera lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="57bd3-107">Retrieves the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="57bd3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57bd3-108">Syntax</span></span>


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a><span data-ttu-id="57bd3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="57bd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57bd3-110">*pJobState* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57bd3-110">*pJobState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57bd3-111">Stato del processo.</span><span class="sxs-lookup"><span data-stu-id="57bd3-111">The state of the job.</span></span> <span data-ttu-id="57bd3-112">Ad esempio, lo stato indica se il processo è in errore, trasferisce i dati o è sospeso.</span><span class="sxs-lookup"><span data-stu-id="57bd3-112">For example, the state reflects whether the job is in error, transferring data, or suspended.</span></span> <span data-ttu-id="57bd3-113">Per un elenco degli Stati del processo, vedere l'enumerazione [**BG_JOB_STATE**](bg-job-state-.md) .</span><span class="sxs-lookup"><span data-stu-id="57bd3-113">For a list of job states, see the [**BG_JOB_STATE**](bg-job-state-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57bd3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57bd3-114">Return value</span></span>

<span data-ttu-id="57bd3-115">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="57bd3-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="57bd3-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="57bd3-116">Return code</span></span>                                                                              | <span data-ttu-id="57bd3-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57bd3-117">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="57bd3-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="57bd3-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="57bd3-119">Lo stato del processo è stato recuperato correttamente.</span><span class="sxs-lookup"><span data-stu-id="57bd3-119">The state of the job was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57bd3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="57bd3-120">Remarks</span></span>

<span data-ttu-id="57bd3-121">Per capire quando un processo è in errore o ha trasferito tutti i file nel processo, è possibile usare questo metodo per eseguire il polling dello stato del processo oppure è possibile registrarsi per ricevere una notifica quando si verificano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="57bd3-121">If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when events occur.</span></span> <span data-ttu-id="57bd3-122">Per informazioni dettagliate sulla registrazione per ricevere la notifica degli eventi, vedere l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="57bd3-122">For details on registering to receive event notification, see the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="57bd3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57bd3-123">Requirements</span></span>



| <span data-ttu-id="57bd3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="57bd3-124">Requirement</span></span> | <span data-ttu-id="57bd3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="57bd3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57bd3-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57bd3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="57bd3-127">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="57bd3-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="57bd3-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57bd3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="57bd3-129">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57bd3-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="57bd3-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57bd3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="57bd3-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="57bd3-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="57bd3-132">IDL</span><span class="sxs-lookup"><span data-stu-id="57bd3-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57bd3-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57bd3-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="57bd3-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="57bd3-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="57bd3-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57bd3-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="57bd3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="57bd3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57bd3-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57bd3-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="57bd3-138">IID</span><span class="sxs-lookup"><span data-stu-id="57bd3-138">IID</span></span><br/>                      | <span data-ttu-id="57bd3-139">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="57bd3-139">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="57bd3-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57bd3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57bd3-141">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="57bd3-141">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="57bd3-142">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="57bd3-142">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="57bd3-143">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="57bd3-143">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> </dl>

 

 





