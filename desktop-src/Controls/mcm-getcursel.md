---
title: Messaggio MCM_GETCURSEL (COMmctrl. h)
description: Recupera la data attualmente selezionata. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetCurSel.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- Controlli di Windows Message MCM_GETCURSEL
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
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477555"
---
# <a name="mcm_getcursel-message"></a>Messaggio di MCM \_ GETcursel

Recupera la data attualmente selezionata. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà le informazioni sulla data attualmente selezionate. Questo parametro deve essere un indirizzo valido e non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario. Questo messaggio avrà sempre esito negativo quando applicato ai controlli calendario mensile impostati sullo stile [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .

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

 

