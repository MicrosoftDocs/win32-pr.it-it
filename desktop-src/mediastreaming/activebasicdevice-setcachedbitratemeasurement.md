---
title: Metodo ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice.h)
description: Imposta la velocità in bit memorizzata nella cache.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- Metodo SetCachedBitrateMeasurement API streaming multimediale
- Metodo SetCachedBitrateMeasurement API Streaming multimediale , interfaccia ActiveBasicDevice
- Interfaccia ActiveBasicDevice API Streaming multimediale, metodo SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf79b7e9066aacfcce1f82c998463d6d620f5061fef4af788104a0c01a44ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952771"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>Metodo ActiveBasicDevice::SetCachedBitrateMeasurement

Imposta la velocità in bit memorizzata nella cache.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*physicalNetworkInterface* \[ Pollici\]
</dt> <dd>

Specifica l'interfaccia di rete fisica.

</dd> <dt>

*velocità in bit* \[ Pollici\]
</dt> <dd>

Valore su cui impostare la velocità in bit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

