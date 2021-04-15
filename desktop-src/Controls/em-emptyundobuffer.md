---
title: Messaggio EM_EMPTYUNDOBUFFER (winuser. h)
description: Reimposta il flag di annullamento di un controllo di modifica. Il flag di annullamento viene impostato ogni volta che un'operazione all'interno del controllo di modifica può essere annullata. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- Controlli di Windows Message EM_EMPTYUNDOBUFFER
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477603"
---
# <a name="em_emptyundobuffer-message"></a>\_Messaggio EMPTYUNDOBUFFER em

Reimposta il flag di annullamento di un controllo di modifica. Il flag di annullamento viene impostato ogni volta che un'operazione all'interno del controllo di modifica può essere annullata. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

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

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il flag di annullamento viene reimpostato automaticamente ogni volta che il controllo di modifica riceve un messaggio di selettore [**WM \_**](/windows/desktop/winmsg/wm-settext) o di [**em \_**](em-sethandle.md) .

**Modificare i controlli e rich edit 1,0:** Il controllo può annullare o ripristinare solo l'operazione più recente.

**Rich Edit 2,0 e versioni successive:** Il **messaggio \_ EMPTYUNDOBUFFER em** svuota tutti i buffer di annullamento e ripristino. I controlli Rich Edit consentono all'utente di annullare o ripristinare più operazioni.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_CANUNDO em**](em-canundo.md)
</dt> <dt>

[**filehandle EM \_**](em-sethandle.md)
</dt> <dt>

[**\_Annulla**](em-undo.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_testo WM**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

