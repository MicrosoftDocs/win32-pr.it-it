---
title: Codice di notifica EN_MSGFILTER (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit una tastiera o un evento del mouse nel controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- Controlli di Windows per il codice di notifica EN_MSGFILTER
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
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119938"
---
# <a name="en_msgfilter-notification-code"></a>\_Codice di notifica en msgfilter

Notifica alla finestra padre di un controllo Rich Edit una tastiera o un evento del mouse nel controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) contenente informazioni sulla tastiera o sul messaggio del mouse. Se la finestra padre modifica questa struttura e restituisce un valore diverso da zero, il messaggio modificato viene elaborato anziché quello originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero se il controllo deve elaborare l'evento della tastiera o del mouse.

Restituisce un valore diverso da zero se il controllo deve ignorare l'evento della tastiera o del mouse.

## <a name="remarks"></a>Commenti

Per ricevere i \_ codici di notifica en msgfilter per gli eventi, specificare uno o più dei flag seguenti nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .



| Contrassegno                                                                             | Significato                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**ENM di \_ UNIformi**](rich-edit-control-event-mask-flags.md)       | Per ricevere i codici di notifica per gli eventi della tastiera.     |
| [**\_MOUSEEVENTS ENM**](rich-edit-control-event-mask-flags.md)   | Per ricevere i codici di notifica per gli eventi del mouse.        |
| [**\_SCROLLEVENTS ENM**](rich-edit-control-event-mask-flags.md) | Per ricevere i codici di notifica per un evento della rotellina del mouse. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**\_notifica WM**](wm-notify.md)
</dt> </dl>

 

 





