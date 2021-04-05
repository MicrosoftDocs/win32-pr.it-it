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
# <a name="devicearrival-event"></a>Evento DeviceArrival

Si verifica quando viene aggiunto un nuovo dispositivo all'elenco di dispositivi restituiti dal metodo [**CachedDevices**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Sintassi


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando il metodo [**Add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) . Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .

 

 