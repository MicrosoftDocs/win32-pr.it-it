---
title: SBM_GETPOS messaggio (Winuser.h)
description: Il messaggio GETPOS SBM \_ viene inviato per recuperare la posizione corrente della casella di scorrimento di un controllo barra di scorrimento.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS di controllo Windows messaggio
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
ms.openlocfilehash: 0105b2c015614c9f064b2c97f60100c2240bd6588612d34b25546c7ced832bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408894"
---
# <a name="sbm_getpos-message"></a>Messaggio \_ GETPOS SBM

Il **messaggio \_ GETPOS SBM** viene inviato per recuperare la posizione corrente della casella di scorrimento di un controllo barra di scorrimento. La posizione corrente è un valore relativo che dipende dall'intervallo di scorrimento corrente. Ad esempio, se l'intervallo di scorrimento è compreso tra 0 e 100 e la casella di scorrimento si trova al centro della barra, la posizione corrente è 50.

Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la [**funzione GetScrollPos.**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) Una finestra riceve questo messaggio tramite la [*relativa funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi perché la **funzione GetScrollPos** funzioni correttamente.

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

Il valore restituito è la posizione corrente della casella di scorrimento nella barra di scorrimento.

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

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGE**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

