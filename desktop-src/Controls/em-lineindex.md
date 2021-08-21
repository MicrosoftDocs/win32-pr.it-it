---
title: EM_LINEINDEX messaggio (Winuser.h)
description: Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_LINEINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 223208b2f9a31dcc1d81d6811aab32210adedbeb807eb0cdbef8c53ec853ab04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171400"
---
# <a name="em_lineindex-message-winuserh"></a>EM_LINEINDEX messaggio (Winuser.h)

Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe. Un indice di caratteri è l'indice in base zero del carattere dall'inizio del controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di riga in base zero. Il valore -1 specifica il numero di riga corrente (la riga che contiene il punto di interruzione).

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice dei caratteri della riga specificata nel *parametro wParam* oppure è -1 se il numero di riga specificato è maggiore del numero di righe nel controllo di modifica.

## <a name="remarks"></a>Commenti

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ LINEFROMCHAR**](em-linefromchar.md)
</dt> </dl>

 

 





