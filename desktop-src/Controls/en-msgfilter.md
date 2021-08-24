---
title: EN_MSGFILTER di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit un evento della tastiera o del mouse nel controllo . Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d2cbe47af3d74deb4795946d58871b4729118db0e839027e78e05976ebf855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436711"
---
# <a name="en_msgfilter-notification-code"></a>Codice \_ di notifica EN MSGFILTER

Notifica alla finestra padre di un controllo Rich Edit un evento della tastiera o del mouse nel controllo . Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**MSGFILTER contenente**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) informazioni sulla tastiera o sul messaggio del mouse. Se la finestra padre modifica questa struttura e restituisce un valore diverso da zero, il messaggio modificato viene elaborato anziché quello originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se il controllo deve elaborare l'evento della tastiera o del mouse.

Restituisce un valore diverso da zero se il controllo deve ignorare l'evento della tastiera o del mouse.

## <a name="remarks"></a>Commenti

Per ricevere i codici di notifica EN MSGFILTER per gli eventi, specificare uno o più dei flag seguenti nella maschera inviata con il messaggio \_ [**EM \_ SETEVENTMASK.**](em-seteventmask.md)



| Contrassegno                                                                             | Significato                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**EVENTI \_ CHIAVE ENM**](rich-edit-control-event-mask-flags.md)       | Per ricevere i codici di notifica per gli eventi della tastiera.     |
| [**ENM \_ MOUSEEVENTS**](rich-edit-control-event-mask-flags.md)   | Per ricevere i codici di notifica per gli eventi del mouse.        |
| [**ENM \_ SCROLLEVENTS**](rich-edit-control-event-mask-flags.md) | Per ricevere i codici di notifica per un evento della rotellina del mouse. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





