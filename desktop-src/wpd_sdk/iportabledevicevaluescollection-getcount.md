---
description: Il metodo GetCount Recupera il numero di elementi nella raccolta.
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'Metodo IPortableDeviceValuesCollection:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5d1eabdcf73d65b42ccff980b15bb15514c3b322
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324506"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="8b31c-103">Metodo IPortableDeviceValuesCollection:: GetCount</span><span class="sxs-lookup"><span data-stu-id="8b31c-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="8b31c-104">Il metodo **GetCount** Recupera il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="8b31c-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b31c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b31c-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="8b31c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b31c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b31c-107">*pcElems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b31c-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b31c-108">Puntatore a un **valore DWORD** che contiene il numero di interfacce **IPortableDeviceValues** nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="8b31c-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b31c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b31c-109">Return value</span></span>

<span data-ttu-id="8b31c-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8b31c-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8b31c-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8b31c-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8b31c-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8b31c-112">Return code</span></span>                                                                               | <span data-ttu-id="8b31c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b31c-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="8b31c-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b31c-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8b31c-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8b31c-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="8b31c-116"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="8b31c-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="8b31c-117">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="8b31c-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8b31c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b31c-118">Requirements</span></span>



| <span data-ttu-id="8b31c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b31c-119">Requirement</span></span> | <span data-ttu-id="8b31c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8b31c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b31c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b31c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8b31c-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b31c-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b31c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b31c-123">Library</span></span><br/> | <dl> <span data-ttu-id="8b31c-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b31c-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b31c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b31c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b31c-126">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="8b31c-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




