---
title: Metodo ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice. h)
description: Imposta la velocità in bit memorizzata nella cache.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- API di streaming multimediale del metodo SetCachedBitrateMeasurement
- API di streaming multimediale del metodo SetCachedBitrateMeasurement, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo SetCachedBitrateMeasurement
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
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478976"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>Metodo ActiveBasicDevice:: SetCachedBitrateMeasurement

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

*physicalNetworkInterface* \[ in\]
</dt> <dd>

Specifica l'interfaccia di rete fisica.

</dd> <dt>

*velocità in bit* \[ in\]
</dt> <dd>

Valore a cui impostare la velocità in bit.

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

 

