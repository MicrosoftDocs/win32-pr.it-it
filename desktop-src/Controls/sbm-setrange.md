---
title: Messaggio SBM_SETRANGE (winuser. h)
description: Il \_ messaggio SBM SEtrange viene inviato per impostare i valori di posizione minimo e massimo per il controllo barra di scorrimento.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- Controlli di Windows Message SBM_SETRANGE
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874421"
---
# <a name="sbm_setrange-message"></a>\_Messaggio SEtrange SBM

Il messaggio **SBM \_ SetRange** viene inviato per impostare i valori di posizione minimo e massimo per il controllo barra di scorrimento.

Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollRange** funzioni correttamente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica la posizione di scorrimento minima.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica la posizione di scorrimento massima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**ComCtl32.dll versione 5,0**: se la posizione della casella di scorrimento è cambiata, il valore restituito è la posizione precedente della casella di scorrimento; in caso contrario, è zero.

**ComCtl32.dll versione 6,0**: la posizione corrente della casella di scorrimento, indipendentemente dal fatto che sia stata modificata.

## <a name="remarks"></a>Commenti

I valori di posizione minima e massima predefiniti sono pari a zero. La differenza tra i valori specificati dai parametri *wParam* e *lParam* non deve essere maggiore di MAXLONG.

Se i valori di posizione minima e massima sono uguali, il controllo barra di scorrimento è nascosto e, in effetti, disabilitato.

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

[**\_SETPOS SBM**](sbm-setpos.md)
</dt> <dt>

[**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)
</dt> </dl>

 

