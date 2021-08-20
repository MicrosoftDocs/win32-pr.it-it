---
title: MM_JOY1BUTTONDOWN messaggio (Mmsystem.h)
description: Il messaggio MM JOY1BUTTONDOWN notifica alla finestra che ha acquisito \_ il joystick JOYSTICKID1 che è stato premuto un pulsante.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- MM_JOY1BUTTONDOWN messaggio Windows Multimediali
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
ms.openlocfilehash: 2d2399eca0de21014b97c9156e6a16349fc5b0b5407b64b022eb077fd59d0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137192"
---
# <a name="mm_joy1buttondown-message"></a>Messaggio \_ MM JOY1BUTTONDOWN

Il **messaggio MM \_ JOY1BUTTONDOWN** notifica alla finestra che ha acquisito il joystick JOYSTICKID1 che è stato premuto un pulsante.


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
| JOY \_ BUTTON1CHG | Lo stato del primo pulsante del joystick è stato modificato.  |
| PULSANTE \_ DI JOY2CHG | Lo stato del secondo pulsante del joystick è stato modificato. |
| PULSANTE \_ DI JOY3CHG | Lo stato del terzo pulsante del joystick è stato modificato.  |
| PULSANTE \_ DI JOY4CHG | Lo stato del quarto pulsante del joystick è stato modificato. |



 

e uno o più degli elementi seguenti:



| Requisito | Valore |
|--------------|------------------------------------|
| PULSANTE \_ DI CONTROLLO DELLA ERTA1 | Viene premuto il primo pulsante del joystick.  |
| PULSANTE \_ DI CONTROLLO DELLA ERTA2 | Viene premuto il secondo pulsante del joystick. |
| PULSANTE \_ DI CONTROLLO DELLA ERTA3 | Viene premuto il terzo pulsante del joystick.  |
| PULSANTE \_ DI GIOIA4 | Viene premuto il quarto pulsante del joystick. |



 

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
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Joystick](joysticks.md)
</dt> <dt>

[Messaggi di joystick multimediali](multimedia-joystick-messages.md)
</dt> </dl>

 

 





