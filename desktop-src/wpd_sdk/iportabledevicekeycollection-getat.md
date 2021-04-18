---
description: Il metodo GetA recupera un PROPERTYKEY dalla raccolta in base all'indice.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'Metodo IPortableDeviceKeyCollection:: GetA (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329895"
---
# <a name="iportabledevicekeycollectiongetat-method"></a><span data-ttu-id="fe465-103">IPortableDeviceKeyCollection:: GetA (metodo)</span><span class="sxs-lookup"><span data-stu-id="fe465-103">IPortableDeviceKeyCollection::GetAt method</span></span>

<span data-ttu-id="fe465-104">Il metodo **Geta** recupera un **PropertyKey** dalla raccolta in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="fe465-104">The **GetAt** method retrieves a **PROPERTYKEY** from the collection by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe465-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe465-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a><span data-ttu-id="fe465-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe465-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe465-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe465-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe465-108">**DWORD** che contiene l'indice della chiave da recuperare.</span><span class="sxs-lookup"><span data-stu-id="fe465-108">**DWORD** that contains the index of the key to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="fe465-109">*pKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe465-109">*pKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe465-110">Puntatore a un oggetto **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="fe465-110">Pointer to a **PROPERTYKEY** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe465-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe465-111">Return value</span></span>

<span data-ttu-id="fe465-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fe465-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fe465-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fe465-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fe465-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fe465-114">Return code</span></span>                                                                                  | <span data-ttu-id="fe465-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe465-115">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="fe465-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe465-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fe465-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="fe465-117">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="fe465-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fe465-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fe465-119">L'indice passato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="fe465-119">The index passed in was out of range.</span></span><br/>     |
| <dl> <span data-ttu-id="fe465-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="fe465-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="fe465-121">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="fe465-121">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="fe465-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="fe465-122">Examples</span></span>

<span data-ttu-id="fe465-123">Per un esempio di come usare questo metodo, vedere [recupero di eventi del servizio supportati](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="fe465-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe465-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe465-124">Requirements</span></span>



| <span data-ttu-id="fe465-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe465-125">Requirement</span></span> | <span data-ttu-id="fe465-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fe465-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe465-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe465-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fe465-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe465-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe465-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe465-129">Library</span></span><br/> | <dl> <span data-ttu-id="fe465-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe465-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe465-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe465-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe465-132">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="fe465-132">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="fe465-133">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="fe465-133">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="fe465-134">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="fe465-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




