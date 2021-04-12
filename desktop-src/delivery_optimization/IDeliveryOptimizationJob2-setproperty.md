---
title: 'Metodo IDeliveryOptimizationJob2:: SetProperty'
description: Questo metodo non è utilizzato.
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IDeliveryOptimizationJob2
- Interfaccia IDeliveryOptimizationJob2, metodo SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400683"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a><span data-ttu-id="2d7a1-106">Metodo IDeliveryOptimizationJob2:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="2d7a1-106">IDeliveryOptimizationJob2::SetProperty method</span></span>

<span data-ttu-id="2d7a1-107">Questo metodo non è utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2d7a1-107">This method is unused.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d7a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d7a1-108">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="2d7a1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d7a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d7a1-110">*propid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d7a1-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d7a1-111">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2d7a1-111">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="2d7a1-112">*PropValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d7a1-112">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d7a1-113">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2d7a1-113">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d7a1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d7a1-114">Return value</span></span>

<span data-ttu-id="2d7a1-115">Se propId è **DOJobPropertyId_ExtendedErrorInfo**, il valore restituito viene **DO_E_READ_ONLY_PROPERTY**. in caso contrario, la funzione restituisce **DO_E_UNKNOWN_PROPERTY_ID**.</span><span class="sxs-lookup"><span data-stu-id="2d7a1-115">If propId is **DOJobPropertyId_ExtendedErrorInfo**, the returned value is **DO_E_READ_ONLY_PROPERTY**, otherwise the function returns **DO_E_UNKNOWN_PROPERTY_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d7a1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d7a1-116">Requirements</span></span>

| <span data-ttu-id="2d7a1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d7a1-117">Requirement</span></span> | <span data-ttu-id="2d7a1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2d7a1-118">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2d7a1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d7a1-119">Minimum supported client</span></span>  | <span data-ttu-id="2d7a1-120">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d7a1-120">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="2d7a1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d7a1-121">Minimum supported server</span></span>  | <span data-ttu-id="2d7a1-122">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d7a1-122">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="2d7a1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d7a1-123">Header</span></span>                    | <span data-ttu-id="2d7a1-124">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="2d7a1-124">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="2d7a1-125">IDL</span><span class="sxs-lookup"><span data-stu-id="2d7a1-125">IDL</span></span>                       | <span data-ttu-id="2d7a1-126">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="2d7a1-126">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="2d7a1-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d7a1-127">Library</span></span>                   | <span data-ttu-id="2d7a1-128">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="2d7a1-128">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="2d7a1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2d7a1-129">DLL</span></span>                       | <span data-ttu-id="2d7a1-130">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="2d7a1-130">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="2d7a1-131">IID</span><span class="sxs-lookup"><span data-stu-id="2d7a1-131">IID</span></span>                       | <span data-ttu-id="2d7a1-132">IID_IDeliveryOptimizationJob2 viene definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="2d7a1-132">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="2d7a1-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d7a1-133">See also</span></span>

[<span data-ttu-id="2d7a1-134">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="2d7a1-134">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
