---
title: RB_DRAGMOVE messaggio (Commctrl.h)
description: Aggiorna la posizione di trascinamento nel controllo Rebar dopo un messaggio RB \_ BEGINDRAG precedente.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a511bd1ad13442489f3f6dbf3de1b897b30e54f9d503b30b9031426b0aedcef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409723"
---
# <a name="rb_dragmove-message"></a>Messaggio RB \_ DRAGMOVE

Aggiorna la posizione di trascinamento nel controllo Rebar dopo un messaggio [**RB \_ BEGINDRAG**](rb-begindrag.md) precedente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valore DWORD** che contiene le nuove coordinate del mouse. La coordinata orizzontale è contenuta in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la coordinata verticale è contenuta in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se si passa (DWORD)-1, il controllo Rebar userà la posizione del mouse l'ultima volta che il thread del controllo ha chiamato [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage.**](/windows/desktop/DevNotes/-peekmessage)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RB \_ ENDDRAG**](rb-enddrag.md)
</dt> </dl>

 

