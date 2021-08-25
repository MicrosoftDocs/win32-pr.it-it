---
title: EM_UNDO messaggio (Winuser.h)
description: Questo messaggio annulla l'ultima operazione di controllo di modifica nella coda di annullamento del controllo. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- EM_UNDO di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d82e6d0685314a79f1f95cff487ee3f52e2d1b70925c3e6e72f9263f442e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047921"
---
# <a name="em_undo-message"></a>Messaggio EM \_ UNDO

Questo messaggio annulla l'ultima operazione di controllo di modifica nella coda di annullamento del controllo. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per un controllo di modifica a riga singola, il valore restituito è sempre **TRUE.**

Per un controllo di modifica su più righe, il valore restituito è **TRUE** se l'operazione di annullamento ha esito positivo oppure **FALSE se** l'operazione di annullamento non riesce.

## <a name="remarks"></a>Commenti

**Controlli di modifica e Rich Edit 1.0:** È anche possibile annullare un'operazione di annullamento. Ad esempio, è possibile ripristinare il testo eliminato con il primo messaggio **EM \_ UNDO** e rimuovere di nuovo il testo con un secondo messaggio **EM \_ UNDO,** purché non sia presente alcuna operazione di modifica.

**Rich Edit 2.0 e versioni successive:** La funzionalità di annullamento è multilivello, quindi **l'invio \_** di due messaggi EM UNDO annulla le ultime due operazioni nella coda di annullamento. Per ripetere un'operazione, inviare il [**messaggio EM \_ REDO.**](em-redo.md)

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> </dl>

 

 





