---
description: La proprietà PKEY \_ AudioEndpoint \_ Supports EventDriven Mode indica se \_ l'endpoint supporta la modalità guidata da \_ eventi.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 280be65d4ae8e0b557bd96320ea31f67ba75657ecb5b685608bd2c314e10836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758921"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>PKEY \_ AudioEndpoint \_ supporta la modalità \_ EventDriven \_

La **proprietà PKEY \_ AudioEndpoint \_ Supports \_ EventDriven \_ Mode** indica se l'endpoint supporta la modalità guidata da eventi.

Il **membro vt** della **struttura PROPVARIANT** è impostato su VT \_ UI4.

Il **membro uintVal** della **struttura PROPVARIANT** è un **valore DWORD** che indica se l'endpoint supporta la modalità basata su eventi.

## <a name="remarks"></a>Commenti

Questo valore della proprietà viene popolato da un OEM audio in un file con estensione inf per indicare che l'hardware HDAudio supporta la modalità basata su eventi in base al requisito WHQL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà dell'endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio di base](core-audio-properties.md)
</dt> </dl>

 

 




