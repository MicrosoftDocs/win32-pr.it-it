---
title: LVM_SCROLL messaggio (Commctrl.h)
description: Scorre il contenuto di un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro ListView \_ Scroll.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 604ef35b6d7e62e626aa7cbee32c1563224794781275c470a1b3cd1727b926bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019229"
---
# <a name="lvm_scroll-message"></a>Messaggio LVM \_ SCROLL

Scorre il contenuto di un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ListView \_ Scroll.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di tipo **int** che specifica la quantità di scorrimento orizzontale, in pixel, rispetto alla posizione corrente del contenuto della visualizzazione elenco. Se il controllo visualizzazione elenco è in visualizzazione elenco, questo valore viene arrotondato per es.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore di tipo **int** che specifica la quantità di scorrimento verticale, in pixel, rispetto alla posizione corrente del contenuto della visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo. in caso contrario, **FALSE.**

## <a name="remarks"></a>Commenti

Quando il controllo visualizzazione elenco è in visualizzazione report, è possibile scorrere il controllo solo verticalmente con incrementi di riga interi. Di conseguenza, il *parametro lParam* verrà arrotondato al numero più vicino di pixel che formano un incremento di riga intero. Ad esempio, se l'altezza di una riga è di 16 pixel e viene passato 8 per *lParam*, l'elenco verrà scorrendo di 16 pixel (1 riga). Se viene passato 7 per *lParam*, l'elenco verrà scorrendo di 0 pixel (0 righe).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





