---
title: Messaggio RB_DRAGMOVE (COMmctrl. h)
description: Aggiorna la posizione del trascinamento nel controllo Rebar dopo un \_ messaggio RB BEGINDRAG precedente.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- Controlli di Windows Message RB_DRAGMOVE
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
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964555"
---
# <a name="rb_dragmove-message"></a>\_Messaggio DRAGMOVE RB

Aggiorna la posizione del trascinamento nel controllo Rebar dopo un messaggio [**RB \_ BEGINDRAG**](rb-begindrag.md) precedente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **DWORD** che contiene le nuove coordinate del mouse. La coordinata orizzontale è contenuta in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la coordinata verticale è contenuta in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se si passa (DWORD)-1, il controllo Rebar utilizzerà la posizione del mouse nell'ultima volta in cui il thread del controllo ha chiamato [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RB \_ ENDDRAG**](rb-enddrag.md)
</dt> </dl>

 

