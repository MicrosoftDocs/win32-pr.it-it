---
description: Il metodo GetA recupera un elemento dalla raccolta in base a un indice in base zero.
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'Metodo IPortableDevicePropVariantCollection:: GetA (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 0833c69b537fa230320ef69707a6f4302a8ca1ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325946"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="58c78-103">IPortableDevicePropVariantCollection:: GetA (metodo)</span><span class="sxs-lookup"><span data-stu-id="58c78-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="58c78-104">Il metodo **Geta** recupera un elemento dalla raccolta in base a un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="58c78-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c78-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58c78-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="58c78-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58c78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c78-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58c78-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c78-108">**DWORD** che contiene l'indice in base zero dell'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="58c78-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="58c78-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="58c78-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58c78-110">Puntatore a una struttura **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="58c78-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="58c78-111">Il chiamante è responsabile della liberazione della memoria chiamando **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="58c78-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c78-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58c78-112">Return value</span></span>

<span data-ttu-id="58c78-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="58c78-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="58c78-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="58c78-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="58c78-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="58c78-115">Return code</span></span>                                                                                  | <span data-ttu-id="58c78-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58c78-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="58c78-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="58c78-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="58c78-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="58c78-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="58c78-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="58c78-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="58c78-120">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="58c78-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="58c78-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="58c78-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="58c78-122">L'indice passato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="58c78-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="58c78-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="58c78-123">Examples</span></span>

<span data-ttu-id="58c78-124">Per un esempio di come usare questo metodo, vedere [recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="58c78-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58c78-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58c78-125">Requirements</span></span>



| <span data-ttu-id="58c78-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="58c78-126">Requirement</span></span> | <span data-ttu-id="58c78-127">Valore</span><span class="sxs-lookup"><span data-stu-id="58c78-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c78-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58c78-128">Header</span></span><br/>  | <dl> <span data-ttu-id="58c78-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="58c78-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="58c78-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="58c78-130">Library</span></span><br/> | <dl> <span data-ttu-id="58c78-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58c78-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58c78-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58c78-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c78-133">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="58c78-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="58c78-134">Recupero di un identificatore di oggetto da un identificatore univoco permanente</span><span class="sxs-lookup"><span data-stu-id="58c78-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="58c78-135">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="58c78-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="58c78-136">Recupero dei formati di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="58c78-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="58c78-137">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="58c78-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="58c78-138">Recupero dei tipi di contenuto supportati da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="58c78-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="58c78-139">Recupero delle categorie funzionali supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="58c78-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="58c78-140">Recupero degli identificatori di oggetti funzionali per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="58c78-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="58c78-141">Recupero delle funzionalità di rendering supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="58c78-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="58c78-142">Impostazione delle proprietà per più oggetti</span><span class="sxs-lookup"><span data-stu-id="58c78-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




