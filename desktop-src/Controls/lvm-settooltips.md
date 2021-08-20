---
title: LVM_SETTOOLTIPS messaggio (Commctrl.h)
description: Imposta il controllo descrizione comando che verrà utilizzato dal controllo visualizzazione elenco per visualizzare le descrizioni comando. Puoi inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetToolTips.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS del messaggio Windows controlli
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bf2256d94630b8e792fd1f148864f3588b27e73ea5781eb0bdcd24bf9571507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170397"
---
# <a name="lvm_settooltips-message"></a>Messaggio \_ LVM SETTOOLTIPS

Imposta il controllo descrizione comando che verrà utilizzato dal controllo visualizzazione elenco per visualizzare le descrizioni comando. Puoi inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Handle per il controllo descrizione comando da impostare.</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle al controllo descrizione comando precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVM \_ GETTOOLTIPS**](lvm-gettooltips.md)
</dt> </dl>

 

 





