---
title: MCM_GETMONTHDELTA messaggio (Commctrl.h)
description: Recupera la frequenza di scorrimento per un controllo calendario mensile. La velocità di scorrimento è il numero di mesi in cui il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA controlli Windows messaggio
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13a13d75a1655c1082b4b4611517915be14e27b0fb1c5f94fb5a17f6db973e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319611"
---
# <a name="mcm_getmonthdelta-message"></a>Messaggio \_ DI MCM GETMONTHDELTA

Recupera la frequenza di scorrimento per un controllo calendario mensile. La velocità di scorrimento è il numero di mesi in cui il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ MonthCal GetMonthDelta.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il delta del mese è stato impostato in precedenza usando il messaggio [**MCM \_ SETMONTHDELTA,**](mcm-setmonthdelta.md) restituisce un valore INT che rappresenta la frequenza di scorrimento corrente del calendario mensile. Se il delta del mese non è stato impostato in precedenza usando il messaggio **MCM \_ SETMONTHDELTA** o se il delta del mese è stato reimpostato sul valore predefinito, restituisce un valore INT che rappresenta il numero corrente di mesi visibili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





