---
title: HDM_ORDERTOINDEX messaggio (Commctrl.h)
description: Recupera un valore di indice per un elemento in base al relativo ordine nel controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro OrderToIndex dell'intestazione.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7afd006c90684137ffc484dac62ab40c04d90c0cdbc87f51102d8e9119e8b14d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576260"
---
# <a name="hdm_ordertoindex-message"></a>Messaggio \_ ORDERTOINDEX HDM

Recupera un valore di indice per un elemento in base al relativo ordine nel controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ OrderToIndex dell'intestazione.**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ordine in cui l'elemento viene visualizzato all'interno del controllo intestazione, da sinistra a destra. Ad esempio, il valore di indice dell'elemento nella colonna all'estrema sinistra sarà 0. Il valore dell'elemento successivo a destra sarà 1 e così via.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce INT che indica l'indice dell'elemento. Se *wParam non* è valido (negativo o troppo grande), il valore restituito è uguale *a wParam*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





