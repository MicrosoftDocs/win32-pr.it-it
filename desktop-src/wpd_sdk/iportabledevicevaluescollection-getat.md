---
description: Il metodo GetA recupera un elemento dalla raccolta in base a un indice in base zero.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'Metodo IPortableDeviceValuesCollection:: GetA (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324511"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="a97b9-103">IPortableDeviceValuesCollection:: GetA (metodo)</span><span class="sxs-lookup"><span data-stu-id="a97b9-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="a97b9-104">Il metodo **Geta** recupera un elemento dalla raccolta in base a un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="a97b9-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a97b9-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="a97b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a97b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97b9-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a97b9-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a97b9-108">**DWORD** che specifica un indice in base zero nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="a97b9-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a97b9-109">*ppValues* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a97b9-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a97b9-110">Indirizzo di una variabile che riceve un puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="a97b9-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="a97b9-111">Il chiamante è responsabile della richiamata della **versione** su questa interfaccia quando viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="a97b9-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a97b9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a97b9-112">Return value</span></span>

<span data-ttu-id="a97b9-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a97b9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a97b9-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a97b9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a97b9-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a97b9-115">Return code</span></span>                                                                                  | <span data-ttu-id="a97b9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a97b9-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a97b9-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a97b9-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a97b9-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a97b9-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="a97b9-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a97b9-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a97b9-120">L'indice in base zero passato non era compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="a97b9-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="a97b9-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a97b9-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="a97b9-122">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="a97b9-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="a97b9-123"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="a97b9-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="a97b9-124">La raccolta contiene un puntatore **IPortableDeviceValues** **null** .</span><span class="sxs-lookup"><span data-stu-id="a97b9-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a97b9-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a97b9-125">Remarks</span></span>

<span data-ttu-id="a97b9-126">Tutte le modifiche apportate ai valori nell'interfaccia recuperata verranno apportate alla versione archiviata nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="a97b9-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="a97b9-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a97b9-127">Requirements</span></span>



| <span data-ttu-id="a97b9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a97b9-128">Requirement</span></span> | <span data-ttu-id="a97b9-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a97b9-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a97b9-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a97b9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a97b9-131"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a97b9-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a97b9-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="a97b9-132">Library</span></span><br/> | <dl> <span data-ttu-id="a97b9-133"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a97b9-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a97b9-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a97b9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a97b9-135">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="a97b9-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




