---
title: MCM_GETCALENDARCOUNT messaggio (Commctrl.h)
description: Ottiene il numero di calendari attualmente visualizzati nel controllo calendario. È possibile inviare questo messaggio in modo esplicito o tramite la macro MonthCal \_ GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- MCM_GETCALENDARCOUNT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9379aa8c273451ba53c2a13d6190712212765b46dc1052a08b6d03ae4ae32e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019049"
---
# <a name="mcm_getcalendarcount-message"></a>Messaggio MCM \_ GETCALENDARCOUNT

Ottiene il numero di calendari attualmente visualizzati nel controllo calendario. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MonthCal \_ GetCalendarCount.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Numero di calendari attualmente visualizzati nel controllo calendario. Il numero massimo di calendari consentiti è 12.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





