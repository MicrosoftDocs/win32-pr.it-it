---
title: Metodo IBasicDevice CanWakeDevices
description: Recupera un valore che indica se il dispositivo può essere riattivato.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API di streaming multimediale del metodo CanWakeDevices
- API di streaming multimediale del metodo CanWakeDevices, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045808"
---
# <a name="ibasicdevicecanwakedevices-method"></a>Metodo IBasicDevice:: CanWakeDevices

Recupera un valore che indica se il dispositivo può essere riattivato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Riceve un puntatore a un valore booleano che è **true** se il dispositivo può essere riattivato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





