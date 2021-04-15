---
title: Messaggio SBM_SETPOS (winuser. h)
description: Il \_ messaggio SETPOS SBM viene inviato per impostare la posizione della casella di scorrimento (Thumb) e, se richiesto, per ricreare la barra di scorrimento in modo da riflettere la nuova posizione della casella di scorrimento.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- Controlli di Windows Message SBM_SETPOS
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479156"
---
# <a name="sbm_setpos-message"></a>\_Messaggio SETPOS SBM

Il **messaggio \_ SETPOS SBM** viene inviato per impostare la posizione della casella di scorrimento (Thumb) e, se richiesto, per ricreare la barra di scorrimento in modo da riflettere la nuova posizione della casella di scorrimento.

Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollPos** funzioni correttamente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica la nuova posizione della casella di scorrimento. Deve trovarsi all'interno dell'intervallo di scorrimento. Se questo parametro è esterno all'intervallo di scorrimento, il valore viene arrotondato per eccesso o per difetto al valore valido più vicino.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica se la barra di scorrimento deve essere ridisegnato per riflettere la nuova posizione della casella di scorrimento. Se questo parametro è **true**, la barra di scorrimento viene ridisegnato. Se è **false**, la barra di scorrimento non viene ridisegnato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**ComCtl32.dll versione 5,0**: se la posizione della casella di scorrimento è cambiata, il valore restituito è la posizione precedente della casella di scorrimento; in caso contrario, è zero.

**ComCtl32.dll versione 6,0**: la posizione corrente della casella di scorrimento, indipendentemente dal fatto che sia stata modificata.

## <a name="remarks"></a>Commenti

Se il controllo barra di scorrimento viene ridisegnato da una chiamata successiva a un'altra funzione, l'impostazione del parametro *lParam* su **false** è utile.

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

[**GetRange di SBM \_**](sbm-getrange.md)
</dt> <dt>

[**\_SEtrange SBM**](sbm-setrange.md)
</dt> <dt>

[**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)
</dt> </dl>

 

