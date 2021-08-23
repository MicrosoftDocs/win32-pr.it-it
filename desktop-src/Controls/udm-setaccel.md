---
title: UDM_SETACCEL messaggio (Commctrl.h)
description: Imposta l'accelerazione per un controllo verso l'alto.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc746e33c14de0dd177ecc31fc237be7cb8be36280bb2a5ceadff31d2b286ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957740"
---
# <a name="udm_setaccel-message"></a>Messaggio UDM \_ SETACCEL

Imposta l'accelerazione per un controllo verso l'alto.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di [**strutture UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) specificate da *aAccels*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di [**strutture UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) che contengono informazioni sull'accelerazione. Gli elementi devono essere ordinati in ordine crescente in base al **membro nSec.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UDM \_ GETACCEL**](udm-getaccel.md)
</dt> </dl>

 

 





