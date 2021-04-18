---
title: Proprietà ActiveBasicDevice IsImageSupported (PlayToDevice. h)
description: Ottiene un valore che indica se il dispositivo supporta le immagini.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- API di streaming multimediale della proprietà IsImageSupported
- API di streaming multimediale della proprietà IsImageSupported, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà IsImageSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e90f51d2dd59ffec8221787b9ee7c247536abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301026"
---
# <a name="activebasicdeviceisimagesupported-property"></a>Proprietà ActiveBasicDevice:: IsImageSupported

Ottiene un valore che indica se il dispositivo supporta le immagini.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un **valore booleano** che indica se il dispositivo supporta le immagini.

**true** se il dispositivo supporta le immagini; in caso contrario, **false**.

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

 

