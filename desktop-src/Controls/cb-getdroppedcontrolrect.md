---
title: CB_GETDROPPEDCONTROLRECT messaggio (Winuser.h)
description: Un'applicazione invia un messaggio CB GETDROPPEDCONTROLRECT per recuperare le coordinate dello schermo di una casella combinata \_ nello stato rilasciato.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT controlli di Windows messaggio
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c140abb139cc47020f333ccf66f71cf36d890449be91d66f51b646db22091c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089281"
---
# <a name="cb_getdroppedcontrolrect-message"></a>CB \_ GETDROPPEDCONTROLRECT message

Un'applicazione invia un **messaggio CB \_ GETDROPPEDCONTROLRECT** per recuperare le coordinate dello schermo di una casella combinata nello stato rilasciato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceve le coordinate della casella combinata nello stato rilasciato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è diverso da zero.

Se il messaggio ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

