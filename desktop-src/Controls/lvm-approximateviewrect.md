---
title: LVM_APPROXIMATEVIEWRECT messaggio (Commctrl.h)
description: Calcola la larghezza e l'altezza approssimative necessarie per visualizzare un determinato numero di elementi. Puoi inviare questo messaggio in modo esplicito o usare la \_ macro ApproximateViewRect di ListView.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fcbb5476f28debd28116a52123bd01b8030c8b0a0c9c52e6598c864caed021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047061"
---
# <a name="lvm_approximateviewrect-message"></a>Messaggio LVM \_ APPROXIMATEVIEWRECT

Calcola la larghezza e l'altezza approssimative necessarie per visualizzare un determinato numero di elementi. Puoi inviare questo messaggio in modo esplicito o usare la macro [**\_ ApproximateViewRect di ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi da visualizzare nel controllo . Se questo parametro è impostato su -1, il messaggio usa il numero totale di elementi nel controllo .

</dd> <dt>

*lParam* 
</dt> <dd>

LoWORD [**è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la dimensione x proposta del controllo, in pixel. Questo parametro può essere impostato su -1 per consentire al messaggio di usare il valore di larghezza corrente.

HIWORD [**è**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la dimensione y proposta del controllo, in pixel. Questo parametro può essere impostato su -1 per consentire al messaggio di usare il valore di altezza corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che contiene la larghezza approssimativa (in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) e l'altezza (in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) necessarie per visualizzare gli elementi, in pixel.

## <a name="remarks"></a>Commenti

L'impostazione delle dimensioni del controllo visualizzazione elenco in base alle dimensioni fornite da questo messaggio può ottimizzare il ridisegno e ridurre lo sfarfallio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

