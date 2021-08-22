---
title: EN_CORRECTTEXT di notifica (Richedit.h)
description: Notifica a una finestra padre del controllo Rich Edit che si è verificato un movimento SYV CORRECT, offrendo alla finestra padre la possibilità di annullare \_ la correzione del testo. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f03bf0d1bd31cc1f4139c24c6b0efa904f013231af4e108b0f97ef7f308bbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019419"
---
# <a name="en_correcttext-notification-code"></a>Codice di notifica EN \_ CORRECTTEXT

Notifica a una finestra padre del controllo Rich Edit che si è verificato un movimento SYV CORRECT, offrendo alla finestra padre la possibilità di annullare \_ la correzione del testo. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) che specifica la selezione da correggere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire zero per ignorare l'azione.

Restituisce un valore diverso da zero per elaborare l'azione.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo se sono disponibili funzionalità penna.

Per ricevere i \_ codici di notifica EN CORRECTTEXT, specificare [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md)

> [!Note]  
> Il codice di notifica EN \_ CORRECTTEXT è supportato solo nella versione Rich Edit 1.0. Non è supportato nelle versioni successive di Rich Edit. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

 

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

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





