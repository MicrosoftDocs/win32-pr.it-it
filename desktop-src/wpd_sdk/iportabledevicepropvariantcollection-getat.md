---
description: 'Metodo IPortableDevicePropVariantCollection::GetAt: il metodo GetAt recupera un elemento dalla raccolta in base a un indice in base zero.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: Metodo IPortableDevicePropVariantCollection::GetAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b901e8fcfa065813e4c0942632f80901800ef0a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106799"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="66a60-103">Metodo IPortableDevicePropVariantCollection::GetAt</span><span class="sxs-lookup"><span data-stu-id="66a60-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="66a60-104">Il **metodo GetAt** recupera un elemento dalla raccolta in base a un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="66a60-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a60-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66a60-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="66a60-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66a60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a60-107">*dwIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="66a60-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a60-108">**DWORD** che contiene l'indice in base zero dell'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="66a60-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="66a60-109">*pValue* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="66a60-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66a60-110">Puntatore a **una struttura PROPVARIANT.**</span><span class="sxs-lookup"><span data-stu-id="66a60-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="66a60-111">Il chiamante è responsabile della liberazione di questa memoria chiamando **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="66a60-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66a60-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66a60-112">Return value</span></span>

<span data-ttu-id="66a60-113">Il metodo restituisce un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="66a60-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="66a60-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="66a60-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="66a60-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="66a60-115">Return code</span></span>                                                                                  | <span data-ttu-id="66a60-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66a60-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="66a60-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66a60-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="66a60-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="66a60-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="66a60-119"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66a60-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="66a60-120">Un argomento del puntatore obbligatorio era **NULL.**</span><span class="sxs-lookup"><span data-stu-id="66a60-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="66a60-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="66a60-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="66a60-122">L'indice passato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="66a60-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="66a60-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="66a60-123">Examples</span></span>

<span data-ttu-id="66a60-124">Per un esempio di come usare questo metodo, vedere [Recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="66a60-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66a60-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66a60-125">Requirements</span></span>



| <span data-ttu-id="66a60-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a60-126">Requirement</span></span> | <span data-ttu-id="66a60-127">Valore</span><span class="sxs-lookup"><span data-stu-id="66a60-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66a60-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66a60-128">Header</span></span><br/>  | <dl> <span data-ttu-id="66a60-129"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="66a60-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="66a60-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="66a60-130">Library</span></span><br/> | <dl> <span data-ttu-id="66a60-131"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="66a60-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a60-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66a60-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a60-133">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="66a60-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="66a60-134">Recupero di un identificatore di oggetto da un identificatore univoco permanente</span><span class="sxs-lookup"><span data-stu-id="66a60-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="66a60-135">Recupero di eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="66a60-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="66a60-136">Recupero di formati di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="66a60-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="66a60-137">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="66a60-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="66a60-138">Recupero dei tipi di contenuto supportati da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="66a60-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="66a60-139">Recupero delle categorie funzionali supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="66a60-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="66a60-140">Recupero degli identificatori di oggetto funzionale per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="66a60-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="66a60-141">Recupero delle funzionalità di rendering supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="66a60-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="66a60-142">Impostazione delle proprietà per più oggetti</span><span class="sxs-lookup"><span data-stu-id="66a60-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




