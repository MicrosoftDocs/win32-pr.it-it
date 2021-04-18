---
description: Il metodo Add aggiunge un elemento alla raccolta.
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'Metodo IPortableDeviceValuesCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f423ac7243c8d16fa75978ae5c9bcf04136bb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324512"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="4f2e1-103">Metodo IPortableDeviceValuesCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="4f2e1-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="4f2e1-104">Il metodo **Add** aggiunge un elemento alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4f2e1-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f2e1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f2e1-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="4f2e1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f2e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f2e1-107">*pvalues* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f2e1-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f2e1-108">Puntatore a un'interfaccia **IPortableDeviceValues** da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4f2e1-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="4f2e1-109">L'interfaccia non viene effettivamente copiata, ma viene chiamato **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="4f2e1-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f2e1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f2e1-110">Return value</span></span>

<span data-ttu-id="4f2e1-111">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4f2e1-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4f2e1-112">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4f2e1-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4f2e1-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4f2e1-113">Return code</span></span>                                                                                   | <span data-ttu-id="4f2e1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f2e1-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f2e1-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f2e1-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4f2e1-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="4f2e1-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="4f2e1-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="4f2e1-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4f2e1-118">La memoria disponibile non è sufficiente per aggiungere il valore alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4f2e1-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4f2e1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f2e1-119">Requirements</span></span>



| <span data-ttu-id="4f2e1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f2e1-120">Requirement</span></span> | <span data-ttu-id="4f2e1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4f2e1-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f2e1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f2e1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4f2e1-123"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f2e1-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f2e1-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f2e1-124">Library</span></span><br/> | <dl> <span data-ttu-id="4f2e1-125"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f2e1-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f2e1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f2e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f2e1-127">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="4f2e1-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




