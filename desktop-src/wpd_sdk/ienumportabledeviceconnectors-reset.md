---
description: Riporta all'inizio la sequenza di enumerazione.
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'Metodo IEnumPortableDeviceConnectors:: Reset (Devpkey. h)'
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
ms.openlocfilehash: 3a6846ea928afb6cd52f20098cd100b94b3a564e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319089"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="c98a3-103">Metodo IEnumPortableDeviceConnectors:: Reset</span><span class="sxs-lookup"><span data-stu-id="c98a3-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="c98a3-104">Il metodo **Reset** Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="c98a3-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="c98a3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c98a3-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="c98a3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c98a3-106">Parameters</span></span>

<span data-ttu-id="c98a3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c98a3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c98a3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c98a3-108">Return value</span></span>

<span data-ttu-id="c98a3-109">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c98a3-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c98a3-110">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c98a3-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c98a3-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c98a3-111">Return code</span></span>                                                                          | <span data-ttu-id="c98a3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c98a3-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c98a3-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c98a3-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c98a3-114">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="c98a3-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c98a3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c98a3-115">Requirements</span></span>



| <span data-ttu-id="c98a3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c98a3-116">Requirement</span></span> | <span data-ttu-id="c98a3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c98a3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c98a3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c98a3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c98a3-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c98a3-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="c98a3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c98a3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c98a3-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c98a3-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="c98a3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c98a3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c98a3-123"><dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c98a3-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="c98a3-124">IDL</span><span class="sxs-lookup"><span data-stu-id="c98a3-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c98a3-125"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c98a3-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="c98a3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c98a3-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c98a3-127"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c98a3-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="c98a3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c98a3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c98a3-129">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="c98a3-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




