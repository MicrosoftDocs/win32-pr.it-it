---
title: MM_JOY1BUTTONUP messaggio (Mmsystem.h)
description: Il messaggio MMMOUSE1BUTTONUP notifica alla finestra che ha acquisito \_ ilstickSTICKSTICKID1 che è stato rilasciato un pulsante.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- MM_JOY1BUTTONUP di Windows multimediali
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70c7b8dda57d91e595bd65223a2fd33ef904679e35a38aaacbaf263b525258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065571"
---
# <a name="mm_joy1buttonup-message"></a>Messaggio \_ MM MMBUTTONUP

Il **messaggio \_ MMMOUSE1BUTTONUP** notifica alla finestra che ha acquisito ilstickSTICKSTICKID1 che è stato rilasciato un pulsante.


```C++
MM_JOY1BUTTONUP 
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
| JOY \_ BUTTON1CHG | Il primo pulsante a levetta è stato modificato.  |
| BUTTON \_ BUTTON2CHG | Il secondo pulsante a levetta è stato modificato. |
| BUTTON \_ BUTTON3CHG | Il terzo pulsante a levetta è stato modificato.  |
| BUTTON \_ BUTTON4CHG | Il quarto pulsante a levetta è stato modificato. |



 

e uno o più degli elementi seguenti:



| Requisito | Valore |
|--------------|------------------------------------|
| JOY \_ BUTTON1 | Viene premuto il primo pulsante a levetta.  |
| JOY \_ BUTTON2 | Viene premuto il secondo pulsante a levetta. |
| PULSANTE \_ BUTTON3 | Viene premuto il terzo pulsante a levetta.  |
| BUTTON \_ BUTTON4 | Viene premuto il quarto pulsante a levetta. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Coordinate x del levetta rispetto all'angolo superiore sinistro dell'area client.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Coordinata y del levetta rispetto all'angolo superiore sinistro dell'area client.

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

[Messaggi a levetta multimediali](multimedia-joystick-messages.md)
</dt> </dl>

 

 





