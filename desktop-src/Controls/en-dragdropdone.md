---
title: Codice di notifica EN_DRAGDROPDONE (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che l'operazione di trascinamento della selezione è stata completata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- Controlli di Windows per il codice di notifica EN_DRAGDROPDONE
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963807"
---
# <a name="en_dragdropdone-notification-code"></a>\_Codice di notifica en DRAGDROPDONE

Notifica alla finestra padre di un controllo Rich Edit che l'operazione di trascinamento della selezione è stata completata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Per ricevere un \_ codice di notifica en DRAGDROPDONE, specificare il flag [**ENM \_ DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .

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

[**\_SETEVENTMASK em**](em-seteventmask.md)
</dt> </dl>

 

 





