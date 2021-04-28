---
description: 'Metodo IPortableDeviceValuesCollection::GetAt: il metodo GetAt recupera un elemento dalla raccolta in base a un indice in base zero.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: Metodo IPortableDeviceValuesCollection::GetAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083259"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="99539-103">Metodo IPortableDeviceValuesCollection::GetAt</span><span class="sxs-lookup"><span data-stu-id="99539-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="99539-104">Il **metodo GetAt** recupera un elemento dalla raccolta in base a un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="99539-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="99539-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99539-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="99539-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99539-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99539-107">*dwIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="99539-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99539-108">**Valore DWORD** che specifica un indice in base zero nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="99539-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="99539-109">*valori ppValues* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="99539-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99539-110">Indirizzo di una variabile che riceve un puntatore a [**un'interfaccia IPortableDeviceValues**](iportabledevicevalues.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="99539-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="99539-111">Il chiamante è responsabile della chiamata **di Release** su questa interfaccia al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="99539-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99539-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99539-112">Return value</span></span>

<span data-ttu-id="99539-113">Il metodo restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="99539-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="99539-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="99539-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="99539-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="99539-115">Return code</span></span>                                                                                  | <span data-ttu-id="99539-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99539-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99539-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="99539-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="99539-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="99539-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="99539-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="99539-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="99539-120">L'indice in base zero passato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="99539-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="99539-121"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="99539-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="99539-122">Un argomento del puntatore obbligatorio era **NULL.**</span><span class="sxs-lookup"><span data-stu-id="99539-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="99539-123"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="99539-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="99539-124">La raccolta contiene un **puntatore** **NULL IPortableDeviceValues.**</span><span class="sxs-lookup"><span data-stu-id="99539-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="99539-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="99539-125">Remarks</span></span>

<span data-ttu-id="99539-126">Tutte le modifiche apportate ai valori nell'interfaccia recuperata verranno apportate alla versione archiviata nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="99539-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="99539-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99539-127">Requirements</span></span>



| <span data-ttu-id="99539-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="99539-128">Requirement</span></span> | <span data-ttu-id="99539-129">Valore</span><span class="sxs-lookup"><span data-stu-id="99539-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99539-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99539-130">Header</span></span><br/>  | <dl> <span data-ttu-id="99539-131"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="99539-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="99539-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="99539-132">Library</span></span><br/> | <dl> <span data-ttu-id="99539-133"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="99539-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99539-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99539-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99539-135">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="99539-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




