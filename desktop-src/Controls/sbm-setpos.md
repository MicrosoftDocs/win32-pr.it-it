---
title: SBM_SETPOS messaggio (Winuser.h)
description: Il messaggio SETPOS SBM viene inviato per impostare la posizione della casella di scorrimento (casella di scorrimento) e, se richiesto, ridisegnare la barra di scorrimento per riflettere la nuova posizione della \_ casella di scorrimento.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- SBM_SETPOS controlli Windows messaggio
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
ms.openlocfilehash: cd753d8ef20d912cd5b50ba0932d54ed231ae19e032d21eb1de6492e5792e1d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332226"
---
# <a name="sbm_setpos-message"></a>Messaggio \_ SETPOS SBM

Il **messaggio \_ SETPOS SBM** viene inviato per impostare la posizione della casella di scorrimento (casella di scorrimento) e, se richiesto, ridisegnare la barra di scorrimento per riflettere la nuova posizione della casella di scorrimento.

Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la [**funzione SetScrollPos.**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) Una finestra riceve questo messaggio tramite la [*relativa funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi per il corretto funzionamento della **funzione SetScrollPos.**

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica la nuova posizione della casella di scorrimento. Deve essere compreso nell'intervallo di scorrimento. Se questo parametro non è compreso nell'intervallo di scorrimento, il valore viene arrotondato per es.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica se la barra di scorrimento deve essere ridisegnata per riflettere la nuova posizione della casella di scorrimento. Se questo parametro è **TRUE,** la barra di scorrimento viene ridisegnata. Se è **FALSE,** la barra di scorrimento non viene ridisegnata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**ComCtl32.dll versione 5.0:** se la posizione della casella di scorrimento è cambiata, il valore restituito è la posizione precedente della casella di scorrimento; in caso contrario, è zero.

**ComCtl32.dll versione 6.0:** posizione corrente della casella di scorrimento, indipendentemente dal fatto che sia stata modificata.

## <a name="remarks"></a>Commenti

Se il controllo barra di scorrimento viene ridisegnato da una chiamata successiva a un'altra funzione, è utile impostare il parametro *lParam* su **FALSE.**

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

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETRANGE**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

