---
title: EM_GETUNDONAME messaggio (Richedit.h)
description: Microsoft Rich Edit 2.0 e versioni successive Recupera il tipo dell'azione di annullamento successiva, se presente. Microsoft Rich Edit 1.0 Questo messaggio non è supportato.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME di controllo Windows messaggio
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
ms.openlocfilehash: d133038c0adad2fe7eaa1ae98cf638fe6bd13fad82df3b3d2d1ac384a30e1a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576641"
---
# <a name="em_getundoname-message"></a>Messaggio \_ EM GETUNDONAME

Microsoft Rich Edit 2.0 e versioni successive: recupera il tipo dell'azione di annullamento successiva, se presente.

Microsoft Rich Edit 1.0: questo messaggio non è supportato.

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

Se è presente un'azione di annullamento, il valore restituito è un valore di enumerazione [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) che indica il tipo dell'azione successiva nella coda di annullamento del controllo.

Se non sono presenti azioni che possono essere annullate o il tipo dell'azione di annullamento successiva è sconosciuto, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I tipi di azioni che è possibile annullare o ripristinare includono operazioni di digitazione, eliminazione, trascinamento, rilascio, taglia e incolla. Queste informazioni possono essere utili per le applicazioni che forniscono un'interfaccia utente estesa per le operazioni di annullamento e ripristino, ad esempio una casella di riepilogo a discesa di azioni che possono essere annullate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





