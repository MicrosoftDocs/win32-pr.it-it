---
title: Evento DeviceArrival
description: Si verifica quando viene aggiunto un nuovo dispositivo all'elenco di dispositivi restituiti dal metodo CachedDevices.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- API di streaming multimediale per gli eventi DeviceArrival
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79fbdd68ae6c77c6a0f3e7bbd3cf976b5d056987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725394"
---
# <a name="devicearrival-event"></a><span data-ttu-id="5c7af-104">Evento DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="5c7af-104">DeviceArrival event</span></span>

<span data-ttu-id="5c7af-105">Si verifica quando viene aggiunto un nuovo dispositivo all'elenco di dispositivi restituiti dal metodo [**CachedDevices**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="5c7af-105">Occurs when a new device is added to the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7af-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c7af-106">Syntax</span></span>


```C++
void DeviceArrival();
```



## <a name="parameters"></a><span data-ttu-id="5c7af-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c7af-107">Parameters</span></span>

<span data-ttu-id="5c7af-108">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="5c7af-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c7af-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c7af-109">Return value</span></span>

<span data-ttu-id="5c7af-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5c7af-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c7af-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c7af-111">Remarks</span></span>

<span data-ttu-id="5c7af-112">Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando il metodo [**Add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="5c7af-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) method.</span></span> <span data-ttu-id="5c7af-113">Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="5c7af-113">To unregister the event handler, use the [**remove\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) method.</span></span>

 

 