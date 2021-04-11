---
title: Messaggio EM_REPLACESEL (winuser. h)
description: Sostituisce il testo selezionato in un controllo di modifica o un controllo Rich Edit con il testo specificato.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- Controlli di Windows Message EM_REPLACESEL
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
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121498"
---
# <a name="em_replacesel-message"></a>\_Messaggio REPLACESEL em

Sostituisce il testo selezionato in un controllo di modifica o un controllo Rich Edit con il testo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se l'operazione di sostituzione può essere annullata. Se il valore è **true**, l'operazione può essere annullata. Se è **false** , l'operazione non può essere annullata.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il testo di sostituzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Usare il **messaggio \_ REPLACESEL em** per sostituire solo una parte del testo in un controllo di modifica. Per sostituire tutto il testo, utilizzare il messaggio [**di \_ testo WM**](/windows/desktop/winmsg/wm-settext) .

Se non è presente alcuna selezione, il testo di sostituzione viene inserito nel punto di inserimento.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

In un controllo Rich Edit il testo di sostituzione acquisisce la formattazione del carattere nel punto di inserimento o, se è presente una selezione, del primo carattere nella selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_testo WM**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

