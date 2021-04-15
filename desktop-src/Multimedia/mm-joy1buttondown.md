---
title: Messaggio MM_JOY1BUTTONDOWN (mmsystem. h)
description: Il \_ messaggio mm JOY1BUTTONDOWN notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che è stato premuto un pulsante.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- MM_JOY1BUTTONDOWN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cefb70e5dd47fc14b39dcdeb59043b6827e7b89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475503"
---
# <a name="mm_joy1buttondown-message"></a>\_Messaggio JOY1BUTTONDOWN mm

Il messaggio **mm \_ JOY1BUTTONDOWN** notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che è stato premuto un pulsante.


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica il pulsante che ha modificato lo stato e i pulsanti premuti. I possibili valori sono i seguenti:



| Requisito | Valore |
|-----------------|-------------------------------------------|
| GIOIA \_ BUTTON1CHG | Il primo pulsante del joystick è stato modificato.  |
| GIOIA \_ BUTTON2CHG | Il secondo pulsante del joystick è stato modificato. |
| GIOIA \_ BUTTON3CHG | Il terzo pulsante del joystick è stato modificato.  |
| GIOIA \_ BUTTON4CHG | Il quarto pulsante del joystick è stato modificato. |



 

e uno o più degli elementi seguenti:



| Requisito | Valore |
|--------------|------------------------------------|
| GIOIA \_ Button1 | Viene premuto il primo pulsante del joystick.  |
| GIOIA \_ Button2 | Viene premuto il secondo pulsante del joystick. |
| GIOIA \_ Button3 | Viene premuto il terzo pulsante del joystick.  |
| GIOIA \_ BUTTON4 | Viene premuto il quarto pulsante del joystick. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Coordinata x del joystick rispetto all'angolo superiore sinistro dell'area client.

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

 

 





