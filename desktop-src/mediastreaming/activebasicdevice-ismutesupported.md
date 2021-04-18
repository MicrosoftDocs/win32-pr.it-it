---
title: Proprietà ActiveBasicDevice IsMuteSupported (PlayToDevice. h)
description: Ottiene un valore che indica se il dispositivo supporta la soppressione dell'audio.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- API di streaming multimediale della proprietà IsMuteSupported
- API di streaming multimediale della proprietà IsMuteSupported, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà IsMuteSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcec2e4520bd3b15b715c01e4369da87887355e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477369"
---
# <a name="activebasicdeviceismutesupported-property"></a>Proprietà ActiveBasicDevice:: IsMuteSupported

Ottiene un valore che indica se il dispositivo supporta la soppressione dell'audio.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un **valore booleano** che indica se il dispositivo supporta la soppressione dell'audio.

**true** se il dispositivo supporta la soppressione dell'audio; in caso contrario, **false**.

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

 

