---
title: EM_REPLACESEL messaggio (Winuser.h)
description: Sostituisce il testo selezionato in un controllo di modifica o in un controllo Rich Edit con il testo specificato.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 478550432aa8c03a081e8de214cdd7e8337a46eca2676a0531b177a81ff20a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831182"
---
# <a name="em_replacesel-message"></a>Messaggio EM \_ REPLACESEL

Sostituisce il testo selezionato in un controllo di modifica o in un controllo Rich Edit con il testo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se l'operazione di sostituzione può essere annullata. Se è **TRUE,** l'operazione può essere annullata. Se è **FALSE,** l'operazione non può essere annullata.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il testo di sostituzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare il **messaggio EM \_ REPLACESEL** per sostituire solo una parte del testo in un controllo di modifica. Per sostituire tutto il testo, usare il [**messaggio WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext)

Se non è presente alcuna selezione, il testo di sostituzione viene inserito in corrispondenza del caret.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

In un controllo Rich Edit, il testo di sostituzione accetta la formattazione del carattere in corrispondenza del punto di selezione o, se è presente una selezione, del primo carattere nella selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

