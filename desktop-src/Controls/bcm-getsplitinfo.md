---
title: BCM_GETSPLITINFO messaggio (Commctrl.h)
description: Ottiene informazioni per un controllo pulsante di menu suddiviso. Inviare questo messaggio in modo esplicito o tramite la \_ macro Button GetSplitInfo.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO di controllo Windows messaggio
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ee0771c8999c6a805931a93ed28c245082d18e538856fde42b69622ee73f9a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921641"
---
# <a name="bcm_getsplitinfo-message"></a>Messaggio \_ GETSPLITINFO di BCM

Ottiene informazioni per un controllo pulsante di menu suddiviso. Inviare questo messaggio in modo esplicito o tramite la macro [**\_ Button GetSplitInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura BUTTON \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) per ricevere informazioni sul pulsante. Il chiamante è responsabile dell'allocazione della memoria per la struttura . Impostare il **membro mask** di questa struttura per determinare quali informazioni ricevere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Usare questo messaggio solo con gli stili dei pulsanti [**\_ BS SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON.**](button-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
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

 

 





