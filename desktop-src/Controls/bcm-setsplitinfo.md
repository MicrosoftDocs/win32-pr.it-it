---
title: BCM_SETSPLITINFO messaggio (Commctrl.h)
description: Imposta le informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite la \_ macro Button SetSplitInfo.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17332ce5f10fa612d739598222e4973000961435fa525190a650adaa9aa9fc4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921421"
---
# <a name="bcm_setsplitinfo-message"></a>Messaggio di BCM \_ SETSPLITINFO

Imposta le informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite la macro [**\_ Button SetSplitInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura BUTTON \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) contenente informazioni sul pulsante di divisione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Usare questo messaggio solo con gli stili dei pulsanti [**\_ BS SPLITBUTTON**](button-styles.md) e [**\_ BS DEFSPLITBUTTON.**](button-styles.md)

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

 

 





