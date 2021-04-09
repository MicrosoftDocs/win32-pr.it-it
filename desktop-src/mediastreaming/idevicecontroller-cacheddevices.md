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
# <a name="idevicecontrollercacheddevices-method"></a>Metodo IDeviceController:: CachedDevices

Recupera una raccolta di puntatori dell'interfaccia [**IBasicDevice**](ibasicdevice.md) che rappresenta la visualizzazione memorizzata nella cache di tutti i dispositivi DLNA individuabili.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve una raccolta enumerabile di puntatori dell'interfaccia [**IBasicDevice**](ibasicdevice.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

