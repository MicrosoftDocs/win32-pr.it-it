---
title: Metodo ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice. h)
description: Ottiene la larghezza di banda effettiva corrente per il dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API di streaming multimediale del metodo GetEffectiveBandwidth
- API di streaming multimediale del metodo GetEffectiveBandwidth, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo GetEffectiveBandwidth
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048715"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>Metodo ActiveBasicDevice:: GetEffectiveBandwidth

Ottiene la larghezza di banda effettiva corrente per il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*transmitSpeed* \[ in, retval\]
</dt> <dd>

Specifica se viene recuperata la velocità di trasmissione o se viene recuperata la velocità di ricezione.

**true** per recuperare la velocità di trasmissione. **false** per recuperare la velocità di ricezione.

</dd> <dt>

*currentSpeed* \[ out\]
</dt> <dd>

Riceve la larghezza di banda effettiva corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

