---
title: HDM_GETOVERFLOWRECT messaggio (Commctrl.h)
description: Ottiene il rettangolo di delimitazione del pulsante di overflow quando lo stile HDS OVERFLOW è impostato sul controllo intestazione e il pulsante \_ di overflow è visibile. Inviare questo messaggio in modo esplicito o tramite la \_ macro Header GetOverflowRect.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f48088ad6c4a1d8cc5b843eeafb167f790bdd8eac06c56e6cb74e8afc18d082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047051"
---
# <a name="hdm_getoverflowrect-message"></a>Messaggio \_ GETOVERFLOWRECT HDM

Ottiene il rettangolo di delimitazione del pulsante di overflow quando lo stile [**\_ HDS OVERFLOW**](header-control-styles.md) è impostato sul controllo intestazione e il pulsante di overflow è visibile. Inviare questo messaggio in modo esplicito o tramite la macro [**\_ Header GetOverflowRect.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato. Deve essere zero.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) per ricevere le informazioni sul rettangolo di delimitazione. Il mittente del messaggio è responsabile dell'allocazione di questa struttura. Le coordinate restituite nella struttura **RECT** sono espresse come coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo. in caso contrario, **FALSE.**

## <a name="remarks"></a>Commenti

Il controllo intestazione deve avere lo stile **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sui controlli intestazione](header-controls.md)
</dt> </dl>

 

