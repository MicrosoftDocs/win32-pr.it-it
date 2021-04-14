---
title: Metodo ActiveBasicDevice GetCachedExtraSinkProtocolInfo (PlayToDevice. h)
description: Ottiene informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- API di streaming multimediale del metodo GetCachedExtraSinkProtocolInfo
- API di streaming multimediale del metodo GetCachedExtraSinkProtocolInfo, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo GetCachedExtraSinkProtocolInfo
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
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400720"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a>Metodo ActiveBasicDevice:: GetCachedExtraSinkProtocolInfo

Ottiene informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out, retval\]
</dt> <dd>

Informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.

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

 

