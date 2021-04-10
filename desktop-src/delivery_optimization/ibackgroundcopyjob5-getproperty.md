---
title: Metodo GetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Metodo generico per ottenere le proprietà del processo di ottimizzazione recapito.
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- Metodo GetProperty
- Metodo GetProperty, interfaccia IBackgroundCopyJob5
- Interfaccia IBackgroundCopyJob5, metodo GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964309"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a><span data-ttu-id="ae2b1-106">Metodo IBackgroundCopyJob5:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="ae2b1-106">IBackgroundCopyJob5::GetProperty method</span></span>

<span data-ttu-id="ae2b1-107">Metodo generico per ottenere le proprietà del processo di ottimizzazione recapito.</span><span class="sxs-lookup"><span data-stu-id="ae2b1-107">A generic method for getting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2b1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae2b1-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="ae2b1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae2b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2b1-110">*PropertyId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae2b1-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2b1-111">ID della proprietà ottenuta specificata come valore di enumerazione [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2b1-111">The ID of the property that is being obtained specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="ae2b1-112">*pPropertyValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae2b1-112">*pPropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2b1-113">Valore della proprietà restituito come Unione BITS_JOB_PROPERTY_VALUE.</span><span class="sxs-lookup"><span data-stu-id="ae2b1-113">The property value returned as a BITS_JOB_PROPERTY_VALUE union.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2b1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae2b1-114">Return value</span></span>

<span data-ttu-id="ae2b1-115">Il metodo restituisce i valori restituiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="ae2b1-115">The method returns the following return values.</span></span>



| <span data-ttu-id="ae2b1-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ae2b1-116">Return code</span></span>                                                                          | <span data-ttu-id="ae2b1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae2b1-117">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="ae2b1-118"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b1-118"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="ae2b1-119">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ae2b1-119">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ae2b1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae2b1-120">Requirements</span></span>



| <span data-ttu-id="ae2b1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae2b1-121">Requirement</span></span> | <span data-ttu-id="ae2b1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ae2b1-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2b1-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae2b1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2b1-124">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae2b1-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ae2b1-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae2b1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2b1-126">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ae2b1-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ae2b1-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae2b1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2b1-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b1-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae2b1-129">IDL</span><span class="sxs-lookup"><span data-stu-id="ae2b1-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae2b1-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b1-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ae2b1-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae2b1-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae2b1-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b1-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ae2b1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ae2b1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae2b1-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b1-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ae2b1-135">IID</span><span class="sxs-lookup"><span data-stu-id="ae2b1-135">IID</span></span><br/>                      | <span data-ttu-id="ae2b1-136">IID_IBackgroundCopyJob5 viene definito come E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="ae2b1-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="ae2b1-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae2b1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2b1-138">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="ae2b1-138">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="ae2b1-139">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="ae2b1-139">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





