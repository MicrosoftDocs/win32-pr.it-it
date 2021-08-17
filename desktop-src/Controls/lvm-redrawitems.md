---
title: LVM_REDRAWITEMS messaggio (Commctrl.h)
description: Impone a un controllo visualizzazione elenco di ridisegnare un intervallo di elementi. È possibile inviare questo messaggio in modo esplicito o tramite la macro ListView \_ RedrawItems.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53fbee43ff8cfcbb14ab357b6e76ab709df3e4a797143d5c4fa2c9b1179153af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261731"
---
# <a name="lvm_redrawitems-message"></a>Messaggio LVM \_ REDRAWITEMS

Impone a un controllo visualizzazione elenco di ridisegnare un intervallo di elementi. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ListView \_ RedrawItems.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice del primo elemento da ridisegnare.

</dd> <dt>

*lParam* 
</dt> <dd>

Indice dell'ultimo elemento da ridisegnare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Gli elementi specificati non vengono effettivamente ridisegnate fino a quando la finestra di visualizzazione elenco non riceve un messaggio [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) da ridisegnare. Per ridisegnare immediatamente, chiamare la [**funzione UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) dopo aver utilizzato questa macro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

