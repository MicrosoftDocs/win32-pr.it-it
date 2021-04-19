---
description: Il metodo GetCount Recupera il numero di elementi in questa raccolta.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'Metodo IPortableDevicePropVariantCollection:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325945"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a><span data-ttu-id="2fd16-103">Metodo IPortableDevicePropVariantCollection:: GetCount</span><span class="sxs-lookup"><span data-stu-id="2fd16-103">IPortableDevicePropVariantCollection::GetCount method</span></span>

<span data-ttu-id="2fd16-104">Il metodo **GetCount** Recupera il numero di elementi in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="2fd16-104">The **GetCount** method retrieves the number of items in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd16-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fd16-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="2fd16-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fd16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fd16-107">*pcElems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fd16-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd16-108">Puntatore a un **valore DWORD** che contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="2fd16-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fd16-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fd16-109">Return value</span></span>

<span data-ttu-id="2fd16-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2fd16-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2fd16-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2fd16-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2fd16-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2fd16-112">Return code</span></span>                                                                               | <span data-ttu-id="2fd16-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fd16-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2fd16-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2fd16-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="2fd16-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2fd16-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="2fd16-116"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="2fd16-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="2fd16-117">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="2fd16-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="2fd16-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="2fd16-118">Examples</span></span>

<span data-ttu-id="2fd16-119">Per un esempio di come usare questo metodo, vedere [recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="2fd16-119">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd16-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fd16-120">Requirements</span></span>



| <span data-ttu-id="2fd16-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd16-121">Requirement</span></span> | <span data-ttu-id="2fd16-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2fd16-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd16-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fd16-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2fd16-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd16-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fd16-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="2fd16-125">Library</span></span><br/> | <dl> <span data-ttu-id="2fd16-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fd16-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd16-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fd16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd16-128">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="2fd16-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="2fd16-129">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="2fd16-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="2fd16-130">Recupero dei formati di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="2fd16-130">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="2fd16-131">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="2fd16-131">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="2fd16-132">Recupero delle categorie funzionali supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="2fd16-132">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="2fd16-133">Impostazione delle proprietà per più oggetti</span><span class="sxs-lookup"><span data-stu-id="2fd16-133">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




