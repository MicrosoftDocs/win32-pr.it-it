---
title: Metodo metodo ibackgroundcopyjob GetNotifyInterface (Deliveryoptimization. h)
description: Recupera il puntatore di interfaccia all'implementazione dell'interfaccia IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Metodo GetNotifyInterface
- Metodo GetNotifyInterface, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302657"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a><span data-ttu-id="05f37-106">Metodo metodo ibackgroundcopyjob:: GetNotifyInterface</span><span class="sxs-lookup"><span data-stu-id="05f37-106">IBackgroundCopyJob::GetNotifyInterface method</span></span>

<span data-ttu-id="05f37-107">Recupera il puntatore di interfaccia all'implementazione dell'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="05f37-107">Retrieves the interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f37-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05f37-108">Syntax</span></span>


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="05f37-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="05f37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f37-110">*ppNotifyInterface* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="05f37-110">*ppNotifyInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05f37-111">Puntatore di interfaccia all'implementazione dell'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="05f37-111">Interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="05f37-112">Al termine, rilasciare *ppNotifyInterface*.</span><span class="sxs-lookup"><span data-stu-id="05f37-112">When done, release *ppNotifyInterface*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f37-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05f37-113">Return value</span></span>

<span data-ttu-id="05f37-114">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="05f37-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="05f37-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="05f37-115">Return code</span></span>                                                                              | <span data-ttu-id="05f37-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05f37-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="05f37-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="05f37-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="05f37-118">Il puntatore all'interfaccia di notifica è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="05f37-118">Notification interface pointer was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05f37-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05f37-119">Requirements</span></span>



| <span data-ttu-id="05f37-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="05f37-120">Requirement</span></span> | <span data-ttu-id="05f37-121">Valore</span><span class="sxs-lookup"><span data-stu-id="05f37-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f37-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05f37-122">Minimum supported client</span></span><br/> | <span data-ttu-id="05f37-123">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="05f37-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="05f37-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05f37-124">Minimum supported server</span></span><br/> | <span data-ttu-id="05f37-125">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="05f37-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="05f37-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05f37-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f37-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="05f37-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="05f37-128">IDL</span><span class="sxs-lookup"><span data-stu-id="05f37-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05f37-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05f37-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="05f37-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="05f37-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="05f37-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05f37-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="05f37-132">DLL</span><span class="sxs-lookup"><span data-stu-id="05f37-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05f37-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f37-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="05f37-134">IID</span><span class="sxs-lookup"><span data-stu-id="05f37-134">IID</span></span><br/>                      | <span data-ttu-id="05f37-135">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="05f37-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="05f37-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05f37-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f37-137">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="05f37-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="05f37-138">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="05f37-138">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="05f37-139">**Metodo ibackgroundcopyjob:: GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="05f37-139">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="05f37-140">**Metodo ibackgroundcopyjob:: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="05f37-140">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





