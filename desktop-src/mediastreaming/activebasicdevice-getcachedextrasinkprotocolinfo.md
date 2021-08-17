---
title: Metodo ActiveBasicDevice GetCachedExtraSinkProtocolInfo (PlayToDevice.h)
description: Ottiene informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- Metodo GetCachedExtraSinkProtocolInfo API di streaming multimediale
- Metodo GetCachedExtraSinkProtocolInfo API di streaming multimediale, interfaccia ActiveBasicDevice
- Interfaccia ActiveBasicDevice API Streaming multimediale, metodo GetCachedExtraSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf4508c40fd0abcb0df809216a9bae1d8811c8a8bd79bfb31dfbbd5062ddce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736407"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a>Metodo ActiveBasicDevice::GetCachedExtraSinkProtocolInfo

Ottiene informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.

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

 

