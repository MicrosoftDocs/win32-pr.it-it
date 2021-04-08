---
title: Messaggio EM_UNDO (winuser. h)
description: Questo messaggio annulla l'ultima operazione di modifica del controllo nella coda di annullamento del controllo. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- Controlli di Windows Message EM_UNDO
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
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741578"
---
# <a name="em_undo-message"></a>\_Messaggio di annullamento em

Questo messaggio annulla l'ultima operazione di modifica del controllo nella coda di annullamento del controllo. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per un controllo di modifica a riga singola, il valore restituito è sempre **true**.

Per un controllo di modifica su più righe, il valore restituito è **true** se l'operazione di annullamento ha esito positivo o **false** se l'operazione di annullamento ha esito negativo.

## <a name="remarks"></a>Commenti

**Modificare i controlli e rich edit 1,0:** Un'operazione di annullamento può anche essere annullata. Ad esempio, è possibile ripristinare il testo eliminato con il primo messaggio di **\_ annullamento em** e rimuovere nuovamente il testo con un secondo messaggio di **\_ annullamento** , purché non sia presente alcuna operazione di modifica.

**Rich Edit 2,0 e versioni successive:** La funzionalità di annullamento è multilivello, quindi l'invio di due messaggi di **\_ annullamento em** Annulla le ultime due operazioni nella coda di annullamento. Per ripetere un'operazione, inviare il messaggio di [**\_ ripetizione em**](em-redo.md) .

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CANUNDO em**](em-canundo.md)
</dt> </dl>

 

 





