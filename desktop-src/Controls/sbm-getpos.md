---
title: Messaggio SBM_GETPOS (winuser. h)
description: Il \_ messaggio GETPOS SBM viene inviato per recuperare la posizione corrente della casella di scorrimento di un controllo barra di scorrimento.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- Controlli di Windows Message SBM_GETPOS
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964633"
---
# <a name="sbm_getpos-message"></a>\_Messaggio GETPOS SBM

Il **messaggio \_ GETPOS SBM** viene inviato per recuperare la posizione corrente della casella di scorrimento di un controllo barra di scorrimento. La posizione corrente è un valore relativo che dipende dall'intervallo di scorrimento corrente. Se, ad esempio, l'intervallo di scorrimento è compreso tra 0 e 100 e la casella di scorrimento si trova al centro della barra, la posizione corrente è 50.

Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollPos** funzioni correttamente.

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

Il valore restituito è la posizione corrente della casella di scorrimento nella barra di scorrimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GetRange di SBM \_**](sbm-getrange.md)
</dt> <dt>

[**\_SETPOS SBM**](sbm-setpos.md)
</dt> <dt>

[**\_SEtrange SBM**](sbm-setrange.md)
</dt> <dt>

[**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)
</dt> </dl>

 

