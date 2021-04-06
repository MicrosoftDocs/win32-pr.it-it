---
title: Metodo SetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Metodo generico per l'impostazione delle proprietà del processo di ottimizzazione recapito.
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IBackgroundCopyJob5
- Interfaccia IBackgroundCopyJob5, metodo SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742858"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a><span data-ttu-id="fdc2b-106">Metodo IBackgroundCopyJob5:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="fdc2b-106">IBackgroundCopyJob5::SetProperty method</span></span>

<span data-ttu-id="fdc2b-107">Metodo generico per l'impostazione delle proprietà del processo di ottimizzazione recapito.</span><span class="sxs-lookup"><span data-stu-id="fdc2b-107">A generic method for setting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc2b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fdc2b-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="fdc2b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fdc2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc2b-110">*PropertyId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fdc2b-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc2b-111">ID della proprietà che viene impostata come valore di enumerazione [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="fdc2b-111">The ID of the property that is being set specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="fdc2b-112">*PropertyValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fdc2b-112">*PropertyValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc2b-113">Valore della proprietà da impostare.</span><span class="sxs-lookup"><span data-stu-id="fdc2b-113">The value of the property that is being set.</span></span> <span data-ttu-id="fdc2b-114">Per mantenere un valore il cui tipo è appropriato per la proprietà, questo valore viene specificato tramite il [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) Unione costituito da tutti i tipi di proprietà noti.</span><span class="sxs-lookup"><span data-stu-id="fdc2b-114">In order to hold a value whose type is appropriate to the property, this value is specified via the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union that is composed of all the known property types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc2b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fdc2b-115">Return value</span></span>

<span data-ttu-id="fdc2b-116">Il metodo restituisce i valori restituiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="fdc2b-116">The method returns the following return values.</span></span>



| <span data-ttu-id="fdc2b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fdc2b-117">Return code</span></span>                                                                          | <span data-ttu-id="fdc2b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdc2b-118">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="fdc2b-119"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fdc2b-119"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="fdc2b-120">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="fdc2b-120">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fdc2b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdc2b-121">Requirements</span></span>



| <span data-ttu-id="fdc2b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc2b-122">Requirement</span></span> | <span data-ttu-id="fdc2b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fdc2b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc2b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdc2b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc2b-125">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="fdc2b-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fdc2b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdc2b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc2b-127">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fdc2b-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fdc2b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdc2b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdc2b-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdc2b-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="fdc2b-130">IDL</span><span class="sxs-lookup"><span data-stu-id="fdc2b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fdc2b-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fdc2b-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="fdc2b-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="fdc2b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="fdc2b-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdc2b-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="fdc2b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fdc2b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdc2b-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdc2b-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="fdc2b-136">IID</span><span class="sxs-lookup"><span data-stu-id="fdc2b-136">IID</span></span><br/>                      | <span data-ttu-id="fdc2b-137">IID_IBackgroundCopyJob5 viene definito come E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="fdc2b-137">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="fdc2b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdc2b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc2b-139">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="fdc2b-139">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="fdc2b-140">**IBackgroundCopyJob5:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="fdc2b-140">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





