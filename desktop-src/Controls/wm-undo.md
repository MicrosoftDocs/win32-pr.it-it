---
title: WM_UNDO messaggio (Winuser.h)
description: Un'applicazione invia un messaggio UNDO WM \_ a un controllo di modifica per annullare l'ultima operazione. Quando questo messaggio viene inviato a un controllo di modifica, il testo eliminato in precedenza viene ripristinato o il testo aggiunto in precedenza viene eliminato.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO controlli di Windows messaggio
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6e4bd0715b7eeb5f99f34f5142ac3198c5c1eae53cf4486c3efce9dace19a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311341"
---
# <a name="wm_undo-message"></a>Messaggio \_ UNDO WM

Un'applicazione invia un **messaggio UNDO WM \_** a un controllo di modifica per annullare l'ultima operazione. Quando questo messaggio viene inviato a un controllo di modifica, il testo eliminato in precedenza viene ripristinato o il testo aggiunto in precedenza viene eliminato.

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

Se il messaggio ha esito positivo, il valore restituito è **TRUE.**

Se il messaggio ha esito negativo, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

**Rich Edit:** È consigliabile usare [**EM \_ UNDO**](em-undo.md) anziché **WM \_ UNDO.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**WM \_ CLEAR**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**WM \_ COPY**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**WM \_ CUT**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**WM \_ PASTE**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

