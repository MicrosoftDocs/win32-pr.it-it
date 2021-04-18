---
title: Messaggio MM_JOY2BUTTONUP (mmsystem. h)
description: Il \_ messaggio mm JOY2BUTTONUP notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che un pulsante è stato rilasciato.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP messaggi multimediali di Windows
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
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302774"
---
# <a name="mm_joy2buttonup-message"></a>\_Messaggio JOY2BUTTONUP mm

Il messaggio **mm \_ JOY2BUTTONUP** notifica alla finestra che ha acquisito il joystick JOYSTICKID2 che un pulsante è stato rilasciato.


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
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**GIOIA \_ BUTTON1CHG**</dt> </dl> | Il primo pulsante del joystick è stato modificato.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**GIOIA \_ BUTTON2CHG**</dt> </dl> | Il secondo pulsante del joystick è stato modificato.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**GIOIA \_ BUTTON3CHG**</dt> </dl> | Il terzo pulsante del joystick è stato modificato.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**GIOIA \_ BUTTON4CHG**</dt> </dl> | Il quarto pulsante del joystick è stato modificato.<br/> |



 

e uno o più degli elementi seguenti:



| Valore                                                                                                                                                   | Significato                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**GIOIA \_ Button1**</dt> </dl> | Viene premuto il primo pulsante del joystick.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**GIOIA \_ Button2**</dt> </dl> | Viene premuto il secondo pulsante del joystick.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**GIOIA \_ Button3**</dt> </dl> | Viene premuto il terzo pulsante del joystick.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**GIOIA \_ BUTTON4**</dt> </dl> | Viene premuto il quarto pulsante del joystick.<br/> |



 

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
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Joystick](joysticks.md)
</dt> <dt>

[Messaggi di joystick multimediali](multimedia-joystick-messages.md)
</dt> </dl>

 

 





