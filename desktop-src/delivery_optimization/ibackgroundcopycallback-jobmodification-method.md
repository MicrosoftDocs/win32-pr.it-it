---
title: Metodo IBackgroundCopyCallback JobModification (Deliveryoptimization. h)
description: Ottimizzazione recapito chiama l'implementazione del metodo JobModification quando il processo è stato modificato.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Metodo JobModification
- Metodo JobModification, interfaccia IBackgroundCopyCallback
- Interfaccia IBackgroundCopyCallback, metodo JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301488"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a><span data-ttu-id="50892-106">Metodo IBackgroundCopyCallback:: JobModification</span><span class="sxs-lookup"><span data-stu-id="50892-106">IBackgroundCopyCallback::JobModification method</span></span>

<span data-ttu-id="50892-107">Ottimizzazione recapito chiama l'implementazione del metodo [**JobModification**](https://www.bing.com/search?q=**JobModification**) quando il processo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="50892-107">Delivery Optimization (DO) calls your implementation of the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method when the job has been modified.</span></span> <span data-ttu-id="50892-108">Il servizio genera questo evento quando vengono trasferiti i byte, i file sono stati aggiunti al processo, le proprietà sono state modificate o lo stato del processo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="50892-108">The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="50892-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50892-109">Syntax</span></span>


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="50892-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="50892-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50892-111">*pJob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50892-111">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50892-112">Contiene i metodi per accedere alle informazioni sulla proprietà, sullo stato di avanzamento e sullo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="50892-112">Contains the methods for accessing property, progress, and state information of the job.</span></span> <span data-ttu-id="50892-113">Non rilasciare *pJob*; Rilascia l'interfaccia quando il metodo [**JobModification**](https://www.bing.com/search?q=**JobModification**) restituisce.</span><span class="sxs-lookup"><span data-stu-id="50892-113">Do not release *pJob*; DO releases the interface when the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="50892-114">*dwReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50892-114">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50892-115">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="50892-115">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50892-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50892-116">Return value</span></span>

<span data-ttu-id="50892-117">Questo metodo deve restituire S_OK.</span><span class="sxs-lookup"><span data-stu-id="50892-117">This method should return S_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="50892-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50892-118">Requirements</span></span>



| <span data-ttu-id="50892-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="50892-119">Requirement</span></span> | <span data-ttu-id="50892-120">Valore</span><span class="sxs-lookup"><span data-stu-id="50892-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50892-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50892-121">Minimum supported client</span></span><br/> | <span data-ttu-id="50892-122">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="50892-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="50892-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50892-123">Minimum supported server</span></span><br/> | <span data-ttu-id="50892-124">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50892-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="50892-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50892-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="50892-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="50892-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="50892-127">IDL</span><span class="sxs-lookup"><span data-stu-id="50892-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50892-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50892-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="50892-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="50892-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="50892-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50892-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="50892-131">DLL</span><span class="sxs-lookup"><span data-stu-id="50892-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50892-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50892-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="50892-133">IID</span><span class="sxs-lookup"><span data-stu-id="50892-133">IID</span></span><br/>                      | <span data-ttu-id="50892-134">IID_IBackgroundCopyCallback viene definito come 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="50892-134">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="50892-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50892-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50892-136">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="50892-136">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="50892-137">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="50892-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





