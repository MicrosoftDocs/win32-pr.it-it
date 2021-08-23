---
title: MM_JOY1ZMOVE messaggio (Mmsystem.h)
description: Il messaggio MMMOV1ZMOVE notifica alla finestra che ha acquisito il levettoSTICKSTICKID1 che la posizione del levetta sull'asse \_ z è stata modificata.
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- MM_JOY1ZMOVE di messaggi Windows multimediali
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
ms.openlocfilehash: b6b0efe11870ac822f7fe8aa0f7aa1deb4856bd8f1394bd1533362d78a3aee00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065541"
---
# <a name="mm_joy1zmove-message"></a>MESSAGGIO \_ MM MMMOVE

Il **messaggio \_ MMMOV1ZMOVE** notifica alla finestra che ha acquisito il levettoSTICKSTICKID1 che la posizione del levetta sull'asse z è stata modificata.


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica i pulsanti premuti. Può essere uno o più dei valori seguenti:



| Requisito | Valore |
|--------------|------------------------------------|
| JOY \_ BUTTON1 | Viene premuto il primo pulsante a levetta.  |
| JOY \_ BUTTON2 | Viene premuto il secondo pulsante a levetta. |
| PULSANTE \_ BUTTON3 | Viene premuto il terzo pulsante a levetta.  |
| BUTTON \_ BUTTON4 | Viene premuto il quarto pulsante a levetta. |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

Coordinata z del levetta.

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

 

 





