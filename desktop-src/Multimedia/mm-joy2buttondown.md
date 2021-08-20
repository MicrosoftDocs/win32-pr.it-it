---
title: MM_JOY2BUTTONDOWN messaggio (Mmsystem.h)
description: Il messaggio MM JOY2BUTTONDOWN notifica alla finestra che ha acquisito \_ il joystick JOYSTICKID2 che è stato premuto un pulsante.
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- MM_JOY2BUTTONDOWN messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e9ad78e914fb74e51f8ebe7a47a65677ac06d27d53eb8f64739ba641f235b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137202"
---
# <a name="mm_joy2buttondown-message"></a>Messaggio \_ MM JOY2BUTTONDOWN

Il **messaggio MM \_ JOY2BUTTONDOWN** notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che è stato premuto un pulsante.


```C++
MM_JOY2BUTTONDOWN 
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

 

 





