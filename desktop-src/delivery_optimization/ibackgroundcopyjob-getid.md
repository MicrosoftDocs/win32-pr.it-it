---
title: Metodo metodo ibackgroundcopyjob GetId (Deliveryoptimization. h)
description: Recupera l'identificatore utilizzato per identificare il processo nella coda.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId (metodo)
- Metodo GetId, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, Metodo GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301593"
---
# <a name="ibackgroundcopyjobgetid-method"></a><span data-ttu-id="0cec7-106">Metodo metodo ibackgroundcopyjob:: GetId</span><span class="sxs-lookup"><span data-stu-id="0cec7-106">IBackgroundCopyJob::GetId method</span></span>

<span data-ttu-id="0cec7-107">Recupera l'identificatore utilizzato per identificare il processo nella coda.</span><span class="sxs-lookup"><span data-stu-id="0cec7-107">Retrieves the identifier used to identify the job in the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cec7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cec7-108">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a><span data-ttu-id="0cec7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cec7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cec7-110">*pJobID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cec7-110">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cec7-111">GUID che identifica il processo all'interno della coda di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0cec7-111">GUID that identifies the job within the DO queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cec7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cec7-112">Return value</span></span>

<span data-ttu-id="0cec7-113">Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.</span><span class="sxs-lookup"><span data-stu-id="0cec7-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cec7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cec7-114">Remarks</span></span>

<span data-ttu-id="0cec7-115">Il servizio genera l'identificatore quando si [Crea](ibackgroundcopymanager-createjob.md) il processo.</span><span class="sxs-lookup"><span data-stu-id="0cec7-115">The service generates the identifier when you [create](ibackgroundcopymanager-createjob.md) the job.</span></span> <span data-ttu-id="0cec7-116">Per usare l'identificatore per recuperare un puntatore di interfaccia [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md) per il processo, chiamare il metodo [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) .</span><span class="sxs-lookup"><span data-stu-id="0cec7-116">To use the identifier to retrieve an [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer for the job, call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cec7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cec7-117">Requirements</span></span>



| <span data-ttu-id="0cec7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cec7-118">Requirement</span></span> | <span data-ttu-id="0cec7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0cec7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cec7-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cec7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0cec7-121">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0cec7-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0cec7-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cec7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0cec7-123">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0cec7-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0cec7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cec7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cec7-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cec7-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cec7-126">IDL</span><span class="sxs-lookup"><span data-stu-id="0cec7-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cec7-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cec7-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0cec7-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="0cec7-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cec7-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cec7-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0cec7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0cec7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cec7-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cec7-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0cec7-132">IID</span><span class="sxs-lookup"><span data-stu-id="0cec7-132">IID</span></span><br/>                      | <span data-ttu-id="0cec7-133">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="0cec7-133">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0cec7-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cec7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cec7-135">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="0cec7-135">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="0cec7-136">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="0cec7-136">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[<span data-ttu-id="0cec7-137">**IBackgroundCopyManager:: GetJob**</span><span class="sxs-lookup"><span data-stu-id="0cec7-137">**IBackgroundCopyManager::GetJob**</span></span>](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





