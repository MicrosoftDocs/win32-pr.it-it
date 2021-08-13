---
title: Proprietà ActiveBasicDevice IsAudioSupported (PlayToDevice.h)
description: Ottiene un valore che indica se il dispositivo supporta l'audio.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- Proprietà IsAudioSupported API Streaming multimediale
- Proprietà IsAudioSupported API Streaming multimediale, interfaccia ActiveBasicDevice
- Interfaccia ActiveBasicDevice API Streaming multimediale , proprietà IsAudioSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20125114b6cd134d153ad6425af5af410faf524714a2e505a37fbf57dcda21e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462425"
---
# <a name="activebasicdeviceisaudiosupported-property"></a>Proprietà ActiveBasicDevice::IsAudioSupported

Ottiene un valore che indica se il dispositivo supporta l'audio.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un **valore booleano** che indica se il dispositivo supporta l'audio.

**true** se il dispositivo supporta l'audio; in caso contrario, **false**.

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

 

