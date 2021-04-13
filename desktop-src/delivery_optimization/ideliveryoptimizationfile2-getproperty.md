---
title: 'Metodo IDeliveryOptimizationFile2:: GetProperty'
description: 'Questo metodo restituisce una singola proprietà del file DO. | Metodo IDeliveryOptimizationFile2:: GetProperty'
keywords:
- Metodo GetProperty
- Metodo GetProperty, interfaccia IDeliveryOptimizationFile2
- Interfaccia IDeliveryOptimizationFile2, metodo GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353726"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a><span data-ttu-id="c6ff6-107">Metodo IDeliveryOptimizationFile2:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="c6ff6-107">IDeliveryOptimizationFile2::GetProperty method</span></span>

<span data-ttu-id="c6ff6-108">Questo metodo restituisce una singola proprietà del file DO.</span><span class="sxs-lookup"><span data-stu-id="c6ff6-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ff6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6ff6-109">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="c6ff6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6ff6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6ff6-111">*propid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6ff6-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ff6-112">ID di proprietà obbligatorio da ottenere di tipo DOFilePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c6ff6-112">The required property ID to get of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="c6ff6-113">*PropValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c6ff6-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ff6-114">Valore della proprietà Archiviato in una variante.</span><span class="sxs-lookup"><span data-stu-id="c6ff6-114">The property value stored in a VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6ff6-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6ff6-115">Return value</span></span>

<span data-ttu-id="c6ff6-116">Questo metodo restituisce i valori HRESULT seguenti.</span><span class="sxs-lookup"><span data-stu-id="c6ff6-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="c6ff6-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c6ff6-117">Return code</span></span>                  | <span data-ttu-id="c6ff6-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6ff6-118">Description</span></span>                                         |
|------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c6ff6-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="c6ff6-119">**S_OK**</span></span>                     | <span data-ttu-id="c6ff6-120">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="c6ff6-120">Success</span></span>                                             |
| <span data-ttu-id="c6ff6-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="c6ff6-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="c6ff6-122">ID proprietà sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c6ff6-122">Unknown property ID.</span></span>                                |
| <span data-ttu-id="c6ff6-123">**DO_E_WRITE_ONLY_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="c6ff6-123">**DO_E_WRITE_ONLY_PROPERTY**</span></span> | <span data-ttu-id="c6ff6-124">La proprietà è di sola scrittura e non può essere letta.</span><span class="sxs-lookup"><span data-stu-id="c6ff6-124">The property is Write only and cannot be read.</span></span>      |
| <span data-ttu-id="c6ff6-125">**E_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="c6ff6-125">**E_NOT_SET**</span></span>                | <span data-ttu-id="c6ff6-126">Nessuna proprietà è stata impostata tramite il metodo SetProperty.</span><span class="sxs-lookup"><span data-stu-id="c6ff6-126">No property was set through the SetProperty method.</span></span> |
| <span data-ttu-id="c6ff6-127">**E_OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="c6ff6-127">**E_OUTOFMEMORY**</span></span>            |  <span data-ttu-id="c6ff6-128">Errore di allocazione della memoria</span><span class="sxs-lookup"><span data-stu-id="c6ff6-128">Memory allocation failure</span></span>                          |

## <a name="requirements"></a><span data-ttu-id="c6ff6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6ff6-129">Requirements</span></span>

| <span data-ttu-id="c6ff6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ff6-130">Requirement</span></span> | <span data-ttu-id="c6ff6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c6ff6-131">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c6ff6-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6ff6-132">Minimum supported client</span></span>  | <span data-ttu-id="c6ff6-133">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6ff6-133">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="c6ff6-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6ff6-134">Minimum supported server</span></span>  | <span data-ttu-id="c6ff6-135">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6ff6-135">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="c6ff6-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6ff6-136">Header</span></span>                    | <span data-ttu-id="c6ff6-137">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="c6ff6-137">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="c6ff6-138">IDL</span><span class="sxs-lookup"><span data-stu-id="c6ff6-138">IDL</span></span>                       | <span data-ttu-id="c6ff6-139">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="c6ff6-139">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="c6ff6-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6ff6-140">Library</span></span>                   | <span data-ttu-id="c6ff6-141">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="c6ff6-141">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="c6ff6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c6ff6-142">DLL</span></span>                       | <span data-ttu-id="c6ff6-143">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="c6ff6-143">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="c6ff6-144">IID</span><span class="sxs-lookup"><span data-stu-id="c6ff6-144">IID</span></span>                       | <span data-ttu-id="c6ff6-145">IID_IDeliveryOptimizationJob2 viene definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="c6ff6-145">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="c6ff6-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6ff6-146">See also</span></span>

[<span data-ttu-id="c6ff6-147">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="c6ff6-147">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
