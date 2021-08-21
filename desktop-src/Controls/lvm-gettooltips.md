---
title: LVM_GETTOOLTIPS messaggio (Commctrl.h)
description: Recupera il controllo descrizione comando utilizzato dal controllo visualizzazione elenco per visualizzare le descrizioni comando. Puoi inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetToolTips.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ca4340a8c57c6551d3c46f9324e4b66250f383c9412a3772df3114f105c5f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019289"
---
# <a name="lvm_gettooltips-message"></a>Messaggio \_ LVM GETTOOLTIPS

Recupera il controllo descrizione comando utilizzato dal controllo visualizzazione elenco per visualizzare le descrizioni comando. Puoi inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView GetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle del controllo descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVM \_ SETTOOLTIPS**](lvm-settooltips.md)
</dt> </dl>

 

 





