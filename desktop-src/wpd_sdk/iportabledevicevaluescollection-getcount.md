---
description: 'Metodo IPortableDeviceValuesCollection::GetCount: il metodo GetCount recupera il numero di elementi nella raccolta.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: Metodo IPortableDeviceValuesCollection::GetCount (PortableDeviceTypes.h)
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
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083179"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="12d72-103">Metodo IPortableDeviceValuesCollection::GetCount</span><span class="sxs-lookup"><span data-stu-id="12d72-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="12d72-104">Il **metodo GetCount** recupera il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="12d72-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d72-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12d72-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="12d72-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12d72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d72-107">*pcElems* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="12d72-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d72-108">Puntatore a **un valore DWORD** che contiene il **numero di interfacce IPortableDeviceValues** nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="12d72-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d72-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12d72-109">Return value</span></span>

<span data-ttu-id="12d72-110">Il metodo restituisce un **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="12d72-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="12d72-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="12d72-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="12d72-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="12d72-112">Return code</span></span>                                                                               | <span data-ttu-id="12d72-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12d72-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="12d72-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12d72-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="12d72-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="12d72-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="12d72-116"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="12d72-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="12d72-117">Un argomento del puntatore obbligatorio era **NULL.**</span><span class="sxs-lookup"><span data-stu-id="12d72-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="12d72-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12d72-118">Requirements</span></span>



| <span data-ttu-id="12d72-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d72-119">Requirement</span></span> | <span data-ttu-id="12d72-120">Valore</span><span class="sxs-lookup"><span data-stu-id="12d72-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d72-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12d72-121">Header</span></span><br/>  | <dl> <span data-ttu-id="12d72-122"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="12d72-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="12d72-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="12d72-123">Library</span></span><br/> | <dl> <span data-ttu-id="12d72-124"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="12d72-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d72-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12d72-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d72-126">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="12d72-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




