---
title: Metodo DeviceController.CachedDevices
description: Recupera una raccolta di puntatori all'interfaccia IBasicDevice che rappresenta la visualizzazione memorizzata nella cache di tutti i dispositivi DLNA individuabili. | Metodo DeviceController.CachedDevices
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- Metodo CachedDevices API Streaming multimediale
- Metodo CachedDevices API Streaming multimediale, interfaccia DeviceController
- Interfaccia DeviceController API Streaming multimediale, metodo CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86e2c4209649450fb3a8df46cde151a0b9899cd26e58bfc0b35fd7ac6e7d02b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236361"
---
# <a name="devicecontrollercacheddevices-method"></a>Metodo DeviceController.CachedDevices

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

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

