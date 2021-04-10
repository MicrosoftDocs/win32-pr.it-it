---
title: Messaggio SBM_GETRANGE (winuser. h)
description: Il \_ messaggio SBM GetRange viene inviato per recuperare i valori di posizione minimo e massimo per il controllo barra di scorrimento.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- Controlli di Windows Message SBM_GETRANGE
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964632"
---
# <a name="sbm_getrange-message"></a>\_Messaggio GETrange di SBM

Il messaggio **SBM \_ GetRange** viene inviato per recuperare i valori di posizione minimo e massimo per il controllo barra di scorrimento.

Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollRange** funzioni correttamente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una variabile che riceve la posizione di scorrimento minima.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una variabile che riceve la posizione di scorrimento massima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

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

[**\_GETPOS SBM**](sbm-getpos.md)
</dt> <dt>

[**\_SETPOS SBM**](sbm-setpos.md)
</dt> <dt>

[**\_SEtrange SBM**](sbm-setrange.md)
</dt> <dt>

[**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)
</dt> </dl>

 

