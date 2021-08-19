---
title: MM_JOY1MOVE messaggio (Mmsystem.h)
description: Il messaggio MM JOY1MOVE notifica alla finestra che ha acquisito \_ il joystick JOYSTICKID1 che la posizione del joystick è stata modificata.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- MM_JOY1MOVE messaggio Windows Multimediali
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
ms.openlocfilehash: d8c8a71bc91b541bc17017fc2673bb6c0ed7e84a2de44ff312954b8f9915dc57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802446"
---
# <a name="mm_joy1move-message"></a>Messaggio \_ MM JOY1MOVE

Il **messaggio MM \_ JOY1MOVE** notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che la posizione del joystick è stata modificata.


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

Identifica i pulsanti premuti. Può essere uno o più dei valori seguenti:



| Requisito | Valore |
|--------------|------------------------------------|
| PULSANTE \_ DI CONTROLLO DELLA ERTA1 | Viene premuto il primo pulsante del joystick.  |
| PULSANTE \_ DI CONTROLLO DELLA ERTA2 | Viene premuto il secondo pulsante del joystick. |
| PULSANTE \_ DI CONTROLLO DELLA ERTA3 | Viene premuto il terzo pulsante del joystick.  |
| PULSANTE \_ GIOIOSO4 | Viene premuto il quarto pulsante del joystick. |



 

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
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Joystick](joysticks.md)
</dt> <dt>

[Messaggi di joystick multimediali](multimedia-joystick-messages.md)
</dt> </dl>

 

 





