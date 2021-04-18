---
title: DeviceController. CachedDevices, metodo
description: Recupera una raccolta di puntatori dell'interfaccia IBasicDevice che rappresenta la visualizzazione memorizzata nella cache di tutti i dispositivi DLNA individuabili. | DeviceController. CachedDevices, metodo
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- API di streaming multimediale del metodo CachedDevices
- API di streaming multimediale del metodo CachedDevices, interfaccia DeviceController
- API di streaming multimediale dell'interfaccia DeviceController, metodo CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321558"
---
# <a name="devicecontrollercacheddevices-method"></a><span data-ttu-id="37ec4-107">DeviceController. CachedDevices, metodo</span><span class="sxs-lookup"><span data-stu-id="37ec4-107">DeviceController.CachedDevices method</span></span>

<span data-ttu-id="37ec4-108">Recupera una raccolta di puntatori dell'interfaccia [**IBasicDevice**](ibasicdevice.md) che rappresenta la visualizzazione memorizzata nella cache di tutti i dispositivi DLNA individuabili.</span><span class="sxs-lookup"><span data-stu-id="37ec4-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ec4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37ec4-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="37ec4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ec4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ec4-111">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="37ec4-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37ec4-112">Riceve una raccolta enumerabile di puntatori dell'interfaccia [**IBasicDevice**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="37ec4-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ec4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37ec4-113">Return value</span></span>

<span data-ttu-id="37ec4-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="37ec4-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="37ec4-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="37ec4-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="37ec4-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="37ec4-116">Return code</span></span>                                                                          | <span data-ttu-id="37ec4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37ec4-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="37ec4-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="37ec4-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="37ec4-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="37ec4-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="37ec4-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37ec4-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="37ec4-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37ec4-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span></span>
</dt> </dl>

 

