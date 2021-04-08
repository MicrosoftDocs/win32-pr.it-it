---
title: Messaggio EM_SETMODIFY (winuser. h)
description: Imposta o cancella il flag di modifica per un controllo di modifica. Il flag di modifica indica se il testo all'interno del controllo di modifica è stato modificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Controlli di Windows Message EM_SETMODIFY
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874037"
---
# <a name="em_setmodify-message"></a>Messaggio di modifica di EM \_

Imposta o cancella il flag di modifica per un controllo di modifica. Il flag di modifica indica se il testo all'interno del controllo di modifica è stato modificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuovo valore per il flag di modifica. Il valore **true** indica che il testo è stato modificato e il valore **false** indica che non è stato modificato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il sistema cancella automaticamente il flag di modifica a zero quando viene creato il controllo. Se l'utente modifica il testo del controllo, il sistema imposta il flag su un valore diverso da zero. È possibile inviare il messaggio [**em \_ GetModify**](em-getmodify.md) al controllo Edit per recuperare lo stato corrente del flag.

**Modifica dettagliata 1,0:** Gli oggetti creati senza il flag **reo \_ DYNAMICSIZE** bloccano gli extent quando il flag di modifica è impostato su **false**.

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

[**GetModify EM \_**](em-getmodify.md)
</dt> <dt>

[**REOBJECT**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





