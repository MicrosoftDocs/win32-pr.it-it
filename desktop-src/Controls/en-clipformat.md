---
title: Codice di notifica EN_CLIPFORMAT (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che è stata eseguita una copia con un formato degli Appunti specifico. Un controllo Rich Edit senza finestra Invia questa notifica tramite il metodo ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- Controlli di Windows per il codice di notifica EN_CLIPFORMAT
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964046"
---
# <a name="en_clipformat-notification-code"></a>\_Codice di notifica en CLIPFORMAT

Notifica alla finestra padre di un controllo Rich Edit che è stata eseguita una copia con un formato degli Appunti specifico. Un controllo Rich Edit senza finestra Invia questa notifica tramite il metodo [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

ID della finestra recuperato chiamando la funzione [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il \_ valore ID GWL.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) che contiene informazioni sul formato degli Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per ricevere \_ i codici di notifica en CLIPFORMAT, specificare [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

