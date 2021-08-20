---
title: MCM_GETCURSEL messaggio (Commctrl.h)
description: Recupera la data attualmente selezionata. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal GetCurSel.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- MCM_GETCURSEL dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40ed6797cd7f40eb68e40a9eac90eb250badd461011e5490c0f4c8473571bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170208"
---
# <a name="mcm_getcursel-message"></a>Messaggio \_ MCM GETCURSEL

Recupera la data attualmente selezionata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ MonthCal GetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà le informazioni sulla data attualmente selezionate. Questo parametro deve essere un indirizzo valido e non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario. Questo messaggio avrà sempre esito negativo se applicato ai controlli calendario mensile impostati sullo [**stile \_ MCS MULTISELECT.**](month-calendar-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Ore nel controllo Calendario mensile](month-calendar-controls.md)
</dt> </dl>

 

