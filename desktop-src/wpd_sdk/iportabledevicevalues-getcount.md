---
description: 'Metodo IPortableDeviceValues::GetCount: il metodo GetCount recupera il numero di elementi nella raccolta.'
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: Metodo IPortableDeviceValues::GetCount (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086239"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="6ee19-103">Metodo IPortableDeviceValues::GetCount</span><span class="sxs-lookup"><span data-stu-id="6ee19-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="6ee19-104">Il **metodo GetCount** recupera il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ee19-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee19-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ee19-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="6ee19-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ee19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee19-107">*pcelt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6ee19-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee19-108">Puntatore a **un valore DWORD** che contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6ee19-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee19-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ee19-109">Return value</span></span>

<span data-ttu-id="6ee19-110">Il metodo restituisce un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6ee19-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6ee19-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6ee19-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6ee19-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6ee19-112">Return code</span></span>                                                                          | <span data-ttu-id="6ee19-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ee19-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6ee19-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ee19-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6ee19-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6ee19-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6ee19-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ee19-116">Requirements</span></span>



| <span data-ttu-id="6ee19-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee19-117">Requirement</span></span> | <span data-ttu-id="6ee19-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6ee19-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee19-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ee19-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6ee19-120"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee19-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ee19-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="6ee19-121">Library</span></span><br/> | <dl> <span data-ttu-id="6ee19-122"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ee19-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee19-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ee19-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee19-124">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="6ee19-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




