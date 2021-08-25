---
title: DTM_GETDATETIMEPICKERINFO messaggio (Commctrl.h)
description: Ottiene informazioni su un controllo di selezione data e ora.
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- DTM_GETDATETIMEPICKERINFO controlli di Windows messaggio
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48dc639a48455564b9f925f7d6eea9634c01e597323f81d951cfde372a34ea37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878221"
---
# <a name="dtm_getdatetimepickerinfo-message"></a>Messaggio DTM \_ GETDATETIMEPICKERINFO

Ottiene informazioni su un controllo di selezione data e ora.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd> Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> per ricevere le informazioni. Il chiamante è responsabile dell'allocazione della memoria per questa struttura. Impostare il **membro cbSize** della struttura su sizeof(DATETIMEPICKERINFO) prima di inviare questo messaggio.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





