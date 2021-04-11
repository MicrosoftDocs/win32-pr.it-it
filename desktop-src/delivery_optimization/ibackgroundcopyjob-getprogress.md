---
title: Metodo getProgress metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera le informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Metodo getProgress
- Metodo getProgress, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo getProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119954"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a><span data-ttu-id="394af-106">Metodo metodo ibackgroundcopyjob:: getProgress</span><span class="sxs-lookup"><span data-stu-id="394af-106">IBackgroundCopyJob::GetProgress method</span></span>

<span data-ttu-id="394af-107">Recupera le informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti.</span><span class="sxs-lookup"><span data-stu-id="394af-107">Retrieves job-related progress information, such as the number of bytes and files transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="394af-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="394af-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="394af-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="394af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="394af-110">*pProgress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="394af-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="394af-111">Contiene i dati che è possibile utilizzare per calcolare la percentuale del processo completato.</span><span class="sxs-lookup"><span data-stu-id="394af-111">Contains data that you can use to calculate the percentage of the job that is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="394af-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="394af-112">Return value</span></span>

<span data-ttu-id="394af-113">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="394af-113">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="394af-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="394af-114">Return code</span></span>                                                                              | <span data-ttu-id="394af-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="394af-115">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="394af-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="394af-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="394af-117">Recupero delle informazioni sullo stato completato.</span><span class="sxs-lookup"><span data-stu-id="394af-117">Progress information was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="394af-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="394af-118">Requirements</span></span>



| <span data-ttu-id="394af-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="394af-119">Requirement</span></span> | <span data-ttu-id="394af-120">Valore</span><span class="sxs-lookup"><span data-stu-id="394af-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="394af-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="394af-121">Minimum supported client</span></span><br/> | <span data-ttu-id="394af-122">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="394af-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="394af-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="394af-123">Minimum supported server</span></span><br/> | <span data-ttu-id="394af-124">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="394af-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="394af-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="394af-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="394af-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="394af-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="394af-127">IDL</span><span class="sxs-lookup"><span data-stu-id="394af-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="394af-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="394af-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="394af-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="394af-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="394af-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="394af-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="394af-131">DLL</span><span class="sxs-lookup"><span data-stu-id="394af-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="394af-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="394af-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="394af-133">IID</span><span class="sxs-lookup"><span data-stu-id="394af-133">IID</span></span><br/>                      | <span data-ttu-id="394af-134">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="394af-134">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="394af-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="394af-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394af-136">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="394af-136">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





