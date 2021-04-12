---
title: Metodo ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice. h)
description: Ottiene la velocità in bit memorizzata nella cache.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API di streaming multimediale del metodo GetCachedBitrateMeasurement
- API di streaming multimediale del metodo GetCachedBitrateMeasurement, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo GetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518700"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a>Metodo ActiveBasicDevice:: GetCachedBitrateMeasurement

Ottiene la velocità in bit memorizzata nella cache.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*physicalNetworkInterface* \[ in\]
</dt> <dd>

Specifica l'interfaccia di rete fisica.

</dd> <dt>

*velocità in bit* \[ out, retval\]
</dt> <dd>

Riceve il valore di velocità in bit.

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

 

