---
title: TCM_GETITEMCOUNT messaggio (Commctrl.h)
description: Recupera il numero di schede nel controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro TabCtrl \_ GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- TCM_GETITEMCOUNT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9bbb954c75a19f15ecee9f946e338a186b6e9903a405aa1c550fb0ccc31392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104881"
---
# <a name="tcm_getitemcount-message"></a>Messaggio GETITEMCOUNT di TCM \_

Recupera il numero di schede nel controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**TabCtrl \_ GetItemCount.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





