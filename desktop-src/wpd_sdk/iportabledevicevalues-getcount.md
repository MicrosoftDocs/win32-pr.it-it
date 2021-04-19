---
description: Il metodo GetCount Recupera il numero di elementi nella raccolta.
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'Metodo IPortableDeviceValues:: GetCount (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 710348b2f2626d39efcbdf68373d1e556ecc335c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333019"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="038f9-103">Metodo IPortableDeviceValues:: GetCount</span><span class="sxs-lookup"><span data-stu-id="038f9-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="038f9-104">Il metodo **GetCount** Recupera il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="038f9-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="038f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="038f9-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="038f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="038f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="038f9-107">*pcelt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="038f9-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="038f9-108">Puntatore a un **valore DWORD** che contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="038f9-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="038f9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="038f9-109">Return value</span></span>

<span data-ttu-id="038f9-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="038f9-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="038f9-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="038f9-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="038f9-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="038f9-112">Return code</span></span>                                                                          | <span data-ttu-id="038f9-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="038f9-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="038f9-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="038f9-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="038f9-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="038f9-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="038f9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="038f9-116">Requirements</span></span>



| <span data-ttu-id="038f9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="038f9-117">Requirement</span></span> | <span data-ttu-id="038f9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="038f9-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038f9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="038f9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="038f9-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="038f9-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="038f9-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="038f9-121">Library</span></span><br/> | <dl> <span data-ttu-id="038f9-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="038f9-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="038f9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="038f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038f9-124">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="038f9-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




