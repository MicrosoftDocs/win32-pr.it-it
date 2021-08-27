---
title: LVM_GETITEMCOUNT messaggio (Commctrl.h)
description: Recupera il numero di elementi in un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView GetItemCount.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- LVM_GETITEMCOUNT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1561e893930e4e3eca8de628c1df555e63794c3463edf81af798c53d873c8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109621"
---
# <a name="lvm_getitemcount-message"></a>Messaggio LVM \_ GETITEMCOUNT

Recupera il numero di elementi in un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView GetItemCount.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





