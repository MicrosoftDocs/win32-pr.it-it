---
description: Il metodo GetCount Recupera il numero di chiavi nella raccolta.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'Metodo IPortableDeviceKeyCollection:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332113"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a><span data-ttu-id="9a9f8-103">Metodo IPortableDeviceKeyCollection:: GetCount</span><span class="sxs-lookup"><span data-stu-id="9a9f8-103">IPortableDeviceKeyCollection::GetCount method</span></span>

<span data-ttu-id="9a9f8-104">Il metodo **GetCount** Recupera il numero di chiavi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-104">The **GetCount** method retrieves the number of keys in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a9f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a9f8-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="9a9f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a9f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a9f8-107">*pcElems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a9f8-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9f8-108">Puntatore a un **valore DWORD** che contiene il numero di chiavi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-108">Pointer to a **DWORD** that contains the number of keys in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a9f8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a9f8-109">Return value</span></span>

<span data-ttu-id="9a9f8-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9a9f8-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9a9f8-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9a9f8-112">Return code</span></span>                                                                               | <span data-ttu-id="9a9f8-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a9f8-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="9a9f8-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a9f8-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="9a9f8-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="9a9f8-116"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="9a9f8-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="9a9f8-117">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="9a9f8-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="9a9f8-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="9a9f8-118">Examples</span></span>

<span data-ttu-id="9a9f8-119">Per un esempio di come usare questo metodo, vedere [recupero di eventi del servizio supportati](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="9a9f8-119">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a9f8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a9f8-120">Requirements</span></span>



| <span data-ttu-id="9a9f8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a9f8-121">Requirement</span></span> | <span data-ttu-id="9a9f8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9a9f8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a9f8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a9f8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9a9f8-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a9f8-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a9f8-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a9f8-125">Library</span></span><br/> | <dl> <span data-ttu-id="9a9f8-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a9f8-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a9f8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a9f8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a9f8-128">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="9a9f8-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="9a9f8-129">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="9a9f8-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="9a9f8-130">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="9a9f8-130">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




