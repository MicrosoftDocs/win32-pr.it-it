---
title: LVM_UPDATE messaggio (Commctrl.h)
description: Aggiorna un elemento di visualizzazione elenco. Se il controllo visualizzazione elenco ha lo stile LVS AUTOARRANGE, questa macro determina la disposta \_ del controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro ListView \_ Update.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE controlli di Windows messaggio
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff9067d6eb80c5db7880ee9331a04e9259e9c841ccfe7dd80158a2afbcd06c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915231"
---
# <a name="lvm_update-message"></a>Messaggio LVM \_ UPDATE

Aggiorna un elemento di visualizzazione elenco. Se il controllo visualizzazione elenco ha lo stile [**LVS \_ AUTOARRANGE,**](list-view-window-styles.md) questa macro determina la disposta del controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**ListView \_ Update.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento da aggiornare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





