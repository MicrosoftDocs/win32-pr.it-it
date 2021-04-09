---
title: Metodo IDeviceController CachedDevices
description: Recupera una raccolta di puntatori dell'interfaccia IBasicDevice che rappresenta la visualizzazione memorizzata nella cache di tutti i dispositivi DLNA individuabili. | Metodo IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- API di streaming multimediale del metodo CachedDevices
- API di streaming multimediale del metodo CachedDevices, interfaccia IDeviceController
- API di streaming multimediale dell'interfaccia IDeviceController, metodo CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969272"
---
# <a name="idevicecontrollercacheddevices-method"></a><span data-ttu-id="cda6c-107">Metodo IDeviceController:: CachedDevices</span><span class="sxs-lookup"><span data-stu-id="cda6c-107">IDeviceController::CachedDevices method</span></span>

<span data-ttu-id="cda6c-108">Recupera una raccolta di puntatori dell'interfaccia [**IBasicDevice**](ibasicdevice.md) che rappresenta la visualizzazione memorizzata nella cache di tutti i dispositivi DLNA individuabili.</span><span class="sxs-lookup"><span data-stu-id="cda6c-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda6c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cda6c-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="cda6c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cda6c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda6c-111">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="cda6c-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cda6c-112">Riceve una raccolta enumerabile di puntatori dell'interfaccia [**IBasicDevice**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="cda6c-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda6c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cda6c-113">Return value</span></span>

<span data-ttu-id="cda6c-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cda6c-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cda6c-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cda6c-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cda6c-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cda6c-116">Return code</span></span>                                                                          | <span data-ttu-id="cda6c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cda6c-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cda6c-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cda6c-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cda6c-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="cda6c-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="cda6c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cda6c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda6c-121">**IDeviceController**</span><span class="sxs-lookup"><span data-stu-id="cda6c-121">**IDeviceController**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

