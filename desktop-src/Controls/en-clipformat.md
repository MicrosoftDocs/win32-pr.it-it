---
title: EN_CLIPFORMAT di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit che si è verificato un'operazione Incolla con un particolare formato degli Appunti. Un controllo Rich Edit senza finestra invia questa notifica usando il metodo ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT del codice di notifica Windows controlli
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
ms.openlocfilehash: 0f4ad87f1c05ac9f5461da8a4ee1d26295be0ae1baafd8991801efc0d90197a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437041"
---
# <a name="en_clipformat-notification-code"></a>Codice di notifica EN \_ CLIPFORMAT

Notifica alla finestra padre di un controllo Rich Edit che si è verificato un'operazione Incolla con un particolare formato degli Appunti. Un controllo Rich Edit senza finestra invia questa notifica usando il [**metodo ITextHost::TxNotify.**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

ID della finestra recuperato chiamando la [**funzione GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il valore \_ GWL ID.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) che contiene informazioni sul formato degli Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per ricevere i \_ codici di notifica EN CLIPFORMAT, specificare [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

