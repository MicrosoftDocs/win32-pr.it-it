---
title: Messaggio CB_GETDROPPEDCONTROLRECT (winuser. h)
description: Un'applicazione invia un \_ messaggio CB GETDROPPEDCONTROLRECT per recuperare le coordinate dello schermo di una casella combinata nello stato di eliminazione.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- Controlli di Windows Message CB_GETDROPPEDCONTROLRECT
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
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477333"
---
# <a name="cb_getdroppedcontrolrect-message"></a>\_Messaggio GETDROPPEDCONTROLRECT CB

Un'applicazione invia un messaggio **CB \_ GETDROPPEDCONTROLRECT** per recuperare le coordinate dello schermo di una casella combinata nello stato di eliminazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve le coordinate della casella combinata nello stato di eliminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è diverso da zero.

Se il messaggio ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

