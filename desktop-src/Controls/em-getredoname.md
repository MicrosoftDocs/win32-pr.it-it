---
title: Messaggio di EM_GETREDONAME (RichEdit. h)
description: Recupera il tipo dell'eventuale azione successiva nella coda di rollforward del controllo Rich Edit.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- Controlli di Windows Message EM_GETREDONAME
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964332"
---
# <a name="em_getredoname-message"></a>\_Messaggi GETredoname em

Recupera il tipo dell'eventuale azione successiva nella coda di rollforward del controllo Rich Edit.

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

Se la coda di rollforward per il controllo non è vuota, il valore restituito è un valore di enumerazione [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) che indica il tipo dell'azione successiva nella coda di rollforward del controllo.

Se non sono presenti azioni ripristinabili o il tipo della successiva azione ripetibile è sconosciuto, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I tipi di azioni che possono essere annullati o ripetuti includono operazioni di digitazione, eliminazione, trascinamento, taglia e incolla. Queste informazioni possono essere utili per le applicazioni che forniscono un'interfaccia utente estesa per operazioni di annullamento e ripristino, ad esempio una casella di riepilogo a discesa di azioni ripristinabili.

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

[**EM \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**\_ripetizione em**](em-redo.md)
</dt> <dt>

[**\_Annulla**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





