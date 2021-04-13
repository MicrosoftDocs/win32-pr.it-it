---
title: 'Metodo IDeliveryOptimizationJob2:: GetProperty'
description: Restituisce una singola proprietà del processo di esecuzione.
keywords:
- Metodo GetProperty
- Metodo GetProperty, interfaccia IDeliveryOptimizationJob2
- Interfaccia IDeliveryOptimizationJob2, metodo GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475934"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a><span data-ttu-id="cd6b4-106">Metodo IDeliveryOptimizationJob2:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="cd6b4-106">IDeliveryOptimizationJob2::GetProperty method</span></span>

<span data-ttu-id="cd6b4-107">Questo metodo restituisce una singola proprietà del processo DO.</span><span class="sxs-lookup"><span data-stu-id="cd6b4-107">This method returns a single property of the DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6b4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd6b4-108">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="cd6b4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd6b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd6b4-110">*propid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd6b4-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6b4-111">ID di proprietà obbligatorio da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cd6b4-111">The required property ID to get.</span></span> <span data-ttu-id="cd6b4-112">È supportata solo **DOJobPropertyId_ExtendedErrorInfo** di tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="cd6b4-112">Only **DOJobPropertyId_ExtendedErrorInfo** of type VT_BSTR is supported.</span></span>

</dd> <dt>

<span data-ttu-id="cd6b4-113">*PropValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd6b4-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6b4-114">Valore della proprietà risultante, archiviato in un tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="cd6b4-114">The resultant property value, stored in a VARIANT type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd6b4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd6b4-115">Return value</span></span>

<span data-ttu-id="cd6b4-116">Questo metodo restituisce i valori HRESULT seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd6b4-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="cd6b4-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cd6b4-117">Return code</span></span>                  | <span data-ttu-id="cd6b4-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd6b4-118">Description</span></span>          |
|------------------------------|----------------------|
| <span data-ttu-id="cd6b4-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="cd6b4-119">**S_OK**</span></span>                     | <span data-ttu-id="cd6b4-120">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="cd6b4-120">Success</span></span>              |
| <span data-ttu-id="cd6b4-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="cd6b4-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="cd6b4-122">ID proprietà sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="cd6b4-122">Unknown property ID.</span></span> |

## <a name="requirements"></a><span data-ttu-id="cd6b4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd6b4-123">Requirements</span></span>

| <span data-ttu-id="cd6b4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd6b4-124">Requirement</span></span> | <span data-ttu-id="cd6b4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cd6b4-125">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cd6b4-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd6b4-126">Minimum supported client</span></span>  | <span data-ttu-id="cd6b4-127">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd6b4-127">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="cd6b4-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd6b4-128">Minimum supported server</span></span>  | <span data-ttu-id="cd6b4-129">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd6b4-129">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="cd6b4-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd6b4-130">Header</span></span>                    | <span data-ttu-id="cd6b4-131">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="cd6b4-131">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="cd6b4-132">IDL</span><span class="sxs-lookup"><span data-stu-id="cd6b4-132">IDL</span></span>                       | <span data-ttu-id="cd6b4-133">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="cd6b4-133">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="cd6b4-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd6b4-134">Library</span></span>                   | <span data-ttu-id="cd6b4-135">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="cd6b4-135">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="cd6b4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cd6b4-136">DLL</span></span>                       | <span data-ttu-id="cd6b4-137">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="cd6b4-137">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="cd6b4-138">IID</span><span class="sxs-lookup"><span data-stu-id="cd6b4-138">IID</span></span>                       | <span data-ttu-id="cd6b4-139">IID_IDeliveryOptimizationJob2 viene definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="cd6b4-139">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="cd6b4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd6b4-140">See also</span></span>

[<span data-ttu-id="cd6b4-141">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="cd6b4-141">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
