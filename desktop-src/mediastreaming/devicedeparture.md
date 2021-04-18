---
title: Evento DeviceDeparture
description: Si verifica quando un nuovo dispositivo viene rimosso dall'elenco di dispositivi restituiti dal metodo CachedDevices.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- API di streaming multimediale per gli eventi DeviceDeparture
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299690"
---
# <a name="devicedeparture-event"></a><span data-ttu-id="69131-104">Evento DeviceDeparture</span><span class="sxs-lookup"><span data-stu-id="69131-104">DeviceDeparture event</span></span>

<span data-ttu-id="69131-105">Si verifica quando un nuovo dispositivo viene rimosso dall'elenco di dispositivi restituiti dal metodo [**CachedDevices**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="69131-105">Occurs when a new device is removed from the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="69131-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69131-106">Syntax</span></span>


```C++
void DeviceDeparture();
```



## <a name="parameters"></a><span data-ttu-id="69131-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="69131-107">Parameters</span></span>

<span data-ttu-id="69131-108">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="69131-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69131-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69131-109">Return value</span></span>

<span data-ttu-id="69131-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="69131-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69131-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="69131-111">Remarks</span></span>

<span data-ttu-id="69131-112">Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando il metodo [**Add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="69131-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) method.</span></span> <span data-ttu-id="69131-113">Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="69131-113">To unregister the event handler, use the [**remove\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) method.</span></span>

 

 