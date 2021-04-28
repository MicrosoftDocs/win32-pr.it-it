---
description: "Metodo IEnumPortableDeviceConnectors::Reset: reimposta la sequenza di enumerazione all'inizio."
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: Metodo IEnumPortableDeviceConnectors::Reset (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083208"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="5ac11-103">Metodo IEnumPortableDeviceConnectors::Reset</span><span class="sxs-lookup"><span data-stu-id="5ac11-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="5ac11-104">Il **metodo Reset** reimposta la sequenza di enumerazione all'inizio.</span><span class="sxs-lookup"><span data-stu-id="5ac11-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac11-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ac11-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="5ac11-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ac11-106">Parameters</span></span>

<span data-ttu-id="5ac11-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5ac11-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ac11-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ac11-108">Return value</span></span>

<span data-ttu-id="5ac11-109">Il metodo restituisce un **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5ac11-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5ac11-110">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5ac11-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5ac11-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5ac11-111">Return code</span></span>                                                                          | <span data-ttu-id="5ac11-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ac11-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5ac11-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac11-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5ac11-114">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5ac11-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5ac11-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ac11-115">Requirements</span></span>



| <span data-ttu-id="5ac11-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac11-116">Requirement</span></span> | <span data-ttu-id="5ac11-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5ac11-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac11-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac11-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac11-119">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ac11-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="5ac11-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac11-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac11-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ac11-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="5ac11-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ac11-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac11-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="5ac11-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="5ac11-124">Idl</span><span class="sxs-lookup"><span data-stu-id="5ac11-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ac11-125"><dt>Portabledeviceconnectapi.idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ac11-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="5ac11-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ac11-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ac11-127"><dt>PortableDeviceGuids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ac11-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="5ac11-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ac11-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac11-129">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="5ac11-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




