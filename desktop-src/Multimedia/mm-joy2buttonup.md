---
title: MM_JOY2BUTTONUP messaggio (Mmsystem.h)
description: Il messaggio MM JOY2BUTTONUP notifica alla finestra che ha acquisito \_ il joystick JOYSTICKID2 che è stato rilasciato un pulsante.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f94a1761686bd2e3ac7c470268427a213d54cdb4b8a58d54fdd6961427c2377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557311"
---
# <a name="mm_joy2buttonup-message"></a>Messaggio \_ MM JOY2BUTTONUP

Il **messaggio MM \_ JOY2BUTTONUP** notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che è stato rilasciato un pulsante.


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

**fwButtons** 
</dt> <dd>

Identifica il pulsante che ha modificato lo stato e i pulsanti premuti. I possibili valori sono i seguenti:



| Valore                                                                                                                                                            | Significato                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**JOY \_ BUTTON1CHG**</dt> </dl> | Lo stato del primo pulsante del joystick è stato modificato.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**PULSANTE \_ DI JOY2CHG**</dt> </dl> | Il secondo pulsante del joystick ha modificato lo stato.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**PULSANTE \_ DI JOY3CHG**</dt> </dl> | Lo stato del terzo pulsante del joystick è stato modificato.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**PULSANTE \_ DI JOY4CHG**</dt> </dl> | Lo stato del quarto pulsante del joystick è stato modificato.<br/> |



 

e uno o più degli elementi seguenti:



| Valore                                                                                                                                                   | Significato                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**PULSANTE \_ DI CONTROLLO DELLA ERTA1**</dt> </dl> | Viene premuto il primo pulsante del joystick.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**PULSANTE \_ DI CONTROLLO DELLA ERTA2**</dt> </dl> | Viene premuto il secondo pulsante del joystick.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**PULSANTE \_ DI GIOIA3**</dt> </dl> | Viene premuto il terzo pulsante del joystick.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**PULSANTE \_ GIOIOSO4**</dt> </dl> | Viene premuto il quarto pulsante del joystick.<br/> |



 

</dd> <dt>

**xPos** 
</dt> <dd>

Coordinate x del joystick rispetto all'angolo superiore sinistro dell'area client.

</dd> <dt>

**yPos** 
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

 

 





