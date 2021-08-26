---
title: Metodo IDeviceController CachedDevices
description: Recupera una raccolta di puntatori all'interfaccia IBasicDevice che rappresenta la visualizzazione memorizzata nella cache di tutti i dispositivi DLNA individuabili. | Metodo IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- Metodo CachedDevices API Streaming multimediale
- Metodo CachedDevices API streaming multimediale, interfaccia IDeviceController
- Interfaccia IDeviceController API Streaming multimediale, metodo CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c624597fb88a45cc9ff91770f164e7c6e6e83ff5eb1b6369ded9d0fc1bbc225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952641"
---
# <a name="idevicecontrollercacheddevices-method"></a>Metodo IDeviceController::CachedDevices

Recupera una raccolta di [**puntatori all'interfaccia IBasicDevice**](ibasicdevice.md) che rappresenta la visualizzazione memorizzata nella cache di tutti i dispositivi DLNA individuabili.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve una raccolta enumerabile di puntatori [**a interfaccia IBasicDevice.**](ibasicdevice.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

