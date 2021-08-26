---
title: EN_REQUESTRESIZE di notifica (Richedit.h)
description: Notifica alla finestra padre di un controllo Rich Edit che il contenuto del controllo è più piccolo o maggiore delle dimensioni della finestra del controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE del codice di notifica Windows controlli
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
ms.openlocfilehash: 9b15c21b180c2843eda7947946f6dc98d42caab1bad90383d6afe4a4f8002739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047581"
---
# <a name="en_requestresize-notification-code"></a>Codice di notifica EN \_ REQUESTRESIZE

Notifica alla finestra padre di un controllo Rich Edit che il contenuto del controllo è più piccolo o maggiore delle dimensioni della finestra del controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) che riceve le dimensioni richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce un valore.

## <a name="remarks"></a>Commenti

Per supportare il comportamento senza fondo di un controllo Rich Edit, la finestra padre deve ridimensionare il controllo quando riceve questo codice di notifica.

Per ricevere i codici di notifica EN \_ REQUESTRESIZE, specificare [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md)

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

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





