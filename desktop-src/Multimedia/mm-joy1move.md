---
title: Messaggio MM_JOY1MOVE (mmsystem. h)
description: Il \_ messaggio mm JOY1MOVE notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che la posizione del joystick è cambiata.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- MM_JOY1MOVE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_JOY1MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78753bd55f6682b3ac3f1514356d93cb455d162
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301077"
---
# <a name="mm_joy1move-message"></a>\_Messaggio JOY1MOVE mm

Il messaggio **mm \_ JOY1MOVE** notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che la posizione del joystick è cambiata.


```C++
MM_JOY1MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
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

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Coordinate x del joystick rispetto all'angolo superiore sinistro dell'area client.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Coordinata y del joystick rispetto all'angolo superiore sinistro dell'area client.

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

 

 





