---
title: TCM_SETTOOLTIPS messaggio (Commctrl.h)
description: Assegna un controllo descrizione comando a un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl SetToolTips.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8bfec3b7272ceae3dcbf1781e3bb17a988f2252b3c0a74822677bff6ea39209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104691"
---
# <a name="tcm_settooltips-message"></a>Messaggio \_ TCM SETTOOLTIPS

Assegna un controllo descrizione comando a un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il controllo descrizione comando.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

È possibile recuperare il controllo descrizione comando associato a un controllo Struttura a schede usando il messaggio [**\_ GETTOOLTIPS di TCM.**](tcm-gettooltips.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





