---
description: Il metodo GetA recupera un valore dalla raccolta utilizzando l'indice in base zero fornito.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'Metodo IPortableDeviceValues:: GetA (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329050"
---
# <a name="iportabledevicevaluesgetat-method"></a><span data-ttu-id="6818b-103">IPortableDeviceValues:: GetA (metodo)</span><span class="sxs-lookup"><span data-stu-id="6818b-103">IPortableDeviceValues::GetAt method</span></span>

<span data-ttu-id="6818b-104">Il metodo **Geta** recupera un valore dalla raccolta utilizzando l'indice in base zero fornito.</span><span class="sxs-lookup"><span data-stu-id="6818b-104">The **GetAt** method retrieves a value from the collection using the supplied zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6818b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6818b-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="6818b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6818b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6818b-107">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6818b-107">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6818b-108">**DWORD** che specifica un indice in base zero nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6818b-108">A **DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="6818b-109">*pKey* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6818b-109">*pKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6818b-110">Puntatore **PropertyKey** facoltativo che recupera la chiave dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="6818b-110">An optional **PROPERTYKEY** pointer that retrieves the key of the specified item.</span></span>

</dd> <dt>

<span data-ttu-id="6818b-111">*pValue* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6818b-111">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6818b-112">**PROPVARIANT** facoltativo che recupera il valore dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="6818b-112">An optional **PROPVARIANT** that retrieves the value of the specified item.</span></span> <span data-ttu-id="6818b-113">Il chiamante deve liberare la memoria chiamando **PropVariantClear** al termine di tale operazione.</span><span class="sxs-lookup"><span data-stu-id="6818b-113">The caller must free the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6818b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6818b-114">Return value</span></span>

<span data-ttu-id="6818b-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6818b-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6818b-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6818b-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6818b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6818b-117">Return code</span></span>                                                                                  | <span data-ttu-id="6818b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6818b-118">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="6818b-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6818b-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6818b-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6818b-120">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="6818b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6818b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6818b-122">È stato specificato un numero di indice non valido.</span><span class="sxs-lookup"><span data-stu-id="6818b-122">An invalid index number was specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6818b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6818b-123">Remarks</span></span>

<span data-ttu-id="6818b-124">Se una proprietà indica un valore di tipo VT \_ Unknown, la proprietà sarà uno dei dispositivi portatili Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) o [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="6818b-124">If a property indicates a value of type VT\_UNKNOWN, the property will be one of the Windows Portable Devices ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) or [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span></span> <span data-ttu-id="6818b-125">Non è possibile restituire altre interfacce da dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="6818b-125">No other interfaces can be returned by Windows Portable Devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="6818b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6818b-126">Requirements</span></span>



| <span data-ttu-id="6818b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6818b-127">Requirement</span></span> | <span data-ttu-id="6818b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6818b-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6818b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6818b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6818b-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6818b-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6818b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="6818b-131">Library</span></span><br/> | <dl> <span data-ttu-id="6818b-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6818b-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6818b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6818b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6818b-134">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="6818b-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="6818b-135">**IPortableDeviceValues:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="6818b-135">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




