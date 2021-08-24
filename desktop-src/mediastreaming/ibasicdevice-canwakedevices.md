---
title: Metodo IBasicDevice CanWakeDevices
description: Recupera un valore che indica se il dispositivo può essere riattivato.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- Metodo CanWakeDevices API Streaming multimediale
- Metodo CanWakeDevices API Streaming multimediale, interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale, metodo CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ebd0cfe9bf773d78297454d4a7643a74c3d6ea23aea01eeb54cd5c014ce73e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847671"
---
# <a name="ibasicdevicecanwakedevices-method"></a>Metodo IBasicDevice::CanWakeDevices

Recupera un valore che indica se il dispositivo può essere riattivato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Cambio\]
</dt> <dd>

Riceve un puntatore a un valore booleano **true se** il dispositivo può essere riattivato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





