---
title: EN_DROPFILES codice di notifica (Richedit.h)
description: Notifica a una finestra padre del controllo Rich Edit che l'utente sta tentando di rilasciare file nel controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM NOTIFY quando \_ riceve il messaggio WM \_ DROPFILES.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8813d3d62883ab607bb898f4aa34a664cbab47b2c8214fbd83fc8cc7913e26ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047781"
---
# <a name="en_dropfiles-notification-code"></a>Codice \_ di notifica EN DROPFILES

Notifica a una finestra padre del controllo Rich Edit che l'utente sta tentando di rilasciare file nel controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio [**WM \_ NOTIFY**](wm-notify.md) quando riceve il [**messaggio WM \_ DROPFILES.**](/windows/desktop/shell/wm-dropfiles)


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) che riceve informazioni sui file eliminati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per consentire l'operazione di rilascio.

Restituisce zero per ignorare l'operazione di rilascio.

## <a name="remarks"></a>Commenti

Perché un controllo Rich Edit riceva [**messaggi WM \_ DROPFILES,**](/windows/desktop/shell/wm-dropfiles) la finestra padre deve registrare il controllo come destinazione di rilascio usando la [**funzione DragAcceptFiles.**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) Il controllo non esegue la registrazione.

Per ricevere i codici di notifica EN \_ DROPFILES, specificare [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

