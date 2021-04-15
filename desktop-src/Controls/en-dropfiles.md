---
title: Codice di notifica EN_DROPFILES (RichEdit. h)
description: Notifica a una finestra padre del controllo Rich Edit che l'utente sta tentando di rilasciare i file nel controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM quando riceve il \_ messaggio WM DROPFILES.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- Controlli di Windows per il codice di notifica EN_DROPFILES
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
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475394"
---
# <a name="en_dropfiles-notification-code"></a>\_Codice di notifica en DropFiles

Notifica a una finestra padre del controllo Rich Edit che l'utente sta tentando di rilasciare i file nel controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) quando riceve il messaggio [**WM \_ DropFiles**](/windows/desktop/shell/wm-dropfiles) .


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

Restituisce zero per ignorare l'operazione DROP.

## <a name="remarks"></a>Commenti

Per un controllo Rich Edit per la ricezione di messaggi [**WM \_ DropFiles**](/windows/desktop/shell/wm-dropfiles) , è necessario che la finestra padre registri il controllo come destinazione di rilascio tramite la funzione [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) . Il controllo non registra se stesso.

Per ricevere \_ i codici di notifica en DropFiles, specificare [**ENM \_ DropFiles**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

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

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

