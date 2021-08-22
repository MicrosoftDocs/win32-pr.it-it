---
title: LVM_SETSELECTIONMARK messaggio (Commctrl.h)
description: Imposta il segno di selezione in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetSelectionMark.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c80f1392b5bb8b8ae49eaefb639a60213b5d4a7deaf153b99262bf608a770e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217361"
---
# <a name="lvm_setselectionmark-message"></a>Messaggio LVM \_ SETSELECTIONMARK

Imposta il segno di selezione in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetSelectionMark.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Indice in base zero del nuovo segno di selezione. Se impostato su -1, il segno di selezione viene rimosso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il segno di selezione precedente oppure -1 se non è presente alcun segno di selezione precedente.

## <a name="remarks"></a>Commenti

Il *segno di selezione* è l'indice dell'elemento da cui inizia una selezione multipla. Questo messaggio non influisce sullo stato di selezione dell'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVM \_ GETSELECTIONMARK**](lvm-getselectionmark.md)
</dt> </dl>

 

 





