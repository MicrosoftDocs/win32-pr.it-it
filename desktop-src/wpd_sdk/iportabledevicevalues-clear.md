---
description: 'Metodo IPortableDeviceValues::Clear: il metodo Clear elimina tutti gli elementi dalla raccolta.'
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: Metodo IPortableDeviceValues::Clear (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8e1df59cd972bc470607ac2b49d05f43dba8b3a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109899"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="82631-103">Metodo IPortableDeviceValues::Clear</span><span class="sxs-lookup"><span data-stu-id="82631-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="82631-104">Il **metodo Clear** elimina tutti gli elementi dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="82631-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="82631-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82631-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="82631-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82631-106">Parameters</span></span>

<span data-ttu-id="82631-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="82631-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82631-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82631-108">Return value</span></span>

<span data-ttu-id="82631-109">Il metodo restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="82631-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="82631-110">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="82631-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="82631-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="82631-111">Return code</span></span>                                                                          | <span data-ttu-id="82631-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82631-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="82631-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82631-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="82631-114">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="82631-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="82631-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="82631-115">Remarks</span></span>

<span data-ttu-id="82631-116">Questo metodo libera la memoria per tutti gli elementi allocati dinamicamente nella raccolta .</span><span class="sxs-lookup"><span data-stu-id="82631-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="82631-117">Per le interfacce, chiama **Release.**</span><span class="sxs-lookup"><span data-stu-id="82631-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="82631-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82631-118">Requirements</span></span>



| <span data-ttu-id="82631-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="82631-119">Requirement</span></span> | <span data-ttu-id="82631-120">Valore</span><span class="sxs-lookup"><span data-stu-id="82631-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82631-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82631-121">Header</span></span><br/>  | <dl> <span data-ttu-id="82631-122"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="82631-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="82631-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="82631-123">Library</span></span><br/> | <dl> <span data-ttu-id="82631-124"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="82631-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82631-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82631-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82631-126">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="82631-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




