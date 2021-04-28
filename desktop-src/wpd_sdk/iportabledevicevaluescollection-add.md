---
description: 'Metodo IPortableDeviceValuesCollection::Add: il metodo Add aggiunge un elemento alla raccolta.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: Metodo IPortableDeviceValuesCollection::Add (PortableDeviceTypes.h)
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
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083242"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="205a5-103">Metodo IPortableDeviceValuesCollection::Add</span><span class="sxs-lookup"><span data-stu-id="205a5-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="205a5-104">Il **metodo Add** aggiunge un elemento alla raccolta .</span><span class="sxs-lookup"><span data-stu-id="205a5-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="205a5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="205a5-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="205a5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="205a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205a5-107">*pValues* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="205a5-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205a5-108">Puntatore a **un'interfaccia IPortableDeviceValues** da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="205a5-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="205a5-109">L'interfaccia non viene effettivamente copiata, **ma su di** essa viene chiamato AddRef.</span><span class="sxs-lookup"><span data-stu-id="205a5-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="205a5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="205a5-110">Return value</span></span>

<span data-ttu-id="205a5-111">Il metodo restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="205a5-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="205a5-112">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="205a5-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="205a5-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="205a5-113">Return code</span></span>                                                                                   | <span data-ttu-id="205a5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="205a5-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="205a5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="205a5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="205a5-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="205a5-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="205a5-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="205a5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="205a5-118">La memoria disponibile non è sufficiente per aggiungere il valore alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="205a5-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="205a5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="205a5-119">Requirements</span></span>



| <span data-ttu-id="205a5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="205a5-120">Requirement</span></span> | <span data-ttu-id="205a5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="205a5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205a5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="205a5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="205a5-123"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="205a5-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="205a5-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="205a5-124">Library</span></span><br/> | <dl> <span data-ttu-id="205a5-125"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="205a5-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="205a5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="205a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205a5-127">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="205a5-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




