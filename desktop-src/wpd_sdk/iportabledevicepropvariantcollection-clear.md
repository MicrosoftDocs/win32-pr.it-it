---
description: Il metodo Clear libera, quindi rimuove tutti gli elementi dalla raccolta. La raccolta viene considerata vuota dopo la chiamata a questo metodo.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'Metodo IPortableDevicePropVariantCollection:: Clear (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330584"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a><span data-ttu-id="864eb-104">Metodo IPortableDevicePropVariantCollection:: Clear</span><span class="sxs-lookup"><span data-stu-id="864eb-104">IPortableDevicePropVariantCollection::Clear method</span></span>

<span data-ttu-id="864eb-105">Il metodo **Clear** libera, quindi rimuove tutti gli elementi dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="864eb-105">The **Clear** method frees, and then removes, all items from the collection.</span></span> <span data-ttu-id="864eb-106">La raccolta viene considerata vuota dopo la chiamata a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="864eb-106">The collection is considered empty after calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="864eb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="864eb-107">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="864eb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="864eb-108">Parameters</span></span>

<span data-ttu-id="864eb-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="864eb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="864eb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="864eb-110">Return value</span></span>

<span data-ttu-id="864eb-111">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="864eb-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="864eb-112">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="864eb-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="864eb-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="864eb-113">Return code</span></span>                                                                          | <span data-ttu-id="864eb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="864eb-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="864eb-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="864eb-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="864eb-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="864eb-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="864eb-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="864eb-117">Remarks</span></span>

<span data-ttu-id="864eb-118">Dopo aver chiamato **Clear**, la raccolta viene considerata senza tipo, ovvero il VarType in precedenza impostato su non limita più le operazioni di **aggiunta** .</span><span class="sxs-lookup"><span data-stu-id="864eb-118">After calling **Clear**, the collection is considered type-less, meaning that the VARTYPE it was previously set to is no longer restricting **Add** operations.</span></span> <span data-ttu-id="864eb-119">Una chiamata a **Add** dopo aver chiamato **Clear** viene considerata l' **aggiunta** "First" per questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="864eb-119">A call to **Add** after calling **Clear** is considered the "first" **Add** for this collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="864eb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="864eb-120">Requirements</span></span>



| <span data-ttu-id="864eb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="864eb-121">Requirement</span></span> | <span data-ttu-id="864eb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="864eb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="864eb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="864eb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="864eb-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="864eb-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="864eb-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="864eb-125">Library</span></span><br/> | <dl> <span data-ttu-id="864eb-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="864eb-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="864eb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="864eb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="864eb-128">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="864eb-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




