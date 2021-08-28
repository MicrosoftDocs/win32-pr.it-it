---
title: SBM_GETRANGE messaggio (Winuser.h)
description: Il messaggio SBM GETRANGE viene inviato per recuperare i valori di posizione minima e \_ massima per il controllo barra di scorrimento.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- SBM_GETRANGE controlli Windows messaggio
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
ms.openlocfilehash: 8e66c6e7bf79c270d66fdeac0ece1a1ce82ed813d1638be3587be7237ecd30e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770041"
---
# <a name="sbm_getrange-message"></a>Messaggio \_ SBM GETRANGE

Il **messaggio SBM \_ GETRANGE** viene inviato per recuperare i valori di posizione minima e massima per il controllo barra di scorrimento.

Le applicazioni non devono inviare questo messaggio direttamente. Devono invece usare la [**funzione GetScrollRange.**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) Una finestra riceve questo messaggio tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi perché la **funzione GetScrollRange** funzioni correttamente.

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

Questo messaggio non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGE**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

