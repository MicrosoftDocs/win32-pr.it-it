---
title: HDM_GETITEMCOUNT messaggio (Commctrl.h)
description: Ottiene un conteggio degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header GetItemCount.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- HDM_GETITEMCOUNT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4500277528cc76012631734d6f7316b29fdcb7a5a92cec3cf7b6bbb42693ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436031"
---
# <a name="hdm_getitemcount-message"></a>Messaggio \_ GETITEMCOUNT HDM

Ottiene un conteggio degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header GetItemCount.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi in caso di esito positivo oppure -1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





