---
title: Messaggio di EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 e versioni successive Recupera il tipo della successiva azione di annullamento, se disponibile. Microsoft Rich Edit 1,0 questo messaggio non è supportato.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- Controlli di Windows Message EM_GETUNDONAME
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964652"
---
# <a name="em_getundoname-message"></a>\_Messaggi GETundoname em

Microsoft Rich Edit 2,0 e versioni successive: Recupera il tipo della successiva azione di annullamento, se disponibile.

Microsoft Rich Edit 1,0: questo messaggio non è supportato.

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

Se è presente un'azione di annullamento, il valore restituito è un valore di enumerazione [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) che indica il tipo dell'azione successiva nella coda di annullamento del controllo.

Se non sono presenti azioni che possono essere annullate o il tipo della successiva azione di annullamento è sconosciuto, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I tipi di azioni che possono essere annullati o ripetuti includono operazioni di digitazione, eliminazione, trascinamento, riduzione e incolla. Queste informazioni possono essere utili per le applicazioni che forniscono un'interfaccia utente estesa per operazioni di annullamento e ripristino, ad esempio una casella di riepilogo a discesa di azioni che possono essere annullate.

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

[**\_GETredoname em**](em-getredoname.md)
</dt> <dt>

[**\_ripetizione em**](em-redo.md)
</dt> <dt>

[**\_Annulla**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





