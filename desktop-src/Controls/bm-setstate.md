---
title: BM_SETSTATE messaggio (Winuser.h)
description: Imposta lo stato di evidenziazione di un pulsante. Lo stato di evidenziazione indica se il pulsante è evidenziato come se l'utente lo avesse premuto. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button SetState.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE controlli Windows messaggio
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3bb9451041c602541f039afcd85a895af2f02302dc5d55d64fbefb5bc6e3ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921211"
---
# <a name="bm_setstate-message"></a>Messaggio \_ BM SETSTATE

Imposta lo stato di evidenziazione di un pulsante. Lo stato di evidenziazione indica se il pulsante è evidenziato come se l'utente lo avesse premuto. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button SetState.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **BOOL** che specifica se il pulsante è evidenziato. Il valore **TRUE evidenzia** il pulsante. Il valore **FALSE rimuove** qualsiasi evidenziazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre zero.

## <a name="remarks"></a>Commenti

L'evidenziazione influisce solo sull'aspetto di un pulsante. Non ha alcun effetto sullo stato di controllo di un pulsante di opzione o di una casella di controllo.

Un pulsante viene evidenziato automaticamente quando l'utente posiziona il cursore su di esso e preme e tiene premuto il pulsante sinistro del mouse. L'evidenziazione viene rimossa quando l'utente rilascia il pulsante del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





