---
title: TCM_GETROWCOUNT messaggio (Commctrl.h)
description: Recupera il numero corrente di righe di schede in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl GetRowCount.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- TCM_GETROWCOUNT di Windows di messaggio
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e67b2ac40834075b31ccf2415a52c96448b8143dde3d6bc67f9c515e1f601a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104871"
---
# <a name="tcm_getrowcount-message"></a>Messaggio TCM \_ GETROWCOUNT

Recupera il numero corrente di righe di schede in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl GetRowCount.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di righe di schede.

## <a name="remarks"></a>Commenti

Solo i controlli struttura a schede con [**lo stile \_ MULTILINE TCS**](tab-control-styles.md) possono avere più righe di schede.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





