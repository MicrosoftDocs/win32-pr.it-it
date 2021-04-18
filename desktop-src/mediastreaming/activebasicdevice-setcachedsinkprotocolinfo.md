---
title: Metodo ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
description: Ottiene le informazioni sul protocollo sink memorizzato nella cache per il dispositivo. | Metodo ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- API di streaming multimediale del metodo SetCachedSinkProtocolInfo
- API di streaming multimediale del metodo SetCachedSinkProtocolInfo, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo SetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321899"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a>Metodo ActiveBasicDevice:: SetCachedSinkProtocolInfo

Ottiene le informazioni sul protocollo sink memorizzato nella cache per il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCachedSinkProtocolInfo(
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

Valore della velocità in bit.

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

 

