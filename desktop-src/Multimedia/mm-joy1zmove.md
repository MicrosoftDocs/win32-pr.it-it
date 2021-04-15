---
title: Messaggio MM_JOY1ZMOVE (mmsystem. h)
description: Il \_ messaggio mm JOY1ZMOVE notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che la posizione del joystick sull'asse z è cambiata.
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- MM_JOY1ZMOVE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_JOY1ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d4db3db8c1817f0502ce14cc5328ad666b32c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479384"
---
# <a name="mm_joy1zmove-message"></a>\_Messaggio JOY1ZMOVE mm

Il messaggio **mm \_ JOY1ZMOVE** notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che la posizione del joystick sull'asse z è cambiata.


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica i pulsanti che vengono premuti. Può essere uno o più dei valori seguenti:



| Requisito | Valore |
|--------------|------------------------------------|
| GIOIA \_ Button1 | Viene premuto il primo pulsante del joystick.  |
| GIOIA \_ Button2 | Viene premuto il secondo pulsante del joystick. |
| GIOIA \_ Button3 | Viene premuto il terzo pulsante del joystick.  |
| GIOIA \_ BUTTON4 | Viene premuto il quarto pulsante del joystick. |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

Coordinata z del joystick.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Joystick](joysticks.md)
</dt> <dt>

[Messaggi di joystick multimediali](multimedia-joystick-messages.md)
</dt> </dl>

 

 





