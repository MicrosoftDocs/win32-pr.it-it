---
title: Codice di notifica EN_REQUESTRESIZE (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che il contenuto del controllo è più piccolo o maggiore delle dimensioni della finestra del controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- Controlli di Windows per il codice di notifica EN_REQUESTRESIZE
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120315"
---
# <a name="en_requestresize-notification-code"></a>\_Codice di notifica en REQUESTRESIZE

Notifica alla finestra padre di un controllo Rich Edit che il contenuto del controllo è più piccolo o maggiore delle dimensioni della finestra del controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) che riceve la dimensione richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Per supportare il comportamento senza fondo di un controllo Rich Edit, la finestra padre deve ridimensionare il controllo quando riceve il codice di notifica.

Per ricevere \_ i codici di notifica en REQUESTRESIZE, specificare [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

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

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**\_notifica WM**](wm-notify.md)
</dt> </dl>

 

 





