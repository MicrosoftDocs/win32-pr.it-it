---
title: Metodo GetType metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera il tipo di trasferimento eseguito, ad esempio il download o il caricamento di un file.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType (metodo)
- Metodo GetType, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetType
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048009"
---
# <a name="ibackgroundcopyjobgettype-method"></a><span data-ttu-id="b87f9-106">Metodo metodo ibackgroundcopyjob:: GetType</span><span class="sxs-lookup"><span data-stu-id="b87f9-106">IBackgroundCopyJob::GetType method</span></span>

<span data-ttu-id="b87f9-107">Recupera il tipo di trasferimento eseguito, ad esempio il download o il caricamento di un file.</span><span class="sxs-lookup"><span data-stu-id="b87f9-107">Retrieves the type of transfer being performed, such as a file download or upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="b87f9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b87f9-108">Syntax</span></span>


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a><span data-ttu-id="b87f9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b87f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b87f9-110">*pJobType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b87f9-110">*pJobType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b87f9-111">Tipo di trasferimento eseguito.</span><span class="sxs-lookup"><span data-stu-id="b87f9-111">Type of transfer being performed.</span></span> <span data-ttu-id="b87f9-112">Per un elenco dei tipi di trasferimento, vedere l'enumerazione [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="b87f9-112">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b87f9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b87f9-113">Return value</span></span>

<span data-ttu-id="b87f9-114">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="b87f9-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="b87f9-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b87f9-115">Return code</span></span>                                                                              | <span data-ttu-id="b87f9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b87f9-116">Description</span></span>                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="b87f9-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b87f9-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b87f9-118">Il tipo di trasferimento è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="b87f9-118">Transfer type was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b87f9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b87f9-119">Remarks</span></span>

<span data-ttu-id="b87f9-120">Consente di specificare il tipo di trasferimento durante la creazione del processo.</span><span class="sxs-lookup"><span data-stu-id="b87f9-120">Specify the type of transfer when you create the job.</span></span>

## <a name="requirements"></a><span data-ttu-id="b87f9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b87f9-121">Requirements</span></span>



| <span data-ttu-id="b87f9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b87f9-122">Requirement</span></span> | <span data-ttu-id="b87f9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b87f9-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b87f9-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b87f9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b87f9-125">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="b87f9-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b87f9-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b87f9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b87f9-127">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b87f9-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b87f9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b87f9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b87f9-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b87f9-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b87f9-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b87f9-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b87f9-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b87f9-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b87f9-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="b87f9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b87f9-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b87f9-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b87f9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b87f9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b87f9-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b87f9-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b87f9-136">IID</span><span class="sxs-lookup"><span data-stu-id="b87f9-136">IID</span></span><br/>                      | <span data-ttu-id="b87f9-137">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="b87f9-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b87f9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b87f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b87f9-139">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="b87f9-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="b87f9-140">**BG_JOB_TYPE**</span><span class="sxs-lookup"><span data-stu-id="b87f9-140">**BG_JOB_TYPE**</span></span>](bg-job-type.md)
</dt> <dt>

[<span data-ttu-id="b87f9-141">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="b87f9-141">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





