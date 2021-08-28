---
title: LB_GETCARETINDEX messaggio (Winuser.h)
description: Recupera l'indice dell'elemento con lo stato attivo in una casella di riepilogo a selezione multipla. L'elemento può essere selezionato o meno.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74732bae571cdcba0cfe8096437bf681e7a339c5c0edb3f18d378ea610bdf8c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085541"
---
# <a name="lb_getcaretindex-message"></a>Messaggio LB \_ GETCARETINDEX

Recupera l'indice dell'elemento con lo stato attivo in una casella di riepilogo a selezione multipla. L'elemento può essere selezionato o meno.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero dell'elemento della casella di riepilogo con lo stato attivo oppure 0 se nessun elemento ha lo stato attivo.

## <a name="remarks"></a>Commenti

Questo messaggio può essere utilizzato anche per ottenere l'indice dell'elemento attualmente selezionato in una casella di riepilogo a selezione singola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ SETCARETINDEX**](lb-setcaretindex.md)
</dt> </dl>

 

 





