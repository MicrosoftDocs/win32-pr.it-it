---
title: LB_GETTOPINDEX messaggio (Winuser.h)
description: Ottiene l'indice del primo elemento visibile in una casella di riepilogo.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- LB_GETTOPINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b23360da45041e5a728f370e54f8250f216507dd439291a2ffce5ed383d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085381"
---
# <a name="lb_gettopindex-message"></a>Messaggio \_ LB GETTOPINDEX

Ottiene l'indice del primo elemento visibile in una casella di riepilogo. Inizialmente l'elemento con indice 0 si trova nella parte superiore della casella di riepilogo, ma se è stato fatto scorrere il contenuto della casella di riepilogo un altro elemento potrebbe essere nella parte superiore. Il primo elemento visibile in una casella di riepilogo a più colonne è l'elemento in alto a sinistra.

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

Il valore restituito è l'indice del primo elemento visibile nella casella di riepilogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ SETTOPINDEX**](lb-settopindex.md)
</dt> </dl>

 

 





