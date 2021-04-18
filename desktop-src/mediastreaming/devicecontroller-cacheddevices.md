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
# <a name="devicecontrollercacheddevices-method"></a>DeviceController. CachedDevices, metodo

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

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

