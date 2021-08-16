---
title: Proprietà ActiveBasicDevice MaxVolume (PlayToDevice.h)
description: Ottiene il volume massimo supportato dal dispositivo.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- Proprietà MaxVolume API Streaming multimediale
- Proprietà MaxVolume API Streaming multimediale, interfaccia ActiveBasicDevice
- Interfaccia ActiveBasicDevice API Streaming multimediale, proprietà MaxVolume
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 803e2e66306bce0d6fd308501edece61668d5f2e0d8041273d508b662f6cd66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736197"
---
# <a name="activebasicdevicemaxvolume-property"></a>Proprietà ActiveBasicDevice::MaxVolume

Ottiene il volume massimo supportato dal dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a **un oggetto UINT32** che specifica il volume massimo supportato dal dispositivo.

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

 

