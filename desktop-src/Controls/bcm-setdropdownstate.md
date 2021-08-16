---
title: BCM_SETDROPDOWNSTATE messaggio (Commctrl.h)
description: Imposta lo stato a discesa per un pulsante con stile TBSTYLE \_ DROPDOWN. Inviare questo messaggio in modo esplicito o tramite la \_ macro Button SetDropDownState.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- BCM_SETDROPDOWNSTATE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b4a04502a730c06a906be28a6915a4e604ff22c4b4e5ae9a4b85c8b464f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833632"
---
# <a name="bcm_setdropdownstate-message"></a>Messaggio \_ DI BCM SETDROPDOWNSTATE

Imposta lo stato a discesa per un pulsante con stile [**TBSTYLE \_ DROPDOWN.**](toolbar-control-and-button-styles.md) Inviare questo messaggio in modo esplicito o tramite la macro [**\_ Button SetDropDownState.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

VALORE **BOOL TRUE** **per lo stato** di BST \_ DROPDOWNPUSHED o **FALSE in caso contrario.**

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[Stili dei pulsanti](button-styles.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di pulsante](button-types-and-styles.md)
</dt> </dl>

 

 





