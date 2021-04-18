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
# <a name="devicedeparture-event"></a>Evento DeviceDeparture

Si verifica quando un nuovo dispositivo viene rimosso dall'elenco di dispositivi restituiti dal metodo [**CachedDevices**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Sintassi


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) usando il metodo [**Add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) . Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .

 

 