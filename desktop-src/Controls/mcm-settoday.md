---
title: Messaggio MCM_SETTODAY (COMmctrl. h)
description: Imposta il \ 0034; Today \ 0034; selezione per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- Controlli di Windows Message MCM_SETTODAY
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743815"
---
# <a name="mcm_settoday-message"></a>Messaggio di data/ \_ ora MCM

Imposta la selezione "Today" per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che contiene la data da impostare come selezione "Today" per il controllo. Se questo parametro è impostato su **null**, il controllo torna all'impostazione predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Se la selezione "Today" è impostata su una data diversa da quella predefinita, si applicano le condizioni seguenti:

-   Il controllo non aggiornerà automaticamente la selezione "Today" quando il tempo passa a mezzanotte del giorno corrente.
-   Il controllo non aggiornerà automaticamente la visualizzazione in base alle modifiche delle impostazioni locali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Orari del controllo calendario mensile](month-calendar-controls.md)
</dt> </dl>

 

