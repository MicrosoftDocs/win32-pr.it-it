---
title: Metodo ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice.h)
description: Ottiene la larghezza di banda effettiva corrente per il dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- Metodo GetEffectiveBandwidth API Streaming multimediale
- Metodo GetEffectiveBandwidth API Streaming multimediale, interfaccia ActiveBasicDevice
- Interfaccia ActiveBasicDevice API Streaming multimediale, metodo GetEffectiveBandwidth
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
ms.openlocfilehash: 7ac51318997e80c043e36dc87b052a5e21bf9933f93e34f2e5071fb20d4bb75b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236783"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>Metodo ActiveBasicDevice::GetEffectiveBandwidth

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

Specifica se viene recuperata la velocità di trasmissione o la velocità di ricezione.

**true per** recuperare la velocità di trasmissione. **false** per recuperare la velocità di ricezione.

</dd> <dt>

*currentSpeed* \[ Cambio\]
</dt> <dd>

Riceve la larghezza di banda effettiva corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

