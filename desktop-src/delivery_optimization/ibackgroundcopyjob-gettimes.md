---
title: Metodo gettimes metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera i timestamp correlati al processo, ad esempio l'ora di creazione o dell'Ultima modifica del processo.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Metodo gettimes
- Metodo gettimes, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo gettimes
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477032"
---
# <a name="ibackgroundcopyjobgettimes-method"></a><span data-ttu-id="d2da8-106">Metodo metodo ibackgroundcopyjob:: gettimes</span><span class="sxs-lookup"><span data-stu-id="d2da8-106">IBackgroundCopyJob::GetTimes method</span></span>

<span data-ttu-id="d2da8-107">Recupera i timestamp correlati al processo, ad esempio l'ora di creazione o dell'Ultima modifica del processo.</span><span class="sxs-lookup"><span data-stu-id="d2da8-107">Retrieves job-related time stamps, such as the time that the job was created or last modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2da8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2da8-108">Syntax</span></span>


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a><span data-ttu-id="d2da8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2da8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2da8-110">*pTimes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d2da8-110">*pTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2da8-111">Contiene i timestamp relativi al processo.</span><span class="sxs-lookup"><span data-stu-id="d2da8-111">Contains job-related time stamps.</span></span> <span data-ttu-id="d2da8-112">Per gli indicatori di tempo disponibili, vedere la struttura [**BG_JOB_TIMES**](bg-job-times.md) .</span><span class="sxs-lookup"><span data-stu-id="d2da8-112">For available time stamps, see the [**BG_JOB_TIMES**](bg-job-times.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2da8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2da8-113">Return value</span></span>

<span data-ttu-id="d2da8-114">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="d2da8-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="d2da8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d2da8-115">Return code</span></span>                                                                              | <span data-ttu-id="d2da8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2da8-116">Description</span></span>                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="d2da8-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d2da8-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="d2da8-118">Timestamp recuperati correttamente.</span><span class="sxs-lookup"><span data-stu-id="d2da8-118">Time stamps were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d2da8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2da8-119">Requirements</span></span>



| <span data-ttu-id="d2da8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2da8-120">Requirement</span></span> | <span data-ttu-id="d2da8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d2da8-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2da8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2da8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2da8-123">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2da8-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d2da8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2da8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2da8-125">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2da8-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d2da8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2da8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2da8-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2da8-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2da8-128">IDL</span><span class="sxs-lookup"><span data-stu-id="d2da8-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2da8-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2da8-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d2da8-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="d2da8-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2da8-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2da8-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d2da8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d2da8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2da8-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2da8-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d2da8-134">IID</span><span class="sxs-lookup"><span data-stu-id="d2da8-134">IID</span></span><br/>                      | <span data-ttu-id="d2da8-135">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="d2da8-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d2da8-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2da8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2da8-137">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="d2da8-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="d2da8-138">**BG_JOB_TIMES**</span><span class="sxs-lookup"><span data-stu-id="d2da8-138">**BG_JOB_TIMES**</span></span>](bg-job-times.md)
</dt> </dl>

 

 





