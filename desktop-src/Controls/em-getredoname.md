---
title: EM_GETREDONAME messaggio (Richedit.h)
description: Recupera il tipo dell'azione successiva, se presente, nella coda di rifornimenti del controllo Rich Edit.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME controlli di Windows messaggio
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
ms.openlocfilehash: 9687ae54223ec7cc0f908d747eff2504216b79469b5f285863f8c8ffdfe91b3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048821"
---
# <a name="em_getredoname-message"></a>Messaggio \_ EM GETREDONAME

Recupera il tipo dell'azione successiva, se presente, nella coda di rifornimenti del controllo Rich Edit.

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

Se la coda di rifornimento per il controllo non è vuota, il valore restituito è un valore di enumerazione [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) che indica il tipo dell'azione successiva nella coda di annullamento del controllo.

Se non sono presenti azioni ripristinabili o il tipo della successiva azione ripristinabile è sconosciuto, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I tipi di azioni che è possibile annullare o ripetere includono le operazioni di digitazione, eliminazione, trascinamento della selezione, taglia e incolla. Queste informazioni possono essere utili per le applicazioni che forniscono un'interfaccia utente estesa per le operazioni di annullamento e ripristino, ad esempio una casella di riepilogo a discesa di azioni ripristinabili.

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

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





