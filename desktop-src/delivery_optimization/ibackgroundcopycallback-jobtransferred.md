---
title: Metodo IBackgroundCopyCallback JobTransferred (Deliveryoptimization. h)
description: Ottimizzazione recapito chiama l'implementazione del metodo JobTransferred quando tutti i file del processo sono stati trasferiti correttamente.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Metodo JobTransferred
- Metodo JobTransferred, interfaccia IBackgroundCopyCallback
- Interfaccia IBackgroundCopyCallback, metodo JobTransferred
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119619"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a><span data-ttu-id="dcc46-106">Metodo IBackgroundCopyCallback:: JobTransferred</span><span class="sxs-lookup"><span data-stu-id="dcc46-106">IBackgroundCopyCallback::JobTransferred method</span></span>

<span data-ttu-id="dcc46-107">Ottimizzazione recapito chiama l'implementazione del metodo **JobTransferred** quando tutti i file del processo sono stati trasferiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="dcc46-107">Delivery Optimization (DO) calls your implementation of the **JobTransferred** method when all of the files in the job have been successfully transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc46-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcc46-108">Syntax</span></span>


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a><span data-ttu-id="dcc46-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcc46-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc46-110">*pJob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcc46-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc46-111">Contiene informazioni relative al processo, ad esempio il momento in cui il processo è stato completato, il numero di byte trasferiti e il numero di file trasferiti.</span><span class="sxs-lookup"><span data-stu-id="dcc46-111">Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred.</span></span> <span data-ttu-id="dcc46-112">Non rilasciare *pJob*; Rilascia l'interfaccia quando il metodo restituisce.</span><span class="sxs-lookup"><span data-stu-id="dcc46-112">Do not release *pJob*; DO releases the interface when the method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc46-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcc46-113">Return value</span></span>

<span data-ttu-id="dcc46-114">Questo metodo deve restituire S_OK.</span><span class="sxs-lookup"><span data-stu-id="dcc46-114">This method should return S_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcc46-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcc46-115">Remarks</span></span>

<span data-ttu-id="dcc46-116">In genere, l'implementazione deve chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) per confermare che i file sono stati trasferiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="dcc46-116">Typically, your implementation should call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that DO successfully transferred the files.</span></span> <span data-ttu-id="dcc46-117">Scaricare i file e il file di risposta non sono disponibili nel client fino a quando non viene chiamato il metodo **completo** .</span><span class="sxs-lookup"><span data-stu-id="dcc46-117">Download files and the reply file are not available on the client until you call the **Complete** method.</span></span>

<span data-ttu-id="dcc46-118">Se non si chiama il metodo [**complete**](ibackgroundcopyjob-complete.md) o il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) , Annulla il processo dopo 30 giorni ed Elimina i file incompleti.</span><span class="sxs-lookup"><span data-stu-id="dcc46-118">If you do not call the [**Complete**](ibackgroundcopyjob-complete.md) method or the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method DO cancels the job after 30 days and deletes the incomplete files.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc46-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcc46-119">Requirements</span></span>



| <span data-ttu-id="dcc46-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcc46-120">Requirement</span></span> | <span data-ttu-id="dcc46-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dcc46-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc46-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcc46-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc46-123">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcc46-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dcc46-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcc46-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc46-125">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dcc46-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dcc46-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcc46-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcc46-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcc46-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="dcc46-128">IDL</span><span class="sxs-lookup"><span data-stu-id="dcc46-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dcc46-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dcc46-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="dcc46-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="dcc46-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcc46-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcc46-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="dcc46-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dcc46-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcc46-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcc46-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="dcc46-134">IID</span><span class="sxs-lookup"><span data-stu-id="dcc46-134">IID</span></span><br/>                      | <span data-ttu-id="dcc46-135">IID_IBackgroundCopyCallback viene definito come 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="dcc46-135">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dcc46-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcc46-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc46-137">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="dcc46-137">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="dcc46-138">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="dcc46-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="dcc46-139">**Metodo ibackgroundcopyjob:: complete**</span><span class="sxs-lookup"><span data-stu-id="dcc46-139">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="dcc46-140">**Metodo ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="dcc46-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





