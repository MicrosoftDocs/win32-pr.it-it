---
title: 'Metodo IDeliveryOptimizationFile2:: SetProperty'
description: 'Questo metodo restituisce una singola proprietà del file DO. | Metodo IDeliveryOptimizationFile2:: SetProperty'
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IDeliveryOptimizationFile2
- Interfaccia IDeliveryOptimizationFile2, metodo SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321671"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a><span data-ttu-id="2a28b-107">Metodo IDeliveryOptimizationFile2:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="2a28b-107">IDeliveryOptimizationFile2::SetProperty method</span></span>

<span data-ttu-id="2a28b-108">Questo metodo restituisce una singola proprietà del file DO.</span><span class="sxs-lookup"><span data-stu-id="2a28b-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a28b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a28b-109">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="2a28b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a28b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a28b-111">*propid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a28b-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a28b-112">ID di proprietà obbligatorio da impostare di tipo DOFilePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2a28b-112">The required property ID to set of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="2a28b-113">*PropValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a28b-113">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a28b-114">Valore della proprietà da impostare, di tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="2a28b-114">The property value to set, of type VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a28b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a28b-115">Return value</span></span>

<span data-ttu-id="2a28b-116">Questo metodo restituisce i valori HRESULT seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a28b-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="2a28b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2a28b-117">Return code</span></span>                  | <span data-ttu-id="2a28b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a28b-118">Description</span></span>                                                        |
|------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2a28b-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="2a28b-119">**S_OK**</span></span>                     | <span data-ttu-id="2a28b-120">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="2a28b-120">Success</span></span>                                                            |
| <span data-ttu-id="2a28b-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="2a28b-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="2a28b-122">ID proprietà sconosciuto</span><span class="sxs-lookup"><span data-stu-id="2a28b-122">Unknown property ID</span></span>                                                |
| <span data-ttu-id="2a28b-123">**DO_E_INVALID_STATE**</span><span class="sxs-lookup"><span data-stu-id="2a28b-123">**DO_E_INVALID_STATE**</span></span>       | <span data-ttu-id="2a28b-124">Il processo non si trova attualmente in uno stato che consente l'impostazione di una proprietà</span><span class="sxs-lookup"><span data-stu-id="2a28b-124">The job is not currently in a state that allows a property setting</span></span> |

## <a name="requirements"></a><span data-ttu-id="2a28b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a28b-125">Requirements</span></span>

| <span data-ttu-id="2a28b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a28b-126">Requirement</span></span> | <span data-ttu-id="2a28b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2a28b-127">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a28b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a28b-128">Minimum supported client</span></span>  | <span data-ttu-id="2a28b-129">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a28b-129">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="2a28b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a28b-130">Minimum supported server</span></span>  | <span data-ttu-id="2a28b-131">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a28b-131">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="2a28b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a28b-132">Header</span></span>                    | <span data-ttu-id="2a28b-133">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="2a28b-133">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="2a28b-134">IDL</span><span class="sxs-lookup"><span data-stu-id="2a28b-134">IDL</span></span>                       | <span data-ttu-id="2a28b-135">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="2a28b-135">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="2a28b-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="2a28b-136">Library</span></span>                   | <span data-ttu-id="2a28b-137">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="2a28b-137">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="2a28b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2a28b-138">DLL</span></span>                       | <span data-ttu-id="2a28b-139">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="2a28b-139">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="2a28b-140">IID</span><span class="sxs-lookup"><span data-stu-id="2a28b-140">IID</span></span>                       | <span data-ttu-id="2a28b-141">IID_IDeliveryOptimizationJob2 viene definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="2a28b-141">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="2a28b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a28b-142">See also</span></span>

[<span data-ttu-id="2a28b-143">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="2a28b-143">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
