---
title: Evento DeviceDeparture
description: Si verifica quando un nuovo dispositivo viene rimosso dall'elenco di dispositivi restituito dal metodo CachedDevices.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- Api Streaming multimediale dell'evento DeviceDeparture
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496fa0fcae3cba51228b37b5f06eb9b06c416322aad22f77be542274088eae32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712951"
---
# <a name="devicedeparture-event"></a>Evento DeviceDeparture

Si verifica quando un nuovo dispositivo viene rimosso dall'elenco di dispositivi restituito dal [**metodo CachedDevices.**](idevicecontroller-cacheddevices.md)

## <a name="syntax"></a>Sintassi


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando [**il metodo add \_ DeviceDeparture.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) Per annullare la registrazione del gestore eventi, usare [**il \_ metodo remove DeviceDeparture.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture)

 

 