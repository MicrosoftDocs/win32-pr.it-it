---
title: Metodo ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice.h)
description: Ottiene le informazioni del protocollo sink memorizzate nella cache per il dispositivo. | Metodo ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice.h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- Metodo GetCachedSinkProtocolInfo API Streaming multimediale
- Metodo GetCachedSinkProtocolInfo API Streaming multimediale, interfaccia ActiveBasicDevice
- Metodo GetCachedSinkProtocolInfo dell'interfaccia ActiveBasicDevice
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a9ebda71f59dc4bd887479b5ff9e763844b32985736f8cf224ed4981f04b34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736397"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a>Metodo ActiveBasicDevice::GetCachedSinkProtocolInfo

Ottiene le informazioni del protocollo sink memorizzate nella cache per il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Informazioni sul protocollo sink memorizzato nella cache per il dispositivo.

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

 

