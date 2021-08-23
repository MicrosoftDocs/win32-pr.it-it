---
title: Evento DeviceArrival
description: Si verifica quando un nuovo dispositivo viene aggiunto all'elenco di dispositivi restituiti dal metodo CachedDevices.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- API Di streaming multimediale dell'evento DeviceArrival
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed65c2b1c37eb91f9bf0a0c060fb76b85cd1f5b3d06b6ff1ab795ec89a0db6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721211"
---
# <a name="devicearrival-event"></a>Evento DeviceArrival

Si verifica quando un nuovo dispositivo viene aggiunto all'elenco di dispositivi restituiti dal [**metodo CachedDevices.**](idevicecontroller-cacheddevices.md)

## <a name="syntax"></a>Sintassi


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando [**il metodo add \_ DeviceArrival.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) Per annullare la registrazione del gestore eventi, usare [**il \_ metodo remove DeviceArrival.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival)

 

 