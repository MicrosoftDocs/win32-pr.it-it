---
description: Il metodo Clear elimina tutti gli elementi dall'insieme.
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: 'Metodo IPortableDeviceValues:: Clear (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 45c04319b5691e3bbcfb56d5a447cf2eb60bfaac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326692"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="7c6d8-103">Metodo IPortableDeviceValues:: Clear</span><span class="sxs-lookup"><span data-stu-id="7c6d8-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="7c6d8-104">Il metodo **Clear** Elimina tutti gli elementi dall'insieme.</span><span class="sxs-lookup"><span data-stu-id="7c6d8-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c6d8-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="7c6d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c6d8-106">Parameters</span></span>

<span data-ttu-id="7c6d8-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7c6d8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c6d8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c6d8-108">Return value</span></span>

<span data-ttu-id="7c6d8-109">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7c6d8-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7c6d8-110">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7c6d8-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7c6d8-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7c6d8-111">Return code</span></span>                                                                          | <span data-ttu-id="7c6d8-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c6d8-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7c6d8-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7c6d8-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7c6d8-114">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7c6d8-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c6d8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c6d8-115">Remarks</span></span>

<span data-ttu-id="7c6d8-116">Questo metodo libera la memoria per tutti gli elementi allocati dinamicamente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="7c6d8-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="7c6d8-117">Per le interfacce, viene chiamato **Release**.</span><span class="sxs-lookup"><span data-stu-id="7c6d8-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6d8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c6d8-118">Requirements</span></span>



| <span data-ttu-id="7c6d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c6d8-119">Requirement</span></span> | <span data-ttu-id="7c6d8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7c6d8-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6d8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c6d8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7c6d8-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c6d8-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c6d8-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c6d8-123">Library</span></span><br/> | <dl> <span data-ttu-id="7c6d8-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c6d8-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c6d8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c6d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6d8-126">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="7c6d8-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




